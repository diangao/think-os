# Think OS

> A framework for building your personal cognitive infrastructure with Claude.

Not a note-taking app. Not a second brain template. **A protocol for turning your file system into an AI-native thinking environment.**

---

## 🎆 New Year, New Mind

**Perfect timing.** Use Think OS to:
- Reflect on 2025 — what worked, what didn't, what you learned about yourself
- Set intentions for 2026 — goals, directions, things you want to explore
- Start building a system that remembers — so next year, you can look back at *everything*

Just run `/startup` and tell Claude: *"I want to reflect on last year and set goals for next year."*

Claude will help you think through it, organize your thoughts into `perspective.md`, track your goals in `todo.md`, and start building a profile of how you think in `me.md`.

> 💡 **Pro tip:** Run `/mid-check` anytime during your conversation. This triggers Claude to log what you've discussed to the right files. The more you use it, the more Claude remembers.

> 🔒 **100% local.** Everything stays on your machine. No cloud. No account. No data leaves your computer. Just you, your files, and Claude.

---

## What is this?

Think OS is a pattern for working with Claude Code where:

- Your **file system** becomes your cognitive architecture
- **Directories** enforce how you organize thinking
- **Protocols** define how Claude reads, writes, and navigates your system
- Claude becomes an **extended mind**, not just an assistant

The result: Claude remembers what you care about, knows where things live, and helps you think — across sessions, across topics, across time.

---

## Why file system, not a single context file?

| Single context.md | File System Structure |
|-------------------|----------------------|
| Everything in one place | Information has **physical location** |
| Claude reads the whole thing | Claude **navigates + selective reads** |
| Gets unwieldy fast | Scales infinitely, each file stays digestible |
| You organize manually | Directory structure **enforces** organization |
| No access patterns | Access path = thinking path |

The insight: **structure is not just organization — it's constraint that shapes thinking.**

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
| `CLAUDE.md` | Protocol — tells Claude how to behave. Includes `@memory/me.md` and `@now.md` references so Claude auto-loads them. |
| `now.md` | Current focus — what you're actively working on |
| `memory/me.md` | Your profile — Claude maintains this as it learns about you |
| `memory/timeline/perspective.md` | Past → Present → Future — your trajectory and goals |
| `memory/timeline/todo.md` | Tasks and to-dos — Claude helps you track |
| `memory/timeline/daily/` | Daily session logs — created by `/wrapup` |
| `tinker/index.md` | Curiosity-driven explorations — ideas you're poking at |

### The Three Core Patterns

**1. Protocol over Content**

`CLAUDE.md` is not "information about me." It's the **operating manual** for how Claude uses your system:
- What each directory is for
- When to read vs write
- Boundaries between you and Claude

**2. Structure as Constraint**

Directories aren't suggestions. They're **enforced categories**.

When you create `journal/` vs `tinker/` vs `archive/`, you're not just organizing — you're declaring "these are fundamentally different types of thinking."

**3. Entry Points + Registries**

- `CLAUDE.md` = where Claude starts
- `now.md` = what's currently active
- `{category}/index.md` = entry point for each domain

Claude doesn't need you to @mention every file. The system tells Claude where to look.

---

## Requirements

You'll need [Claude Code](https://docs.anthropic.com/en/docs/claude-code) — the CLI tool that lets Claude read/write files, run commands, and actually *do* things.

