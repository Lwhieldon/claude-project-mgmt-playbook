# Claude Code Project Management Playbook

A templatized baseline for consulting delivery teams who want to use Claude and Claude Code to accelerate engagement work: reviewing Statements of Work, drafting status reports, analyzing meeting transcripts, prepping for stakeholder meetings, and more. Clone this repo, open it in Claude Code, and you have a team-ready starting point tuned for project leadership. No engineering background required.

## Prerequisites

- [Claude Code](https://claude.ai/code) installed globally: `npm install -g @anthropic-ai/claude-code`
- A paid Anthropic plan (Pro, Team, or API key with credits)
- Git and a terminal

## Quickstart

```bash
git clone https://github.com/YOUR_ORG/claude-project-mgmt-playbook.git
cd claude-project-mgmt-playbook
claude
```

Once Claude Code opens, try your first command:

```
/sow-review sample-projects/acme-data-warehouse/sow.md
```

Or explore the sample transcript:

```
/transcript-actions sample-projects/acme-data-warehouse/meeting-transcript.txt
```

## Repo Map

```
claude-project-mgmt-playbook/
├── README.md                          This file
├── CLAUDE.md                          Persistent project context (edit for your engagement)
├── docs/
│   ├── getting-started.md             Step-by-step setup and first session guide
│   └── glossary.md                    Key terms: CLAUDE.md, slash commands, skills, subagents
├── .claude/
│   └── commands/                      Slash commands (type /name inside Claude Code)
│       ├── status-report.md           Generate a weekly status report from project data
│       ├── transcript-actions.md      Extract action items and decisions from a transcript
│       ├── sow-review.md              Review a Statement of Work for risks and gaps
│       ├── stakeholder-prep.md        Prep for a stakeholder meeting and draft a follow-up
│       ├── change-request.md          Draft a formal change request document
│       ├── code-review-light.md       Non-engineer-friendly review of code or data artifacts
│       └── exec-summary.md            Compress a long document into a 1-page executive summary
├── skills/                            Skills (Claude invokes these on relevant tasks)
│   ├── deliverable-qa/SKILL.md        QA a client deliverable against consulting quality standards
│   ├── meeting-prep/SKILL.md          Prepare for a client or internal meeting
│   └── status-comms/SKILL.md          Draft multi-format status communications
└── sample-projects/                   Fictional practice projects, safe to share and experiment with
    ├── acme-data-warehouse/           Retail data warehouse modernization (Snowflake migration)
    └── globex-erp-migration/          Manufacturing ERP implementation (SAP S/4HANA)
```

## Adapting for Your Engagement

1. Edit `CLAUDE.md`: fill in the `[PLACEHOLDER]` fields with your client, project phase, and team.
2. Use `sample-projects/` as a reference when setting up your real project folder.
3. Add project-specific slash commands under `.claude/commands/` as you discover repeating patterns.
4. See `docs/getting-started.md` for a full walkthrough.

## Contributing

If you develop a slash command or skill that saves time on a project, consider contributing it back so the whole team benefits. Open a PR with the new file and a one-line description of when to use it.

## License

MIT. See [LICENSE](LICENSE).
