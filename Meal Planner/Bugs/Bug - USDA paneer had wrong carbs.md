---
type: bug
status: fixed
severity: medium
area: nutrition
date: 2026-09-27
step: 17
found_by: claude
tags: [meal-planner, bug, data-quality]
---
# USDA paneer had wrong numbers

- **Symptom:** USDA's "paneer" listed 22 g carbs per 100 g (real paneer has ~3 g); calories didn't match the macros.
- **Cause:** USDA data for Indian foods can be inaccurate.
- **Fix:** The ingredient importer lets the owner edit numbers, and warns when calories are >7% off the macro
  estimate (fibre counted at 2 kcal/g).
- **Lesson:** Validate third-party data with simple sanity checks.

Related: [[Bug - Rice saved with cooked calories]] · [[Bugs]]
