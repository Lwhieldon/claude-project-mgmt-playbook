---
name: status-comms
description: Draft a status email, weekly report, or executive update from project data or a summary of the week
---

# Status Communications

Draft multi-format status communications from project data or a conversational summary of the week.

## Step 1: Understand What's Needed

Determine:
- **Audience:** Who is receiving this? (Client executive, internal team, steering committee, project sponsor)
- **Format:** Email, slide bullets, dashboard narrative, formal report, or all of the above
- **Source data:** CSV status file, free-text summary, or conversation context
- **Tone:** How sensitive is the current situation? Is there bad news to communicate?

If a `status-data.csv` or project notes are referenced, read them to inform the output.

## Step 2: Assess and Summarize Status

Before drafting, synthesize:
- Overall RAG status (🔴 Red / 🟡 Amber / 🟢 Green) with specific rationale
- Key wins this period
- Active risks or issues and their trajectory (getting better, stable, getting worse)
- Notable upcoming milestones in the next 2 weeks

## Step 3: Draft in Requested Format(s)

### Email Format
Professional status email suitable for forwarding to client stakeholders.

Subject line: `[Project Name]: Week [#] Status Update | [RAG Status]`

Structure:
- Opening sentence: overall status and one-line summary
- Accomplishments: 3–5 bullets
- Upcoming: 3–5 bullets with dates
- Risks/Issues: brief table or 2–3 bullets
- Actions needed from client: explicit asks, if any
- Closing

### PowerPoint / Slide Format
Short bullets optimized for a status slide:
- Overall: [RAG]: [one-line rationale]
- Accomplishments: 3–5 bullets (≤ 10 words each)
- Next 2 weeks: 3–5 bullets with dates
- Key risks: 2–3 bullets with owner
- Actions: table with Action | Owner | Due Date

### Dashboard / Narrative Format
2–3 paragraph narrative suitable for a project management dashboard or executive briefing note.

## Handling Bad News

When status is 🔴 Red or the situation is sensitive:
1. Lead with facts, not apologies
2. State the issue clearly in the first sentence
3. Immediately follow with: what caused it, what is being done, and by when the situation will be resolved or re-assessed
4. Avoid hedging language such as "we believe," "hopefully," or "it seems." Replace with direct statements or explicit uncertainty: "we do not yet know X; we will have an answer by [date]"

## Tone Calibration

| Audience | Tone | Lead With |
|---|---|---|
| C-suite / Board | Concise, decisive | Bottom line, then evidence |
| Project sponsor | Direct, collaborative | Status + what you need |
| Internal team | Frank, action-focused | Issues + next steps |
| Client PM | Professional, detailed | Accomplishments + risks |
