---
description: Create a client-ready weekly status report from project artifacts and data
argument-hint: [path-to-project-folder-or-files]
---

You are preparing a weekly consulting delivery status update.
Use `CLAUDE.md` defaults and produce concise, client-facing output using inputs at `$ARGUMENTS`.

Steps:
1. Read the provided project folder or files.
2. Infer overall RAG status with a one-line rationale.
3. Summarize accomplishments and next-period plan.
4. Extract risks/issues and decisions needed.
5. Output in markdown with clear headings and tables.

Expected inputs:
- Project folder path or explicit file list in `$ARGUMENTS`
- Reporting period (optional)
- Audience (client team, steering committee, or internal leadership)

Reference output format:
## Overall status: **AMBER**
Data model build is on track, but UAT start is at risk due to delayed source-system access.

## Accomplishments
- Completed dimensional model for finance and sales domains.
- Finalized data quality rules with client SME group.

## Plan next period
- Complete ETL pipeline performance tuning.
- Start UAT dry run with 6 priority scenarios.

## Risks / issues
| Item | Owner | Due | Mitigation |
|---|---|---|---|
| Source API credential delay | Client IT | 2026-05-14 | Escalate via weekly steering committee |

## Decisions needed
| Decision | Owner | Needed by |
|---|---|---|
| Approve UAT entry criteria exception | Program Sponsor | 2026-05-13 |
