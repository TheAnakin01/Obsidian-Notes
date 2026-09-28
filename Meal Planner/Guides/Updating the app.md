---
type: guide
tags: [meal-planner, guide, deploy]
---
# Updating the app

Back to [[Meal Planner Home]]

## The normal flow
1. Ask Claude Code (in the `C:\Meal_Planner` project) for the change.
2. Claude runs the checks — **tests, lint, type check, build** — and updates `README.md` / `CLAUDE.md`.
3. Claude commits and pushes to GitHub (`main`).
4. **Vercel** deploys automatically (~1–2 minutes). `https://meal-planner-pied-beta.vercel.app/api/version` shows the live version.
5. **Supabase** applies any new database migration automatically — see the "Supabase Preview" check on the commit.
   Don't paste migrations into the SQL Editor ([[Decision - Migrations applied by Supabase GitHub integration]]).
6. Phones: the installed app refreshes itself when reopened ([[Bug - UI changes not showing on phone]]).

## When you change a secret key
Vercel → Project → Settings → Environment Variables → edit → **Redeploy** (Deployments → ⋯ → Redeploy).
Keys starting with `NEXT_PUBLIC_` only take effect after a redeploy.

## Adding recipes
Admin → Recipes → **Draft with AI** or **New** → review → publish. Many drafts at once → **Publish ready drafts**.

## Afterwards
Ask Claude to add the change to this vault ([[Build Log]], new [[Bugs]] or [[Decisions]] notes).
