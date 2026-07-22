# Unified Operations Intelligence for Multi-Location & Franchise Networks

> Product Requirements & Strategy — **PRD v1.0**, Draft for review
> Category: Franchise / multi-location ops · Primary users: Franchisors & field consultants · Author: Siddharth Jaiswal, Product

This is the canonical, versioned PRD for the platform described across `/strategy`, `/gtm`, and the rest of `/product`. Where this document and other product docs differ in specifics (e.g. Location Health Score dimension names, roadmap phase boundaries), **this PRD is the source of truth** — it is the most recent, most tightly scoped statement of what ships and in what order. Other docs retain the fuller strategic narrative and should be read as elaboration, not contradiction.

A franchisor and field-consultant platform that turns fragmented location data into health intelligence, grounded AI coaching, and an agentic loop from signal to verified outcome.

---

## 1. Executive Summary & Strategic Thesis

Multi-location and franchise networks sell consistency, but execution happens in hundreds or thousands of locations that no single system fully sees. Operations platforms know whether work got done. They do not know whether the location is healthy, because sales, profitability, customer sentiment, labor, and support signals live in separate systems. The result is that field business consultants (FBCs) manually stitch six or seven tools together before every coaching call, leadership has no unified view of location health, and the data shows execution but never root cause or business impact.

This product closes that gap. It brings the highest-signal external systems into one platform, normalizes everything around the franchise hierarchy, and computes a **Location 360** profile and a **Location Health Score** for every location. A grounded AI layer turns those signals into prioritization, root-cause explanations, and FBC coaching briefs. An agentic workflow then closes the loop: it detects risk, proposes a plan, helps the FBC act, and verifies whether the metrics actually improved.

> **The strategic thesis.** The category is moving from a system of execution to a system of intelligence. The winner will not be the platform with the most modules. It will be the one that closes the loop from signal to verified action across a network, grounded in a data model that understands how networks are actually owned and operated.

**What makes this defensible**

- **A franchise-native data model** with canonical location matching and ownership-hierarchy rollups that is hard to retrofit and hard to copy.
- **A verification loop** that generates proprietary outcome data — which interventions actually work — compounding over time into better recommendations.
- **Enterprise-grade governance**: citations, confidence, human approval, and financial-data permissioning that PE-backed and enterprise buyers increasingly require.

**Who it serves.** The buyer is operations or performance leadership at a franchisor, or a multi-unit operator, increasingly a private-equity-backed platform. The primary daily users are field business consultants and the operators and managers they coach. Winning requires both: ROI for the buyer and adoption-grade usability for the user, because low field adoption starves the intelligence the product depends on.

---

## 2. Problem Statement & Current State

Workflow data is necessary but not sufficient. A platform that only tracks task and audit completion can tell you a location is following the routine, but not whether the routine is working. A location can have perfect task completion and still be failing on sales and reviews. Real location health is a function of operational, financial, customer, labor, and support signals together.

**The current-state FBC workflow.** Before a coaching call or site visit, an FBC manually opens and reconciles, by hand:

- The **operations platform** for tasks, audits, training, compliance, and site-visit history
- **POS** for sales, transactions, and daypart trends
- **Accounting** for revenue, expenses, and profitability
- **Reviews** for customer sentiment and complaint themes
- **CRM** for franchisee lifecycle, tenure, and context
- **Payroll / HCM** for staffing and labor signals
- **Ticketing** for open operational issues

This is slow, coverage across a portfolio is uneven, and coaching quality depends on which consultant you get and how much time they have that week.

**The dependency chain.** Each gap compounds into the next:

| If you are missing | Then |
|---|---|
| Integrations | Insights are partial. You cannot reason about health from execution data alone. |
| A franchise-native data model | Integrated data is noise. Raw feeds mean nothing until matched to the right location and rolled up the right hierarchy. |
| An AI intelligence layer | Unified data is still hard to interpret. A human staring at five dashboards is back to the original problem. |
| Workflow automation | Insight does not become action. A great root-cause explanation that no one acts on changes nothing. |
| Verification | Teams cannot prove impact, improve the system, or defend its ROI. |

