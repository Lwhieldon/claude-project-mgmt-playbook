---
description: Draft a structured change request with delivery, schedule, and commercial impact
argument-hint: [path-to-sow-or-change-details]
---

Create a formal change request draft suitable for client review using inputs at `$ARGUMENTS`.

Steps:
1. Define the requested change and business rationale.
2. Capture impact on scope, timeline, cost, and risks.
3. List options (recommended, minimum, defer).
4. Note dependencies and assumptions.
5. Add approval workflow and decision deadline.

Expected inputs:
- Existing SOW or baseline scope in `$ARGUMENTS`
- Requested change details
- Known effort/cost/time impacts (if available)

Reference output format:
## Change request: CR-004 — Add procurement analytics dashboard

### Rationale
Client leadership requires procurement savings visibility for Q3 board reporting.

### Impact summary
| Dimension | Baseline | Proposed | Delta |
|---|---|---|---|
| Scope | 12 dashboards | 13 dashboards | +1 dashboard |
| Timeline | Go-live 2026-07-10 | Go-live 2026-07-17 | +5 business days |
| Cost | $480,000 | $516,000 | +$36,000 |

### Approval needed
- Approver: Steering Committee Chair
- Decision deadline: 2026-05-20
