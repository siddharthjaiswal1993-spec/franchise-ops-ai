# AI Use Case Prioritization Matrix

> 15 AI use cases ranked by business impact, implementation feasibility, data readiness, and demo/GTM value. Sorted by priority score.

---

## Scoring Criteria

| Criterion | 1 | 3 | 5 |
|---|---|---|---|
| **Business Impact** | Marginal efficiency gain | Meaningful operational improvement | Measurable ROI in weeks; prevents significant revenue loss |
| **Implementation Feasibility** | Requires 12+ months; novel technology | Requires 6-12 months; established approach | Requires 3-6 months; proven techniques |
| **Data Readiness** | Requires data not yet in platform | Requires new integrations (buildable) | Uses data already available or easy to integrate |
| **Demo/GTM Value** | Difficult to show value in demo; abstract | Visible in demo; resonates with secondary personas | Immediately compelling in demo; resonates with economic buyer |

---

## Prioritization Matrix

| Rank | Use Case | Business Impact | Impl. Feasibility | Data Readiness | Demo/GTM Value | Priority Score | Recommendation |
|---|---|---|---|---|---|---|---|
| 1 | Voice-to-Structured Notes | 5 | 5 | 4 | 5 | **19** | Build Now |
| 1 | AI Field Visit Summaries | 5 | 5 | 4 | 5 | **19** | Build Now |
| 1 | AI-Generated Corrective Action Plans | 5 | 5 | 4 | 5 | **19** | Build Now |
| 4 | SOP Assistant | 4 | 5 | 4 | 5 | **18** | Build Now |
| 5 | Location Health Scoring | 5 | 4 | 3 | 5 | **17** | Build Now |
| 5 | AI Executive Summaries | 5 | 4 | 3 | 5 | **17** | Build Now |
| 5 | Launch Delay Prediction | 4 | 5 | 4 | 4 | **17** | Build Now |
| 5 | Royalty Anomaly Detection | 5 | 4 | 3 | 5 | **17** | Build Now |
| 9 | AI Operational Benchmarking | 4 | 4 | 3 | 4 | **15** | Build Next |
| 9 | Compliance Risk Prediction | 4 | 4 | 4 | 3 | **15** | Build Next |
| 11 | Franchisee Health Scoring | 4 | 3 | 3 | 4 | **14** | Build Next |
| 11 | Escalation Prediction | 3 | 4 | 4 | 3 | **14** | Build Next |
| 13 | Peer Benchmarking Recommendations | 4 | 3 | 2 | 4 | **13** | Build Next |
| 13 | AI Performance Coaching | 4 | 3 | 2 | 4 | **13** | Build Next |
| 15 | AI Training Recommendations | 3 | 3 | 3 | 3 | **12** | Future |

---

## Build Now (Score 17-19)

These use cases should be in the active product roadmap for Phase 1 and Phase 2.

**Voice-to-Structured Notes, AI Field Visit Summaries, AI-Generated Corrective Action Plans** form the core AI Field Consultant MVP. All three require mobile app infrastructure, LMS integration, and audit history access — all buildable in Phase 1 with established technology (speech-to-text APIs, LLM prompting for generation, structured tagging taxonomy).

**SOP Assistant** requires the brand's SOP library in indexable digital format plus a RAG-based AI inference setup. Technically straightforward with current LLM API capabilities. High demo value makes it a strong sales tool.

**Location Health Scoring, AI Executive Summaries, Launch Delay Prediction, Royalty Anomaly Detection** are all Phase 2 items that require integration expansion (POS for royalty, multi-source for health score) but are technically achievable with current AI capabilities.

---

## Build Next (Score 13-15)

These use cases should enter the active roadmap in Phase 2-3, after the Build Now use cases are in production.

**AI Operational Benchmarking and Compliance Risk Prediction** require sufficient historical data from Phase 1 deployments to train reliable models. Both are high-value capabilities that unlock new buyer personas (compliance leaders for risk prediction; MUOs and franchisees for benchmarking).

**Franchisee Health Scoring, Escalation Prediction, Peer Benchmarking Recommendations, AI Performance Coaching** require richer data models and more complex model development. All are Phase 3 capabilities that depend on the data accumulated from Phase 1-2 deployments.

---

## Future (Score 12 and below)

**AI Training Recommendations** requires per-employee performance linkage to training completion data — a data modeling challenge that requires HRIS integration and operational performance attribution at the individual employee level. High long-term value but data infrastructure requirements push it to Phase 3-4.

---

## Demo Sequencing Recommendation

For a 20-minute demo following the DETECT -> DECIDE -> ACT -> VERIFY narrative:

1. **Open with Location Health Score** (DETECT) — the hook that shows the AI knows what's wrong before you ask
2. **AI-generated recommendation with source citations** (DECIDE) — the trust moment
3. **Pre-visit brief generation** (ACT setup) — show the 30-second synthesis
4. **Voice-to-structured notes** (ACT execution) — live demo moment; most impressive single feature
5. **AI corrective action plan draft** (ACT close) — auto-generated before leaving the parking lot
6. **Visit effectiveness tracking** (VERIFY) — close with the evidence that it worked
7. **Executive Command Center brief** (optional close for C-suite audience) — board-ready in one view