> **The problem in one line.** The product has to close all five gaps, in order, or it collapses back into a prettier dashboard.

---

## 3. Goals, Non-Goals & Success Criteria

**Goals**

- Replace the manual multi-system FBC prep with a single grounded brief per location.
- Give every location a continuously updated, explainable health score.
- Make coaching consistent across consultants by starting everyone from the same intelligence.
- Enable earlier intervention by detecting risk before lagging financials confirm it.
- Give leadership and owners a rollup view of network and portfolio health.
- Close the loop: tie every recommendation to an action and verify the outcome.

**Non-goals (explicitly out of scope)**

- Replacing the POS, accounting, or payroll systems. This platform reads from them; it is not a system of record for transactions or pay.
- Autonomous action without human approval. The AI proposes; the FBC decides.
- Directing franchisee labor or operations prescriptively in ways that raise joint-employer exposure. Guidance is decision support, not command.
- A generic conversational chatbot as the primary surface. Intelligence is pushed and prioritized, not only pulled.

**Success criteria**

| Outcome | How we know |
|---|---|
| FBCs trust and use the intelligence | AI recommendation acceptance rate; weekly active FBC usage |
| Prep is faster | Reduction in visit-prep time; locations reviewed per FBC per week |
| Coaching produces outcomes | Corrective-action closure rate; audit-score and review improvement on coached locations |
| The platform becomes the source of truth for health | Health-score coverage; percent of locations with complete data |

All targets are instrumented from launch. The lead metric is **AI recommendation acceptance rate** — the best single proxy for whether the intelligence is trusted and useful.

---

## 4. Users, Personas & Jobs to Be Done

Four user types, each with a distinct job. The product has to serve all four without forcing one into another's surface.

| Persona | Role | JTBD |
|---|---|---|
| **Franchisor leadership** | Buyer · COO / VP Operations | When I oversee hundreds of locations, I want to know which are at risk so I can direct resources and intervene before revenue, compliance, or brand standards decline. |
| **Field business consultant** | Primary user · FBC / district manager | When I prepare for a visit, I want the risks, history, and recommended coaching focus in one brief so my limited time goes to the locations and issues that matter most. |
| **Franchisee / operator** | User · single or multi-unit owner | When I run my locations, I want to know what needs attention today and how to improve, with help that feels like support rather than surveillance. |
| **Store manager** | User · location-level execution | When I execute the daily routine, I want clear priorities and corrective actions so I can fix the right things without guesswork. |

**The PE / multi-brand dimension.** Ownership in this category is consolidating. The decisive buyer is increasingly a professional multi-unit, often multi-brand operator, frequently private-equity backed. That buyer needs portfolio and ownership-group rollups as first-class views, standardized auditable reporting, and performance monitoring treated as a value-creation lever. The data model and permissions are designed for this from the start, not retrofitted.

> **Design tension to hold.** The same data serves the franchisor as risk visibility and the franchisee as improvement help. If the operator experiences it as surveillance, adoption dies, and adoption is what feeds the entire system.

---

## 5. Product Scope & the Four Pillars

The product is built on four layers, each a prerequisite for the next.

| Pillar | Description |
|---|---|
| **1. Integration layer** | Bi-directional connectors to POS, accounting, reviews, CRM, ticketing, and payroll. Framed as intelligence infrastructure: each system is a new dimension of location health. |
| **2. Franchise-native data model** | Canonical location matching and ownership-hierarchy rollups. Turns raw external feeds into structured, permissioned, source-of-truth data. |
| **3. Intelligence layer** | Location 360, Health Score with explainable sub-scores, risk drivers, root cause, benchmarking, and grounded AI prioritization and recommendations. |
| **4. Agentic workflow** | Detect, decide, act, verify. The FBC agent runs the visit lifecycle and the system verifies whether interventions moved the metrics. |

**Sequencing principle.** The pillars ship in dependency order. Integrations and the data model come first because the intelligence and agentic layers are worthless without them. The MVP deliberately picks a thin slice through all four rather than building any one pillar to completion in isolation.

