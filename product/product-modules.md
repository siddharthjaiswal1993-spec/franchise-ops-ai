# Product Modules: Franchise Operational Intelligence Platform

> Detailed documentation of 12 platform modules — users, buyers, problems solved, features, AI capabilities, and success metrics.

---

## Module 1: Executive Command Center

| Dimension | Detail |
|---|---|
| **Primary User** | CEO, COO, PE Operating Partner |
| **Economic Buyer** | CEO, Board, PE Firm |
| **Problem Solved** | Executives have no real-time portfolio health view. Weekly or monthly reports are manually compiled from multiple systems, arrive too late to act on, and don't surface what the executive actually needs: where is my risk concentrated, and what is being done about it? |

**Key Features:**
1. Portfolio health score distribution (how many locations are Healthy, Watchlist, At Risk, Critical)
2. Top-10 risk locations with score state, trend direction, and recommended intervention
3. System-wide corrective action pipeline — open items, aging analysis, closure rate trend
4. AI-generated weekly portfolio intelligence brief (2-page summary, automatically generated)
5. Board-ready metrics package (AUV trend, audit pass rate, location health distribution, field visit effectiveness)

**AI Capability:** AI-generated executive briefs synthesize portfolio health, surface top risk concentrations, and recommend portfolio-level interventions. Briefs are generated on a configurable schedule (weekly default) and include source citations for all data points.

**GTM Value:** Unlocks CEO and COO as economic buyers. Creates board-level visibility that justifies enterprise tier pricing. PE operating partner use case creates multi-portfolio expansion opportunity.

**Expansion Value:** Entry point for Executive Intelligence Tier upgrade. Once deployed, creates strong retention through senior leadership dependency.

**Success Metrics:**
1. Weekly active use rate for executive users (target: 80%+ weekly active)
2. Time to generate board-ready portfolio report (target: under 1 hour from platform data, vs. 2 days manually)
3. Executive brief satisfaction score (target: 4.5/5 or higher)

---

## Module 2: Field Consultant Workspace

| Dimension | Detail |
|---|---|
| **Primary User** | Field Consultants, District Managers, Area Development Managers |
| **Economic Buyer** | VP Field Operations, COO |
| **Problem Solved** | Field consultants manage 30-50 locations with inadequate tools — visit plans built in spreadsheets, notes captured in email, corrective actions tracked in shared documents, and no measurement of whether their visits actually improved location performance. |

**Key Features:**
1. AI-prioritized portfolio view (which locations need attention this week, ranked by health score and visit cadence)
2. AI-generated pre-visit brief (health score summary, open corrective actions, training gaps, staff changes, recommended focus areas)
3. Structured visit execution with observation capture (templates + voice-to-structured notes)
4. Post-visit summary auto-generation from structured notes
5. Visit history and trend tracking (health score trajectory by location over time)

**AI Capability:** Pre-visit brief generation aggregates 6+ data sources in under 30 seconds. Voice-to-structured notes transcribes and auto-tags observations in real time. Post-visit summary AI drafts a structured visit record from tagged observations.

**GTM Value:** This is the primary wedge module. Highest pain, fastest ROI, strongest pilot evidence.

**Expansion Value:** Field visit data feeds Location Health Score training data; corrective action patterns feed Compliance Copilot; visit frequency and quality data feeds Executive Intelligence Layer.

**Success Metrics:**
1. Hours of administrative time recaptured per FC per week (target: 8+ hours)
2. Time from visit end to visit summary submission (target: under 2 hours, vs. 24-48 hours currently)
3. Field consultant NPS for pre-visit briefs (target: 70+ NPS)

---

## Module 3: Location Health Score

| Dimension | Detail |
|---|---|
| **Primary User** | COO, VP Operations, Field Consultants, Franchisees (their own score) |
| **Economic Buyer** | COO, CEO |
| **Problem Solved** | No unified, explainable view of location health exists. Operational assessment is based on individual metric reviews in disconnected systems, field consultant subjective opinion, and quarterly reports — not a continuous, multi-signal, benchmarked health model. |

**Key Features:**
1. Composite health score (0-100) with 6 dimension scores (operations, training, compliance, financial, customer experience, field engagement)
2. Score state classification (Healthy / Watchlist / At Risk / Critical) with recommended action per state
3. Score explainability: top 3 drivers of current score, source data citations, confidence indicator
4. Peer benchmarking: where does this location rank vs. peer group, brand average, and top quartile
5. Score trajectory visualization and trend analysis

**AI Capability:** Weighted composite model trained on franchise-specific operational data. Anomaly detection identifies statistically unusual signal combinations that precede performance decline. Continuously updated as new signals arrive.

**GTM Value:** The unifying product asset. Every other module either contributes to the health score or responds to it. Makes the platform indispensable once adopted.

