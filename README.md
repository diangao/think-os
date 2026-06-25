# Think OS

> A framework for building your personal cognitive infrastructure with Claude.

Not a note-taking app. Not a second brain template. A protocol for turning your file system into an AI-native thinking environment.

---

## Reflect and plan with it

Use Think OS to:

- Reflect on the past — what worked, what didn't, what you learned about yourself
- Set intentions for what comes next — goals, directions, things you want to explore
- Start building a system that remembers, so you can look back later

Run `/startup` and tell Claude what you want to think through. Claude will help you organize your thoughts into `perspective.md`, track your goals in `todo.md`, and build a profile of how you think in `me.md`.

Run `/mid-check` anytime during a conversation. It triggers Claude to log what you've discussed to the right files. The more you use it, the more Claude can follow.

Everything stays on your machine. No cloud. No account. No data leaves your computer. Just you, your files, and Claude.

---

## What is this?

Think OS is a pattern for working with Claude Code where:

- Your file system becomes your cognitive architecture
- Directories enforce how you organize thinking
- Protocols define how Claude reads, writes, and navigates your system
- Claude becomes an extended mind, not just an assistant

Claude remembers what you care about, knows where things live, and helps you think — across sessions, across topics, across time.

---

## Why a file system, not a single context file?

| Single context.md | File System Structure |
|-------------------|----------------------|
| Everything in one place | Information has a physical location |
| Claude reads the whole thing | Claude navigates and reads selectively |
| Gets unwieldy fast | Scales, each file stays digestible |
| You organize manually | Directory structure enforces organization |
| No access patterns | Access path equals thinking path |

Structure is not just organization. It is constraint that shapes thinking.

---

## Core Architecture

```
your-think-os/
├── CLAUDE.md                    # Protocol: how Claude uses this system
├── now.md                       # Registry: what's currently active
├── memory/
│   ├── me.md                    # About you (Claude maintains)
│   └── timeline/
│       ├── perspective.md       # Past → Present → Future
│       ├── todo.md              # Tasks and to-dos
│       └── daily/               # Daily activity index
├── tinker/                      # Curiosity-driven exploration
│   └── index.md                 # Topics you're poking at
└── .claude/
    └── commands/                # Executable workflows
        ├── startup.md           # Begin session
        ├── mid-check.md         # Ensure nothing missed
        └── wrapup.md            # End session
```

### What's in each file

| File | Purpose |
|------|---------|
| `CLAUDE.md` | Protocol. Tells Claude how to behave. References `@memory/me.md` and `@now.md` so Claude auto-loads them. |
| `now.md` | Current focus — what you're actively working on. |
| `memory/me.md` | Your profile. Claude maintains this as it learns about you. |
| `memory/timeline/perspective.md` | Past → Present → Future. Your trajectory and goals. |
| `memory/timeline/todo.md` | Tasks and to-dos. Claude helps you track. |
| `memory/timeline/daily/` | Daily session logs. Created by `/wrapup`. |
| `tinker/index.md` | Curiosity-driven explorations. Ideas you're poking at. |

### The three core patterns

**1. Protocol over content**

`CLAUDE.md` is not "information about me." It's the operating manual for how Claude uses your system:

- What each directory is for
- When to read vs write
- Boundaries between you and Claude

**2. Structure as constraint**

Directories aren't suggestions. They're enforced categories.

When you create `journal/` vs `tinker/` vs `archive/`, you're not just organizing — you're declaring that these are different types of thinking.

**3. Entry points and registries**

- `CLAUDE.md` is where Claude starts.
- `now.md` is what's currently active.
- `{category}/index.md` is the entry point for each domain.

Claude doesn't need you to @mention every file. The system points Claude to where to look.

---

## Requirements

You'll need [Claude Code](https://docs.anthropic.com/en/docs/claude-code), the CLI tool that lets Claude read and write files, run commands, and do things.

Cost: roughly $20/month. Claude Pro includes Claude Code access. You can also use the API directly (usually cheaper for light use).

This won't work in the Claude web app. Claude Code is needed because it can navigate your file system and run slash commands.

---

## Quick Start

```bash
# Clone this repo
git clone https://github.com/diangao/think-os.git my-think-os
cd my-think-os

# Open in Claude Code
claude

# Start your first session
/startup
```

Claude will read the protocol, understand its role, and start observing.