> **The build philosophy.** Ship the smallest thing that delivers real value, proves the data model, and creates the data exhaust the rest of the strategy needs. Do not try to connect every system or build the full loop on day one.

---

## 6. Integration Strategy & Requirements

Integrations here are not plumbing. They are the intelligence roadmap. Every connected system is a new question the platform can answer.

| System | Example tools | Data needed | Business question answered |
|---|---|---|---|
| POS / Sales | Toast, Square, Lightspeed | Sales, transactions, daypart mix, voids, average ticket | Is the location growing or declining, and where? |
| Reviews | Google, Yelp | Rating trend, review volume, complaint themes | How do customers actually experience this location? |
| Financials / P&L | QuickBooks, NetSuite | Revenue, expenses, margin, labor and food cost | Is the location profitable, not just busy? |
| CRM | HubSpot, Salesforce | Franchisee profile, tenure, lifecycle, agreements | Who is this operator and what context shapes coaching? |
| Ticketing | Zendesk, Freshdesk, Intercom | Open tickets, volume trend, recurring themes | What operational issues are actively burning? |
| HCM / Payroll | ADP, Gusto, Workday | Staffing levels, turnover, labor hours, scheduling | Is the location staffed to succeed? |
| Marketing | Local campaign & ad platforms | Local spend, campaign performance, promo calendar | Is demand soft, or is execution the problem? |
| Scheduling | Workforce management | Shift coverage, schedule adherence | Are the right people on at the right times? |
| Internal ops | This platform | Tasks, audits, training, compliance, visits, actions | Is the operational routine being executed? |

> **On CRM specifically.** CRM contextualizes health rather than driving it. Operator tenure and relationship status change how an FBC reads a bad signal, but CRM is a later-phase integration: useful for tenure-aware coaching, not a health-score driver.

**Integration priority.** Sequencing principle: prioritize by `signal value × adoption ÷ integration cost`, not by whichever partner has the easiest API. POS and reviews move first because they are highest-signal and felt fastest; profitability follows; context systems come later.

| Priority | System | Signal value | Adoption | Rationale |
|---|---|---|---|---|
| P1 | POS | Very high | High | Fastest, hardest health signal |
| P1 | Reviews | High | Very high | Leading indicator, near-universal |
| P2 | Financials | Very high | Medium | Profitability truth owners care about |
| P2 | Ticketing | Med-high | Medium | Active pain, recurring-issue detector |
| P3 | HCM / Payroll | High | Medium | Labor as root cause of execution failure |
| P3 | CRM | Medium | Medium | Tenure and lifecycle context |
| P3 | Marketing / Scheduling | Medium | Lower | Separates demand gaps from execution gaps |

**Integration requirements**

| ID | Requirement | Priority |
|---|---|---|
| INT-01 | Support incremental and scheduled sync with configurable frequency per source. | MUST |
| INT-02 | Normalize every inbound record to the canonical location entity at ingestion. | MUST |
| INT-03 | Expose sync status, last-sync time, and failure reason per location per source. | MUST |
| INT-04 | Tolerate partial data: degrade gracefully and flag completeness rather than failing. | MUST |
| INT-05 | Provide an open API and webhook layer for systems without a native connector. | SHOULD |
| INT-06 | Honor source-of-truth rules when two systems report the same metric. | MUST |

---

## 7. Franchise-Native Data Model

Integrated data is noise until it is structured the way networks are actually owned and operated. This model is the foundation everything else stands on.

**Entities:** Brand, Franchisor, Franchisee, Ownership Group, Location Group, Territory, Region, Location, FBC, Store Manager, Employee, Audit, Task, Training Record, Compliance Doc, Support Ticket, Review, POS Transaction, Financial Metric, Corrective Action.

