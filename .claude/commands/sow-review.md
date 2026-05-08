# Purpose
Review a Statement of Work for scope clarity, delivery risk, and governance gaps.

# Prompt
Perform an SOW quality and risk review for consulting delivery leadership.

Steps:
1. Summarize scope, milestones, assumptions, and exclusions.
2. Identify ambiguous wording that could cause scope creep.
3. Flag delivery, dependency, and commercial risks.
4. Recommend negotiation or clarification points.
5. Provide a go/no-go readiness view.

# Expected inputs
- Path to `sow.md` (or folder containing it)
- Contract stage (draft/final)
- Priority concerns (optional)

# Example output
## SOW review summary
Scope covers discovery through go-live, but support model post-hypercare is underspecified.

## Key risk flags
| Area | Risk | Severity | Recommendation |
|---|---|---|---|
| Environment readiness | Client-owned dependencies lack due dates | High | Add dated client obligations schedule |
| Change control | No approval SLA for CR decisions | Medium | Define 5-business-day CR decision SLA |

## Clarifications to request
- Define success criteria for data reconciliation acceptance.
- State whether weekend cutover support is in scope.
- Add named approvers for milestone sign-off.
