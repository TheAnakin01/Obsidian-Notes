---
type: bug
status: fixed
severity: medium
area: ui
date: 2026-09-27
step: 35
found_by: claude
tags: [meal-planner, bug, css, animation]
---
# Page animation trapped the tab bar

- **Symptom:** In testing, a bottom bar placed inside a page scrolled away instead of staying pinned.
- **Cause:** The page fade-in animation left an (invisible) transform on the page wrapper, which traps anything
  "position: fixed" inside it.
- **Fix:** The page animation now uses fill-mode `backwards`, so nothing is left behind after it finishes.
- **Lesson:** CSS transforms change how fixed elements behave — check after adding animations.

Related: [[Design System]] · [[Bugs]]
