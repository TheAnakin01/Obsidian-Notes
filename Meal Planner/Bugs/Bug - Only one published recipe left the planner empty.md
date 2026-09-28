---
type: bug
status: fixed
severity: high
area: content
date: 2026-09-27
step: 34
found_by: claude
tags: [meal-planner, bug, content]
---
# Only one published recipe left the planner empty

- **Symptom:** After launch the library had 1 published recipe and 6 ingredients, so weekly plans were nearly empty
  (Jain and vegan users had nothing).
- **Fix:** Wrote a starter library — 64 USDA-backed ingredients + 79 Indian recipes — as one SQL file, loaded as
  drafts, plus a **Publish ready drafts** button. Tests prove every diet gets a full week with no gaps.
- **Result:** 80 published recipes; every diet has 7+ recipes per meal.
- **Lesson:** An app is only as good as its content — plan the data, not just the code.

Related: [[Decision - Recipes seeded as drafts, owner publishes]] · [[Database]] · [[Bugs]]
