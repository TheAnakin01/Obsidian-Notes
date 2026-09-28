---
type: decision
status: accepted
area: recipes
date: 2026-09-27
step: 34
tags: [meal-planner, decision, content]
---
# Recipes seeded as drafts, owner publishes

- **Context:** The library needed ~80 recipes fast ([[Bug - Only one published recipe left the planner empty]]).
- **Decision:** Claude wrote 79 recipes + 64 ingredients (USDA numbers) as one SQL file that adds them as **drafts**.
  A **Publish ready drafts** button recomputes each with the app's own engine and publishes only complete recipes with
  no allergen/diet warnings.
- **Why:** A human stays in control of what users see; the engine — not the author — decides nutrition and allergens.
- **Result:** 80 published recipes; tests prove every diet + common allergy mix gets a full week.

Related: [[Database]] · [[Decisions]]
