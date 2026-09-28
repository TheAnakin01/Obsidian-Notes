---
type: overview
tags: [meal-planner, glossary, learning]
---
# Glossary (plain language)

Back to [[Meal Planner Home]]

- **API** — a way for one program to ask another for data (e.g. our app asks USDA "how many calories in rice?").
- **API key** — a password for an API. Secret keys never go in GitHub; they live in `.env.local` and in Vercel settings.
- **Commit / push** — a saved snapshot of the code / sending it to GitHub. Every push to `main` makes Vercel redeploy.
- **Deploy** — putting the new version on the live website.
- **Environment variables** — settings like API keys kept outside the code (Vercel → Settings → Environment Variables).
- **Migration** — a file that changes the database structure (adds tables or columns). See [[Database]].
- **RLS (Row Level Security)** — the database rule "you can only see your own rows". See [[Security & Privacy]].
- **PWA (Progressive Web App)** — a website you can install like an app and use offline. See [[Offline & PWA]].
- **Service worker** — a small script the phone keeps that saves pages for offline use and shows notifications.
- **Server action** — code that runs on the server when you tap a button (keeps secrets safe).
- **Supabase** — our database and login provider.
- **Vercel** — where the website is hosted.
- **pg_cron** — a timer inside the database; it triggers our reminders every 15 minutes.
- **Realtime** — Supabase feature that instantly pushes changes to other phones (household list).
- **Macros** — protein, carbohydrates, fat.
- **TDEE** — calories your body uses per day, including activity.
- **axe** — an automatic accessibility checker (contrast, labels, headings).
- **Lint** — an automatic code-style checker.
- **Vitest** — the tool that runs our automated tests.
- **Canvas / Base / Wikilink** — Obsidian features, see [[How to use this vault]].
