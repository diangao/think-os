# Think OS

> A framework for building your personal cognitive infrastructure with Claude.

Not a note-taking app. Not a second brain template. **A protocol for turning your file system into an AI-native thinking environment.**

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
├── CLAUDE.md              # Protocol: how Claude uses this system
├── now.md                  # Registry: what's currently active
├── memory/
│   ├── me.md               # About you (Claude maintains)
│   └── timeline/           # Time-based records
│       └── daily/          # Daily activity index
└── {your-categories}/      # Your own thinking domains
    └── index.md            # Entry point for each domain
```

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

## How to Use This

### Option 1: Fork and Customize

1. Fork this repo
2. Modify the directory structure to match how **you** think
3. Rewrite `CLAUDE.md` to define **your** protocol
4. Let Claude learn your system

### Option 2: Start Minimal

Create just three files:

```
my-os/
├── CLAUDE.md    # "Read now.md to see active topics. Read memory/me.md to understand who I am."
├── now.md       # "- [ ] Project A \n - [ ] Idea B"
└── memory/
    └── me.md    # "I'm [name]. I work on [thing]. I prefer [style]."
```

Then grow organically. Add directories when you need them. Update the protocol as patterns emerge.

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

*Built with Claude Code. Maintained by Dian & Cindy.*
