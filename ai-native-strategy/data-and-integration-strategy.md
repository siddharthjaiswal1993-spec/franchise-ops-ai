# Data and Integration Strategy

---

## Why Integration Depth Is a Prerequisite for AI Quality

Every AI capability in the franchise operational intelligence platform depends on the data it can access. A Location Health Score computed from 2 data sources is a guess. A Location Health Score computed from 8 data sources is an intelligence asset.

This is not a metaphor. The predictive accuracy of a health model is empirically bounded by the signal quality available to it. A model that can see only audit scores and training completion rates can identify about 45% of at-risk locations before they deteriorate. Add POS financial data, customer review sentiment, and field visit frequency, and that detection rate rises to 70%. Add HRIS turnover data and support ticket patterns, and it rises to 80%+.

Integration depth is not a product feature — it is the prerequisite for AI quality. Every integration that is added to the platform improves the intelligence for every customer on the platform. This is the data network effect that compounds with scale.

**Integration strategy principle:** Prioritize the integration sources that contribute most to health score accuracy. Build those integrations deeply and reliably before building breadth across many shallow integrations.

---

## Priority Integrations

### Tier 1: Critical (Required for Reliable Health Scoring)

**POS Systems — Toast, PAR Technology, Square, Oracle MICROS, Aloha**

*Data ingested:* Gross sales by day and by hour; transaction count; average ticket size; labor hours and cost (for POS systems with scheduling integration); product mix data

*Why it is critical:* Financial performance is 20% of the Location Health Score. Sales trend, labor cost %, and transaction count are among the highest-predictive signals for location operational health. Without POS data, the financial dimension of the health score cannot be populated, and the royalty anomaly detection use case is impossible.

*Integration architecture:* Real-time webhook for sales close events (daily); batch sync for weekly financial summaries. APIs exist for all major QSR POS systems.

**LMS / Training Systems — FranConnect LMS, Trainual, TalentLMS, Cornerstone**

*Data ingested:* Training completion by employee and module; certification currency; quiz scores; time-on-task; onboarding completion status

*Why it is critical:* Training completion is 18% of the health score. The relationship between training completion decline and subsequent audit failure is one of the strongest predictive signals in the model. Without LMS data, training-driven risk cannot be detected.

*Integration architecture:* Daily batch sync; real-time webhook for certification expiration events.

**Audit Platforms — FranConnect Compliance, Zenput, FranchiseBlast**

*Data ingested:* Audit scores by date; item-level findings; corrective action creation and closure data; audit schedule data

*Why it is critical:* Compliance is 22% of the health score and the primary risk indicator for regulatory exposure. Audit data is also the primary outcome metric for verifying intervention effectiveness.

*Integration architecture:* Real-time sync for corrective action status changes; batch sync for audit completion records.

---

### Tier 2: High Value (Substantially Improves Model Accuracy)

**HRIS / Payroll — ADP, Paychex, Rippling, Workday**

*Data ingested:* Employee count and turnover rate; manager change events; new hire dates; wage rate data; labor cost by location

*Why it is valuable:* Staff turnover and manager changes are strong leading indicators of operational instability. A location that has had two manager changes in 60 days is at significantly elevated risk. Labor cost data enables the financial dimension's efficiency analysis.

*Integration architecture:* Weekly batch sync; real-time event for manager change records.

**Review Platforms — Google Business Profile API, Yelp API, brand-specific review systems**

*Data ingested:* Star rating trend; review count; sentiment keyword frequency; flagged review themes (food safety terms, service complaints, wait time complaints)

*Why it is valuable:* Customer review signals are a lagging indicator of operational quality but an early leading indicator of customer attrition. Review sentiment data that no other internal system captures provides a unique external validation signal.

*Integration architecture:* Daily API pull; real-time webhook for new review events (where supported).

**Ticketing and Support — Zendesk, Intercom, internal support systems**

*Data ingested:* Support ticket volume by location; ticket categories; escalation events; resolution time

*Why it is valuable:* Support ticket patterns are a proxy for franchisee operational stress and engagement levels. High ticket volume in specific categories (e.g., food safety questions) is a signal that precedes audit failures.

---

### Tier 3: Supplementary (Valuable for Specific Use Cases)

**CRM — FranConnect CRM, Salesforce, HubSpot**

*Data ingested:* Franchisee relationship history; communication frequency; franchise candidate pipeline

*Use case:* Franchisee engagement signal; development pipeline for launch delay prediction.

**Scheduling and Workforce — 7shifts, Homebase, Hot Schedules**

*Data ingested:* Scheduled vs. actual hours; manager shift coverage; staffing level vs. forecasted demand

*Use case:* Staffing adequacy signal for Location Health Score; labor optimization recommendations.

