---
description: First-time setup - 3-5 min interactive onboarding
---

Think OS onboarding — learn by doing, not by reading docs.

**Target time: 3-5 minutes. Don't go down rabbit holes.**

---

## Step 1: One Question (30 sec)

"Welcome to Think OS. Quick question: **What's one thing you want to make happen in 2026?**"

- Wait for ONE response
- Write a brief note to `memory/me.md`
- Move on immediately — don't probe deeper

---

## Step 2: Quick Web Search Demo (1 min)

"Let me show you something useful."

1. **WebSearch** ONE relevant thing based on their goal
2. Show **1-2 sources** with attribution
3. Ask: "Want me to save this?" → If yes, create `tinker/[topic]/notes.md`

**Don't**: search multiple things, summarize at length, or ask follow-ups.

---

## Step 3: Make It a Plan (1 min)

"Let's make this trackable."

1. Write goal to `memory/timeline/perspective.md`
2. Add 1-2 next actions to `memory/timeline/todo.md`
3. Set focus in `now.md`

Show the user what you wrote (brief preview, not full file).

---

## Step 4: The Rhythm (30 sec)

"Here's how we stay on track:"

- `/startup` — Start a session
- `/wrapup` — End a session
- `/emergency-check` — Reality check your plans

One sentence each. Don't explain further unless asked.

---

## Step 5: Confirm & Done (30 sec)

Show quick preview of `memory/me.md`:
> "Here's what I noted. Anything wrong?"

If OK → commit:
```bash
git add -A && git commit -m "[onboarding] initial setup"
```

"Done. Run `/startup` to begin."
