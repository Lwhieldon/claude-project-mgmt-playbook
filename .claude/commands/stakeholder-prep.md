---
description: Prepare agenda, talking points, anticipated objections, and a follow-up email for a stakeholder meeting
---

# /stakeholder-prep

## Purpose

Prepares you for a stakeholder meeting: agenda, talking points, anticipated objections with responses, and a ready-to-send follow-up email template. Run this 30–60 minutes before a client call.

## Usage

```
/stakeholder-prep $ARGUMENTS
```

`$ARGUMENTS` — Describe the meeting: who you're meeting, the purpose, and any context (e.g., "CFO review of project status, we're 2 weeks behind schedule and need to discuss a scope reduction").

## Inputs

- Who the stakeholders are and their roles
- The meeting purpose or agenda
- Any relevant context: current project status, recent issues, what you need to get out of the meeting
- Optional: reference a project file, e.g. `/stakeholder-prep -- see sample-projects/acme-data-warehouse/sow.md; meeting with CFO to discuss Q2 timeline`

---

Using the meeting context provided in $ARGUMENTS, prepare the following:

**Meeting Objective:** One sentence — what a successful meeting looks like.

**Suggested Agenda** (with time allocations):
- Item 1 — X min
- Item 2 — X min
- ...

**Key Talking Points:**
For each agenda item, 2–3 crisp, evidence-backed bullets. Executive audience: lead with the bottom line, follow with supporting detail.

**Anticipated Objections / Tough Questions:**
| Question or Objection | Recommended Response |
|---|---|

**What You Need From Them:**
- Specific decisions, approvals, or inputs — be explicit

**Follow-Up Email Template:**

Subject: [Meeting topic] — Follow-Up and Next Steps

[Opening sentence referencing the meeting]

[Summary of key decisions or agreements — 2–4 bullets]

[Action items table with owner and due date]

[Closing with next scheduled touchpoint]

Use a professional, confident tone. For the objections section, be direct — anticipate the hardest questions, not just the easy ones.

---

## Example Output

**Meeting Objective:** Secure CFO approval for a 2-week timeline extension and agree on the scope reduction approach before the board update on May 15.

**Anticipated Objections:**
| Question | Recommended Response |
|---|---|
| "Why are we behind? You committed to this date." | "We hit two dependencies on client data access that weren't in the original plan. We flagged them in the Week 6 status report. Here's what we did to recover time..." |
| "What does a 2-week delay cost us?" | "Direct cost: approximately $X in additional resource time. Indirect: UAT readiness shifts to [date]. We've modeled three options — happy to walk through them." |
