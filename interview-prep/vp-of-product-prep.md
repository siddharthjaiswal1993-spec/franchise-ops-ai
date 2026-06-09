# VP of Product Interview Prep: FranConnect

---

## Role Context

The VP of Product at FranConnect is responsible for the product strategy and roadmap during what may be the most consequential 24-month window in the company's history. The franchise software category is at an inflection point. The right product bets now determine whether FranConnect defines the franchise operational intelligence category or watches challengers define it.

This prep document reflects a specific strategic point of view on the product decisions that matter most — not a comprehensive feature list, but a principled product strategy framework.

---

## Future of Franchise Software: The Category Evolution Thesis

Franchise software is in the middle of a four-stage category evolution:

- **Stage 2 (Current):** Systems of workflow — FranConnect's core strength; audit forms, onboarding workflows, LMS, royalty calculation
- **Stage 3 (Ongoing):** Systems of execution — mobile-first, real-time task management (Delightree's entry point)
- **Stage 4 (The opportunity):** Systems of intelligence — Location Health Score, AI Field Consultant, predictive compliance risk
- **Stage 5 (The future):** Systems of autonomous operations — AI agents, closed-loop execution without manual initiation

FranConnect has a structural advantage entering Stage 4: the franchise-native data model, the multi-lifecycle coverage, and the customer relationships. The product strategy must convert this starting advantage into a compounding data moat before AI-native entrants accumulate sufficient deployment scale to build their own.

The product VP's job is to ensure FranConnect wins Stage 4 — not just feature-parity with Stage 3 competitors.

---

## Product Vision Statement

**Become the AI-native operational intelligence OS for franchise brands and multi-location businesses** — the platform that turns every operational signal into verified action, enables every franchise system to run at peak consistency, and gives every leader the real-time intelligence they need to make confident decisions.

The key word in this vision is "verified." Not just intelligence — verified outcomes. The platform that closes the loop produces evidence that AI recommendations produce real results. That evidence is the competitive moat.

---

## Platform Strategy: Field -> Health Score -> Intelligence -> Agents

The platform strategy follows a deliberate expansion path that creates compounding data advantages at each stage:

**Field Intelligence First (AI Field Consultant):** Win the field consulting problem with a purpose-built AI tool that recaptures 8+ hours/week per field consultant. This creates the structured visit and corrective action data that powers the health model.

**Health Score as the Unifying Asset (Location Health Score):** Build the health model from the data created by field consulting deployments. The health score becomes the single language for operational health — used by FCs, compliance managers, COOs, and franchisees simultaneously. This is the platform's retention mechanism.

**Intelligence Expansion (Compliance Copilot, Executive Layer):** Once the health score is established as the operational standard, expand to compliance risk prediction, executive portfolio intelligence, and cross-brand benchmarking. Each expansion module creates new buyer relationships and new data sources.

**Autonomous Operations (AI Agents):** With 18-24 months of outcome-linked data from the field consulting and health scoring deployments, AI agents can operate with high reliability. The outcome data from Stages 1-3 is the training data that makes Stage 4 agents trustworthy.

---

## Wedge Prioritization Rationale

Why field consulting before health score? Because data quality.

The Location Health Score requires multi-source, high-quality, integrated data to be reliable. That data infrastructure takes 4-6 months to build at each customer deployment. If the health score is the first product the customer sees, the first 4-6 months are a waiting period — poor user experience, limited value, high churn risk.

If the AI Field Consultant is the first product, those 4-6 months are high-value utility (field consultants recapture hours immediately) AND data infrastructure construction. By the time the health score is ready to deploy, there is already 6 months of structured field visit and corrective action data in the system, and the AI model has meaningful training signal.

The wedge choice is not just about pain intensity. It is about sequencing the data creation that makes every subsequent module reliable.

---

## AI Roadmap: 3 Phases, 18 Months

**Phase 1 (Months 0-6): AI Field Consultant MVP**
Pre-visit brief generation, voice-to-structured notes, corrective action plan drafting, post-visit summary, visit effectiveness tracking. Integration stack: LMS + audit history + basic POS. Target: 10 pilot deployments, 7 conversions, case study evidence of ROI.

**Phase 2 (Months 6-12): Location Health Score + Compliance Copilot**
6-dimension health score with explainability, risk-stratified audit scheduling, AI corrective action plans from audit findings, compliance risk prediction model. Integration expansion: POS real-time + review platforms. Executive Command Center v1.

**Phase 3 (Months 12-18): Operator Command Center + Executive Intelligence + AI Agents v1**
MUO portfolio view, PE Operating Partner cross-portfolio view, board-ready metrics package, supervised AI agents (Field Consultant Agent, Compliance Agent). Cross-brand benchmarking at vertical level.

---

## Integration Strategy

Integration depth is the prerequisite for AI quality. The integration roadmap should be sequenced by health score signal contribution:

**Priority 1 (Phase 1 requirement):** LMS/Training (training completion data — 18% of health score), Audit platform (compliance data — 22% of health score)

**Priority 2 (Phase 2 requirement):** POS — Toast and PAR first (financial data — 20% of health score), Review platforms — Google Business Profile API (customer experience — 10% of health score)

**Priority 3 (Phase 3 enrichment):** HRIS/Payroll — ADP and Paychex (staffing stability data), Ticketing — Zendesk (support signal)

**Integration architecture requirements:** API-first (no screen scraping), webhook support for real-time events, data quality monitoring in the pipeline, graceful degradation when integrations fail (downgrade confidence, don't fail silently).

---

## Data Moat Strategy

The data moat has three layers that compound with platform scale:

**Layer 1 (Franchise-native data model):** Building it correctly requires franchise domain expertise. The model becomes more refined with every customer deployment that surfaces new edge cases in the franchise relationship structure.

**Layer 2 (Cross-brand benchmarking data):** Statistical significance for vertical benchmarks requires 100+ brands in the same vertical. This is only achievable at FranConnect's current scale — a new entrant cannot acquire this data.

**Layer 3 (Outcome-linked AI):** Every verified field visit outcome is a training data point. Every corrective action closure with health score measurement is a model improvement signal. The model improves continuously with every deployment, and the improvement compounds with scale.

**Tactical implication:** Every product decision should ask: "Does this create structured data that feeds the intelligence layer?" Features that do not generate data are less strategically valuable than features that do.

---

## Health Score Design Principles

1. **Explainability over accuracy.** A score that cannot explain itself will not be trusted, regardless of its predictive accuracy. Build the explainability architecture before worrying about incremental accuracy improvement.

2. **Multi-signal required.** A health score based on 2-3 data sources is not reliable enough for operational decision-making. The minimum viable health score requires at least 4 integrated data sources.

3. **Continuous update, not batch.** The score should update as new signals arrive, not on a nightly batch schedule. An audit failure should update the score within minutes.

4. **Benchmark by default.** Every score display should show the peer group context by default — not just an absolute number.

5. **Confidence is honest.** Data staleness and integration gaps should lower the confidence indicator, not silently inflate the score.

---

## Trust Architecture as Product Differentiator

The trust architecture is the product feature that enables enterprise sales. Without it, the conversation with compliance-sensitive enterprise buyers stalls at "how can we trust your AI?"

With it, the conversation becomes: "Here are your source citations, here is the confidence level, here is the human approval gate, here is the audit log, here is the override capture. Your compliance team can review our governance documentation. Your legal team can review our audit logs. Your operations team can flag AI recommendations they disagree with and see those flags incorporated into model improvement."

This is the AI conversation that enterprise franchise buyers need to have before they can deploy AI in their operations. The vendor that can have this conversation credibly will win the enterprise segment.

Build vs. buy decision for trust architecture: build the governance layer (audit logs, approval workflows, source citation infrastructure, override capture) as core platform infrastructure. Buy generic LLM capabilities (GPT-4 API for summary generation, speech-to-text for voice notes). The governance layer is the IP; the generic LLM capabilities are commodity services.

---

## Build vs. Buy Decisions for AI

| Component | Build or Buy | Rationale |
|---|---|---|
| Location Health Score model | Build | Franchise-native, proprietary training data, core IP |
| Compliance risk prediction model | Build | Franchise domain knowledge required; proprietary outcome data |
| Voice-to-structured notes transcription | Buy (Deepgram or Whisper API) | Commodity capability; specialized providers are 2-3 years ahead of in-house |
| SOP assistant (RAG) | Build framework, buy LLM | Franchise-native document retrieval is a build; LLM inference is a buy (OpenAI API) |
| Corrective action plan generation | Build prompt engineering, buy LLM | The templates and domain knowledge are a build; the generation is a buy |
| Executive brief generation | Build prompt engineering, buy LLM | Same as above |
| Data pipeline and integration infrastructure | Build | Franchise-native data normalization requires franchise domain expertise |
| Trust architecture (audit logs, approvals) | Build | Core product infrastructure; cannot be outsourced |

---

## 8 Smart Questions to Ask the VP of Product

1. "What is the current product investment split between maintaining and improving the core workflow platform vs. building the AI intelligence layer? And is that balance where you want it?"

2. "How are you thinking about the data model — specifically, how integrated is the current platform architecture, and what is the biggest technical debt challenge for the AI intelligence roadmap?"

3. "Where does the Location Health Score stand in the product roadmap? Has it been built, piloted, or is it still in design?"

4. "What is the product team's current philosophy on the build vs. buy decision for AI capabilities — specifically for LLMs and specialized AI providers?"

5. "How are you approaching the trust architecture question? Are enterprise customers already asking about AI governance, and how is the team thinking about source citations, confidence scoring, and audit logs?"

6. "What is the biggest constraint on AI feature velocity right now — data quality, integration depth, trust architecture, or engineering capacity?"

7. "How is the product team organized around AI — is there a dedicated AI/ML function, or is it embedded in the platform engineering team? And how are product and data science collaborating on health score development?"

8. "From a competitive standpoint, how is the product team thinking about Delightree's trajectory? Are you primarily competing in the same market, or are they serving a different segment?"
