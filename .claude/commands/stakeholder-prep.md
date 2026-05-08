---
description: Prepare talking points, likely questions, and decision asks for stakeholder meetings
argument-hint: [path-to-project-folder-or-files]
---

Build a stakeholder briefing pack from project artifacts at `$ARGUMENTS`.

Steps:
1. Summarize current status in 5 bullets.
2. Identify audience priorities and concerns.
3. Draft meeting agenda with timeboxes.
4. Prepare likely questions with suggested responses.
5. List specific decisions/asks needed in the meeting.

Expected inputs:
- Stakeholder type (sponsor, steering committee, workstream lead)
- Project files/folder path in `$ARGUMENTS`
- Meeting duration and objective

Reference output format:
## Suggested agenda (45 min)
1. Delivery status and milestones (10)
2. Risks and mitigations (10)
3. Budget/scope changes (10)
4. Decisions required (10)
5. Next steps and owners (5)

## Likely questions and responses
- **Q:** Why did timeline confidence drop to amber?
  **A:** Integration environment access arrived 8 business days late; recovery plan keeps go-live intact with parallel testing.

## Decisions needed
| Ask | Decision owner | Deadline |
|---|---|---|
| Approve two-week UAT overlap model | Program Sponsor | 2026-05-15 |