**Expansion Value:** Every subsequent module (Compliance Copilot, Executive Command Center, Benchmarking) requires the health score as its foundation.

**Success Metrics:**
1. Health score prediction accuracy (target: 80%+ of At Risk score states followed by measurable performance decline within 45 days if no intervention)
2. Customer retention rate for locations using the health score (target: 95%+ annual retention)
3. Corrective action conversion rate from health score alerts (target: 70%+ of health score alerts result in documented intervention)

---

## Module 4: Visit Intelligence

| Dimension | Detail |
|---|---|
| **Primary User** | Field Consultants, District Managers |
| **Economic Buyer** | Director of Field Operations, VP Operations |
| **Problem Solved** | Field visit quality is inconsistent and unmeasured. There is no standard framework for what a high-quality field visit looks like, no mechanism for capturing structured visit data at scale, and no measurement of whether visits produce measurable location improvements. |

**Key Features:**
1. Visit quality scoring (structured observation categories with scoring rubrics)
2. Voice-to-structured notes with real-time transcription and auto-tagging
3. Observation library (structured tagging vocabulary for consistent cross-visit comparison)
4. AI-generated visit summaries from tagged observations
5. Visit effectiveness analytics (health score and audit score change 30/60/90 days post-visit)

**AI Capability:** Voice transcription and tag classification. AI-generated visit summaries that synthesize observations into structured, readable records. Visit effectiveness attribution (which consultants, which visit types, which corrective action categories produce the most measurable outcomes).

**GTM Value:** Supports the field consultant productivity story; adds measurement dimension to the AI Field Consultant ROI.

**Expansion Value:** Visit quality data is a dimension input for the Location Health Score (field engagement dimension).

**Success Metrics:**
1. Visit summary submission rate within 2 hours of visit end (target: 90%+)
2. Structured observation tag adoption (target: 85%+ of visits with 5+ tagged observations)
3. Visit-to-health-score-improvement correlation coefficient (tracked and shared with customers quarterly)

---

## Module 5: Closed-Loop Actions

| Dimension | Detail |
|---|---|
| **Primary User** | Franchisees, Field Consultants, Compliance Managers |
| **Economic Buyer** | VP Operations, COO |
| **Problem Solved** | Corrective action closure rates average 55-65% across franchise systems. Identified problems are documented, assigned, and then forgotten. There is no systematic mechanism to ensure corrective actions are completed, verified as effective, and closed. |

**Key Features:**
1. Structured corrective action creation with category, owner, deadline, and verification requirement
2. AI-generated corrective action plans from visit observations or audit findings (auto-populated, human-reviewed)
3. Multi-party action management (field consultant, franchisee, specific employee assignments)
4. Deadline tracking with escalation automation (configurable reminder chain)
5. Closure verification workflow (documented evidence of resolution, not just checkbox closure)

**AI Capability:** AI-generated corrective action plans from structured audit findings or visit observations. Priority scoring for action items based on risk level and historical closure probability. Escalation prediction — which actions are most likely to expire unclosed.

**GTM Value:** Direct ROI story: improvement in corrective action closure rate is a headline metric that every compliance and operations leader tracks.

**Expansion Value:** Corrective action patterns feed the Compliance Copilot risk model. Closure rates and outcomes feed the Location Health Score.

**Success Metrics:**
1. Corrective action closure rate (target: 85%+ within deadline, vs. industry average 55-65%)
2. Average time from action creation to closure (target: 30%+ reduction vs. baseline)
3. Corrective action re-occurrence rate (target: less than 20% of closed items re-appear at next audit)

---

## Module 6: Compliance and Audit Intelligence

| Dimension | Detail |
|---|---|
| **Primary User** | Compliance Manager, Field Consultants |
| **Economic Buyer** | COO, VP Operations, Legal |
| **Problem Solved** | Audit scheduling is static and risk-unaware. Corrective action closure rates are below 65%. Compliance risk is identified only during audits, not between them. There is no mechanism for predicting which locations are most likely to fail their next audit. |

**Key Features:**
1. Digital audit forms with multi-category scoring and photo documentation
2. Risk-stratified audit scheduling (high-risk locations audited more frequently; low-risk locations on extended cycles)
3. AI-generated corrective action plans from audit findings (category-specific recommendations based on historical efficacy)
4. Audit trend analysis (repeat violation tracking, brand-standard compliance trend by category)
5. Predictive compliance risk scoring (probability of audit failure based on leading indicator signals)

**AI Capability:** Compliance risk prediction model using training data, task completion, health score signals, and prior audit history. Automated corrective action plan generation from audit finding categories. Repeat violation pattern detection.

**GTM Value:** Strong ROI story for compliance-focused buyers. Regulatory risk reduction is a budget-unlocking value proposition for legal and compliance leadership.