| Challenge | Why it matters |
|---|---|
| **Location matching** | The same store is "#4471" in POS, "Miami Lakes" in ops, another ID in accounting, and a Place ID in reviews. Resolving all of these to one canonical location across messy third-party data is real engineering and a genuine differentiator. |
| **Ownership hierarchy** | A franchisee can own many locations; an ownership group can span brands and regions. Signals must roll up so an owner sees their portfolio and a brand sees the network. |
| **Multi-brand rollups** | The decisive buyer runs multiple brands across regions. The ownership group and portfolio must be first-class entities, not an afterthought. |
| **Permissions in the model** | Visibility is enforced at the data layer, not the UI: franchisee sees own locations, FBC sees assigned portfolio, no one sees a peer's financials. |
| **Source-of-truth rules** | When POS sales and accounting revenue disagree, a defined authority per metric prevents every number from becoming arguable. |

**Data model requirements**

| ID | Requirement | Priority |
|---|---|---|
| DM-01 | Maintain a canonical location entity with a resolution layer mapping external identifiers, including human-assisted resolution for ambiguous matches. | MUST |
| DM-02 | Model ownership hierarchy (location → franchisee → ownership group → brand) and support rollups at every level. | MUST |
| DM-03 | Enforce row-level visibility derived from the hierarchy and role. | MUST |
| DM-04 | Store a per-metric source-of-truth configuration. | MUST |

---

## 8. Location 360 & Health Score

The insight layer turns normalized data into something a human can act on: one profile, one defensible score, ranked risk drivers.

**The insight stack**

- **Location 360:** one normalized profile per location fusing execution, financial, customer, labor, and support signals.
- **Location Health Score:** a composite with explainable sub-scores, so the number is always defensible.
- **Risk drivers:** the specific signals pulling a score down, ranked.
- **Root-cause analysis:** correlation across functions to separate symptom from cause.
- **Benchmarking:** fair, like-for-like comparison by format, daypart, tenure, and market.
- **Recommended actions and KPI impact prediction:** specific next steps tied to the risk drivers, with an estimate of which metric should move.

**Health Score input framework**

| Sub-score | Inputs | Source |
|---|---|---|
| Revenue health | Sales trend, average ticket, daypart mix | POS |
| Profitability | Margin, labor and food cost | Accounting |
| Customer experience | Rating trend, volume, complaint themes | Reviews, ticketing |
| Operational execution | Audit scores, task completion, corrective actions | Internal ops |
| Compliance | Compliance docs, audit failures | Internal ops |
| Labor | Staffing levels, turnover, schedule adherence | HCM / payroll |
| **Composite** | Weighted, benchmarked like-for-like | All sources |

**Requirements**

| ID | Requirement | Priority |
|---|---|---|
| LH-01 | Compute a composite health score and named sub-scores per location, recomputed on data change. | MUST |
| LH-02 | Every score is decomposable to its contributing signals and source records. | MUST |
| LH-03 | Benchmark like-for-like; never compare across incomparable formats or markets. | MUST |
| LH-04 | Allow brand-configurable sub-score weights. | SHOULD |

> This PRD's six-sub-score model (Revenue, Profitability, Customer Experience, Operational Execution, Compliance, Labor) is a tighter, launch-scoped version of the eight-category, six-weighted-dimension model in `location-health-score.md`. Treat this PRD's version as the MVP cut; the fuller model in `location-health-score.md` is the target state as Phase 3–4 (accounting, ticketing, payroll integrations) land.

**Worked example: a single location**

This illustrates the difference between data and intelligence. The signals alone do not tell an FBC what to do. The insight does.

> **Location: Miami Lakes** — Health: At Risk
> Sales −14% · Audit fails 3× · Rating 4.3 → 3.8 · Open tickets 8 · Overdue actions 5 · Training: High
>
> **AI insight.** This is very likely not an onboarding or knowledge problem. Training completion is high, so the team knows what to do. The pattern of repeated audit failures, a falling rating, open tickets, and overdue actions points to an operational-routine breakdown and a customer-experience issue, not a skills gap. The sales decline is most plausibly a downstream effect of the experience problem, not soft demand.
>
> **Recommended actions.** Schedule an FBC visit (prioritized by score). Coach the manager on opening and daily procedures where audit failures cluster. Assign and close the five overdue actions. Review complaint themes in ticket and review text. Monitor audit score and rating over 30 days to verify recovery.

