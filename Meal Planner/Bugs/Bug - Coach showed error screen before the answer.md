---
type: bug
status: fixed
severity: high
area: ai
date: 2026-09-27
step: 27
found_by: owner
tags: [meal-planner, bug, ai, ux]
---
# Coach showed the error screen before the answer

- **Symptom:** Every question showed "Try again"; after tapping it, the answer appeared.
- **Cause:** After the slow AI call, the server re-rendered the whole coach page (`revalidatePath`), which failed/timed out.
- **Fix:** The coach actions now return the saved messages and the chat updates itself; no page refresh. Shared ~75 s deadline.
- **Lesson:** Don't re-render a whole page after a slow call — update just what changed.

Related: [[AI Coach]] · [[Bugs]]
