# AI Field Consultant: Product Strategy

---

## Problem Statement

Field consulting is the most human-intensive, highest-cost, and least-tooled function in franchise operations. Field consultants — variously titled area managers, franchise business consultants, district managers, or regional operations managers — are the operational backbone of franchise systems. They visit locations, build franchisee relationships, identify performance problems, deliver coaching, and drive corrective actions.

Yet the tools they use for this work are embarrassingly primitive. A field consultant managing 40 locations in 5 states prepares visit plans from memory and spreadsheets, reviews data from 4-6 disconnected systems before each visit, captures observations in email or Word documents during the visit, spends 2-4 hours after each visit writing up notes and follow-up communications, and tracks corrective actions in a shared Google spreadsheet that is out of date the moment it is opened.

The result: field consultants spend an estimated 30-40% of their work time on administrative tasks that do not require their expertise, their relationships, or their judgment. That is 1.5-2 days per week of a $80,000-$120,000 annual salary employee spent on work that AI can do better and faster.

More importantly: because visit preparation is laborious, visit quality is inconsistent. Because note capture is unstructured, visit data cannot be analyzed across the portfolio. Because corrective action follow-up is manual, closure rates are low. Because visit outcomes are never measured, there is no evidence that field consulting is producing operational improvement — which makes it politically vulnerable in budget discussions.

The AI Field Consultant module solves all of this.

---

## Target Users

| User | Role | Primary Use Case |
|---|---|---|
| Field Consultant / Franchise Business Consultant | Individual contributor | Pre-visit preparation, in-visit note capture, corrective action drafting |
| District Manager | Manager of 3-5 FCs | FC portfolio monitoring, visit quality oversight, corrective action pipeline management |
| Area Development Manager | Regional leadership | Territory health monitoring, FC team performance, escalation management |
| VP of Field Operations | Department head | Portfolio-level visit effectiveness measurement, resource allocation, team performance analytics |

---

## Core Workflow (9 Steps)

**Step 1: Weekly Portfolio Prioritization**
The FC opens the platform Monday morning and sees their portfolio sorted by AI-recommended visit priority — not just by schedule, but by health score state, days since last visit, and open corrective action urgency. The FC reviews the priority list, adjusts as needed based on relationship context, and confirms the week's visit plan.

**Step 2: Pre-Visit Brief Generation**
24-48 hours before each visit, the FC opens the location's pre-visit brief. The AI generates a 1-page summary in under 30 seconds: current health score and dimension breakdown; open corrective actions from the last visit (with ages and closure status); training completion rate for the last 30 days; recent customer review themes; any anomaly alerts triggered in the last 14 days; recommended focus areas for the visit; and key staff context (recent manager change, new hires, certification lapses).

**Step 3: Contextual Review**
The FC reviews the brief, adds their own relationship context (conversation history with the franchisee, recent phone calls, known personal situations that affect the location), and confirms or adjusts the recommended visit focus areas.

**Step 4: Visit Execution with Voice-to-Structured Notes**
During the visit, the FC uses the mobile app to capture observations using voice-to-structured notes. The FC speaks their observations naturally ("The opening checklist is not completed before first customer — this is the third time I've seen this. Manager seems understaffed on morning shift."), and the app transcribes and auto-tags: `opening_procedure: non-compliant, staffing: concern, repeat_finding: true`.

**Step 5: Real-Time Corrective Action Flagging**
As tagged observations are captured, the app flags which observations should become corrective action items and pre-populates corrective action drafts. The FC can confirm, reject, or modify in real time during the visit.

**Step 6: AI-Generated Corrective Action Plan Draft**
Before the visit ends, the app has auto-generated a draft corrective action plan based on the confirmed corrective action items: specific action descriptions, recommended owners (field consultant, franchisee, specific named employees where available from LMS data), and suggested timelines based on severity.

**Step 7: Franchisee Review and Sign-Off**
The FC and franchisee review the corrective action plan together before leaving the location. The franchisee acknowledges ownership of their assigned actions in the app. The FC notes any commitments the franchisee made verbally that differ from the written plan.

**Step 8: Visit Summary Auto-Generation**
Within 30 minutes of leaving the location, the app generates a structured visit summary from the tagged observations, corrective action plan, and franchisee acknowledgment. The FC reviews the summary, makes any edits, and submits. Total time: under 15 minutes vs. 2-4 hours for manual write-up.

