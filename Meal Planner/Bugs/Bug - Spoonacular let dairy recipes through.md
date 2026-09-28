---
type: bug
status: fixed
severity: critical
area: allergens
date: 2026-09-27
step: 9
found_by: claude
tags: [meal-planner, bug, safety]
---
# Spoonacular let dairy recipes through

- **Symptom:** A real test asking for dairy-free recipes returned 6 recipes — 2 of them (breakfast sausage, chocolate
  chips) were flagged `dairyFree: false` by Spoonacular itself.
- **Cause:** The API's own allergy filter isn't reliable.
- **Fix:** Added a second, independent check on every recipe (flags + keyword scan of title and ingredients).
- **Lesson:** Never trust a single filter for safety-critical data. Test with real responses.

Related: [[Allergen Safety]] · [[Decision - Two-layer allergen checks]] · [[Bugs]]
