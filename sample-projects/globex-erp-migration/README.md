# Sample Project: Globex Industries — ERP Migration (SAP S/4HANA)

**Fictional project. All names, figures, and details are invented for training purposes.**

---

## Project Overview

Globex Industries is a mid-size discrete manufacturer ($780M revenue, 2,200 employees) replacing their 15-year-old SAP ECC 6.0 system with SAP S/4HANA. This is a greenfield implementation with a "clean core" approach — minimal customization, heavy reliance on standard SAP processes with business process redesign where needed.

- **Contract value:** $2.1M (time & materials, $350K/month cap)
- **Duration:** January 2026 – June 2027 (18 months)
- **Phase (as of this snapshot):** Blueprint / Design (Month 4)
- **Current challenge:** Client is requesting a custom inventory module that was not in the original scope — a significant scope change with a contested price tag

---

## Files in This Folder

| File | What it contains | Best slash command |
|---|---|---|
| `sow.md` | Full Statement of Work — scope, phases, assumptions, T&M pricing | `/sow-review sow.md` |
| `change-request.md` | Drafted CR for the custom inventory module request | Review directly; use `/exec-summary change-request.md` for a summary |

---

## Suggested Practice Sequence (5 minutes)

1. **Review the SOW** — look for the T&M cap language, assumptions about client resource commitment, and the change control provisions:
   ```
   /sow-review sample-projects/globex-erp-migration/sow.md
   ```

2. **Summarize the change request for an executive audience** — the CR is detailed; practice compressing it:
   ```
   /exec-summary sample-projects/globex-erp-migration/change-request.md -- audience is the CFO
   ```

3. **Prep for a difficult conversation** — practice the stakeholder prep command:
   ```
   /stakeholder-prep meeting with Globex CFO to discuss CR-002 (custom inventory module); she is skeptical of the added cost and believes it should have been in the original scope
   ```

4. **Draft the change request from scratch** (advanced) — delete `change-request.md` and regenerate it:
   ```
   /change-request Adding a custom inventory lot-tracking module to the S/4HANA implementation. Client asked for it in Month 3. Adds 6 weeks and approximately $180K in effort. Client believes it was implied in the original scope; we believe it is new work.
   ```

---

## Things to Notice

- The SOW has a T&M cap — this is different from Acme's fixed-price structure; the risk profile is different
- The change request document has a deliberately ambiguous "Reason for Change" section — is this a new requirement or something that was missed in scoping?
- The SOW's client responsibility section is weaker than it should be — SME availability is "encouraged" rather than contractually required
- This CR represents ~8% of total contract value — large enough to require escalation
