---
description: Session wrapup - create daily index and commit
---

Think OS session wrapup. Execute the following:

1. **Review this session's changes**:
   ```bash
   git log --oneline -20
   git diff --stat HEAD~10
   ```

2. **Create/update daily index** at `memory/timeline/daily/{today's date}.md`:

**Daily index format**:
```markdown
# {YYYY-MM-DD}

## Commits ({N} total)

```
{paste git log output - don't summarize, show actual commits}
```

---

## Files Changed

### {Category} (Major updates)
- {What changed}

## Key Discoveries
- **{Discovery}**: {Brief explanation}

## Open Threads
- [ ] {Thread for next session}
```

3. **Clean up completed todos**:
   - Check `memory/timeline/todo.md` for completed items marked `[x]`
   - Move them to a "Completed" section at bottom with date
   - Keep main todo list clean (only pending items)

4. **Check now.md**:
   - Any tinker topic becoming more serious? → Consider moving to active focus
   - Any active topic no longer active? → Consider moving to Paused
   - Update `now.md` if needed

5. **Final commit**:
   ```bash
   git add -A
   git commit -m "[daily] {date} session wrap-up"
   ```

6. **Confirm**: "Session wrapped up. Daily index created at memory/timeline/daily/{date}.md"
