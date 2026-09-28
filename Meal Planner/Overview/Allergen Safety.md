---
type: overview
tags: [meal-planner, allergens, safety]
---
# Allergen Safety

Back to [[Meal Planner Home]] · Why: [[Decision - Two-layer allergen checks]] · Proof it was needed: [[Bug - Spoonacular let dairy recipes through]]

> [!danger] Rule
> A recipe that **might** contain a user's allergen must never be shown. A missing suggestion is an inconvenience;
> a wrong one could hurt someone.

## 16 allergens + "other" words
Peanuts, tree nuts, dairy, eggs, soy, wheat, gluten, fish, shellfish, crustaceans, molluscs, sesame, mustard, celery,
lupin, sulphites — plus any free-text words the user types (e.g. "kiwi").

## Two independent checks — both must pass
1. **Tags:** every ingredient is tagged with the allergens it contains (set by the owner, reviewed).
2. **Word check:** titles and ingredient names are scanned for keywords (dairy → milk, butter, ghee, paneer, curd…),
   with safe phrases allowed (coconut milk, peanut butter for dairy).

## Where it runs
Planner, recipe pages, swaps, shopping, barcode scans (Open Food Facts tags + words) and even **AI coach replies**
(a warning is added if the reply mentions your allergen). Diet rules (veg / Jain / vegan…) use the same double check.

## Cautious choices
- Bread is tagged **dairy + soy** because many Indian breads contain milk solids and soya.
- Asafoetida (hing) was left out of starter recipes — most Indian hing contains wheat flour.
- Tests: `tests/allergens.test.ts`, `tests/starter-library.test.ts` (runs all 79 starter recipes through the engine).
