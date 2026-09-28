---
type: bug
status: fixed
severity: medium
area: config
date: 2026-09-27
step: 31
found_by: owner
tags: [meal-planner, bug, config, reminders]
---
# Reminders said "not set up yet"

- **Symptom:** The Profile page said reminders weren't set up on the live site.
- **Cause:** The new keys (VAPID public/private, cron secret) were missing on Vercel or the site wasn't redeployed.
- **Fix:** Owner added them in Vercel → Settings → Environment Variables and redeployed. Endpoint now answers correctly.
- **Lesson:** `NEXT_PUBLIC_` keys are baked in at build time — a redeploy is required after changing them.

Related: [[Bug - Spoonacular key rejected on Vercel]] · [[Decision - Supabase pg_cron for reminders]] · [[Bugs]]