**Cost**: ~$20/month
- Claude Pro ($20/mo) includes Claude Code access
- Or use API directly (pay per token, usually cheaper if you're not a heavy user)

> 💡 This won't work with the Claude web app — you need Claude Code because it can navigate your file system and run slash commands. That's the magic.

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

That's it. Claude will read the protocol, understand its role, and start observing.

<details>
<summary><b>Don't use git?</b></summary>

1. Click the green "Code" button above → "Download ZIP"
2. Unzip to a folder (e.g., `my-think-os`)
3. Open Terminal, navigate to the folder: `cd ~/Downloads/my-think-os`
4. Run `claude` to start Claude Code
5. Type `/startup` to begin

</details>

---

## Your First Session

Here's what a typical first session looks like:

1. **Run `/startup`** — Claude reads your system and asks what you want to focus on
2. **Just talk** — Tell Claude about your goals, what you're working on, what's on your mind
3. **Run `/mid-check`** — This triggers Claude to log everything to the right files. Use it often!
4. **Correct it** — If Claude gets something wrong, just say so. It will update.
5. **Run `/wrapup`** — Claude creates a daily log and commits everything

**New Year example**:
> "I want to reflect on 2025 and set goals for 2026."

Claude will help you think through it, write your reflections to `perspective.md`, add goals to `todo.md`, and capture patterns it notices about you in `me.md`.

---

### Slash Commands

These are executable workflows that ritualize your thinking sessions:

| Command | When to use |
|---------|-------------|
| `/startup` | Begin a session — loads context, asks what to focus on |
| `/mid-check` | Mid-session — ensures nothing is missed, checks todos |
| `/emergency-check` | Reality check — reviews deadlines, flags what's urgent |
| `/wrapup` | End a session — creates daily index, commits changes |

---

## How to Use This

1. **Clone this repo** — everything you need is already here
2. **Run `claude`** — it reads the protocol and knows what to do
3. **Start talking** — Claude will observe, record, and organize
4. **Grow organically** — add directories when you need them, update the protocol as patterns emerge

The skeleton is ready to go. Just clone and start.

---

## Design Philosophy

This is what happens when you take Claude Code's design philosophy seriously:

| Claude Code Principle | Think OS Application |
|----------------------|---------------------|
| File system as interface | Your repo **is** the interface |
| "Hackable, extensible, customizable" | You design your own protocol |
| AI as collaborator, not autonomous agent | Claude helps; you own the system |
| Local-first, transparent | Everything in git, fully inspectable |

> "Claude Code gives you a hackable AI terminal. Think OS shows what you can build with it — a personal operating system for thinking."

---

## What This Enables

Once you have a working Think OS:

- **Cross-session memory**: Claude knows what you worked on yesterday
- **Contextual awareness**: Claude understands your projects, preferences, people
- **Active navigation**: Claude finds relevant files instead of you @mentioning them
- **Externalized cognition**: Your thinking compounds across time

---

## This is a Framework, Not a Template

The value isn't in copying my directory structure. It's in understanding the **pattern**:

1. **Protocols** tell Claude how to behave
2. **Directories** enforce thinking categories
3. **Registries** point Claude to active work
4. **The file system** becomes cognitive architecture

Build your own. Make it weird. Make it yours.

---

## Agents

Think OS isn't just for Claude Code. Any AI agent can read and write to it.

### S.P.A.R.K.

[S.P.A.R.K.](https://github.com/diangao/S.P.A.R.K.) — the Telegram bot that texts you first. It integrates with Think OS to:

- **Know what you're avoiding** — reads your daily files and schedule
- **Hold you accountable** — guilt trips you when you ghost your own goals
- **Learn what works** — writes to `memory/spark/learned.md` over time
- **Track your sins** — remembers how many times you've ignored it in `memory/spark/state.json`

It's the annoying friend who sends "bruhh" when you said you'd finish something and didn't. Except it never forgets. And it has access to your goals.

```
spark: how's the MCP research going
you: [no reply for 20 min]
spark: bruhh
you: [still nothing]
spark: u literally wrote "ship this week" in ur goals
```

Think OS gives Spark context. Spark makes sure you actually do the thing.

---

## FAQ

**Is this just CLAUDE.md with extra steps?**

CLAUDE.md is one file. Think OS uses CLAUDE.md as the entry point to an entire file system. The difference: Claude can navigate, read selectively, and write to specific locations.

**How is this different from Obsidian / Notion / Roam?**

Those are note-taking tools. This is a protocol layer for working with an AI. They can coexist — Think OS can wrap around your existing notes.

**Does this work with other AI assistants?**

The pattern is general. The implementation assumes Claude Code. Adapting to other tools would require rewriting the protocol.

**What if my structure gets messy?**

Refactor it. The protocol evolves with you. That's the point.

---

## License

MIT. Take it, modify it, make it yours.

---

*Built with Claude Code, with ❤️ by Dian.*
