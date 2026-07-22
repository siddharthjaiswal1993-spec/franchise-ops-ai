# AI Product Judgment — AI-Native Franchise Operations GTM Strategy

---

## Decision 1: Location Health Score as the single product anchor

**What:** The platform is anchored around a single, composite, explainable Location Health Score per location — not a dashboard of separate metrics.

**Why:** Franchise operations leaders look at 15+ data streams today. What they lack is not more data; it is a single answer to "is this location healthy?" A composite score that synthesises operational, financial, compliance, and customer signals into one number — with the ability to drill into contributing factors — provides the answer that the existing tool stack cannot.

The alternative (a dashboard of separate indicators) preserves the fragmentation problem. A field consultant looking at 12 separate charts still has to synthesise them manually to form a judgment. The composite score does that synthesis and presents the conclusion.

**What this reflects:** When users have too much information, the product's job is to synthesise, not to display. Adding more data surfaces to an already-overloaded user makes the problem worse. The right product decision is to reduce the signal to a decision-relevant summary.

---

## Decision 2: DETECT → DECIDE → ACT → VERIFY as the architecture, not just messaging

**What:** The four-stage loop is not a positioning framework — it is the architecture. Each stage has specific functionality: signal ingestion (DETECT), root cause AI analysis (DECIDE), recommended action routing (ACT), and outcome verification (VERIFY). The platform is incomplete if any stage is missing.

**Why:** Most operational software solves one or two stages. Audit tools detect; they do not recommend. Task management tools act; they do not detect or verify. The full loop creates a value that no individual stage provides: the ability to measure whether interventions worked, which closes the feedback loop that makes the detection model improve.

Without VERIFY, there is no learning signal. Without ACT, the recommendations are just insights. Without DECIDE, the detections are just alerts. The product value is in owning all four.

**What this reflects:** End-to-end loop ownership is a product strategy decision. It is harder to build, harder to sell (requires more stakeholder buy-in), and harder to maintain. But the defensible position — the moat — is in the full loop, not in any individual stage.

---

## Decision 3: AI Field Consultant as the trust-building wedge

**What:** The AI Field Consultant module (augmenting field consultant visit workflows with pre-visit preparation, real-time intelligence, and post-visit action routing) is the first capability to ship — not the most strategically interesting capability (portfolio intelligence).

**Why:** Field consultants are the most operationally embedded people in the platform's user base. They visit locations, they have direct relationships with franchisees, and they have domain expertise to evaluate whether the AI is generating useful context.

Starting with field consultant workflows has a trust-building function: the AI system earns credibility with the most skeptical and most domain-expert users first. If it generates useful pre-visit intelligence for a field consultant who knows the location well, it will generate useful intelligence for an analyst who does not.

**What this reflects:** In enterprise AI, the product earns trust in the order: most skeptical user → most high-stakes workflow → most strategic value. Starting with portfolio intelligence (the most interesting product) before earning trust from field consultants (the most skeptical users) is the wrong sequencing.

---

## Decision 4: Explainable root cause over black-box prediction

**What:** The Location Health Score includes an explainable root cause analysis — the AI explains why the score is low, not just that it is low.

**Why:** A field consultant who sees that Location 047 has a health score of 52 needs to know whether the primary driver is a sales decline (operational problem), a compliance gap (process problem), or a franchisee relationship issue (people problem). The response is different in each case. A score without a root cause explanation is an alert, not an action trigger.

The explainability requirement also functions as a quality filter: the AI is forced to produce an explanation that a domain expert can evaluate. If the explanation is wrong or implausible, the field consultant rejects it. That rejection is the feedback signal that improves the model.

**What this reflects:** In domain-expert contexts, unexplained AI outputs do not get acted on. The explanation is not supplementary to the recommendation — it is the mechanism by which the expert validates whether to act.
