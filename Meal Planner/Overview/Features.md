---
type: overview
tags: [meal-planner, features]
---
# Features

Back to [[Meal Planner Home]]

## For every user
| Feature | What it does | More |
|---|---|---|
| Personal targets | Calories + protein/carbs/fat from age, weight, height, gender, activity, goal | Mifflin–St Jeor formula, safety floor 1200 / 1500 kcal |
| Indian diet types | Veg, eggetarian, vegan, **Jain** (no onion/garlic/roots), non-veg | [[Allergen Safety]] |
| Strict allergy safety | 16 allergens + your own words, checked **twice** everywhere | [[Decision - Two-layer allergen checks]] |
| Today | Greeting, calorie ring, macro bars, quick actions, today's meals with swap | [[Design System]] |
| Weekly plan | 7 days × 3 meals, portions scaled 0.5–2×, variety rules, lock / swap / regenerate, leftovers mode | [[Architecture]] |
| Shopping list | Added up from the plan, rounded to packs, grouped by aisle, pantry, WhatsApp share | [[Decision - Store deep links instead of checkout]] |
| Buy online | One tap to BigBasket, Blinkit, Zepto, Swiggy Instamart, Amazon.in, JioMart | |
| Recipe pages | Your portion's nutrition, ingredients with buy links, allergy-safe swap ideas, numbered steps | |
| Food diary | Log planned meals in one tap, scan barcodes (Open Food Facts), allergy warnings | |
| Progress | Streaks, days on target, 14-day calories chart, weight trend | |
| AI coach | Opt-in chat that knows your plan; proposes swaps / list items that you confirm | [[AI Coach]] |
| Reminders | Push notifications at meal times | [[Decision - Supabase pg_cron for reminders]] |
| Household | Invite family by code; one combined live shopping list | [[Decision - Households share the list, not the plan]] |
| Offline app | Install to home screen; Today, Week, Shopping work offline; ticks sync later | [[Offline & PWA]] |
| Auto-update | The installed app reloads itself when a new version is live | [[Bug - UI changes not showing on phone]] |
| Discover | Extra ideas from Spoonacular (limited free plan) | [[Decision - Spoonacular instead of Edamam]] |

## For the owner (admin)
- Recipe library editor with live nutrition from USDA
- **Draft with AI** (Gemini) → review → publish
- **Publish ready drafts** — one tap publishes every safe, complete draft
- Ingredient importer (USDA search, editable numbers, warnings for typos and cooked values)
- See [[Decision - Recipes seeded as drafts, owner publishes]]
