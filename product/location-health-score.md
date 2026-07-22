# Location Health Score: Product Specification

> **Relationship to the PRD:** `unified-operations-intelligence-prd.md` (§8) specifies a tighter, six-sub-score MVP cut of this model (Revenue, Profitability, Customer Experience, Operational Execution, Compliance, Labor) scoped to what Phase 1–2 integrations can actually support. Treat this document as the fuller target-state model as later-phase integrations (accounting, ticketing, payroll) land; treat the PRD as the near-term, shippable spec.

---

## Purpose and Strategic Value

The Location Health Score is the platform's central intelligence asset — a continuously updated, explainable, benchmarked, and actionable composite score that represents the operational health of each location in a franchise system.

The health score serves three purposes simultaneously. For operations leaders, it is the unified portfolio management tool — a single number with dimension breakdown that replaces the manual process of pulling reports from six systems. For field consultants, it is the visit prioritization engine — the objective signal that tells them which locations need attention now, not which ones are scheduled next on a calendar. For franchisees, it is the performance coaching tool — a transparent indicator of where they stand relative to peers, with specific recommendations for improvement.

The Location Health Score is also the primary mechanism by which the platform's AI-native architecture becomes visible and valuable. Every AI recommendation that flows through the DETECT -> DECIDE -> ACT -> VERIFY loop is grounded in the health score. The health score is where the platform's intelligence becomes tangible to the buyer.

---

## Input Signals

The Location Health Score aggregates signals from 8 categories:

### Category 1: Operations and Execution
- Daily/weekly task completion rate
- Opening and closing checklist completion rate
- SOP acknowledgment currency (how recently have SOPs been read and acknowledged)
- Equipment downtime incidents
- Inventory management compliance

### Category 2: Training and People
- Training completion rate by employee and module (last 30/60/90 days)
- Certification currency rate (% of employees with current required certifications)
- New hire onboarding completion rate and time-to-certification
- Employee turnover rate (last 90 days)
- Manager tenure and stability (manager change events)

### Category 3: Compliance and Audit
- Audit score (last 2 audits, trend)
- Repeat violation rate (items that failed in consecutive audits)
- Corrective action closure rate (% of prior audit corrective actions closed on time)
- Days since last audit (relative to scheduled audit frequency)
- Pre-opening checklist completion (for locations in first year)

### Category 4: Financial Performance
- Sales trend vs. prior year (same-store comparison)
- Sales vs. peer group average (benchmarked)
- Labor cost as % of revenue (vs. brand target, vs. peer average)
- Royalty payment timeliness (on-time vs. delinquent)
- Average ticket size trend

### Category 5: Customer Experience
- Review platform rating trend (Google, Yelp, brand-specific — last 30/60 days)
- Review volume (low review volume can indicate low traffic — a risk signal)
- Review sentiment keyword frequency (food safety terms, service complaints, etc.)
- Support ticket volume and theme (internal and external complaint signals)

### Category 6: Field Engagement
- Days since last field visit (relative to standard visit frequency)
- Corrective action initiation rate from last visit (were actions created after the visit?)
- Franchisee portal engagement (login frequency, communication response rate)
- Open corrective actions from last visit (number and age)

