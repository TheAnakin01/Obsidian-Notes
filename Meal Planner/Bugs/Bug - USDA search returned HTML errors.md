---
type: bug
status: fixed
severity: medium
area: nutrition
date: 2026-09-27
step: 16
found_by: claude
tags: [meal-planner, bug, api]
---
# USDA search returned HTML "400" errors

- **Symptom:** Ingredient searches sometimes failed with an HTML error page instead of data.
- **Cause:** USDA's GET search choked on the data type name "Survey (FNDDS)" in the web address.
- **Fix:** Switched to a POST request with the filters in the body; handle non-JSON answers gracefully.
- **Lesson:** Intermittent failures often come from special characters in URLs.

Related: [[Decision - Own recipe library with USDA nutrition]] · [[Bugs]]
