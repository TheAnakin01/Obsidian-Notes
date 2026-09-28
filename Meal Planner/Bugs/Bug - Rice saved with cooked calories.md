---
type: bug
status: fixed
severity: high
area: nutrition
date: 2026-09-27
step: 19
found_by: claude
tags: [meal-planner, bug, data-quality]
---
# Rice saved with cooked calories

- **Symptom:** Rice was stored at 112 kcal/100 g (cooked), but recipes use raw weights — every rice dish looked far
  lighter than it is.
- **Cause:** Picking the "cooked" USDA entry by mistake.
- **Fix:** Owner corrected it to 356 kcal (raw). The importer now warns when a dry staple (rice, dal, flour, oats…)
  looks like a cooked value (< 250 kcal/100 g).
- **Lesson:** Units and states (raw vs cooked) matter as much as numbers.

Related: [[Bug - Moong sprouts flagged as cooked]] · [[Bugs]]
