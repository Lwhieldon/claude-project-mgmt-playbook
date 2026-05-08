---
description: Provide a non-engineer-friendly review of technical changes focused on delivery risk
argument-hint: [pr-link-or-diff]
---

Review the supplied diff, PR, or technical notes at `$ARGUMENTS` and assess delivery impact.

Steps:
1. Summarize change intent in plain language.
2. Identify release, testing, and operational risks.
3. Check for documentation and training impacts.
4. Suggest PM actions before approval.

Keep explanations business-friendly and concise.

Expected inputs:
- PR link or diff text in `$ARGUMENTS`
- Planned release date
- Environment scope (dev/test/prod)

Reference output format:
## Plain-language summary
This change replaces a batch load job with event-based updates to reduce data lag.

## Delivery risk check
| Risk | Level | Why it matters | PM action |
|---|---|---|---|
| Monitoring gaps | Medium | Real-time jobs fail faster and noisier | Confirm alert thresholds before release |
| Rollback complexity | Medium | Event replay may duplicate records | Request tested rollback runbook |

## Recommendation
Proceed only after proving rollback in QA and confirming support team handoff notes.
