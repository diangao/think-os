---
description: Mid-session check - ensure nothing is missed
---

Review the conversation so far:

## 1. Anything that should be logged but hasn't been?

Check against trigger table:

| If this happened... | Should go to... | Logged? |
|---------------------|-----------------|---------|
| User expressed preference/habit/pattern | `memory/me.md` | ? |
| Past event or life milestone | `memory/timeline/perspective.md` | ? |
| Goal or future direction | `memory/timeline/perspective.md` | ? |
| Today's discovery or progress | `memory/timeline/daily/{date}.md` | ? |
| Task or todo mentioned **with deadline** | `memory/timeline/todo.md` | ? |
| Curiosity/exploration topic | `tinker/{topic}/notes.md` | ? |

## 2. Topic registration check

- New active focus? → Update `now.md`
- New exploration/curiosity? → Add to `tinker/index.md`
- Something no longer active? → Move to Paused in `now.md`

## 3. Any new understanding of the user?

Go deep, not surface:
- Don't just log what they said — understand WHY
- What does this reveal about how they think?
- What mental models are they using?
- Connect to patterns already in `memory/me.md`

## 4. Hidden todos?

Scan conversation for implicit tasks:
- User said "I should do X" / "Later I'll Y" / "Next week Z" → Might be a todo
- Mentioned deadline but not in todo.md → Ask to confirm
- Discussed plan but not written down → Proactively ask if they want to add it

**Ask for timing**:
- "When does this need to be done?"
- "Is there a deadline?"
- "Should I add this to todo.md?"

## 5. Pending commits?

```bash
git status
```

If there are uncommitted changes, commit them:

```bash
git add -A && git commit -m "[topic] description"
```

## Output

List anything missing, then log it immediately. Don't wait.
