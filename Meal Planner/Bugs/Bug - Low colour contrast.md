---
type: bug
status: fixed
severity: medium
area: accessibility
date: 2026-09-27
step: 12
found_by: tests
tags: [meal-planner, bug, a11y]
---
# Low colour contrast

- **Symptom:** The axe accessibility checker flagged light-grey text and pale green buttons as hard to read.
- **Fix:** White-text buttons use emerald-700; secondary text uses zinc-600 (light) / zinc-400 (dark). Now 0 issues.
- **Lesson:** Run an automatic accessibility check on every page in light **and** dark mode.

Related: [[Design System]] · [[Bugs]]
