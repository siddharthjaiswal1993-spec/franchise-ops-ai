# Lovable Prototype Demo Script

> 10-step demo script for https://nexus-foresight-hub.lovable.app following the DETECT -> DECIDE -> ACT -> VERIFY narrative.

**URL:** https://nexus-foresight-hub.lovable.app
**Duration:** 20-25 minutes
**Audience:** VP of Operations, COO, Director of Field Operations

---

## Demo Setup Context

Set the scene before opening the prototype: "Let me show you what operational intelligence looks like in practice. This is a prototype built around a concept I call 'signal to verified action' — a platform that detects operational risk before it shows up in your weekly report, recommends the right intervention, routes the action, and then verifies that it actually worked. Let me walk you through a live example."

---

## Step 1: Portfolio Health Overview

**What to show:** The main portfolio dashboard showing location health score distribution. Point out the breakdown: how many locations are Healthy, Watchlist, At Risk, Critical.

**Script:** "This is your portfolio health view. Every location in your system has a continuously updated health score — not a snapshot from last Friday's report, but updated as signals come in from your POS, your LMS, your audit system, and your customer reviews. Right now I can see at a glance that 3 locations are in Critical state. Let me show you what that means for one of them."

**Key point to land:** The health score is continuous, not periodic. You know right now, not when the report runs.

**Likely question:** "What data feeds this score?"
**Answer:** "POS sales data, LMS training completion, audit history, customer review signals, field visit frequency, corrective action closure rates — and we show you exactly which signals are driving the score for every location."

---

## Step 2: Zoom Into an At Risk Location

**What to show:** Click into a specific At Risk location. Show the location profile with the overall score (e.g., 61/100), the 6 dimension scores, and the score trajectory showing declining trend.

**Script:** "This is Location 247 in Atlanta. Health score: 61 — which puts it in At Risk. But more important than the number is the trajectory — it's been declining for 3 weeks. Let me show you why."

**Key point to land:** The score is explained, not just displayed. Every number has a reason.

**Likely question:** "Who is this score designed for — HQ or the franchisee?"
**Answer:** "Both. HQ sees the portfolio health distribution and uses it for visit prioritization. The franchisee sees their own score with peer benchmarking context — they know where they stand relative to comparable locations and exactly what they need to do to improve."

---

## Step 3: Score Explainability — Top Drivers

**What to show:** The score driver panel showing the top 3 factors pulling down the score for Location 247. Each driver shows the data source, value, and timestamp.

**Script:** "Here are the top 3 score drivers. The compliance dimension is down 18 points from last month — driven by two repeat violations from the last two audit cycles: food safety handling and opening procedures. The training dimension is down 12 points — training completion for the morning shift dropped from 78% to 52% after two staff departures three weeks ago. And the customer experience dimension is declining — Google reviews dropped from 4.2 to 3.8 over the last 30 days. Here's the critical insight: none of these signals individually crossed a threshold that would have triggered an alert in a traditional system. But together, they match a pattern the AI has seen at 34 other locations — and all 34 went on to fail their next audit if no intervention occurred."

**Key point to land:** Multi-signal pattern detection that no single-metric alert system can replicate.

**Likely question:** "How accurate is this prediction?"
**Answer:** "At this confidence level — 74% — the model is calibrated against 34 comparable historical cases. We show you the confidence level explicitly so you can decide how much urgency to apply. The governance architecture means every number here is traceable to a source."

---

## Step 4: DETECT Stage Summary

**What to show:** A brief pause to summarize the DETECT stage before moving to DECIDE.

**Script:** "That's the DETECT stage — the platform continuously aggregates multi-signal data and surfaces the locations where the pattern of signals suggests risk, before any individual metric has crossed an alert threshold. The AI is essentially looking at the combination of signals the way an experienced field consultant would — except it's doing it for every location in your portfolio, continuously, 24/7. Now let me show you what happens when it detects a pattern like this."

---

## Step 5: AI Recommendation — The DECIDE Stage

**What to show:** The AI-generated recommendation for Location 247. Show the recommended action, confidence score, rationale, source citations, and the comparable cases panel.

**Script:** "The platform has generated a recommendation: schedule a focused field visit within 7 days, with specific focus on food safety handling procedures and opening procedures. Confidence: 74%. Here are the three specific data points that drove this recommendation — and here are the 34 comparable cases showing that a focused visit with targeted corrective actions in these categories produced an average 15-point audit score recovery within 45 days. Critically — this recommendation does not execute until a field consultant reviews it and approves. The AI is a decision-support layer, not an autonomous system."

**Key point to land:** Source citations and human approval gates are the governance architecture that makes AI trustworthy in compliance-sensitive operations.

