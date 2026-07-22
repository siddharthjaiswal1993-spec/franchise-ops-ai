# AI Evaluation Framework

This is the evals set for the AI intelligence layer and agentic FBC workflow described in `/product/unified-operations-intelligence-prd.md`. It exists because the PRD's central risk is trust: "one confident wrong recommendation poisons credibility" (Section 16), and the entire agentic loop is only as good as the guardrails in Section 9 (AI-01 to AI-04) and Section 10 (Detect → Decide → Act → Verify).

Every golden case below traces back to a specific PRD requirement ID, so a failing eval tells you exactly which requirement regressed — not just "the AI got something wrong."

---

## Structure

```
evals/
├── README.md                                          ← this file
├── test-prompts.md                                     ← sample prompts, happy path + edge cases
├── metrics-baseline.md                                 ← offline eval metrics, targets, and online metric linkage
└── golden-datasets/
    ├── location-health-score-cases.json                ← LH-01..04: score computation, decomposability, benchmarking
    ├── data-model-resolution-cases.json                ← DM-01..04, INT-06: canonical matching, source-of-truth
    ├── ai-grounding-and-guardrails-cases.json           ← AI-01..04: citations, confidence, "insufficient data", approval gating
    └── agentic-fbc-workflow-cases.json                 ← FR-D1..D5: detect/decide/act/verify loop
```

## How the four datasets map to the PRD

| Dataset | PRD section(s) | What a failure means |
|---|---|---|
| `location-health-score-cases.json` | §8 Location 360 & Health Score | The score is not defensible — the number moved without a traceable cause, or a sub-score can't be decomposed to source records. |
| `data-model-resolution-cases.json` | §7 Franchise-native data model, §6 Integration requirements | Two records for the same physical store did not resolve to one canonical location, or a metric conflict was resolved against the wrong source of truth. |
| `ai-grounding-and-guardrails-cases.json` | §9 AI intelligence layer | The AI fabricated a claim, hid low confidence, guessed instead of returning "insufficient data," or produced an action without a human-approval gate. |
| `agentic-fbc-workflow-cases.json` | §10 Agentic FBC workflow, §11 Epic D | The loop broke somewhere in Detect → Decide → Act → Verify — most commonly, verification never ran, which silently turns an "agentic" product back into an assistive one. |

## Priority convention

Each case carries the same MoSCoW priority as the requirement it tests (`MUST` / `SHOULD`), copied from the PRD. A `MUST`-priority case failing blocks release; a `SHOULD`-priority case failing is a tracked regression, not a blocker.

## Offline vs. online

This is the **offline** eval suite: fixed golden cases with expected outputs, run against any candidate model/prompt version before it ships. It is a prerequisite for, not a replacement for, the **online** metrics in the PRD's Section 15 (AI recommendation acceptance rate, override rate, etc.) and the AI Quality Metrics table in `/product/product-success-metrics.md`. See `metrics-baseline.md` for how the two connect.

## Running locally

These are portfolio/spec-stage golden datasets (JSON fixtures + expected-output rubrics), not a live model harness — there is no production model behind this repo to call. To use them:

1. Point whatever LLM/prompt you are evaluating (e.g. a Claude-based grounding prompt for the AI intelligence layer) at the `input` field of each case.
2. Score the model's output against `expected` and `must_not` using the rubric in that case's `grading` field.
3. Aggregate pass rates per dataset and compare against the thresholds in `metrics-baseline.md`.
4. Track failing case IDs over time — a case that regresses after a prompt change is the fastest signal you have that a guardrail broke.

Extend the datasets by adding cases with new sequential IDs (`LH-00N`, `DM-00N`, `AI-GR-00N`, `AG-00N`) — never renumber existing ones, since case IDs are referenced from the PRD and from postmortems.
