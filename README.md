# claude-project-mgmt-playbook
Practical Claude and Claude Code patterns for project managers and delivery leads. CLAUDE.md examples, slash commands, and ready-to-use prompts for status reports, transcripts, requirements, change requests, and more.

## Prerequisites
- [Claude Code](https://docs.anthropic.com/en/docs/claude-code) installed
- Active Claude paid plan with Claude Code access
- Git and a terminal

## Quickstart
```bash
git clone https://github.com/Lwhieldon/claude-project-mgmt-playbook.git
cd claude-project-mgmt-playbook
claude
```

## Repository tree
```text
claude-project-mgmt-playbook/
├── CLAUDE.md                           # Project leadership context and output standards
├── docs/
│   ├── getting-started.md              # Install steps, first session, first prompt
│   └── glossary.md                     # CLAUDE.md, skills, slash commands, subagents terms
├── .claude/commands/
│   ├── status-report.md                # Weekly status report generator
│   ├── transcript-actions.md           # Transcript-to-actions converter
│   ├── sow-review.md                   # SOW scope and risk reviewer
│   ├── stakeholder-prep.md             # Stakeholder meeting prep pack
│   ├── change-request.md               # Structured change request draft
│   ├── code-review-light.md            # Delivery-risk review of technical changes
│   ├── exec-summary.md                 # Leadership-ready executive summary
│   └── post-meeting-email.md           # Client-facing follow-up email draft
├── skills/
│   ├── deliverable-qa/SKILL.md         # Deliverable quality and readiness skill
│   ├── meeting-prep/SKILL.md           # Meeting prep and decision support skill
│   └── status-comms/SKILL.md           # Audience-tailored status communication skill
└── sample-projects/
    ├── acme-data-warehouse/            # Fictional project artifacts for quick practice
    └── globex-erp-migration/           # Fictional project artifacts for quick practice
```

## Contributing
Contributions are welcome. Please open an issue or pull request with clear examples, expected outputs, and updates to sample artifacts where relevant.

## License
This repository is licensed under the MIT License. See `LICENSE` for details.
