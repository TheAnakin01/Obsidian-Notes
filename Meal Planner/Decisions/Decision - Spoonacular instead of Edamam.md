---
type: decision
status: accepted
area: recipes
date: 2026-09-27
step: 8
tags: [meal-planner, decision]
---
# Spoonacular instead of Edamam

- **Context:** The spec said Edamam, but it has no free plan ([[Bug - Edamam has no free plan]]).
- **Options:** Spoonacular free (50 points/day, recipes + nutrition + allergy flags) · TheMealDB (free but no
  nutrition or allergy data) · pay for Edamam (breaks the ₹0 rule).
- **Decision:** Spoonacular free plan, signed up directly (not RapidAPI, which asks for a card).
- **Consequences:** Limited to ~12 plan views/day; strict terms ([[Bug - Spoonacular terms forbid caching and storing]]).
  Later demoted to the "Discover" tab when we built our own library → [[Decision - Own recipe library with USDA nutrition]].

Related: [[Decisions]]