**Regulatory Databases — State health department inspection records (where publicly available)**

*Data ingested:* Health inspection results; violations; compliance notices

*Use case:* External compliance signal for regulated verticals (food service, childcare, healthcare-adjacent).

---

## Integration Strategy: API-First, Webhook-Based Real-Time Where Possible

### Integration Architecture Principles

**API-first:** All integrations use documented APIs rather than database-level connections or screen scraping. This ensures stability, vendor relationship quality, and compliance with data access terms.

**Webhook for real-time events, batch for history:** For events that affect the health score in real time (new audit completion, certification expiration, manager change), use webhook-based event streaming where the source system supports it. For historical data (training completion history, audit history, financial history), use daily or weekly batch sync.

**Data quality monitoring at ingestion:** Every integration pipeline includes data quality monitoring — schema validation, completeness checks (required fields present), freshness checks (data is not stale), and anomaly detection on the data pipeline itself (detect integration failures before they degrade AI quality). Data quality issues are surfaced to both the platform's data engineering team and the customer's admin user.

**Graceful degradation under data loss:** If an integration fails or a data source becomes stale, the health score confidence level is downgraded (not silently maintained). Users see: "This location's health score confidence is Medium because POS data has not been updated in 5 days. The financial dimension may not reflect current performance."

---

## Data Normalization Across Multi-Brand Environments

### The Multi-Brand Normalization Challenge

A franchise operations platform serving 200 brands will encounter 200 different data conventions. Location names that are meaningful in one brand's context are arbitrary IDs in another. Training module names are inconsistent. Audit finding categories use different terminology. Financial metrics are calculated differently.

Without normalization, cross-brand benchmarking is impossible — you cannot compare a QSR brand's "food safety score" with another QSR brand's "food handling compliance score" unless you know they measure the same thing.

### Normalization Strategy

**Canonical data model:** A master taxonomy for operational concepts — audit finding categories, training module types, corrective action categories, health score dimensions — that maps each brand's specific terminology to the platform's canonical taxonomy.

**Brand-specific mapping layer:** A configuration layer that maps each brand's data labels to the canonical taxonomy. This mapping is built during customer onboarding and maintained by the customer success team.

**Normalized benchmark pools:** Cross-brand benchmarks use normalized data only — location performance is compared against the canonical health score model, not against raw source data. This ensures that comparisons across brands are meaningful.

---

## The Franchise-Native Data Model

### Hierarchy Structure

```
Platform
└── Brand (franchise brand — e.g., "Fast Tacos by Brand X")
    └── Region (geographic region — e.g., "Southeast")
        └── District (district management territory — e.g., "Atlanta Metro District")
            └── Location (individual store/unit — e.g., "Atlanta Peachtree Location #247")
                └── Unit (sub-location for multi-concept locations — rare but required)
```

### Role-Aware Data Access

| Role | Data Access Scope |
|---|---|
| Frontline Employee | Own training records, own task assignments, own location's SOP library |
| Franchisee | All data for their owned location(s); brand average benchmarks (anonymized peer comparison) |
| Store Manager | Location operational data; employee training records for their staff |
| Multi-Unit Operator | All data for their owned locations; brand average benchmarks |
| Field Consultant | All locations in their assigned territory portfolio; district average benchmarks |
| District Manager | All locations in their district; regional average benchmarks |
| VP Field Operations | All locations in the brand; full benchmarking |
| COO / CEO | Full brand portfolio view; cross-brand executive summary |
| PE Operating Partner | Cross-portfolio view across all portfolio companies on the platform |
| Platform Admin | Full data access with audit logging |

---

## Cross-Brand Benchmarking Data as a Compounding Moat

Cross-brand benchmarking is the platform capability that improves most directly with platform scale.

**At 10 brands:** Brand-level averages are reliable; vertical benchmarks are not statistically significant.

**At 50 brands:** Vertical benchmarks (QSR, home services, fitness) are statistically meaningful for common metrics. Peer group benchmarks (QSR brands in Southeast with 50-200 locations) are reliable.

**At 200 brands:** Highly segmented peer groups are available — QSR brands in Southeast with 100-300 locations, 5-8 years old, with franchisee-owned model vs. company-owned hybrid. Practice difference analysis between top-quartile and bottom-quartile performers is statistically robust.

**At 500 brands:** Cross-vertical pattern detection is possible — operational patterns that predict risk across both QSR and home services. Intervention efficacy data is sufficient for high-confidence, segment-specific recommendations.

Each brand added to the platform improves benchmarks for every existing brand. This is the cross-brand data network effect — a compounding competitive advantage that is impossible for a new entrant to replicate without years of multi-brand deployment.
