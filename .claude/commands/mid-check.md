---
description: Mid-session check - ensure nothing is missed
---

Review the conversation so far:

## 1. Anything that should be logged but hasn't been?

| If this happened... | Should go to... | Logged? |
|---------------------|-----------------|---------|
| User expressed preference/habit/pattern | `memory/me.md` | ? |
| Past event or life milestone | `memory/timeline/perspective.md` | ? |
| Goal or future direction | `memory/timeline/perspective.md` | ? |
| Today's discovery or progress | `memory/timeline/daily/{date}.md` | ? |
| Task or todo mentioned | `memory/timeline/todo.md` | ? |
| Curiosity/exploration topic | `tinker/{topic}/notes.md` | ? |

## 2. Todo check

Read `memory/timeline/todo.md`:
- Any task mentioned in conversation but not in todo.md? → Add it
- Any task completed? → Mark [x]
- Any task with deadline discussed? → Note the deadline
- Anything blocked? → Ask about it

## 3. Topic registration check

- New active focus? → Update `now.md`
- New exploration/curiosity? → Add to `tinker/index.md`
- Something no longer active? → Move to Paused

## 4. Any new understanding of the user?

Go deep, not surface:
- Don't just log what they said — understand WHY
- What does this reveal about how they think?
- Connect to patterns already in `memory/me.md`

## 5. Pending commits?

```bash
git status
git add -A && git commit -m "[topic] description"
```

## Output

List anything missing, then log it immediately.
