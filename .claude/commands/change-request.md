---
description: Draft a formal change request document from a description of the proposed scope change
---

# /change-request

## Purpose

Drafts a formal change request document from a description of the proposed change. Produces a structured document ready for client review and approval signature.

## Usage

```
/change-request $ARGUMENTS
```

`$ARGUMENTS` — Describe the change: what is changing, why, and any known impact on scope, timeline, or cost.

## Inputs

- Description of the requested change and why it's needed
- Known impact: additional effort (hours or days), timeline shift, cost delta
- Who is requesting the change (client or firm)
- Optional: reference the original SOW for baseline context

---

Using the change description provided in $ARGUMENTS, draft a formal change request document:

**Change Request**
**CR Number:** CR-[###]
**Date:** [Today's date]
**Project:** [Project name from CLAUDE.md]
**Requested By:** [Client or firm]
**Status:** Pending Approval

---

**1. Change Description**
Clear, specific description of what is changing and what is not changing. No vague language.

**2. Reason for Change**
Business or technical justification. Why is this change necessary or beneficial?

**3. Impact Assessment**

| Dimension | Baseline | Revised | Delta |
|---|---|---|---|
| Scope | [Original] | [Revised] | [Added / Removed] |
| Timeline | [Original end date] | [Revised end date] | [+/- days] |
| Estimated Cost | [Original] | [Revised] | [+/- $] |

**4. Assumptions**
List assumptions underlying this change estimate.

**5. Out of Scope**
Explicitly state what this change does NOT include to prevent scope creep on the change itself.

**6. Approval**

| Role | Name | Signature | Date |
|---|---|---|---|
| Client Sponsor | | | |
| Engagement Lead | | | |
| Client PM | | | |

---

## Example Output

**CR Number:** CR-004
**Change Description:** Add a custom inventory aging report to the data warehouse delivery. The original SOW included 12 standard reports; this adds one additional report with custom aging buckets (30/60/90/120+ days) defined by the client's finance team.

**Impact Assessment:**
| Dimension | Baseline | Revised | Delta |
|---|---|---|---|
| Scope | 12 standard reports | 13 reports (12 standard + 1 custom) | +1 custom report |
| Timeline | Jun 30, 2025 | Jul 14, 2025 | +14 days |
| Estimated Cost | $485,000 | $512,000 | +$27,000 |
