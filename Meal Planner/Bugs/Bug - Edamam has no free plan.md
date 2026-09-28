---
type: bug
status: fixed
severity: high
area: recipes
date: 2026-09-27
step: 8
found_by: claude
tags: [meal-planner, bug, cost]
---
# Edamam has no free plan

- **Symptom:** The original plan used the Edamam recipe API, but its cheapest plan is $9/month (prepaid).
- **Cause:** Edamam removed its free developer tier. This broke the "never spend money" rule.
- **Fix:** Stopped before signing up, told the owner, switched to Spoonacular's free plan (owner's choice).
- **Lesson:** Check pricing pages *before* building on a service; keep provider code in one file so it can be swapped.

Related: [[Decision - Spoonacular instead of Edamam]] · [[Free Plan Limits]] · [[Bugs]]
