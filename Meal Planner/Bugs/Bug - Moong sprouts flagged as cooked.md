---
type: bug
status: fixed
severity: low
area: nutrition
date: 2026-09-27
step: 34
found_by: tests
tags: [meal-planner, bug, data-quality]
---
# Moong sprouts flagged as "cooked"

- **Symptom:** The "looks cooked" warning fired for moong sprouts (30 kcal/100 g) because the name contains "moong".
- **Cause:** The warning checks dry-staple words; sprouts are fresh produce and genuinely light.
- **Fix:** Sprouted items are skipped by the check; new unit test added. Also loosened a test that was stricter than
  USDA's own data (USDA calorie factors for lemons and spices differ by up to ~25%).
- **Lesson:** Rules need exceptions — tests with real data find them.

Related: [[Bug - Rice saved with cooked calories]] · [[Bugs]]
