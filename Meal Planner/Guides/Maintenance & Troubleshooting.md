---
type: guide
tags: [meal-planner, guide, troubleshooting]
---
# Maintenance & Troubleshooting

Back to [[Meal Planner Home]] · Limits: [[Free Plan Limits]]

| Problem | Likely cause | Fix |
|---|---|---|
| App says "Something went wrong" everywhere | Supabase free project **paused** after ~1 week without visits | supabase.com → project → **Restore** (free) |
| Discover says the daily recipe limit is reached | Spoonacular 50 points/day used up | Wait until midnight UTC (5:30 am IST). Never upgrade |
| "The recipe service didn't accept our key" | Wrong/expired Spoonacular key | Fix key in Vercel env vars → Redeploy ([[Bug - Spoonacular key rejected on Vercel]]) |
| Coach says it's resting | Daily AI limit or Gemini busy | Try later; limits reset after 24 h |
| Reminders don't arrive | Keys missing on Vercel, notifications blocked, or iPhone app not installed | [[Bug - Reminders not set up yet]]; iPhone needs Add to Home Screen (iOS 16.4+) |
| Phone shows the old design | Old version still open | Reopen the app (auto-updates); worst case swipe it closed and reopen |
| Red "Supabase Preview" check on GitHub | A migration failed | Ask Claude to read the error ([[Bug - Supabase Preview check failing]]) |
| A meal says "No safe recipe yet" | Library has nothing safe for that diet/allergy mix | Intended — add more recipes (Admin) |
| Sign-up email never arrives | Supabase's free email limit (a few per hour) | Wait an hour and try again |

## Regular check-ups (monthly)
- [ ] Open the live app (keeps Supabase awake)
- [ ] Vercel / Supabase / Google AI Studio still on **free** plans, no card added
- [ ] Ask Claude to run `npm audit` and update packages