<details>
<summary><b>Don't use git?</b></summary>

1. Click the green "Code" button above, then "Download ZIP"
2. Unzip to a folder (e.g., `my-think-os`)
3. Open Terminal and navigate to the folder: `cd ~/Downloads/my-think-os`
4. Run `claude` to start Claude Code
5. Type `/startup` to begin

</details>

---

## Your first session

A typical first session:

1. Run `/startup`. Claude reads your system and asks what you want to focus on.
2. Talk. Tell Claude about your goals, what you're working on, what's on your mind.
3. Run `/mid-check`. This triggers Claude to log everything to the right files. Use it often.
4. Correct it when Claude gets something wrong. It will update.
5. Run `/wrapup`. Claude creates a daily log and commits everything.

A simple opener:

> "I want to reflect on the past year and set goals for the next one."

Claude will help you think through it, write your reflections to `perspective.md`, add goals to `todo.md`, and capture patterns it notices about you in `me.md`.

---

### Slash commands

These are executable workflows that ritualize your thinking sessions:

| Command | When to use |
|---------|-------------|
| `/startup` | Begin a session. Loads context, asks what to focus on. |
| `/mid-check` | Mid-session. Ensures nothing is missed, checks todos. |
| `/emergency-check` | Reality check. Reviews deadlines, flags what's urgent. |
| `/wrapup` | End a session. Creates daily index, commits changes. |

---

## How to use this

1. Clone this repo. Everything you need is already here.
2. Run `claude`. It reads the protocol and knows what to do.
3. Start talking. Claude will observe, record, and organize.
4. Grow it organically. Add directories when you need them. Update the protocol as patterns emerge.

The skeleton is ready. Just clone and start.

---

## Design Philosophy

This is what happens when you take Claude Code's design philosophy seriously:

| Claude Code Principle | Think OS Application |
|----------------------|---------------------|
| File system as interface | Your repo is the interface |
| Hackable, extensible, customizable | You design your own protocol |
| AI as collaborator, not autonomous agent | Claude helps. You own the system. |
| Local-first, transparent | Everything in git, fully inspectable |

> "Claude Code gives you a hackable AI terminal. Think OS shows what you can build with it — a personal operating system for thinking."

---

## What this enables

Once you have a working Think OS:

- Cross-session memory. Claude knows what you worked on yesterday.
- Contextual awareness. Claude understands your projects, preferences, people.
- Active navigation. Claude finds relevant files instead of you @mentioning them.
- Externalized cognition. Your thinking can compound across time.

---

## This is a framework, not a template

The value isn't in copying my directory structure. It's in the pattern:

1. Protocols tell Claude how to behave.
2. Directories enforce thinking categories.
3. Registries point Claude to active work.
4. The file system becomes cognitive architecture.

Build your own. Adapt it to how you actually think.

---

## Agents

Think OS isn't only for Claude Code. Any AI agent can read and write to it.

### S.P.A.R.K.

[S.P.A.R.K.](https://github.com/diangao/S.P.A.R.K.) is a Telegram bot that texts you first. It integrates with Think OS to:

- Know what you're avoiding. Reads your daily files and schedule.
- Hold you accountable. Nudges you when you ghost your own goals.
- Learn what works. Writes to `memory/spark/learned.md` over time.
- Track its own state. Remembers prior interactions in `memory/spark/state.json`.

Example:

```
spark: how's the MCP research going
you: [no reply for 20 min]
spark: still on it?
you: [still nothing]
spark: u literally wrote "ship this week" in ur goals
```

Think OS gives Spark context. Spark makes sure you actually do the thing.

---

## FAQ

**Is this just CLAUDE.md with extra steps?**

CLAUDE.md is one file. Think OS uses CLAUDE.md as the entry point to an entire file system. Claude can navigate, read selectively, and write to specific locations.

**How is this different from Obsidian, Notion, or Roam?**

Those are note-taking tools. This is a protocol layer for working with an AI. They can coexist. Think OS can wrap around your existing notes.

**Does this work with other AI assistants?**

The pattern is general. The implementation assumes Claude Code. Adapting to other tools would require rewriting the protocol.

**What if my structure gets messy?**

Refactor it. The protocol evolves with you. That's the point.

---

## License

MIT. Take it, modify it, make it your own.

---

Built with Claude Code by Dian.
