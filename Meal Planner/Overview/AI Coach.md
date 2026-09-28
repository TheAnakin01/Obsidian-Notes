---
type: overview
tags: [meal-planner, ai, gemini]
---
# AI Coach

Back to [[Meal Planner Home]] · Why Gemini: [[Decision - Gemini free tier for AI]]

- **Opt-in** with a clear notice (Google's free service may use messages to improve its products).
- **Minimal data:** age range, goal, targets, diet, allergies, this week's meal titles. Never name, email, weight or height.
- **Actions:** the coach can *propose* "swap this meal" or "add to shopping list" — nothing changes until you tap
  **Confirm**, and the server re-checks allergies and ownership.
- **Safety:** no medical advice; recommends a professional for conditions; never below the calorie floor; allergy
  warning added automatically if a reply mentions your allergen.
- **Limits:** 20 questions per person per day, 200 per day for everyone; history kept 30 days and deletable.
- **Models:** tries several Gemini Flash models in order (free tier is sometimes overloaded), ~75 s total deadline.
- **Admin recipe drafting:** describe a dish → Gemini returns a structured draft → our engine computes nutrition,
  allergens and diets → owner reviews and publishes.

Bugs met here: [[Bug - Gemini model retired or overloaded]] · [[Bug - Coach showed error screen before the answer]]
