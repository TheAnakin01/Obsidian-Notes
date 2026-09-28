---
type: log
tags: [meal-planner, log, timeline]
---
# Build Log

Back to [[Meal Planner Home]] · Steps: [[Roadmap]] · 54 commits in total (repo `TheAnakin01/meal-planner`)

## 2026-09-27 — v1 (medium version)
- `0264e4d` Spec (CLAUDE.md) and .gitignore
- `ea4e02b` Next.js app scaffolded; `4615b10` calorie & macro maths with tests; live on Vercel
- `6a0872c` Profile form with live results
- `c7669f9` Supabase clients, session proxy, first migration
- `71332f4` Sign-up / sign-in / sign-out and page protection
- `e445b76` Profile saved to Supabase, dashboard page
- `44654fc` **Switched Edamam → Spoonacular** ([[Bug - Edamam has no free plan]])
- `41fef5d` **Second-layer allergen check** ([[Bug - Spoonacular let dairy recipes through]])
- `c264f7b` Allergy-safe recipe cards; `cc4b5a5` API-key trimming fix
- `cf63be1` Saved recipes, no caching (Spoonacular terms)
- `95fa8e4` Polish: accessible colours, error/404/loading pages
- `b192627` Launch check recorded → **v1 done** (~5/10, medium level)

## 2026-09-27 — v2 (advanced)
- `676c166` v2 spec: own recipe library, weekly plans, shopping list, PWA, AI coach
- `e365489` Diet type, store, timezone · `523812a` recipe library schema + admins
- `2552e08` USDA nutrition engine & ingredient importer · `783eb79` admin recipe editor
- `dee2405` AI recipe drafting (Gemini)
- `bd32665` Weekly planner engine · `460eda3` week page · `beb5782` shopping list
- `2281d58` Buy-online links + WhatsApp share · `392d3cf` Today reads the week plan; Discover tab
- `155a003` Installable app · `183c222` offline support · `72e1aa6` fix: in-app navigation saved offline
- `5764505` AI coach · `e01ee39` coach actions · `b0c47dc` fix: coach error screen
- `df88a39` Food diary + barcodes · `14408b3` progress charts · `49b893f` swap ideas
- `11f112b` Meal reminders (pg_cron + web push)
- `34c8552` MIT license + full README · `706246f` env vars listed
- `a563e32` Household sharing (live list)
- `722b1b0` v2 launch check: security headers, audits

## 2026-09-27 — polish
- `7acd545` Starter library (79 recipes) + one-tap publish
- `24c5c07` Week page redesign (day picker, rings, motion) · `43dd30a` README wording
- `25e128d` Installed app auto-updates
- `1ab5d4e` New app shell (tab bar, More sheet, page transitions), Today redesign
- `2a00629` Every page redesigned; README + spec updated
- `21cd04b` Blurred background; migrations documented
- `b620025` Re-ran Supabase check → ✅ green · `acb3300` noted the fix

## 2026-09-28
- Project notes moved into this Obsidian vault; project rated ~8/10, advanced ([[Project Assessment]]).
