---
type: overview
tags: [meal-planner, costs, limits]
---
# Free Plan Limits

Back to [[Meal Planner Home]] · Ground rule: **never spend money** — no cards, no upgrades, no trials.

| Service | Free limit | What happens at the limit | Our design |
|---|---|---|---|
| Supabase Free | 500 MB DB, pauses after ~1 week without visits | App shows "Something went wrong" | Dashboard → **Restore** (free). See [[Maintenance & Troubleshooting]] |
| Vercel Hobby | Personal / non-commercial, function time limits | — | AI calls capped at ~75 s; pages allow 60–120 s |
| Spoonacular Free | 50 points/day (≈12 Discover views) | HTTP 402 until midnight UTC — it never charges | Discover only; no caching (terms) |
| USDA FoodData Central | ~1,000–3,600 requests/hour | Temporary error | Each ingredient looked up once and stored |
| Gemini free tier | Per-minute / per-day caps; Google may use data to improve products | "Coach is resting" message | 20 questions/user/day, 200/day total, minimal data → [[AI Coach]] |
| Open Food Facts | Fair use; attribution required | — | Only on barcode scans; credit shown |
| GitHub Free | Plenty | — | — |

The owner confirmed every plan is free on 2026-09-27 ([[Roadmap]] Step 33).
