---
type: overview
tags: [meal-planner, security, privacy]
---
# Security & Privacy

Back to [[Meal Planner Home]]

- **Row Level Security on every table** — people only ever read/change their own rows (household members see only
  display names and the shared list).
- **Stranger test (2026-09-27):** as an anonymous visitor, all 19 tables read `[]`, every write was refused (401),
  private functions refused, the secrets table is not reachable. See [[Roadmap]] Step 33.
- **Secrets** (Spoonacular, USDA, Gemini, VAPID private key, cron secret) live only in `.env.local` and Vercel —
  never in GitHub; git history checked clean.
- **Reminder scheduler** is protected by a secret; wrong secret → 401 / nothing returned.
- **Browser security headers:** no-sniff, no framing, referrer policy, permissions policy (camera allowed for the scanner).
- **Sign-out** clears offline copies on the phone.
- **AI privacy:** see [[AI Coach]].
- `npm audit`: 0 known vulnerabilities in the app's packages.

> [!warning] This vault
> No passwords or secret keys are stored in these notes — keep it that way (Obsidian Sync may upload notes).