**Expansion Value:** Audit data is a critical signal for the Location Health Score compliance dimension.

**Success Metrics:**
1. Audit failure prediction accuracy (target: 75%+ of predicted failures confirmed at next audit if no intervention)
2. Corrective action plan adoption rate (% of AI-generated plans accepted vs. modified or rejected)
3. Repeat violation rate reduction (target: 30%+ reduction within 12 months)

---

## Module 7: Operator Command Center

| Dimension | Detail |
|---|---|
| **Primary User** | Multi-Unit Operators (MUOs), MUO Operations Managers |
| **Economic Buyer** | MUO Owner, MUO COO |
| **Problem Solved** | Multi-unit operators managing 5-100 locations have no portfolio-level operational intelligence tool designed for their specific needs. Franchisor tools are built for HQ oversight, not for an independent operator managing a portfolio across multiple markets. |

**Key Features:**
1. Portfolio health score view across all owned locations
2. Cross-location performance comparison with peer benchmarking
3. Labor cost analysis across the portfolio (vs. brand average, vs. own portfolio average)
4. Portfolio risk alerts (which locations are at risk this week and why)
5. Consolidated corrective action view across all locations

**AI Capability:** Portfolio-level risk prioritization. AI summary of portfolio health status for weekly operator review. Staffing and scheduling optimization recommendations across the portfolio.

**GTM Value:** Opens MUO as a direct buyer persona. MUOs are active technology evaluators with independent purchasing budgets.

**Expansion Value:** MUO adoption creates bottom-up pressure on franchisors who are not yet FranConnect customers.

**Success Metrics:**
1. MUO weekly active use rate (target: 90%+)
2. Portfolio health score improvement for MUOs using the Command Center (target: measurable improvement within 90 days vs. non-users)
3. MUO expansion rate (% of MUO customers who expand location count within 12 months)

---

## Module 8: Franchise Support Desk

| Dimension | Detail |
|---|---|
| **Primary User** | Franchisees, Store Managers, Frontline Employees |
| **Economic Buyer** | VP Operations, COO |
| **Problem Solved** | Franchisees and store managers need fast, accurate answers to operational questions. HQ support teams are overwhelmed with repetitive questions that could be answered by an AI system with access to the brand's SOPs, training materials, and operational playbooks. |

**Key Features:**
1. AI-powered SOP search — natural language questions answered with citations from the brand's own operational documents
2. Ticket routing — support requests automatically routed to the right team (field consultant, compliance, training, HQ support) based on content analysis
3. Self-service resolution — AI resolves common questions without human involvement; escalates complex issues
4. Ticket pattern analytics — HQ can see which questions are asked most frequently, identifying training gaps and SOP clarity issues
5. Escalation prediction — AI identifies tickets that are likely to escalate and routes them proactively

**AI Capability:** RAG-based (Retrieval-Augmented Generation) SOP assistant that answers questions using the brand's own documents with citations. Ticket classification and routing. Escalation risk scoring.

**GTM Value:** Franchisee adoption driver. Reduces HQ support burden. Strong ROI story for support team efficiency.

**Expansion Value:** Question pattern data reveals operational knowledge gaps that feed back into the LMS and SOP improvement processes.

**Success Metrics:**
1. Self-service resolution rate (target: 70%+ of tickets resolved without human agent)
2. Average time to resolution (target: under 4 hours for self-service; under 24 hours for human-agent)
3. Franchisee satisfaction with support experience (target: 4.5/5 or higher CSAT)

---

## Module 9: Risk and Alerts Engine

| Dimension | Detail |
|---|---|
| **Primary User** | COO, VP Operations, Field Consultants, Compliance Managers |
| **Economic Buyer** | COO |
| **Problem Solved** | Current franchise platforms surface alerts based on individual metric thresholds. These alerts create noise (false positives at low thresholds) or miss early risk signals (thresholds too high). A true risk alerting engine must detect multi-signal patterns, not just individual metric breaches. |

**Key Features:**
1. Multi-signal anomaly detection (detect combinations of signals that historically precede performance decline)
2. Risk alert routing (alerts routed to the appropriate owner based on alert type and severity)
3. Configurable alert thresholds with role-based delivery (COO gets portfolio alerts; FC gets location-level alerts)
4. Alert fatigue management (suppress low-priority alerts; surface only actionable signals)
5. Alert effectiveness tracking (which alert types lead to documented interventions)

**AI Capability:** Statistical anomaly detection using historical operational signal data. Cross-signal correlation model. Alert scoring (severity, urgency, confidence). Alert fatigue reduction through relevance scoring.

**GTM Value:** Supporting module that amplifies the value of the Location Health Score and Field Consultant Workspace.

**Expansion Value:** Feeds recommendations into the Decision Layer (Layer 3 of the intelligence stack).

