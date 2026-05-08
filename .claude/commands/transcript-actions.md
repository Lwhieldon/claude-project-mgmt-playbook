# Purpose
Turn meeting transcripts into clean actions, owners, due dates, and open questions.

# Prompt
Analyze the transcript and extract execution-ready follow-up items.

Steps:
1. Capture key decisions already made.
2. Convert implied tasks into explicit actions.
3. Assign owner if named; otherwise mark `Unassigned`.
4. Add target dates when stated; otherwise propose a date.
5. Flag ambiguities as open questions.

Output sections:
- Decisions made
- Action log table
- Open questions
- Suggested stakeholder follow-up note (5 sentences max)

# Expected inputs
- Path to transcript text file
- Meeting date (optional)
- Default target cadence (for proposing dates)

# Example output
## Decisions made
- UAT window moved from 27 May to 3 June.
- CRM integration testing will run in parallel with training prep.

## Action log
| Action | Owner | Due date | Notes |
|---|---|---|---|
| Confirm API whitelist in QA environment | Client IT lead | 2026-05-12 | Needed for integration tests |
| Publish revised UAT schedule | PMO | 2026-05-13 | Include business tester allocations |

## Open questions
- Who signs off on cutover rehearsal completion criteria?
- Is weekend deployment support contractually included?
