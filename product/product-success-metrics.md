# Product Success Metrics Framework

> A comprehensive metrics framework covering all platform modules, AI quality, and business outcomes.

---

## Field Consultant Module Metrics

| Metric | Description | Target | Owner | Frequency |
|---|---|---|---|---|
| Admin time recaptured per FC/week | Hours saved from AI pre-visit prep, note capture, summary generation | 8+ hours | Product, CS | Monthly |
| Pre-visit brief generation time | Time from request to brief ready | <30 seconds | Engineering | Weekly |
| Voice note tag accuracy | % of auto-assigned tags confirmed by FC without correction | 85%+ | ML/AI | Weekly |
| Time-to-visit-summary submission | Hours from visit end to summary submitted | <2 hours (vs. 24-48 baseline) | CS | Monthly |
| Corrective action plan adoption rate | % of AI-generated CA plans accepted vs. modified or rejected | 75%+ accepted or minor modification | Product | Monthly |
| FC NPS for pre-visit briefs | Net Promoter Score from field consultant users | 70+ | CS | Quarterly |
| Visit completion rate vs. schedule | % of scheduled visits completed on time | 95%+ | CS | Monthly |
| FC daily active use rate | % of FCs logging in on days they have scheduled visits | 90%+ | Product | Weekly |

---

## Location Health Score Metrics

| Metric | Description | Target | Owner | Frequency |
|---|---|---|---|---|
| Health score prediction accuracy | % of At Risk / Critical locations that show measurable decline if no intervention within 45 days | 80%+ | ML/AI | Quarterly |
| Score state distribution stability | % of portfolio in Healthy state (brand benchmark) | Varies; improve over time | CS | Monthly |
| Score explainability satisfaction | User rating of score driver explanations (1-5 scale) | 4.3/5 or higher | Product | Quarterly |
| Benchmark data freshness | % of peer group benchmarks using data <7 days old | 95%+ | Data Engineering | Weekly |
| Health score update latency | Time from new signal ingestion to score update | <4 hours for real-time events | Engineering | Weekly |
| Score-to-intervention conversion rate | % of At Risk / Critical alerts resulting in documented intervention within 7 days | 75%+ | CS | Monthly |
| Health score confidence rate | % of locations with High confidence score (sufficient data quality) | 80%+ of active locations | Data Engineering | Monthly |

---

## Compliance Module Metrics

| Metric | Description | Target | Owner | Frequency |
|---|---|---|---|---|
| Corrective action closure rate | % of CAs closed within deadline | 85%+ | CS | Monthly |
| CA re-occurrence rate | % of closed CAs where same finding recurs at next audit | <20% | CS | Quarterly |
| Audit failure prediction accuracy | % of predicted high-risk locations confirmed failing at next audit | 75%+ | ML/AI | Quarterly |
| Compliance risk prediction lead time | Days before audit failure that risk is flagged | 21+ days | ML/AI | Quarterly |
| Risk-stratified scheduling adoption | % of customers using AI-recommended audit cadences | 70%+ by Month 12 | CS | Monthly |
| Repeat violation rate reduction | % change in repeat violations after Copilot deployment | -30% within 12 months | CS | Quarterly |
| Overdue CA escalation rate | % of at-risk CAs escalated before expiration | 90%+ | Engineering | Weekly |

---

## Operator Command Center Metrics

| Metric | Description | Target | Owner | Frequency |
|---|---|---|---|---|
| MUO weekly active use | % of MUO customers with weekly active sessions | 90%+ | Product | Weekly |
| Portfolio health improvement | Average health score improvement for MUO portfolios 90 days post-deployment | 5+ points average improvement | CS | Quarterly |
| Labor cost variance reduction | % reduction in labor cost variance across portfolio | 15%+ within 6 months | CS | Monthly |
| Portfolio risk alert action rate | % of AI portfolio risk alerts resulting in documented action | 70%+ | CS | Monthly |
| MUO expansion rate | % of MUOs expanding location count using the platform | Tracks system growth; positive correlation expected | CS | Annual |

---

## Executive Module Metrics

| Metric | Description | Target | Owner | Frequency |
|---|---|---|---|---|
| Executive weekly brief open rate | % of generated briefs opened within 24 hours | 80%+ | Product | Weekly |
| Board package preparation time | Hours required to prepare board-ready metrics package | <1 hour (vs. 2+ days manually) | CS | Quarterly |
| Executive dashboard weekly active use | % of C-level users with weekly active sessions | 80%+ | Product | Weekly |
| PE multi-portfolio expansion | Number of portfolio companies added by PE operating partner customers | Tracked per PE firm | Sales/CS | Quarterly |
| Executive tier NPS | NPS from CEO / COO / PE Partner users | 50+ | CS | Quarterly |

---

## AI Quality Metrics

| Metric | Description | Target | Owner | Frequency |
|---|---|---|---|---|
| Recommendation accuracy | % of AI recommendations that, when followed, produce predicted outcome within stated confidence interval | 78%+ for 75%+ confidence recommendations | ML/AI | Monthly |
| Confidence calibration error | Difference between stated confidence % and actual accuracy rate | <10 percentage points | ML/AI | Monthly |
| Override rate | % of AI recommendations that are overridden by human reviewers | Track trend; ideally declining as model improves | Product | Monthly |
| Override reason quality | % of overrides with a structured reason captured | 95%+ | Product | Monthly |
| False positive rate (alerts) | % of alerts rated as not actionable by the receiving owner | <15% | ML/AI | Monthly |
| Data freshness compliance | % of AI inferences using data meeting freshness requirements | 90%+ | Engineering | Weekly |
| AI response latency (pre-visit brief) | Time from brief request to brief ready | <30 seconds (P95) | Engineering | Weekly |
| Model drift detection | Automated monitoring for model accuracy degradation | Alert if accuracy drops >5 points | ML/AI | Weekly |

---

## Business Metrics

| Metric | Description | Target | Owner | Frequency |
|---|---|---|---|---|
| Annual Recurring Revenue (ARR) | Total contracted annual revenue | Per-phase targets in roadmap | Finance/Sales | Monthly |
| Average Contract Value (ACV) | Average annual contract value per customer | $180,000+ by Year 2 | Sales | Monthly |
| Net Revenue Retention (NRR) | Revenue retained + expansion from existing customers | 125%+ | CS | Monthly |
| Customer Count by Tier | Customers in Foundation / Operations / Intelligence / Enterprise | Intelligence tier: 50%+ of active customers by Year 2 | Sales | Monthly |
| Locations Under Management | Total active locations on the platform | 10,000+ by Year 2 | Sales | Monthly |
| Time-to-Value | Weeks from contract to first documented customer outcome | <8 weeks for AI Field Consultant | CS | Monthly |
| Gross Revenue Retention (GRR) | Revenue retained after churn and downgrades | 90%+ | CS | Monthly |
| Pilot-to-Contract Conversion | % of pilots that convert to full platform contracts | 70%+ | Sales/CS | Monthly |
| Expansion Revenue | Revenue from module and tier upgrades in existing accounts | 40%+ of new ARR | CS | Monthly |
| Customer Health Score (platform's own internal CHS) | Internal scoring of customer adoption, engagement, and outcome achievement | 80%+ of customers in Healthy state | CS | Monthly |