> **Why the example matters.** The value is not that AI summarized the data. It is that the system distinguished a routine-and-CX breakdown from an onboarding problem, which sends the FBC to a completely different intervention. This exact case is codified as `LH-001` in the eval golden dataset — see `/evals/golden-datasets/location-health-score-cases.json`.

---

## 9. AI Intelligence Layer

AI here is an operational intelligence layer, not a generic chatbot. A chatbot answers questions you think to ask. An intelligence layer tells you which location to worry about before you ask, why, and what to do.

**Capabilities**

- Summarize location health in plain language and explain root causes across functions.
- Prioritize the locations that need attention now.
- Generate FBC pre-visit briefs and recommend coaching and corrective actions.
- Draft franchisee follow-up messages and executive rollup summaries.
- Predict which KPI an action should move, to prioritize effort.

**Guardrails, and why each matters**

| Guardrail | Why |
|---|---|
| Integrations first | Without unified data, AI can only summarize execution, the partial picture we started with. The integration layer is a prerequisite, not a parallel track. |
| Context is the game | "Sales are down" is noise. "Sales down 14% while reviews fell and audits failed 3×, but training is complete" is a diagnosis. |
| Source grounding | Every claim cites the underlying record. An FBC can tap a recommendation and see the audit or number behind it. No data means "insufficient data," not a guess. |
| Human approval | The AI proposes; the FBC decides. Nothing becomes an assigned action without sign-off, which keeps accountability with the human. |

**Requirements**

| ID | Requirement | Priority |
|---|---|---|
| AI-01 | Every AI output cites the source records it is grounded in. | MUST |
| AI-02 | Attach a confidence indicator; flag low-confidence outputs rather than presenting them as fact. | MUST |
| AI-03 | Return "insufficient data" when grounding is inadequate; never fabricate. | MUST |
| AI-04 | Route all recommendations through human approval before they become actions. | MUST |

AI-01 through AI-04 are exactly what the `/evals/golden-datasets/ai-grounding-and-guardrails-cases.json` suite is built to catch regressions on — see the `/evals` section below.

---

## 10. Agentic FBC Workflow & the Loop

The FBC agent runs the full visit lifecycle. This is where strategy becomes a daily-use product.

**The visit lifecycle**

| Stage | What the system does |
|---|---|
| **Before** | Ranks the FBC's locations by risk; generates a pre-visit brief (score, top risk drivers, root-cause hypothesis); summarizes changes since the last visit; suggests a coaching focus and drafts questions to ask the franchisee. |
| **During** | Risk-tuned mobile checklist; note, photo, and document capture; voice-to-structured-notes so the FBC talks instead of types; live theming of notes. |
| **After** | Generates a structured visit summary; creates corrective actions; assigns owners and due dates; sends follow-up nudges; links relevant SOPs and training to each action. |
| **Verify** | Checks whether actions were completed; monitors audit score, reviews, tickets, and revenue trend; updates the Location Health Score to reflect the outcome. |

> **The step everyone drops.** Verification is what makes the loop agentic rather than merely assistive. Checking whether the metric actually moved after the intervention is the difference between a smart assistant and an accountable system.

**The loop, formalized**

| | 01 Detect | 02 Decide | 03 Act | 04 Verify |
|---|---|---|---|---|
| Data | POS, audits, reviews, tickets, overdue actions | Full Location 360 | SOPs, tasks, training, contacts | Audits, reviews, tickets, sales |
| AI | Pattern & anomaly detection | Root cause & recommendation | Draft actions, owners, nudges | Check if metrics moved |
| Human | Confirm the risk | Approve or adjust plan | Assign, coach, sign off | Validate result |
| Output | Prioritized risk alert | Coaching plan | Assigned action plan | Verified impact, updated score |

**Workflow automation, tied to outcomes.** The point is not automation for its own sake. Every automated step is wired to a business outcome.

