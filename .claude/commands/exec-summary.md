---
description: Compress a document into a 1-page executive summary for a senior or C-suite audience
---

# /exec-summary

## Purpose

Compresses a long document (SOW, report, assessment, or proposal) into a tight 1-page executive summary. Written for a C-suite or board audience who will not read the full document.

## Usage

```
/exec-summary $ARGUMENTS
```

`$ARGUMENTS`: File path to the document to summarize, optionally followed by audience context.

Example: `/exec-summary sample-projects/globex-erp-migration/sow.md -- audience is the CFO, focus on cost and timeline`

## Inputs

- The document to summarize (any format Claude can read)
- Optional: audience role and what they care most about
- Optional: specific sections to emphasize or de-emphasize

---

Read the document at: $ARGUMENTS

Write a 1-page executive summary using the following structure:

**Executive Summary: [Document Title]**
*Prepared for: [Audience if specified | Senior Leadership]*
*Date: [Today's date]*

---

**Situation** (2–3 sentences):
What is this document about? What decision or context does it address?

**Key Findings / What's in This Document:**
- 3–5 bullets covering the most important points
- Lead with the "so what": not just what it says, but why it matters

**Risks or Open Issues:**
- Top 2–3 risks, gaps, or items requiring attention or decision

**Recommendations / Proposed Next Steps:**
| Recommendation | Owner | Target Date |
|---|---|---|

**Bottom Line:**
One sentence. If the reader remembers one thing from this document, it should be this.

---

Use concise, executive-level prose. No jargon without explanation. Bullets should be ≤ 12 words. The total summary should fit on one printed page (approximately 350–450 words).

---

## Example Output

**Executive Summary: Acme Corp Data Warehouse SOW**
*Prepared for: CFO and Project Sponsor*
*Date: May 8, 2025*

**Situation:**
This Statement of Work defines the scope, timeline, and pricing for a 6-month data warehouse modernization project. It replaces Acme's on-premise SQL Server environment with a cloud-based Snowflake platform to support faster reporting and analytics.

**Key Findings:**
- Total contract value: $485,000 fixed-price
- Go-live target: December 12, 2025 (assumes client data access by June 1)
- Three workstreams: data migration, reporting layer, and user training

**Risks or Open Issues:**
- Acceptance criteria are not defined; "fully functional" language creates ambiguity
- Change control process is absent; any scope additions will require a CR process to be established

**Bottom Line:**
The SOW is directionally sound but needs two additions before signing: defined acceptance criteria and a change control clause.
