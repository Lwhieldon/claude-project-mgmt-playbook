# Getting started

## 1) Install prerequisites
1. Install Claude Code.
2. Confirm you can run `claude` from your terminal.
3. Ensure your account has an active paid plan with Claude Code access.

## 2) Start your first session
```bash
git clone https://github.com/Lwhieldon/claude-project-mgmt-playbook.git
cd claude-project-mgmt-playbook
claude
```

## 3) Project context loading
When Claude Code starts in this repository, it automatically loads `CLAUDE.md`. You can still open it to review or tailor firm-specific language.

## 4) Run your first prompt
Use this prompt to produce a first status update from sample data:

```text
Create a weekly client status report using sample-projects/acme-data-warehouse/status-data.csv and sample-projects/acme-data-warehouse/meeting-transcript.txt. Use the default format from CLAUDE.md, include RAG status, and list decisions needed in a table with owner and due date.
```

## 5) Try slash commands
- `/status-report sample-projects/acme-data-warehouse`
- `/transcript-actions sample-projects/acme-data-warehouse/meeting-transcript.txt`
- `/exec-summary sample-projects/globex-erp-migration`

## 6) Next steps
- Adapt `CLAUDE.md` for your firm language and governance standards.
- Copy `sample-projects/*` structure for each active client.
- Add or tune commands in `.claude/commands` for your delivery workflow.