| Before (manual) | After (automated, outcome-linked) |
|---|---|
| FBC checks six or seven reports by hand | System assembles one grounded brief → saves prep time, more locations covered |
| FBC hand-prepares notes and coaching focus | System surfaces root cause and recommended focus → consistent coaching |
| FBC manually creates and emails follow-ups | System drafts actions, assigns owners and due dates → higher closure |
| FBC tracks actions in a spreadsheet or memory | System tracks closure and sends nudges → fewer stalled actions |
| No one checks whether the fix worked | System verifies metric movement → provable impact, better recommendations |

> **The discipline.** Automation that does not connect to an outcome is just motion. Every step here ends in a measurable result: time saved, closure raised, or impact verified.

---

## 11. Functional Requirements

Organized by epic. Each requirement has an ID and a MoSCoW priority. User stories follow the "as a [role], I want [capability], so that [outcome]" form.

**Epic A · Integrations & data foundation**

| ID | User story / requirement | Priority |
|---|---|---|
| FR-A1 | As an admin, I want to connect a POS, reviews, accounting, ticketing, or payroll system, so that location data flows in automatically. | MUST |
| FR-A2 | As an admin, I want to see sync health per source and location, so that I can trust the data is current. | MUST |
| FR-A3 | As the system, I want to resolve external identifiers to a canonical location, so that all data lines up. | MUST |
| FR-A4 | As an admin, I want to resolve ambiguous location matches manually, so that bad matches do not corrupt scores. | SHOULD |

**Epic B · Location 360 & Health Score**

| ID | User story / requirement | Priority |
|---|---|---|
| FR-B1 | As an FBC, I want a single profile per location across all sources, so that I stop checking many systems. | MUST |
| FR-B2 | As leadership, I want a health score per location that rolls up by region, owner, and brand, so that I can target attention. | MUST |
| FR-B3 | As an FBC, I want to see the ranked drivers behind a score, so that I know what is actually wrong. | MUST |
| FR-B4 | As an operator, I want fair benchmarking against comparable locations, so that targets feel legitimate. | SHOULD |

**Epic C · AI intelligence**

| ID | User story / requirement | Priority |
|---|---|---|
| FR-C1 | As an FBC, I want an AI pre-visit brief with root cause and coaching focus, so that I prepare in minutes. | MUST |
| FR-C2 | As an FBC, I want every AI claim to cite its source, so that I can trust and verify it. | MUST |
| FR-C3 | As leadership, I want AI executive rollups, so that I get network insight without an analyst. | SHOULD |

**Epic D · Agentic FBC workflow**

| ID | User story / requirement | Priority |
|---|---|---|
| FR-D1 | As an FBC, I want my locations ranked by risk, so that my week is prioritized by need. | MUST |
| FR-D2 | As an FBC, I want a mobile checklist with photo and voice capture, so that I record a visit hands-free. | MUST |
| FR-D3 | As an FBC, I want an auto-generated visit summary with corrective actions, owners, and due dates, so that follow-up is automatic. | MUST |
| FR-D4 | As an FBC, I want follow-up nudges on open actions, so that nothing stalls. | SHOULD |
| FR-D5 | As the system, I want to verify whether metrics improved after an intervention and update the health score, so that impact is provable. | MUST |

**Epic E · Acceptance criteria (representative)**

Each Must requirement carries explicit acceptance criteria. Representative examples:

| For | Acceptance criteria |
|---|---|
| FR-A3 | Given inbound records from two sources for the same physical store, when ingested, then both resolve to one canonical location with a confidence score, and matches below threshold are queued for human review. |
| FR-B2 | Given a location with data from at least the P1 sources, when the score is viewed, then a composite and all sub-scores display, each expandable to source records, and the score rolls up correctly to owner and brand. |
| FR-C2 | Given any AI recommendation, when displayed, then each claim links to the specific source records, and no uncited claim is shown. |
| FR-D5 | Given a closed corrective action, when 30 days elapse, then the system reports the change in the targeted metric and updates the health score and the verified-impact record. |

These four acceptance criteria are transcribed directly into the eval golden datasets (`FR-A3` → `DM-002`/`DM-003` in the data-model cases; `FR-B2` → `LH-002`; `FR-C2` → `AI-GR-001`–`004`; `FR-D5` → `AG-004`) so eval failures map straight back to a PRD requirement ID.

