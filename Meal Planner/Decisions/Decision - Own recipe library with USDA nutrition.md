---
type: decision
status: accepted
area: recipes
date: 2026-09-27
step: 15
tags: [meal-planner, decision]
---
# Own recipe library with USDA nutrition

- **Context:** v2 needed weekly plans, shopping lists, buy links and offline use. Spoonacular's terms forbid storing
  ingredients/nutrition and the free plan allows ~2 weekly plans a day.
- **Decision:** Our own `recipes` / `ingredients` tables in Supabase; ingredient nutrition from USDA FoodData Central
  (public domain — we may store it forever). Owner chose this.
- **Consequences:** Unlimited use, Indian dishes, full control — but someone must add recipes
  ([[Bug - Only one published recipe left the planner empty]] → [[Decision - Recipes seeded as drafts, owner publishes]]).
  USDA data needs sanity checks ([[Bug - USDA paneer had wrong carbs]]).

Related: [[Database]] · [[Decisions]]
