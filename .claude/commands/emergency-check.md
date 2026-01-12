---
description: Emergency check - reality check deadlines and buffers
---

Review all deadlines and ensure you have enough buffer.

## 1. Read files
- `memory/me.md` — Communication preferences
- `memory/timeline/perspective.md` — Long-term goals and deadlines
- `memory/timeline/todo.md` — Current tasks
- `memory/timeline/daily/{today}.md` — Today's plan (if exists)

## 2. Check for completed todos
- If `todo.md` has any `[x]` completed items, ask: "I see X completed todos. Want to archive them?"
- If confirmed, move to end of file under a "Completed" section with date

## 3. Fact-check each deadline

For each deadline, verify:

| Question | Answer |
|----------|--------|
| What is it? | |
| When is it due? | |
| Days remaining? | |
| Working days remaining? (exclude weekends) | |
| Started yet? What's the progress? | |
| Estimated time needed? | |
| Buffer enough? | |

## 4. Buffer calculation

For each major deadline:
- Estimate actual work time needed
- Add buffer for unexpected issues (typically 1.5x-2x)
- Calculate: If deadline is X, with Y buffer needed, should finish by Z
- If buffer is already gone, flag immediately

## 5. Flag issues (prioritize)

- 🚨 **Red**: Buffer already gone, needs immediate action
- ⚠️ **Yellow**: Buffer tight, needs attention
- 💡 **Note**: Could be optimized

## 6. Help prioritize

- List today's possible tasks (from todo.md + today's notes)
- Categorize by urgent/important 2x2 matrix
- Discuss: What should today's Top 3 really be?

## 7. Output format

```
🔍 Emergency Check — {date} ({weekday})

## Deadline Fact-Check

| Deadline | Due Date | Days Left | Working Days | Status |
|----------|----------|-----------|--------------|--------|
| [Name] | [Date] | X days | Y work days | [Not started/In progress/Blocked] |

## Flags

🚨 **[Urgent Issue]**
- What's the problem
- What's the impact
- Suggested action

⚠️ **[Needs Attention]**
- ...

## Buffer Analysis

[Deadline Name]:
- Estimated work: X days
- Recommended buffer: +Y days (1.5x)
- Ideal completion: Z
- Actual remaining: ...
- Conclusion: Sufficient / Tight / Insufficient

## Today's Options

### Urgent + Important
- ...

### Important but Not Urgent
- ...

### Urgent but Not Important
- ...

---

Based on the above, what should today's Top 3 be?
(Discuss with user to help them decide)
```

## Style

- **Direct**: No beating around the bush
- **Data-driven**: Use specific numbers
- **Actionable**: Give concrete suggestions, not vague advice
- **Buffer mindset**: Always assume unexpected issues will arise
- **Help prioritize**: Don't decide for them, help them see trade-offs

## Holidays to consider

- Major holidays
- Weekends don't count as working days