---

## 12. Non-Functional Requirements

The qualities the system must hold regardless of feature — the things enterprise and PE buyers actually evaluate.

| Category | Requirement | Priority |
|---|---|---|
| Performance | Location 360 and health score load within a target latency budget even with all sources connected; score recompute is incremental, not full-network. | MUST |
| Scale | Support networks from tens to tens of thousands of locations across multiple brands without architecture change. | MUST |
| Reliability | Integration sync failures are isolated per source and never block the rest of the platform. | MUST |
| Data freshness | Each source has a defined freshness SLA, surfaced to users as a per-location completeness and freshness indicator. | MUST |
| Security | Tenant isolation, encryption in transit and at rest, and identity-provider integration. | MUST |
| Data residency | Configurable residency for networks operating across jurisdictions. | SHOULD |
| Auditability | All data access, AI outputs, approvals, and overrides are logged and queryable. | MUST |
| Mobile | The FBC visit experience is fully usable on mobile, including degraded connectivity during a visit. | MUST |
| Accessibility | Meet a recognized accessibility standard for core workflows. | SHOULD |

---

## 13. Governance, Security & Permissions

Governance is not a compliance checkbox. It is what makes financial data and AI recommendations safe to deploy across independently owned businesses, and a signal of platform maturity.

| Control | What it does |
|---|---|
| Role-based access | Spans franchisor, franchisee, FBC, manager, and frontline, derived from the ownership hierarchy. |
| Financial-data permissioning | The most sensitive class, scoped tightly: a franchisee sees own P&L, an FBC sees operational metrics per brand policy, no one sees a peer's numbers. |
| Location-level access | Enforced at the data layer, not the UI. |
| Audit logs | Who saw and changed what, queryable for enterprise audit. |
| AI source citations | Every recommendation traces to underlying records. |
| Confidence scores | Low-confidence outputs are flagged, not presented as fact. |
| Human approval | Required before recommendations become assigned actions. |
| Override capture | When a human overrides the AI, it is recorded, protecting accountability and creating training signal. |
| Data sync & quality score | Per-location completeness and freshness, surfaced to users. |
| Source-of-truth rules | Authoritative system defined per metric. |

> **Why it is a differentiator.** Enterprise and PE-backed buyers increasingly require auditable AI. Built as a first-class capability rather than overhead, governance becomes a reason to buy, not a box to check.

---

## 14. Phased Roadmap: MVP to Enterprise

The pillars ship in dependency order. Each phase deepens the data model and the loop, so intelligence compounds rather than fragments.

| Phase | Theme | What ships |
|---|---|---|
| **Phase 1** (0–4 mo) | Foundation & first signal | POS + reviews + internal ops integrations; canonical location matching; Location 360; first health score with explainable sub-scores. |
| **Phase 2** (4–8 mo) | FBC intelligence | AI pre-visit brief with citations; risk ranking; mobile visit capture; auto visit summary with assigned actions and nudges. |
| **Phase 3** (8–14 mo) | Close the loop | Add accounting + ticketing; verification step and verified-impact tracking; root-cause across more functions; executive rollups. |
| **Phase 4** (14–24 mo) | Enterprise & multi-brand | Add payroll + marketing; ownership-group and multi-brand rollups; configurable weights; predictive decline models; full governance and residency. |

**The MVP, precisely.** Phase 1 plus the Phase 2 pre-visit brief is the smallest thing that delivers real value, proves the data model, and creates the data exhaust the rest needs. It is a thin slice through all four pillars, not any one pillar built to completion.

> **Sequencing rule.** Integrations and the data model first; intelligence and the agentic loop on top. Building the loop before the data exists produces a convincing demo and a useless product.

This four-phase sequence is a tighter, launch-focused reading of the fuller 4-phase roadmap in `product-roadmap.md` (AI Field Consultant → Location Health Score → Operator/Executive Command Center → Autonomous Operations). Treat phase names/dates here as the concrete near-term plan; treat `product-roadmap.md` as the longer-horizon expansion and revenue narrative.

