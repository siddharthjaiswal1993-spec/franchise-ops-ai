# Product Roadmap: 4-Phase AI-Native Franchise Intelligence

> **Relationship to the PRD:** `unified-operations-intelligence-prd.md` (§14) defines a tighter 4-phase, 0–24 month sequence (Foundation → FBC Intelligence → Close the Loop → Enterprise & Multi-Brand) scoped strictly to the four pillars (integrations, data model, intelligence layer, agentic workflow). This document's phases carry the fuller revenue, persona-unlock, and go-to-market narrative for the same underlying sequence — read the PRD for what ships, this doc for the business case around it.

---

## Roadmap Philosophy

The product roadmap follows the wedge expansion path: start with the highest-pain, fastest-ROI module (AI Field Consultant), build the data infrastructure that powers every subsequent module, and expand systematically through the intelligence stack. Each phase delivers customer value independently while building toward the full autonomous operations vision.

---

## Phase 1 (Months 0-6): AI Field Consultant MVP

### Theme: Win the Field Operations Problem

The first phase is entirely focused on making the AI Field Consultant module production-ready and deploying it with 10+ customers in pilot engagements. This phase is the foundation — everything that comes after depends on the data and trust that Phase 1 deployments create.

### Key Deliverables

1. **AI pre-visit brief engine** — multi-source data aggregation (LMS + audit history + basic health indicators), 30-second brief generation, source citation for every data point
2. **Voice-to-structured notes (mobile)** — iOS and Android app with offline capability, real-time transcription, auto-tagging with 80%+ tag accuracy
3. **AI corrective action plan drafting** — auto-populated from tagged observations, category-specific action templates, owner assignment, timeline suggestion, human review required
4. **Post-visit summary generation** — structured summary from tagged observations, 5-minute human review and submit workflow
5. **Visit effectiveness tracking** — 30/60/90-day health indicator change tracking post-visit, basic corrective action closure rate measurement

### New Personas Unlocked
- Field Consultants (daily active users)
- Director of Field Operations (active user and economic buyer)
- VP of Operations (champion and executive sponsor)

### Revenue Potential
- 8-week funded pilot: $15,000-$25,000 per brand
- Full FC platform contract: $80,000-$200,000 ARR per brand (Intelligence Tier pricing for FC module)
- Target: 10 pilots, 7 conversions, $700,000-$1.4M ARR from Phase 1 cohort

### Key Risks
- Integration complexity at customer sites delays pilot start dates
- Field consultant change management — adoption is a cultural challenge, not a technical one
- AI brief quality insufficient for trust at early pilots — requires human-review UX that maintains trust while model improves

---

## Phase 2 (Months 6-12): Location Health Score and Compliance Copilot

### Theme: From Field Intelligence to Portfolio Intelligence

With 6 months of structured field visit data, corrective action records, and multi-source integration data from Phase 1 deployments, Phase 2 builds the Location Health Score and the Compliance Copilot. This phase expands the platform from a field consulting tool to an operational intelligence platform.

### Key Deliverables

1. **Location Health Score v1** — 6-dimension composite score, continuous update, score state classification (Healthy/Watchlist/At Risk/Critical), top-3 driver explainability with source citations, peer benchmarking (brand average and peer group)
2. **Risk and Alerts Engine** — multi-signal anomaly detection, score state change notifications, rapid decline alerts, configurable routing by role
3. **Compliance Copilot v1** — risk-stratified audit scheduling, AI-generated corrective action plans from audit findings, compliance risk prediction model (accuracy target: 70%+), repeat violation pattern detection
4. **Executive Command Center v1** — portfolio health score distribution, top-10 risk dashboard, basic AI weekly brief (1-page), corrective action pipeline view
5. **POS integration expansion** — real-time webhook-based data ingestion for Toast and PAR Technology; financial dimension powered by POS data

### New Personas Unlocked
- COO (health score becomes the executive operational dashboard)
- CEO (Executive Command Center brief is their weekly touchpoint)
- Compliance Manager (Compliance Copilot is a dedicated compliance tool)

### Revenue Potential
- Phase 1 customers expand from FC module to Intelligence Tier: average +$75,000 ARR per brand
- Net revenue retention for Phase 1 cohort: 150-175%
- New logo acquisition with Intelligence Tier as the lead offer: 15+ new customers

### Key Risks
- Health score accuracy insufficient — requires validation against historical data before customer-facing deployment
- Data quality at customer locations is lower than expected — some locations have insufficient integration depth for reliable scoring
- Executive Command Center adoption — CEOs and COOs are busy; onboarding requires dedicated customer success support

---

## Phase 3 (Months 12-18): Operator Command Center and Executive Intelligence Layer

