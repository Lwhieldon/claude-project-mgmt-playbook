---
description: Review a Statement of Work for scope risks, ambiguous language, and negotiation points
---

# /sow-review

## Purpose

Reviews a Statement of Work for scope risks, ambiguous language, missing protections, and negotiation opportunities. Best run before signatures, not after.

## Usage

```
/sow-review $ARGUMENTS
```

`$ARGUMENTS`: File path to a SOW document (`.md`, `.txt`, or `.pdf` if readable).

## Inputs

- The full SOW document
- Optional: append context after the file path, e.g. `/sow-review sow.md -- fixed-price contract, client wants to start in 3 weeks`

---

Read the Statement of Work at: $ARGUMENTS

Review the document across these dimensions and produce a structured assessment:

**Overall Risk Rating:** [🔴 High / 🟡 Medium / 🟢 Low]: one-sentence summary

**Scope Risks:**
- Ambiguous deliverables, undefined acceptance criteria, or scope that could "expand by interpretation"
- Quote the specific language and explain the risk

**Commercial Risks:**
- Pricing assumptions that may not hold, payment terms, penalty clauses, IP ownership, limitation of liability gaps

**Timeline Risks:**
- Aggressive milestones, dependencies on client actions not contractually required, holidays or blackout periods unaccounted for

**Assumptions & Exclusions:**
- List any assumptions that shift risk to the client. Are they explicit and strong enough?
- Flag any missing exclusions that should be there

**Change Control:**
- Is there a defined change control process? What triggers it? Who approves?

**Recommended Negotiation Points:**
- Top 3–5 specific changes to request before signing, with suggested replacement language

Use direct, practical language. This review is for the delivery lead, not the client.

---

## Example Output

**Overall Risk Rating:** 🔴 High. Acceptance criteria are undefined and the change control section is absent.

**Scope Risks:**
- "The team will deliver a fully functional data warehouse" (Section 2.1). "Fully functional" is undefined. Recommend replacing with a specific list of deliverables and a signed acceptance checklist.

**Recommended Negotiation Points:**
1. Add an Acceptance Criteria section specifying test pass rates and sign-off process
2. Insert a Change Control clause (suggested template available in `.claude/commands/change-request.md`)
3. Clarify client responsibilities for data access and SME availability (currently missing)
