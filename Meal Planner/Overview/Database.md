---
type: overview
tags: [meal-planner, database, supabase]
---
# Database (Supabase)

Back to [[Meal Planner Home]] · Security rules: [[Security & Privacy]]

## Migrations (in order)
| # | File | Adds |
|---|---|---|
| 0001 | init | `profiles`, `saved_recipes` |
| 0002 | saved_recipes_spoonacular | saved recipes keep only id / title / image ([[Bug - Spoonacular terms forbid caching and storing]]) |
| 0003 | profile_diet_store_timezone | diet type, preferred store, timezone |
| 0004 | recipe_library | `admins`, `is_admin()`, `ingredients`, `recipes`, `recipe_ingredients` |
| 0005 | save_recipe | atomic `save_recipe()`; published recipes must have nutrition |
| 0006 | meal_plans | `meal_plans`, `meal_plan_items`, leftovers mode |
| 0007 | shopping_list | `shopping_list_items` (ticks + extras), `pantry_items` |
| 0008 | coach | coach on/off, `coach_messages`, daily question counter |
| 0009 | coach_actions | proposed actions the user confirms |
| 0010 | food_log | food diary |
| 0011 | weight_log | one weigh-in per day |
| 0012 | reminders | reminder times, push subscriptions, reminder log, private secrets, `claim_due_reminders()` |
| 0013 | households | households, members, invite codes, shared list (Realtime) |

## How migrations get applied (important!)
The Supabase project is connected to GitHub. **Pushing a new migration file applies it automatically** — the
"Supabase Preview" check on each commit shows the result. Do **not** also run it in the SQL Editor.
Story: [[Bug - Supabase Preview check failing]] · [[Decision - Migrations applied by Supabase GitHub integration]].

Not automatic (run by hand): `supabase/seed/starter-library.sql` (recipes) and the git-ignored reminder scheduler SQL.

## Recipe library
80 published recipes (28 breakfast, 51+ lunch/dinner) and 70 ingredients with USDA nutrition.
Every diet type has at least 7 recipes per meal. See [[Decision - Recipes seeded as drafts, owner publishes]].