### Theme: Expanding to Every Stakeholder

Phase 3 expands the platform's reach to multi-unit operators (a new direct buyer) and deepens the executive intelligence capabilities to the board-reporting level. This phase is also when the cross-brand benchmarking capability reaches sufficient scale to be meaningfully differentiated.

### Key Deliverables

1. **Operator Command Center** — MUO portfolio health dashboard, cross-location performance comparison, portfolio risk prioritization, AI weekly portfolio brief, consolidated corrective action view, labor cost analysis
2. **Executive Command Center v2** — AI-generated board-ready metrics packages, risk concentration analysis, intervention effectiveness reporting (did our actions produce measurable outcomes?), PE Operating Partner multi-portfolio view
3. **Cross-Brand Benchmarking Engine** — peer group matching algorithm, top-quartile driver analysis, cross-brand benchmark data available for top 3 verticals (QSR, home services, fitness)
4. **Franchise Support Desk** — RAG-based SOP assistant, ticket routing and classification, escalation prediction, ticket pattern analytics, resolution suggestions for agents
5. **AI Agents v1 (supervised)** — AI Launch Coordinator (pre-opening milestone monitoring and escalation), AI Compliance Agent (risk-stratified audit scheduling automation with human approval)

### New Personas Unlocked
- Multi-Unit Operators (direct buyer with independent budget authority)
- PE Operating Partners (cross-portfolio intelligence view)
- Franchisees (Operator Command Center and Support Desk)

### Revenue Potential
- MUO direct sales: $25,000-$100,000 per MUO depending on portfolio size
- PE operating partner multi-portfolio expansion: $300,000-$1M+ per PE firm with 3+ portfolio companies
- Executive tier upgrade for existing customers: +$50,000-$150,000 per brand
- Total target ARR by end of Phase 3: $8-12M

### Key Risks
- AI Agent governance — supervised AI agents require careful human oversight UX design to avoid trust failures
- MUO go-to-market requires separate packaging and positioning from franchisor GTM
- Cross-brand benchmarking data quality — requires sufficient deployment scale for statistical significance in vertical-level benchmarks

---

## Phase 4 (Months 18-24): Autonomous Operations and Cross-Brand Intelligence

### Theme: From Operational Intelligence to Operational Autonomy

Phase 4 moves from AI-assisted human decisions to supervised AI agents that can initiate and execute certain operational actions within defined guardrails. This is not full autonomy — human oversight gates are maintained for all high-stakes decisions — but it represents a step-change in the efficiency of operational management for brands that have built sufficient trust in the platform through Phase 1-3 deployments.

### Key Deliverables

1. **AI Field Consultant Agent (supervised)** — autonomously generates pre-visit briefs, proposes visit schedules, drafts corrective action plans, and submits post-visit summaries. Human approval required for all actions before dispatch to franchisee.
2. **AI Compliance Agent (semi-autonomous)** — autonomously schedules and adjusts audit cadences based on risk scores; generates and routes corrective action plans; sends automated compliance reminders. Human override available; high-risk escalations always require approval.
3. **AI Executive Intelligence Agent** — autonomously generates weekly portfolio briefs; identifies emerging systemic trends; drafts board-ready metrics packages. Human review before distribution.
4. **AI Financial Analyst Agent (supervised)** — monitors for royalty anomalies; generates financial distress signals; drafts financial exception reports. Human review before action.
5. **Cross-Brand Intelligence Service** — a premium service that delivers cross-brand best-practice insights, vertical-level performance benchmarks, and AI recommendations informed by outcomes across the full platform dataset. Available to Intelligence Tier and Enterprise Tier customers.
6. **Outcome-Linked AI Reporting** — quarterly intervention efficacy reports showing how the platform's AI recommendations performed against predicted outcomes, with model calibration transparency.

### New Personas Unlocked
- CFO (financial AI agent capabilities)
- Board Members (autonomous board-ready report generation)
- PE Limited Partners (LP-ready operational metrics packages)

### Revenue Potential
- Autonomous Operations feature set justifies Enterprise Tier pricing uplift: +$20-40 per location per month for agent-enabled customers
- Cross-Brand Intelligence Service as a premium add-on
- Target ARR by end of Phase 4: $20-30M

### Key Risks
- Trust failure from AI agent errors — a single high-visibility AI agent error (incorrect corrective action dispatched, wrong audit scheduled) can damage trust across the customer base
- Regulatory uncertainty around AI in employment-related operational decisions
- Customer readiness varies — some brands are not ready for supervised AI agents even at Phase 4, requiring continued human-approval-first options
- Competitive response — by Phase 4, Delightree and new AI-native entrants may have launched competing intelligence products
