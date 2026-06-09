# Franchise Support Desk: Product Strategy

---

## Problem

Franchisees, store managers, and frontline employees have operational questions every day. What is the correct holding temperature for product X? What is the approved protocol for handling a customer complaint? What training is required before a new employee can operate the fryer? What are the steps for a health inspection?

These questions are answered somewhere in the brand's SOP documentation, training materials, or operational playbooks. But finding the right answer requires searching through PDFs, navigating a training portal, or sending an email to the field consultant or HQ support team — all of which take time that a store manager in the middle of a lunch rush does not have.

The result is two failure modes: either the question goes unanswered and the employee guesses, creating operational inconsistency and compliance risk; or the question is emailed to HQ, joining a queue of support tickets that HQ support teams are chronically overwhelmed managing.

Industry estimates suggest that 60-70% of franchise support tickets are answerable by referencing existing brand documentation — but the documentation is not searchable or accessible in a way that enables self-service.

The Franchise Support Desk is an AI-powered knowledge management and support system that enables franchisees and store-level employees to get instant, accurate, source-cited answers to operational questions — and helps HQ support teams handle the remaining complex or sensitive questions more efficiently.

---

## Target Users

- Franchisees (operational questions about their business)
- Store Managers (in-shift operational reference)
- Frontline Employees (training-related questions)
- HQ Support Team (ticket management and quality oversight)

---

## Core AI Capabilities

**SOP Search and Answer (RAG-Based AI):**
A natural language question interface that searches the brand's own operational documents — SOPs, training materials, compliance guides, brand standards — and generates a plain-language answer with citations to the specific document, section, and page. The system does not generate answers from generic knowledge; it generates answers only from the brand's own approved content. Users see not just the answer but the source, enabling verification.

**Ticket Routing:**
When a question cannot be self-served from the SOP library, the system classifies the support request and routes it to the appropriate team — field consultant for operational support, compliance team for regulatory questions, training team for curriculum questions, HQ operations for escalations. Routing reduces the time spent by HQ support manually triaging inbound requests.

**Escalation Prediction:**
AI analyzes the content and pattern of support tickets to identify which ones are likely to escalate beyond a first-level response — for example, tickets indicating a franchisee in operational distress, tickets related to unresolved corrective actions, or tickets suggesting a systemic issue at a location. These are proactively elevated rather than waiting for the franchisee to escalate.

**Resolution Suggestions for Agents:**
For human agents handling escalated tickets, the system surfaces: the franchisee's Location Health Score and recent health score trend; any open corrective actions at the location; the most recent field visit summary; and relevant SOP sections that address the ticket topic. This context significantly reduces the time agents spend researching before responding.

**Ticket Pattern Analytics:**
System-level analytics showing which questions are asked most frequently, which SOP categories generate the most support tickets, and which locations generate the highest ticket volumes. These patterns are fed back into the LMS and SOP improvement processes — high-volume question categories indicate SOP clarity gaps or training deficiencies that should be addressed at the system level.

---

## Success Metrics

| Metric | Target |
|---|---|
| Self-service resolution rate | 70%+ of tickets resolved without human agent involvement |
| Average time to resolution (self-service) | Under 30 seconds for answered questions |
| Average time to resolution (agent) | Under 4 hours |
| Franchisee CSAT for support experience | 4.5/5 or higher |
| HQ support team ticket volume reduction | 40-50% reduction in tier-1 ticket volume |
| SOP improvement cycles triggered by ticket patterns | Monthly review cycle established |

---

## Integration with the Intelligence Platform

The Franchise Support Desk is integrated with the Location Health Score and the Field Consultant Workspace in two ways:

**Into the health score:** High support ticket volumes at a location are a signal in the Location Health Score (operational stress indicator). Escalation frequency is a franchisee engagement signal.

**Into the field consultant pre-visit brief:** Recent support tickets from a location — the topics raised, the frequency, and whether they were resolved — are included in the field consultant's pre-visit brief, giving the consultant context about what the franchisee has been struggling with since the last visit.

This integration turns the Support Desk from a cost reduction tool into a signal generation tool — adding another layer of operational intelligence to the platform's health model.