---

## 15. Metrics & ROI Framework

Four groups. All instrumented from launch and framed as targets to track, not claimed results.

| A · FBC efficiency | B · Operational execution |
|---|---|
| Visit-prep time reduction | Corrective-action closure rate |
| Locations reviewed per FBC per week | Repeat-issue reduction |
| Weekly active FBC usage | Audit-score improvement |
| AI brief usage rate | Task-completion improvement |
| Time to create a visit summary | Compliance-risk reduction |

| C · Business outcomes | D · Platform value |
|---|---|
| Sales-trend improvement on coached locations | Integrations connected per location |
| Review-rating improvement | Percent of locations with complete data |
| Ticket-volume reduction | AI recommendation acceptance rate |
| Launch-readiness improvement | Health-score coverage |
| P&L-visibility improvement | Executive dashboard usage |

**ROI logic.** The case is built per location: hours saved across managers and consultants, points of audit-score improvement, basis points of cost variance, avoided closures from earlier intervention, and reduced support cost. A pilot demonstrating even a fraction of these on a defined cohort justifies network rollout.

> **The lead metric.** AI recommendation acceptance rate is the single best proxy for whether the intelligence is trusted and useful. Almost everything else follows from it.

This framework is the eval program's north star metric set — see `metrics-baseline.md` for how each offline eval metric (grounding accuracy, confidence calibration, hallucination rate) is expected to move the online metrics above.

---

## 16. Risks, Assumptions & Dependencies

The honest list. Each risk has a mitigation; pretending they do not exist is the real risk.

| Risk | Mitigation |
|---|---|
| **Data quality & location matching** — the whole system collapses if data is wrong or mismatched. | Canonical matching with human-assisted resolution; per-location quality score; source-of-truth rules; degrade gracefully on partial data. |
| **Adoption & surveillance perception** — if franchisees feel policed, adoption dies and starves the data. | Frame as operator support; give franchisees their own value; never expose peers' data; invest in onboarding and change management as product. |
| **AI trust** — one confident wrong recommendation poisons credibility. | Grounding, citations, confidence, "insufficient data" over guessing, and human approval before action. |
| **Integration fragility** — third-party APIs are brittle and vendor-specific. | Isolate failures per source; robust sync monitoring; open API fallback; sequence by value so early integrations are the most reliable. |
| **Legal / joint-employer** — over-prescriptive direction of franchisee operations raises exposure. | Position AI as decision support; preserve operator discretion; involve legal in workflow design. |

**Assumptions & dependencies**

- Networks use mainstream POS, accounting, and review systems with accessible APIs.
- FBCs are willing to shift prep into the platform if it demonstrably saves time.
- Brands will define source-of-truth and permission policies during onboarding.
- A pilot cohort with reasonable data completeness is available to prove ROI.

---

## 17. Appendix: Glossary & Open Questions

**Glossary**

| Term | Meaning |
|---|---|
| FBC | Field business consultant: the person who coaches a portfolio of locations through visits and calls. |
| Location 360 | One normalized profile per location fusing all connected signals. |
| Location Health Score | An explainable composite of revenue, profitability, customer experience, operations, compliance, and labor sub-scores. |
| Canonical location | The single internal identity a physical location maps to across all external systems. |
| Source of truth | The authoritative system designated for a given metric when sources disagree. |
| The loop | Detect → Decide → Act → Verify: the agentic cycle from signal to verified outcome. |

**Open questions for review**

- Default sub-score weighting: one model across brands, or brand-configured from day one?
- FBC visibility into franchisee financials: platform default or per-brand policy?
- Verification window: fixed 30 days, or per-metric and per-action-type?
- Build versus buy for the integration connector layer in Phase 1.
- Whether predictive decline modeling is Phase 3 or deferred to Phase 4.

> **Final point of view.** Tasks, audits, training, and compliance are workflow primitives. They tell you whether work happened, not whether the business is healthy. The strategic move is to connect the external data, understand location health, explain root cause, recommend action, and verify whether it worked. That is the shift from a system of execution to a system of intelligence, and it is where this category is heading.
