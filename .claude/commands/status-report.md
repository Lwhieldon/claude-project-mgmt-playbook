---
description: Generate a weekly project status report from a CSV file or free-text project notes
---

# /status-report

## Purpose

Generates a structured weekly status report from project data or a free-text summary. Output is formatted for direct use in a client email or PowerPoint status slide.

## Usage

```
/status-report $ARGUMENTS
```

`$ARGUMENTS` — File path to a `status-data.csv` or a brief free-text description of the week pasted after the command.

## Inputs

- A CSV file with weekly project data (% complete, budget burn, issues, milestones) — see `sample-projects/acme-data-warehouse/status-data.csv` for the expected format
- Or a plain-text description: accomplishments, blockers, upcoming work, any open issues
- Optional: paste or reference last week's status for a comparison view

---

Read the project data or notes provided in: $ARGUMENTS

Generate a weekly project status report with the following sections:

**Overall Status:** [🔴 Red / 🟡 Amber / 🟢 Green] — one-sentence rationale

**Accomplishments This Week:**
- 3–5 bullet points tied to specific deliverables or milestones

**Upcoming (Next 2 Weeks):**
- 3–5 bullet points with target dates

**Risks & Issues:**
| Risk/Issue | Severity | Owner | Mitigation / Status |
|---|---|---|---|

**Action Items:**
| Action | Owner | Due Date | Priority |
|---|---|---|---|

Use professional, direct consulting language. No filler sentences. If data is missing or ambiguous, flag it explicitly with [NEEDS INPUT] rather than guessing.

---

## Example Output

**Overall Status:** 🟡 Amber — Sprint 4 velocity is 15% below plan due to delayed UAT environment setup; mitigation plan in progress.

**Accomplishments This Week:**
- Completed data migration scripts for Orders and Inventory modules
- Delivered revised data mapping document to client for sign-off
- Onboarded two new client SMEs to the UAT process

**Action Items:**
| Action | Owner | Due Date | Priority |
|---|---|---|---|
| Finalize UAT environment configuration | Dev Lead | Fri May 10 | High |
| Client sign-off on data mapping document | Client PM | Wed May 8 | High |