**Likely question:** "What if the field consultant disagrees with the recommendation?"
**Answer:** "They can modify or override it — and we capture the reason for that override in a structured format. That override data actually improves the model over time. If field consultants are consistently overriding recommendations in a specific situation, that tells us the model needs refinement for that scenario."

---

## Step 6: Pre-Visit Brief Generation

**What to show:** The field consultant workspace showing the AI-generated pre-visit brief for Location 247. Highlight the 30-second generation, the source citations, and the recommended focus areas.

**Script:** "Once the field consultant approves the visit, the platform generates a pre-visit brief — here, in about 30 seconds. It shows the current health score, the open corrective actions from the last visit with their ages and closure status, the training completion by employee for the last 30 days, recent customer review themes, the anomaly flags that triggered this visit, and recommended talking points for the franchisee conversation. A brief like this would take a field consultant 45 minutes to compile manually from 4-5 different systems. The AI does it in 30 seconds, with source citations for every data point."

**Key point to land:** 45 minutes to 30 seconds. 8+ hours per week per field consultant recaptured.

**Likely question:** "Does the field consultant actually trust a brief generated by AI?"
**Answer:** "In our early pilots, field consultants initially read the brief skeptically — and they found it was usually accurate and often surfaced things they hadn't noticed. Within a few weeks, the briefs become a trusted starting point that they add their own relationship context to, rather than starting from scratch."

---

## Step 7: Voice-to-Structured Notes (During Visit)

**What to show:** The mobile visit interface showing voice-to-structured notes. If possible, demonstrate a live voice capture or show a recorded example of a voice note being converted to tagged observations.

**Script:** "During the visit, the field consultant uses voice-to-structured notes. They speak their observations naturally — 'The opening checklist is not being completed before the first customer arrives, this is the third consecutive visit where I've observed this' — and the app transcribes it and auto-tags it: opening_procedure: non-compliant, repeat_finding: true. No typing. No post-visit transcription. The observations are structured and searchable the moment they're captured."

**Key point to land:** Unstructured voice becomes structured, searchable, comparable operational data in real time.

---

## Step 8: Corrective Action Plan Auto-Draft

**What to show:** The auto-generated corrective action plan drafted from the tagged observations. Show the specific action items, suggested owners, and timelines.

**Script:** "Before the field consultant leaves the location, the platform has auto-drafted a corrective action plan from the tagged observations. Food safety training for three specific employees — Sarah M., James T., and David K. — with a 14-day deadline. Opening procedure refresher for the morning shift — with a 21-day deadline. The franchisee reviews this plan with the field consultant during the visit, makes any adjustments, and acknowledges ownership of each item in the app. The whole process — plan generation, review, and sign-off — takes 10 minutes instead of the 45-60 minutes it would take to write manually and follow up by email."

**Key point to land:** Corrective action plans that actually get closed because they are structured, assigned, and tracked from the first moment.

---

## Step 9: Corrective Action Tracking and Escalation (ACT)

**What to show:** The corrective action pipeline for Location 247 showing the newly created actions with deadlines, owners, and status indicators.

**Script:** "The corrective actions are now tracked in the platform. The deadline clock is running. If Sarah, James, or David hasn't completed their training by Day 14, the platform sends automated reminders — and escalates to the field consultant and franchisee 3 days before the deadline. If the action expires unclosed, it escalates to the district manager. No action falls through the cracks."

**Key point to land:** From 55% corrective action closure rate to 85%+ because every action is tracked, reminded, and escalated systematically.

---

## Step 10: VERIFY — Outcomes Tracked

**What to show:** The verification dashboard showing the 45-day outcome record for Location 247 — health score recovery, corrective action closure rate, follow-up audit score.

**Script:** "Forty-five days later — here is the verification record. Three of four corrective actions were closed on time. The fourth — the opening procedure refresher — was closed 5 days late after a second escalation. The health score has moved from 61 (At Risk) to 73 (Watchlist). The follow-up audit score recovered from 72 to 81. The platform records this as an effective intervention — and that record is now part of the outcome dataset that makes the model's next recommendation more accurate. This is signal to verified action. Not just an alert. Not just a recommendation. A verified operational outcome."

**Key point to land:** This is what verified action looks like. The loop is closed. The outcome is documented. The model is smarter for the next time.

**Likely question:** "Can we export this data for our operations reviews?"
**Answer:** "Yes — the platform produces a structured outcome report that can be exported for your operations reviews or board reporting. The Executive Command Center generates a weekly AI brief that includes these outcome summaries at the portfolio level."

**Close:** "What you've just seen is the full DETECT -> DECIDE -> ACT -> VERIFY loop in franchise operations. From a multi-signal risk pattern detected before any KPI threshold was crossed, to a field visit with AI-generated preparation and real-time note capture, to a corrective action plan that was tracked, closed, and verified as effective — in 45 days. This is franchise operational intelligence. From signal to verified action."
