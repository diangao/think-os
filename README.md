# Think OS

A filesystem protocol for working with Claude Code across sessions.

Think OS is not a note-taking app or a second-brain template. It is a repo
structure plus a set of operating instructions. The structure gives Claude Code
a predictable way to load context, record decisions, and write session notes to
files you can inspect.

Everything stays local unless you choose to push the repo.

---

## What It Does

Think OS gives Claude Code a small working environment:

- `CLAUDE.md` defines the startup protocol
- `now.md` lists active topics
- `memory/` stores profile, timeline, and task records
- `.claude/commands/` contains repeatable workflows
- Git shows exactly what changed

The goal is to keep context recoverable without relying on one long chat
history.

---

## Reflect and Plan With It

Use Think OS to:

- review what happened
- record what worked and what did not
- choose current priorities
- turn decisions into tasks
- keep daily session notes

Run `/startup` and tell Claude Code what to focus on. It reads the protocol and
loads the files that define current state.

Run `/mid-check` during a conversation to write down what has changed so far.

Run `/wrapup` at the end of a session to create a daily log and commit the
changes.

---

## Why Files

| One large context file | Filesystem structure |
|------------------------|----------------------|
| Everything is mixed together | Each file has a clear job |
| Every session reads the same dump | Claude Code can read only what matters |
| Changes are hard to inspect | Git shows exact diffs |
| No write boundaries | Paths define where updates belong |
| Context grows stale quickly | Active work and archive can split cleanly |

The main rule: structure should make the next read or write obvious.

---

## Core Architecture

```text
your-think-os/
|-- CLAUDE.md                    # Protocol: startup order and file rules
|-- now.md                       # Registry: active topics
|-- memory/
|   |-- me.md                    # Durable profile maintained by Claude Code
|   `-- timeline/
|       |-- perspective.md       # Past, present, future
|       |-- todo.md              # Tasks and to-dos
|       `-- daily/               # Daily session logs
|-- tinker/
|   `-- index.md                 # Low-commitment exploration
`-- .claude/
    `-- commands/
        |-- startup.md           # Begin session
        |-- mid-check.md         # Record current state
        `-- wrapup.md            # End session
```

### What's In Each File

| File | Purpose |
|------|---------|
| `CLAUDE.md` | Entry protocol. Defines startup order, boundaries, and write rules. |
| `now.md` | Current focus and active topics. |
| `memory/me.md` | Durable profile. Claude Code updates it when stable facts or preferences change. |
| `memory/timeline/perspective.md` | Long-range trajectory and major milestones. |
| `memory/timeline/todo.md` | Task list. |
| `memory/timeline/daily/` | Daily session logs created by `/wrapup`. |
| `tinker/index.md` | Exploratory topics that are not yet active work. |

---

## Core Patterns

### 1. Protocol Over Content

`CLAUDE.md` is the entry point. It should define:

- what to read first
- what each directory is for
- when to read versus write
- which files the human owns
- which files Claude Code may update

This keeps the system usable after long gaps or context resets.

### 2. Structure as Boundary

Directories encode different kinds of work.

For example:

- `memory/` is durable state
- `timeline/` is time-based recordkeeping
- `tinker/` is loose exploration
- `archive/` is inactive material
- `scratch/` is temporary work

Clear boundaries reduce accidental writes and make review easier.

### 3. Registries and Entry Points

Small index files tell Claude Code where to look:

- `now.md` for active topics
- `tinker/index.md` for exploratory topics
- `memory/timeline/daily/YYYY-MM-DD.md` for daily changes
- topic-level `current.md` files when a topic grows large enough

The system should not require scanning the whole repo every time.

---

## Requirements

- [Claude Code](https://docs.anthropic.com/en/docs/claude-code)
- Git
- A local folder where Claude Code has file access

This does not run inside the Claude web app because the web app cannot manage
local files or run slash-command workflows.

---

## Quick Start

```bash
git clone https://github.com/diangao/think-os.git my-think-os
cd my-think-os
claude
/startup
```

If you do not use Git:

1. Download the ZIP from GitHub.
2. Unzip it to a local folder.
3. Open a terminal in that folder.
4. Run `claude`.
5. Type `/startup`.

---

## First Session

A typical first session:

1. Run `/startup`.
2. Describe what you want to work through.
3. Correct Claude Code when it records something inaccurately.
4. Run `/mid-check` if the conversation is long.
5. Run `/wrapup` to create a daily log and commit changes.

Example opener:

```text
I want to review the past year and decide what to focus on next.
```

Claude Code should write durable conclusions to the right files instead of
leaving them only in the chat.

---

## Slash Commands

These commands are repeatable workflows:

| Command | When to use |
|---------|-------------|
| `/startup` | Begin a session. Loads context and asks what to focus on. |
| `/mid-check` | Mid-session. Records the current state and checks open tasks. |
| `/emergency-check` | Reviews deadlines and urgent items. |
| `/wrapup` | Ends a session. Creates a daily log and commits changes. |

---

## Customizing It

Start with the existing structure, then change it when repeated work needs a
better path.

Common changes:

- rename `memory/me.md`
- add `journal/` for active long-running topics
- add `archive/` for inactive material
- split large files into topic files
- rewrite `CLAUDE.md` when the workflow changes

Keep the protocol short enough to read at startup.

---

## Design Principles

- Local first: files live on your machine.
- Transparent: updates are reviewable as Git diffs.
- Small files over one large context dump.
- Human-owned: the human decides the structure and can override it.
- Agent-readable: names and paths should be obvious.
- Record while working: important state should be written before it is forgotten.

---

## What This Enables

With a working Think OS, Claude Code can:

- resume work across sessions
- keep profile, current work, history, and drafts separate
- find relevant files without being handed every path
- keep topic notes current over time
- leave an audit trail through Git

The value is not the exact directory tree. The value is having a protocol that
makes context recoverable.

---

## Agents

Think OS can be used by any agent that can read and write files.

### S.P.A.R.K.

[S.P.A.R.K.](https://github.com/diangao/S.P.A.R.K.) is a proactive Telegram bot
that uses Think OS for context.

It can:

- read active goals and recent session logs
- send check-ins or reminders
- write learned patterns to approved files
- keep state in `memory/spark/state.json`

Keep integrations narrow:

- read only the files the agent needs
- write only to approved paths
- keep automated writes visible in Git
- keep secrets outside the repo

---

## FAQ

### Is this just `CLAUDE.md`?

No. `CLAUDE.md` is the entry point. Think OS is the surrounding file structure
that gives the protocol places to read from and write to.

### How is this different from Obsidian, Notion, or Roam?

Those tools are primarily for human note-taking. Think OS is a working protocol
for Claude Code operating over local files. It can sit alongside other note
systems, or wrap a subset of their exported content.

### Does this work with other assistants?

Yes, if the assistant can read files, write files, and follow a startup
protocol. The exact commands may change, but the pattern is tool-agnostic.

### What if the structure gets messy?

Refactor it. Move stale topics to archive, split large files, and update
`CLAUDE.md` when the protocol changes.

---

## License

MIT.

Built by Dian Gao.
