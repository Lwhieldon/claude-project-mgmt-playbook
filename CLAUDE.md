# Project Leadership: Claude Code Context

This file gives Claude persistent context about who we are, how we work, and the standards that apply to every task in this project. Edit the `[PLACEHOLDER]` fields before your first session.

---

## Firm & Practice Context

- **Firm:** [YOUR FIRM NAME]
- **Practice:** [e.g., Enterprise Advisory & Transformation]
- **Engagement type:** [e.g., ERP implementation / Data modernization / Process transformation]
- **Client:** [CLIENT NAME]: [one-liner: industry, company size, what they do]
- **Engagement phase:** [e.g., Discovery / Design / Build / UAT / Hypercare]
- **Engagement lead:** [Your name and title]
- **Key client contacts:** [Name, Title; Name, Title]
- **Contract value / duration:** [e.g., $850K / 12 months ending Dec 2025]

---

## Communication Standards

All client-facing content must be:

- **Professional and precise**: no filler phrases, no hedging without substance behind it
- **Audience-appropriate**: executive summaries at the C-suite level; working docs for the delivery team
- **Action-oriented**: every recommendation names an owner and a deadline
- **Formatted for reuse**: headers, bullets, and tables so output drops into PowerPoint or Word with minimal editing

Internal working documents may be more direct and less formal.

When tone is not specified, default to **professional consulting** style: confident, concise, recommendation-forward.

---

## Confidentiality Rules

- **Never paste raw client data into a prompt.** Sanitize or anonymize first.
- Treat all PII, financial figures, and proprietary process details as confidential.
- When in doubt, describe the data structure rather than sharing the data itself.
- Store session-specific sensitive notes in `CLAUDE.local.md` (gitignored), not here.
- Do not include client names or identifying details in commit messages.

---

## Common Artifact Types

| Artifact | Purpose | Key Sections |
|---|---|---|
| Statement of Work (SOW) | Defines scope, timeline, cost | Scope, Deliverables, Assumptions, Pricing, Change Control |
| Status Report | Weekly engagement health update | RAG status, Accomplishments, Milestones, Risks/Issues, Actions |
| Change Request | Documents scope changes formally | Description, Impact (scope/time/cost), Approvals required |
| Executive Summary | Compresses a document for senior audience | Situation, Key findings, Recommendations, Next steps |
| Meeting Summary | Captures decisions and actions from a meeting | Attendees, Decisions, Action items (owner + due date) |
| Risk Register | Tracks project risks over time | Risk, Likelihood, Impact, Mitigation, Owner, Status |

---

## Default Output Formats

- **Status:** Use RAG indicators (🔴 Red / 🟡 Amber / 🟢 Green) for overall status and each workstream
- **Action items:** Always include: Action, Owner, Due Date, Priority (High/Med/Low)
- **PowerPoint-ready content:** Short bullets (≤ 12 words), no nesting deeper than 2 levels
- **Word/email content:** Full sentences, structured headers, professional closing
- **Tables:** Use Markdown tables; they paste cleanly into Word and most PM tools

---

## Available Slash Commands

Type `/` in Claude Code to browse these commands, defined in `.claude/commands/`:

| Command | What it does |
|---|---|
| `/status-report` | Generate a weekly status report from a CSV or free-text summary |
| `/transcript-actions` | Extract action items, decisions, and risks from a meeting transcript |
| `/sow-review` | Review a Statement of Work for risks, gaps, and negotiation points |
| `/stakeholder-prep` | Prepare talking points and a follow-up email for a stakeholder meeting |
| `/change-request` | Draft a formal change request document |
| `/code-review-light` | Plain-English review of a code file or data artifact |
| `/exec-summary` | Compress a long document into a 1-page executive summary |

---

## Available Skills

Skills in `skills/` are invoked automatically when you describe matching work:

| Skill | Triggers when you... |
|---|---|
| `deliverable-qa` | Ask to review or QA a client deliverable |
| `meeting-prep` | Mention preparing for or planning a meeting |
| `status-comms` | Ask to draft a status email, report, or dashboard update |

---

## Project Notes

Add running notes here as the engagement progresses. Commit updates so the whole team shares context.

**Key decisions:**
- [Date] | [Decision] | [Rationale] | [Owner]

**Open risks:**
- [Risk description] | [Owner] | [Status]

**Team / capacity notes:**
- [Person] | [Role] | [Availability / travel / coverage notes]
