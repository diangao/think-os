---
description: Review recent activity - yesterday, this week, or custom range
---

Think OS activity review. Check what was accomplished recently.

## 1. Determine time range

Based on user request, choose one:
- **Yesterday**: Read `memory/timeline/daily/{yesterday's date}.md`
- **This week**: Read all daily indices from this week in `memory/timeline/daily/`
- **Custom**: Read specified date range

## 2. Check todos

- Read `memory/timeline/todo.md` for tasks
- Check which todos were completed vs still pending
- Note any new todos added during this period

## 3. Also check git history

```bash
# For yesterday
git log --oneline --since="yesterday" --until="today"

# For this week
git log --oneline --since="last monday"
```

## 4. Output format

```
## Activity Review: {time range}

### Commits ({N} total)
{list commits grouped by day if multiple days}

### Todos

**Completed:**
- [x] {completed task}

**Pending:**
- [ ] {pending task} (deadline: {date})

### Key Discoveries
{extract from daily indices}

### Topics Touched
- {topic 1}: {what happened}
- {topic 2}: {what happened}

### Open Threads
{any unfinished items from daily indices}

### Progress Summary
{brief narrative of what was accomplished}
```

## 5. Default behavior

If no time range specified, default to "yesterday + today so far".
