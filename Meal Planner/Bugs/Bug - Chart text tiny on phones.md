---
type: bug
status: fixed
severity: medium
area: ui
date: 2026-09-27
step: 29
found_by: claude
tags: [meal-planner, bug, charts]
---
# Chart text tiny on phones

- **Symptom:** Labels on the Progress charts shrank to ~6 px on phones.
- **Cause:** The charts were drawn at a fixed width and scaled down to fit narrow screens, shrinking the text too.
- **Fix:** Charts measure their real width and draw at actual pixel size, so text stays 11 px.
- **Lesson:** Always check charts at 360 px wide.

Related: [[Design System]] · [[Bugs]]
