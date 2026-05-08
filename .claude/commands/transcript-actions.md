---
description: Extract action items, decisions, and risks from a meeting transcript
---

# /transcript-actions

## Purpose

Parses a meeting transcript and extracts all action items, key decisions, open questions, and risks, plus a brief meeting summary. Saves 20-30 minutes of manual note cleanup after every client call.

## Usage

```
/transcript-actions $ARGUMENTS
```

`$ARGUMENTS`: File path to a `.txt` or `.md` transcript file.

## Inputs

- A meeting transcript exported from Teams, Zoom, Otter.ai, or typed notes
- Works best when the transcript includes speaker labels (e.g., "Sarah: We need to...")
- No minimum length required; works on partial or rough notes

---

Read the meeting transcript at: $ARGUMENTS

Produce the following sections:

**Meeting Summary** (3–5 sentences): Who attended, the stated purpose, and top outcomes or decisions.

**Decisions Made:**
- List each decision with context. Format: "[Decision]: [Rationale if stated]"

**Action Items:**
| # | Action | Owner | Due Date | Priority | Notes |
|---|---|---|---|---|---|

Extract all explicit and implied action items. If owner or due date is not stated, use [TBD] and flag it. Priority: High / Medium / Low based on language and context.

**Open Questions / Parking Lot:**
- Items raised but not resolved during the meeting

**Risks or Concerns Flagged:**
- Any risks, blockers, or concerns mentioned, including informal ones

Be thorough. Do not summarize away specifics. The value is in the detail.

---

## Example Output

**Meeting Summary:** Sprint 3 retrospective with 6 team members and 2 client stakeholders (May 6, 2025). Team reviewed velocity showing a 12% shortfall against plan. Main outcome: agreed to reduce scope on the reporting module and add one buffer week before UAT. Client stakeholders requested a revised project plan by Friday.

**Action Items:**
| # | Action | Owner | Due Date | Priority | Notes |
|---|---|---|---|---|---|
| 1 | Revise project plan with updated UAT dates | Sarah M. | Fri May 10 | High | PMO sign-off required |
| 2 | Send updated scope reduction memo to client | PM | Mon May 13 | High | Draft first, PM to review |
| 3 | Schedule UAT kick-off call with client SMEs | Coordinator | Wed May 8 | Medium | Include test script overview |
