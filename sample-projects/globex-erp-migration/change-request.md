# Change Request — CR-002
## Globex Industries ERP Implementation

**CR Number:** CR-002
**Date Initiated:** April 22, 2026
**Project:** Globex Industries — SAP S/4HANA Implementation
**Requested By:** Linda Hargrove, VP of Operations, Globex Industries
**Status:** Pending Approval
**Priority:** High

---

## 1. Change Description

Globex's Operations team is requesting the development of a custom lot-tracking and traceability module within SAP S/4HANA's inventory management (MM-IM) area. This module would capture and expose lot-level genealogy data — supplier lot, receipt date, storage location, consumption date, and production order linkage — for all raw materials and work-in-process inventory.

The request covers:

1. **Custom lot genealogy data model** — extending SAP's standard batch management to capture four additional data fields not available in standard S/4HANA: supplier quality certificate number, country of origin (at lot level), shelf-life override flag, and customer-specific lot allocation.
2. **Custom Fiori application** — a purpose-built inventory traceability screen accessible to shop floor supervisors and quality technicians (approximately 85 users).
3. **Reporting integration** — three additional reports for the Quality Management dashboard.
4. **Data migration** — migration of historical lot data from the legacy system (estimated 4.2M lot records dating back to 2018).

---

## 2. Reason for Change

The Operations team states that lot traceability at this level of granularity is a regulatory requirement under their aerospace customer contracts (AS9100D compliance). They assert that this requirement was discussed during discovery and was assumed to be covered by SAP's standard batch management functionality.

**Firm's position:** Standard SAP batch management covers basic lot tracking. The four custom data fields, the custom Fiori application, and the historical data migration were not documented in the fit-gap analysis (D4, approved April 15, 2026) and are not referenced in the Blueprint (D5, under review). The Firm acknowledges that AS9100D compliance was discussed in discovery but maintains that the agreed scope was standard batch management, not the custom solution described here.

This represents a contested change — both parties have reasonable positions. Resolution may require executive review.

---

## 3. Impact Assessment

| Dimension | Baseline (SOW) | Revised (with CR-002) | Delta |
|---|---|---|---|
| Scope | Standard SAP batch management | Custom lot genealogy module + Fiori app + 3 reports + data migration | +1 custom RICEFW package (counted as 4 objects, bringing total to 16 vs. SOW cap of 15) |
| Timeline | Go-live Manufacturing: Apr 1, 2027 | Go-live Manufacturing: May 15, 2027 | +45 days for Manufacturing go-live |
| Estimated Effort | — | +730 hours (design, build, test, migrate) | +$182,500 at blended rate |
| Data Migration | Standard lot data | Standard + 4.2M historical lot records | +$22,000 data migration effort |
| **Total Cost Impact** | — | — | **+$204,500** |

*Revised contract total: $2,304,500 — exceeds current ceiling of $2,100,000 by $204,500. Requires CFO approval per SOW Section 8.*

---

## 4. Assumptions Underlying This Estimate

1. The four custom data fields are defined and finalized before design begins. Scope changes to the field list after design kickoff will be treated as a separate change request.
2. The Fiori application uses SAP standard UX patterns — no custom UI framework development.
3. Historical lot data quality is sufficient for migration without major remediation. A data profiling spike (8 hours, included in estimate) will validate this; if remediation is needed, a separate estimate will be required.
4. Globex's IT team will provide extract scripts for the legacy lot data by May 15, 2026.
5. UAT for this module will be incorporated into the existing UAT Cycle 2 schedule (Jan 16, 2027) — does not require a third UAT cycle.

---

## 5. What This Change Does NOT Include

- Custom lot traceability for finished goods (only raw materials and WIP as described above)
- Any changes to the Quality Management module beyond the three dashboard reports listed
- Customer-facing lot traceability portal or external system integrations
- Additional Fiori applications beyond the single shop floor traceability screen

---

## 6. Options for Consideration

The Firm presents three options for Client consideration:

| Option | Description | Cost | Timeline Impact |
|---|---|---|---|
| A — Full CR | Implement as described above | +$204,500 | +45 days to Manufacturing go-live |
| B — Standard Only | Use SAP standard batch management; defer custom work to post-go-live Phase 2 | $0 | No impact |
| C — Partial | Implement custom data fields and reports only; defer Fiori app and historical migration | +$67,000 | +10 days |

**Firm recommendation:** Option B or C. Going live with standard functionality and planning a post-go-live enhancement is lower risk than extending the build phase. However, if AS9100D compliance cannot be met with standard functionality, Option A is necessary and the timeline extension is justified.

---

## 7. Decision Required

A decision is requested by **May 2, 2026** to preserve any chance of maintaining the April 2027 go-live date. Delay beyond May 2nd will require re-evaluation of all three options.

---

## 8. Approvals

| Role | Name | Decision (Approve / Reject / Defer) | Signature | Date |
|---|---|---|---|---|
| Globex CFO | _________________ | _________________ | _________________ | _________________ |
| Globex VP Operations | Linda Hargrove | _________________ | _________________ | _________________ |
| Firm Engagement Lead | _________________ | _________________ | _________________ | _________________ |
| Firm Principal | _________________ | _________________ | _________________ | _________________ |
