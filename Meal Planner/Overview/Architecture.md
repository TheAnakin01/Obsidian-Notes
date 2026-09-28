---
type: overview
tags: [meal-planner, architecture]
---
# Architecture

Back to [[Meal Planner Home]] · Visual version: [[Meal Planner Architecture.canvas]]

## The big picture
```mermaid
flowchart LR
  Phone["📱 Phone / browser<br/>(installed PWA)"] -->|pages, taps| Vercel["▲ Vercel<br/>Next.js app"]
  Phone <-->|offline copies| SW["Service worker<br/>public/sw.js"]
  Vercel -->|login, data (RLS)| Supa[("Supabase<br/>Postgres + Auth")]
  Supa -->|live list changes| Phone
  Vercel --> USDA["USDA<br/>nutrition"]
  Vercel --> OFF["Open Food Facts<br/>barcodes"]
  Vercel --> Gemini["Gemini<br/>AI coach"]
  Vercel --> Spoon["Spoonacular<br/>Discover"]
  Cron["pg_cron<br/>every 15 min"] -->|/api/cron/reminders| Vercel
  Vercel -->|web push| Phone
  GitHub["GitHub repo"] -->|push = deploy| Vercel
  GitHub -->|new migrations| Supa
```

## How a week plan is made
1. Take every **published** recipe.
2. Remove anything unsafe for the user: allergy tags **and** a word check, plus diet rules → [[Allergen Safety]].
3. For each day and meal, pick a recipe and a **portion (0.5×–2×)** that lands within ±10% of that meal's calories
   (breakfast 25%, lunch 35%, dinner 40% of the day).
4. Variety rules: at most 2× a week, not on consecutive days; relaxed only when the library is small (with a note).
5. Empty slots stay empty rather than filled unsafely.
All of this is pure code with tests — no API cost. Code: `src/lib/planner.ts`.

## Shopping list
Plan → add up grams × portions → subtract pantry → round **up** to packs → group by aisle. Water is never listed.
Household mode adds up everyone's plans. Code: `src/lib/shopping.ts`.

## Where things live in the code
| Folder | Contents |
|---|---|
| `src/app/` | Pages (Today = `dashboard`, `week`, `shopping`, `diary`, `progress`, `coach`, `household`, `profile`, `admin`) and API routes |
| `src/components/` | Building blocks; `AppNav` (tab bar), `ui/` (icons, page header), `meal-ui` |
| `src/lib/` | Logic with tests: nutrition, allergen safety, diets, planner, shopping, coach, diary, progress |
| `supabase/migrations/` | Database structure — see [[Database]] |
| `supabase/seed/` | Starter recipe library |
| `public/sw.js` | Offline + notifications — see [[Offline & PWA]] |
| `tests/` | 293 Vitest tests |
