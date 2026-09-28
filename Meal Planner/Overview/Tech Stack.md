---
type: overview
tags: [meal-planner, tech-stack]
---
# Tech Stack

Back to [[Meal Planner Home]] · Terms explained in [[Glossary]]

| Layer | Tool | Plan / cost | Used for |
|---|---|---|---|
| Framework | **Next.js 16** (App Router, TypeScript) | Free | Pages and server logic |
| Styling | **Tailwind CSS v4** | Free | All styling and animations → [[Design System]] |
| Hosting | **Vercel** | Hobby (free) | Live site, auto-deploy from GitHub |
| Database + login | **Supabase** | Free | Postgres, Auth, Row Level Security, Realtime, pg_cron → [[Database]] |
| Code storage | **GitHub** | Free | Repo `TheAnakin01/meal-planner` |
| Nutrition data | **USDA FoodData Central** | Free key | Ingredient nutrition per 100 g |
| Packaged food | **Open Food Facts** | Free, open data (ODbL) | Barcode scans in the diary |
| AI | **Google Gemini** | Free tier | Coach and recipe drafting → [[AI Coach]] |
| Extra recipes | **Spoonacular** | Free (50 points/day) | Discover page only |
| Push notifications | **web-push** + VAPID keys | Free | Meal reminders |
| Tests | **Vitest** | Free | 293 unit tests |
| Validation | **zod** | Free | Checking every form and API response |

Limits of each free plan: [[Free Plan Limits]]. Why each was chosen: [[Decisions]].
