# Getting Started

This guide gets you from zero to your first Claude Code session in under 10 minutes.

---

## Step 1: Install Claude Code

Claude Code is a command-line tool. Install it with npm:

```bash
npm install -g @anthropic-ai/claude-code
```

Verify the install:

```bash
claude --version
```

**Requirements:** Node.js 18+, and a paid Anthropic account (Pro, Team, or Max plan).

---

## Step 2: Clone and Open This Repo

```bash
git clone https://github.com/YOUR_ORG/claude-project-mgmt-playbook.git
cd claude-project-mgmt-playbook
claude
```

On first run, Claude Code will prompt you to authenticate via browser. Follow the prompt.

Claude Code automatically reads `CLAUDE.md` at startup, giving Claude the context it needs about your engagement before you type a single message.

---

## Step 3: Try Your First Commands

Once inside Claude Code, try these against the sample projects:

**Review a Statement of Work:**
```
/sow-review sample-projects/acme-data-warehouse/sow.md
```

**Extract action items from a meeting transcript:**
```
/transcript-actions sample-projects/acme-data-warehouse/meeting-transcript.txt
```

**Generate a status report from data:**
```
/status-report sample-projects/acme-data-warehouse/status-data.csv
```

**Draft an executive summary:**
```
/exec-summary sample-projects/globex-erp-migration/sow.md
```

---

## Step 4: Personalize CLAUDE.md

Before using this on a real engagement, open `CLAUDE.md` and fill in:

1. Your firm and practice name
2. The client name (or a code name if sensitive)
3. The engagement type and current phase
4. Your key client contacts
5. Any project notes in the **Project Notes** section

Commit the updated `CLAUDE.md` so your whole team shares the same context when they open the repo.

---

## Step 5: Set Up Your Project Folder

Copy one of the sample projects as a starting point:

```bash
cp -r sample-projects/acme-data-warehouse my-projects/client-name
```

Then add your real project files: SOW, transcripts, status data, change requests.

---

## Tips for Non-Engineers

- **Natural language works.** "Summarize this SOW and flag the top 3 risks" is just as valid as `/sow-review`. Slash commands are shortcuts for your most-used prompts.
- **Reference files by path.** Instead of pasting a 20-page SOW into chat, say: "Read `my-projects/client/sow.md` and review it." Claude Code reads the file directly.
- **Iterate.** Ask Claude to shorten, reformat, adjust tone, or focus on a specific section after a first draft.
- **Use the Up arrow** to recall your last prompt and edit it.
- **`/clear`** starts a fresh conversation when context feels cluttered.

---

## Useful Commands Inside Claude Code

| Command | What it does |
|---|---|
| `/` | Browse all available slash commands |
| `/clear` | Start a new conversation |
| `/help` | Show Claude Code help |
| `Esc` | Cancel the current operation |
| `Shift+Enter` | New line in your message |

---

## Where to Go Next

- `docs/glossary.md`: Key terms explained (CLAUDE.md, skills, slash commands, subagents)
- `.claude/commands/`: Browse and edit the slash commands
- `skills/`: Browse the available skills
- `sample-projects/`: Practice with the fictional Acme and Globex projects