**Step 9: Visit Effectiveness Analytics**
The platform tracks corrective action closure rates, audit score changes, and health score trajectory in the 30-60-90 days following each visit. The FC sees a "visit effectiveness" indicator for each location that shows whether the visit produced measurable outcomes. This data is aggregated at the FC team level to show which consultants, which visit types, and which corrective action categories produce the most reliable improvements.

---

## MVP Features

**Pre-visit brief generation (required):** AI-generated 1-page location summary aggregating health score, corrective action history, training data, and recommended focus areas. Must include source citations for every data point.

**Voice-to-structured notes (required):** Mobile audio capture with real-time transcription and auto-tagging into predefined observation categories. Must work offline with sync.

**Corrective action draft from observations (required):** Auto-populates corrective action plan from tagged observations. Human review and approval before dispatch.

**Post-visit summary generation (required):** Auto-generates structured visit summary from tagged observations and confirmed corrective actions. Human review and submit.

**Visit effectiveness tracking (required):** Tracks health score and corrective action closure changes in the 30-60-90 days after each visit. Reports back to FC.

---

## Integration Requirements

| System | Data Ingested | Why It Matters |
|---|---|---|
| POS (Toast, PAR, Square) | Sales trend, labor cost %, transaction count | Financial dimension for health score; context for pre-visit brief |
| Audit platform (FranConnect, Zenput) | Audit score history, item-level findings, corrective action history | Compliance dimension; prior corrective actions for pre-visit brief |
| LMS (FranConnect LMS, Trainual) | Training completion by employee, certification lapses, overdue items | Training dimension; identifies staff knowledge gaps for visit focus |
| Review platforms (Google, Yelp) | Rating trend, review volume, sentiment keywords | Customer experience dimension; franchisee-facing context |

---

## AI Capabilities

**Pre-visit brief engine:** Multi-source data aggregation with citation tracking. Summary generation using structured templates with location-specific data insertion. Recommended focus area generation based on health score dimension analysis and historical visit patterns.

**Voice-to-structured notes:** Real-time speech-to-text transcription optimized for franchise operations vocabulary. Auto-tagging using an observation taxonomy (food safety, opening procedures, customer service, training, staffing, equipment, etc.). Confidence scoring on auto-assigned tags with easy human correction.

**Corrective action generation:** Maps tagged observations to corrective action templates based on finding category. Suggests owners from available HR/LMS data. Calibrates timelines based on severity classification and historical closure data for similar findings.

**Visit effectiveness measurement:** Causal analysis of health score changes following visits with corrective action completion as a mediating variable. Attribution of score improvements to specific corrective action categories.

---

## Trust Requirements

- Every data point in the pre-visit brief must show its source system and timestamp (users must be able to verify that the data is accurate and current)
- Confidence scores on all AI-generated corrective action plans (users need to know when the AI is uncertain)
- Human review required before any corrective action is dispatched to a franchisee
- Override capture: when a FC modifies or rejects an AI suggestion, the reason is captured for model improvement
- No AI recommendation should trigger an automated external communication without explicit human approval

---

## Success Metrics

| Metric | Baseline (Typical) | Target (Post-Deployment) |
|---|---|---|
| Admin time per FC per week | 12-15 hours | 4-6 hours (-60%) |
| Time-to-visit-summary submission | 18-36 hours | 1-2 hours (-90%) |
| Corrective action closure rate | 55-65% | 80-85% |
| Pre-visit brief satisfaction (FC rating) | N/A | 4.5/5 or higher |
| Visit effectiveness score (locations improving post-visit) | Unmeasured | 70%+ of visits show health score improvement within 45 days |
| FC time spent coaching vs. admin | 60% coaching | 80%+ coaching |

---

## Phased Roadmap

**Phase 1 (0-6 months): Core FC Workflow**
Pre-visit brief generation, voice-to-structured notes, corrective action drafting, post-visit summary, basic visit history. Integration: LMS + audit history. Target: MVP for 8-week pilot deployment.

**Phase 2 (6-12 months): Intelligence and Measurement**
Visit effectiveness analytics, FC portfolio health dashboard, cross-location trend identification, real-time anomaly alerts from POS and review platform integrations. Expanded integration: POS + review platforms.

**Phase 3 (12-18 months): Closed-Loop and Learning**
Outcome-linked recommendation improvement (AI recommendations refined by verified visit outcomes), FC performance benchmarking, team-level visit effectiveness reporting, AI coaching recommendations for FC skill development based on pattern analysis.
