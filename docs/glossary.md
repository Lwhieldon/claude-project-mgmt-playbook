# Glossary

Key terms you'll encounter when using Claude Code for consulting delivery work.

---

## CLAUDE.md

A Markdown file in your project root that gives Claude persistent context about your engagement. Think of it as a briefing document that Claude re-reads at the start of every session. It holds your communication standards, stakeholder map, artifact formats, and running project notes.

- **Shared:** `CLAUDE.md` (committed to git, visible to the whole team)
- **Personal:** `CLAUDE.local.md` (gitignored, for your own notes and sensitive context)
- **Best practice:** Keep it under 200 lines. Long files slow sessions and increase cost.
- **Import syntax:** Use `@path/to/file` inside CLAUDE.md to pull in a supporting document without duplicating it.

---

## Slash Commands

Predefined prompts you invoke by typing `/command-name` inside Claude Code. They live as Markdown files in `.claude/commands/`. The filename becomes the command name.

- **Example:** `/status-report` runs the prompt in `.claude/commands/status-report.md`
- **With arguments:** `/sow-review sample-projects/acme/sow.md` passes the file path as `$ARGUMENTS`
- **Creating your own:** Add a `.md` file to `.claude/commands/` and it's immediately available
- **Browsing:** Type `/` in Claude Code to see all available commands

---

## Skills

Reusable, multi-step capabilities defined in a `SKILL.md` file. Unlike slash commands (which you trigger manually), skills can be invoked automatically when you describe a task matching the skill's `description` field.

- **Example:** The `meeting-prep` skill triggers when you say "I need to prep for a meeting with the client."
- **Where they live:** `skills/<skill-name>/SKILL.md` in this repo, or `~/.claude/skills/` for personal skills
- **Key frontmatter fields:**
  - `name`: lowercase, hyphens only, max 64 characters
  - `description`: the trigger sentence; Claude matches your request against this
- **Manual invoke:** Type `/skill-name` to invoke a skill directly

---

## $ARGUMENTS

A placeholder used inside slash command files. When you type `/status-report my-file.csv`, everything after `/status-report` (in this case `my-file.csv`) is substituted wherever `$ARGUMENTS` appears in the command prompt.

This is what makes slash commands flexible: the same command works with different inputs each time.

---

## Context Window

The amount of text Claude can hold in memory during a single session. Every message, every file Claude reads, and every response it generates consumes context.

- **Practical implication:** Reference files by path rather than pasting large documents into chat.
- **When context fills up:** Claude Code automatically compresses prior messages. You may notice it becomes less aware of early conversation details.
- **Reset anytime:** `/clear` starts a fresh session with a clean context window.

---

## Subagents

When you give Claude Code a complex task, it may delegate portions to focused subagents, each handling one piece of the work in parallel. For example, "review the SOW and also generate a risk register" might spawn two subagents working simultaneously.

You generally don't manage this directly. It's why some multi-part requests complete faster than you might expect.

---

## Memory (CLAUDE.md vs. Session Context)

| Type | Scope | How to use |
|---|---|---|
| `CLAUDE.md` | Persists across all sessions | Engagement context, firm standards, standing instructions |
| `CLAUDE.local.md` | Persists, personal only (gitignored) | Personal preferences, sensitive notes |
| Session context | Current session only | In-progress work, conversation thread |

Anything you want Claude to "remember" next week should go in `CLAUDE.md` or `CLAUDE.local.md`, not just in the chat.

---

## RAG Status

Red / Amber / Green is a standard project health indicator used in consulting status reports.

| Color | Meaning |
|---|---|
| 🔴 Red | At risk; requires immediate escalation or action |
| 🟡 Amber | Caution; on watch; mitigation in progress |
| 🟢 Green | On track; no significant concerns |

The `/status-report` command uses RAG by default. See `CLAUDE.md` → Default Output Formats for the full convention.
