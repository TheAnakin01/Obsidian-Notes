---
type: roadmap
tags: [meal-planner, roadmap]
---
# Roadmap (Steps 0–37, all done ✅)

Back to [[Meal Planner Home]] · Timeline: [[Build Log]]

## v1 — basic app (medium level)
- [x] 0 Planning: spec (`CLAUDE.md`), Git, GitHub
- [x] 1 Scaffold Next.js app
- [x] 2 Deploy early on Vercel
- [x] 3 Calorie & macro maths + tests
- [x] 4 Profile form with validation
- [x] 5 Supabase: database, clients, session proxy → [[Bug - profiles already exists when running migration 0001]]
- [x] 6 Sign up / sign in / sign out
- [x] 7 Save profile
- [x] 8 Recipe API → [[Decision - Spoonacular instead of Edamam]]
- [x] 9 Allergen safety → [[Decision - Two-layer allergen checks]]
- [x] 10 Dashboard UI → [[Bug - Spoonacular key rejected on Vercel]]
- [x] 11 Saved recipes → [[Bug - Spoonacular terms forbid caching and storing]]
- [x] 12 Polish & accessibility → [[Bug - Low colour contrast]]
- [x] 13 Launch check (owner tested on phone)

## v2 — advanced app
**Phase A — Foundations**
- [x] 14 Diet type, preferred store, timezone
- [x] 15 Recipe library schema + admins → [[Decision - Own recipe library with USDA nutrition]]
- [x] 16 USDA nutrition engine → [[Bug - USDA search returned HTML errors]]
- [x] 17 Admin recipe editor → [[Bug - USDA paneer had wrong carbs]]
- [x] 18 AI recipe drafting → [[Bug - Gemini model retired or overloaded]]

**Phase B — Weekly plan, shopping list, buy online** (owner's first priority)
- [x] 19 Weekly planner engine → [[Bug - Planner picked variety over calorie fit]] · [[Bug - Rice saved with cooked calories]]
- [x] 20 Week view UI
- [x] 21 Shopping list
- [x] 22 Buy online & WhatsApp share → [[Decision - Store deep links instead of checkout]]
- [x] 23 Today view (Spoonacular moved to Discover)

**Phase C — Offline-first app**
- [x] 24 Installable PWA
- [x] 25 Offline data & sync → [[Bug - Shopping list said You're offline]]

**Phase D — AI coach**
- [x] 26 Coach chat (opt-in, private, limited)
- [x] 27 Coach actions → [[Bug - Coach showed error screen before the answer]]

**Phase E — Add-ons**
- [x] 28 Food diary + barcode scan
- [x] 29 Progress charts → [[Bug - Chart text tiny on phones]]
- [x] 30 Smart allergen-safe swaps
- [x] 31 Meal reminders → [[Decision - Supabase pg_cron for reminders]] · [[Bug - Reminders not set up yet]]
- [x] 32 Household sharing → [[Decision - Households share the list, not the plan]]
- [x] 33 v2 launch check (security, a11y, free plans) → [[Bug - Missing security headers]]

**Phase F — Polish**
- [x] 34 Starter library (79 recipes) + bulk publish → [[Bug - Only one published recipe left the planner empty]]
- [x] 35 App-wide redesign with motion → [[Design System]] · [[Bug - Page animation trapped the tab bar]]
- [x] 36 Auto-update installed app → [[Bug - UI changes not showing on phone]]
- [x] 37 Blurred background + Supabase migration check fixed → [[Bug - Supabase Preview check failing]]

## Ideas for later
- [ ] Recipe photos
- [ ] 200+ recipes (use "Draft with AI")
- [ ] Hindi language option
- [ ] End-to-end tests and error monitoring (free tiers)
- [ ] Get 20–50 real users and collect feedback
