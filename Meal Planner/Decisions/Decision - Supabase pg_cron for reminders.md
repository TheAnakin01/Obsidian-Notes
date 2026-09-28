---
type: decision
status: accepted
area: reminders
date: 2026-09-27
step: 31
tags: [meal-planner, decision, reminders]
---
# Supabase pg_cron for reminders

- **Context:** Meal reminders must be checked every 15 minutes. Vercel's free plan only runs scheduled jobs once a day.
- **Decision:** A timer inside the database (pg_cron + pg_net) calls `/api/cron/reminders` every 15 minutes with a
  secret; database functions check the secret, so no all-powerful database key is ever needed.
- **Consequences:** Free and reliable; the scheduler SQL contains a secret, so it lives only on the owner's computer
  (git-ignored). Needed env vars on Vercel ([[Bug - Reminders not set up yet]]).

Related: [[Decisions]]