**Success Metrics:**
1. Alert-to-action rate (target: 80%+ of Urgent and High alerts result in documented response within 48 hours)
2. False positive rate (target: under 15% of alerts rated as not actionable by receiving owner)
3. Early warning detection rate (% of location performance declines that were preceded by an alert at least 14 days before KPI threshold breach)

---

## Module 10: Benchmarking

| Dimension | Detail |
|---|---|
| **Primary User** | COO, VP Operations, Field Consultants, Franchisees |
| **Economic Buyer** | COO |
| **Problem Solved** | Franchise operators have no objective comparison framework for location performance. Without benchmarking, field consultants can only compare a location to its own history — not to how similar locations in the system or industry are performing. |

**Key Features:**
1. Peer group benchmarking (locations matched by brand, vertical, geography, age, and format type)
2. Brand average benchmarks across all operational dimensions
3. Top-quartile benchmarks with driver analysis (what are the top-quartile locations doing differently?)
4. Cross-brand benchmarking (compare against all locations in the same vertical on the platform)
5. Benchmarking trends (how is this location's position in its peer group changing over time?)

**AI Capability:** Peer group construction algorithm (multi-factor matching). Driver analysis that identifies which practices differentiate top-quartile from bottom-quartile locations.

**GTM Value:** High motivation for franchisees and MUOs; strong differentiation story for the platform's data network effect.

**Expansion Value:** The more brands on the platform, the better the cross-brand benchmarks — compounding competitive moat.

**Success Metrics:**
1. Franchisee engagement rate with benchmarking views (target: 60%+ monthly active among franchisee users)
2. Correlation between peer group rank improvement and health score improvement (validates benchmarking as a coaching tool)
3. Platform scale milestone: cross-brand benchmarks available for top 3 verticals (QSR, home services, fitness)

---

## Module 11: Data and Integrations Layer

| Dimension | Detail |
|---|---|
| **Primary User** | CTO, Data Engineering, Operations (indirect) |
| **Economic Buyer** | CTO, COO |
| **Problem Solved** | Franchise systems use 6-10 operational software platforms simultaneously. None of these systems were designed to share data. Without a unified data layer, AI quality is limited by data fragmentation. |

**Key Features:**
1. Pre-built API integrations with major POS, LMS, HRIS, payroll, review, and ticketing platforms
2. Data quality monitoring (track signal completeness, freshness, and consistency)
3. Real-time event ingestion via webhooks (near-real-time health score updates as signals arrive)
4. Multi-brand data normalization (consistent data model across brands operating different systems)
5. Integration monitoring dashboard (data pipeline health, latency, error rates)

**AI Capability:** Data quality scoring that identifies which locations have insufficient integration depth for reliable health score calculation. Anomaly detection in the data pipeline itself (detect integration failures before they degrade AI quality).

**GTM Value:** Integration depth is the prerequisite for every AI feature. This module enables the intelligence layer.

**Expansion Value:** Each new integration added to the platform expands the health score signal quality for all customers.

**Success Metrics:**
1. Average number of integrations per customer (target: 4+ by Month 12)
2. Data freshness (% of health score calculations using data less than 24 hours old — target: 90%+)
3. Integration reliability (target: 99.5%+ uptime for all integration pipelines)

---

## Module 12: Governance and Trust Layer

| Dimension | Detail |
|---|---|
| **Primary User** | Compliance Manager, Legal, CTO, Operations Leaders |
| **Economic Buyer** | COO, CTO, Legal |
| **Problem Solved** | Enterprise franchise buyers cannot adopt AI platforms that cannot be audited, explained, or overridden. The governance layer is the product infrastructure that makes AI safe for compliance-sensitive franchise operations. |

**Key Features:**
1. AI recommendation audit log — every recommendation, every human decision, every override, timestamped and searchable
2. Source citation on every AI output — which data from which system drove the recommendation
3. Confidence scoring with uncertainty explanation
4. Role-based AI permissions (who can see AI recommendations; who must approve before action is dispatched)
5. Override capture — structured note required for any human decision that differs from the AI recommendation

**AI Capability:** The governance layer is meta-AI — it monitors the AI system's recommendation quality, calibration accuracy, and override patterns to identify model improvement opportunities.

**GTM Value:** Enterprise differentiation story. The governance layer is the answer to "how do we trust your AI?" in enterprise sales cycles.

**Expansion Value:** Override data and feedback signals feed back into the AI models, improving quality over time.

**Success Metrics:**
1. Audit log completeness (target: 100% of AI recommendations with complete human decision records)
2. Time-to-produce-AI-audit-report (target: under 30 minutes for any date range)
3. Model calibration accuracy (target: 80%+ of confidence scores within 10% of actual outcome rates)
