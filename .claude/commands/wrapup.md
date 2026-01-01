---
description: Session wrapup - create daily index and commit
---

Think OS session wrapup. Execute the following:

1. **Review this session**:
   - What topics were discussed?
   - What decisions were made?
   - What was learned?

2. **Create/update daily index** at `memory/timeline/daily/{today's date}.md`:

```markdown
# {YYYY-MM-DD}

## Summary

(Brief overview of the session)

## Key Discoveries

- **{Discovery}**: {Brief explanation}

## Todos Updated

- Added: ...
- Completed: ...

## Open Threads

- [ ] {Thread for next session}
```

3. **Check files that might need updates**:
   - `memory/me.md` — any new patterns observed?
   - `memory/timeline/perspective.md` — any goals/milestones discussed?
   - `memory/timeline/todo.md` — any tasks to add/complete?
   - `now.md` — any focus changes?

4. **Commit your work**:
```bash
git add -A
git commit -m "[daily] {date} session wrap-up"
```

5. **Confirm**: "Session wrapped up. Daily index created."
