# Sample Project: Acme Corp — Data Warehouse Modernization

**Fictional project. All names, figures, and details are invented for training purposes.**

---

## Project Overview

Acme Corp is a mid-size specialty retailer ($1.2B revenue) migrating their on-premise SQL Server data warehouse to Snowflake on AWS. The engagement is a 6-month, fixed-price implementation covering data migration, a new reporting layer, and end-user training.

- **Contract value:** $485,000 fixed-price
- **Duration:** July 2025 – December 2025
- **Phase (as of this snapshot):** Build (Sprint 4 of 8)
- **Overall status:** 🟡 Amber — velocity behind plan due to delayed UAT environment

---

## Files in This Folder

| File | What it contains | Best slash command |
|---|---|---|
| `sow.md` | Full Statement of Work — scope, timeline, pricing, risks | `/sow-review sow.md` |
| `meeting-transcript.txt` | Sprint 4 retrospective with 8 attendees, several buried action items | `/transcript-actions meeting-transcript.txt` |
| `status-data.csv` | 12 weeks of project health data with a visible schedule trend | `/status-report status-data.csv` |

---

## Suggested Practice Sequence (5 minutes)

1. **Start with the SOW review** — flags the missing acceptance criteria and change control gaps:
   ```
   /sow-review sample-projects/acme-data-warehouse/sow.md
   ```

2. **Pull action items from the transcript** — there are 6 buried action items and 2 unresolved risks:
   ```
   /transcript-actions sample-projects/acme-data-warehouse/meeting-transcript.txt
   ```

3. **Generate a status report from the CSV** — Week 9 shows a budget spike worth flagging:
   ```
   /status-report sample-projects/acme-data-warehouse/status-data.csv
   ```

4. **Try a free-form prompt** — describe what you need without a slash command:
   ```
   Read status-data.csv and tell me if this project is in trouble. What should I tell the client sponsor?
   ```

---

## Things to Notice

- The SOW uses vague acceptance language ("fully functional") — a real risk in fixed-price contracts
- The meeting transcript has an action item buried in the middle of a long exchange that's easy to miss manually
- The status CSV shows budget burn accelerating in Weeks 9–10 while % complete stays flat — a warning sign
- The transcript includes a stakeholder disagreement about scope that never got formally resolved
