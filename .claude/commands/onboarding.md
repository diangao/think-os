---
description: First-time setup - get to know you and show you around
---

Think OS onboarding. This is an interactive experience, not a form.

## Phase 1: Get to Know You

Start with ONE question, wait for response, then continue conversationally. Don't dump all questions at once.

**Opening:**
"Welcome to Think OS. I'm going to learn about you through conversation — not a boring questionnaire. Let's start with something interesting."

**Questions to weave in naturally** (pick based on flow, not all required):
- "What's something you've been curious about lately but haven't had time to explore?"
- "When you have a random thought worth remembering, where does it usually go? (Notes app? Nowhere?)"
- "What's a topic you know way more about than most people would expect?"
- "What are you actually trying to figure out in life right now — not the polished version, the real one?"

After each meaningful response, **immediately write to `memory/me.md`** — show the user you're doing this:
> "I'm noting this down in your profile..."

---

## Phase 2: Show the Magic — Live Web Search

Based on something the user mentioned being curious about, do a live demo:

"You mentioned [topic]. Let me show you something — I can search the web and bring back real sources."

1. **Use WebSearch** to find something relevant to their interest
2. **Show the results with proper source attribution** — demonstrate credibility
3. **Ask**: "Want me to save this to your exploration notes? I'll put it in `tinker/[topic]/notes.md`"

If they say yes, create the file and show them the structure.

---

## Phase 3: Introduce the Daily Rhythm

"Now let me show you how this becomes a daily companion, not just a one-time setup."

Briefly explain (keep it short):
- **`/startup`** — "Start your day. I'll remind you what you were working on."
- **`/wrapup`** — "End your session. I'll log what we discovered."
- **`/emergency-check`** — "Reality check. I'll flag if your plans are unrealistic."
- **`/mid-check`** — "Mid-session check. Make sure nothing's falling through the cracks."

---

## Phase 4: First Entry

"Let's make your first real entry. Based on our conversation, here's what I've learned about you so far:"

Show them a preview of `memory/me.md`, then ask:
> "Anything wrong here? I'd rather you correct me now than let me build on a wrong assumption."

---

## Wrap Up

"You're set up. A few things to remember:
- I observe and record — you'll see me writing to files as we talk
- Correct me anytime — I calibrate based on your feedback
- This system grows with you — the more we talk, the better it gets

Ready to start? Run `/startup` anytime to begin a session."

**Commit the changes:**
```bash
git add -A
git commit -m "[onboarding] initial profile created"
```