### Category 7: Operational Context
- Location age (new locations have different baselines than mature ones)
- Seasonal adjustment (locations in seasonal markets have different baseline patterns)
- Market conditions (labor market tightness in the location's geography)
- Recent events (manager change, franchisee change, remodel, natural disaster)

### Category 8: Predictive Signals
- Pre-opening checklist completion score (for locations in Year 1 — predicts Year 1 performance)
- Training velocity trend (improving or declining training completion patterns)
- Review sentiment trend direction (improving or declining review sentiment)

---

## Scoring Model Structure

The Location Health Score is a weighted composite of dimension scores. Each dimension score is itself a composite of the signals in its category.

**Composite score formula:**
`Health Score = Σ (Dimension Score × Dimension Weight)`

**Default dimension weights** (configurable by brand):

| Dimension | Default Weight | Rationale |
|---|---|---|
| Operations and Execution | 20% | Daily operational consistency is the foundation |
| Training and People | 18% | Training directly predicts operational consistency |
| Compliance and Audit | 22% | Audit performance is the primary compliance signal; highest regulatory risk |
| Financial Performance | 20% | Financial health reflects operational success; PE-relevant dimension |
| Customer Experience | 10% | Lagging indicator but high visibility; guest satisfaction proxy |
| Field Engagement | 10% | Field engagement quality is a proxy for support quality and relationship health |

**Score calculation specifics:**
- Dimension scores are normalized to 0-100 before weighting
- Signals within dimensions are sub-weighted based on their historical predictive power (determined by model training)
- Seasonal adjustments applied for financial and customer experience dimensions
- Data freshness weighting: signals older than 14 days are down-weighted; signals older than 30 days are marked stale

---

## Output: Score and Score States

### Overall Score
A single integer from 0 to 100 representing composite location health.

### Dimension Scores
Six integer scores (0-100) for each dimension, displayed alongside the overall score.

### Score States

| Score Range | State | Display Color | Default Recommended Action |
|---|---|---|---|
| 80-100 | Healthy | Green | Maintain cadence; share as best-practice example; reduce visit frequency if appropriate |
| 65-79 | Watchlist | Yellow | Schedule check-in call; review open corrective actions; flag for next scheduled visit |
| 50-64 | At Risk | Orange | Schedule focused field visit within 7 days; AI-generate corrective action plan; notify district manager |
| Below 50 | Critical | Red | Immediate intervention required; escalate to District Manager or VP Operations; emergency field visit; franchisee support call |

### Score Trajectory Indicator
- Improving (score rising over last 30 days)
- Stable (score within ±3 points over last 30 days)
- Declining (score falling over last 30 days)
- Accelerating Decline (rate of score decline increasing)

---

## Explainability Requirements

Every score state and every score change must be explainable. The platform must show:

**Top 3 score drivers:** The three signals or signal categories that have the greatest impact on the current score, expressed in plain language. Example: "Your compliance score is being pulled down primarily by two repeat violations from the last audit (food safety handling, opening procedures), a corrective action closure rate of 42% over the last 90 days, and audit data that is 73 days old — overdue for a re-audit."

**Source data citations:** For every driver, show the specific data point, the system it came from, and the timestamp. The franchisee and field consultant must be able to verify every claim in the health score by tracing it to a source.

**Confidence indicator:** A qualitative confidence indicator (High / Medium / Low) reflecting data completeness. A location with full POS, LMS, and audit integration has a High confidence score. A location where LMS data is 40 days stale has a Low confidence score, and the score should be flagged accordingly.

**Score change explanation:** When a score changes by more than 3 points, the platform automatically generates an explanation: "Your score dropped 8 points in the last 7 days. Primary driver: 3 new customer reviews with food safety concerns (Google average dropped from 4.1 to 3.7). Secondary driver: Training completion rate fell from 74% to 58% after 2 employee departures."

---

## Recommended Actions by Score State

| Score State | AI-Recommended Action | Routing |
|---|---|---|
| Healthy | "No urgent action required. Consider sharing this location's practices with Watchlist locations in the same peer group." | Informational to FC |
| Watchlist | "Schedule a check-in call with the franchisee within 5 days. Review open corrective actions. Flag for discussion at next scheduled visit." | Routed to assigned FC |
| At Risk | "Schedule a focused field visit within 7 days. Review the AI-generated corrective action plan draft. Notify district manager." | Urgent routing to FC + DM notification |
| Critical | "Immediate intervention required. Escalate to District Manager and VP Operations. Schedule emergency field visit within 48 hours. Initiate franchisee support protocol." | Emergency escalation to DM + VP Ops |

---

## Alert Thresholds and Routing

| Alert Type | Trigger | Routing |
|---|---|---|
| Score state change | Any transition between states | FC assigned + Manager notification |
| Critical state entry | Score drops below 50 | FC + DM + VP Operations urgent notification |
| Rapid decline | Score drops 10+ points in 7 days | FC + Manager notification with explanation |
| Anomaly detection | Multi-signal pattern detected (pre-threshold) | FC notification with pattern explanation |
| Data staleness | Key signal source >14 days old | Data team + FC notification |

---

## Benchmarking

Every Location Health Score display includes a benchmarking context panel showing:

- **Peer group rank:** Where this location ranks among its peer group (matched by brand, vertical, geography, location age, format type). Example: "This location is in the 34th percentile among peer QSR locations in the Southeast with 3-5 years of operation."
- **Brand average:** How the location compares to the brand average score and dimension scores.
- **Top-quartile benchmark:** What score the top 25% of peer locations are achieving, and which dimensions drive the top-quartile locations' higher scores.
- **Improvement pathway:** "To move from the 34th to the 50th percentile, the top opportunity is the Compliance dimension. Top-quartile locations in this peer group have average corrective action closure rates of 89% vs. this location's 52%."

---

## Anti-Gaming Principles

The Location Health Score must be resistant to manipulation by franchisees or managers who might attempt to improve their score without actually improving operations:

- **Audit verification:** Corrective action closure requires documented evidence, not just checkbox completion. Unverified closures are flagged.
- **Self-reported data down-weighting:** Signals that are entirely self-reported (manual task completion entries without verification) receive lower weight than verified signals (audit-confirmed, POS-sourced, or LMS-verified).
- **Anomaly detection on suspicious patterns:** If a location shows sudden improvement in self-reported metrics without corresponding improvement in audited or POS-sourced metrics, the platform flags the pattern for review.
- **Score history and explanation logging:** Every score and every score change is logged permanently. Score manipulation attempts are detectable through pattern analysis of the score history.

---

## Trust Architecture for the Score

The Location Health Score is used to make real decisions: visit scheduling, corrective action prioritization, franchisee conversations, board reporting. This means it must be trusted — which requires more than accuracy.

Trust requirements:
- Full data lineage: every score can be traced to its source data, system, and timestamp
- Model documentation: the scoring methodology is documented and explainable, not a black box
- Calibration reporting: quarterly report showing how often score states predicted actual performance outcomes
- Override capability: operations leaders can flag a score as "under manual review" when they have context the model lacks
- Feedback mechanism: franchisees and field consultants can flag disagreements with score components, with these flags reviewed and used for model improvement
