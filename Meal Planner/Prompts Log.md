---
type: log
tags: [meal-planner, prompts, ai]
---
# Prompts Log (what I asked Claude → what happened)

Back to [[Meal Planner Home]] · Also linked from [[AI]]

| # | My prompt (short) | Result |
|---|---|---|
| 1 | Plan a meal recommendation app (profile → calories/macros → allergy-safe recipes), Next.js + Supabase + Vercel, **never spend money**; write CLAUDE.md, set up GitHub | Spec + roadmap written, repo pushed |
| 2 | Repo link, "what to choose", "deployed on vercel" | Vercel Hobby set up, live URL |
| 3 | "start step 3" … "start step 13" | v1 built step by step ([[Roadmap]]) |
| 4 | Errors: "relation profiles already exists", "column source_url does not exist" | Explained, no harm ([[Bug - profiles already exists when running migration 0001]]) |
| 5 | "the recipe service didn't accept our key" | Key trimming + redeploy ([[Bug - Spoonacular key rejected on Vercel]]) |
| 6 | Rate my project 1–10, level, duration, roadmap, more advanced apps | ~5/10 medium, ideas list ([[Project Assessment]]) |
| 7 | Advanced level: buy ingredients online, offline mobile app, AI coach, weekly plans + shopping list, "add your addons" | v2 spec (Steps 14–33); choices: plan+list first, India, Gemini free, own library |
| 8 | "where is draft with ai" / "do I re-add rice, cumin…" | Explained admin flow |
| 9 | "give me short summaries" · "notify me on my phone" | Short reports; phone push blocked by a setting ([[Bug - Phone notifications from Claude not arriving]]) |
| 10 | "shopping list says you're offline" | Fixed ([[Bug - Shopping list said You're offline]]) |
| 11 | "coach shows try-again page first" | Fixed ([[Bug - Coach showed error screen before the answer]]) |
| 12 | "reminders aren't set up… keep README updated, get an MIT licence" | Env vars + redeploy; README; MIT license |
| 13 | "start step 33" (launch check) | Security/a11y/free-plan audit ✅ |
| 14 | "all good, work on remaining steps" | Starter library of 79 recipes + bulk publish |
| 15 | "there is no regenerate week" | Correct button is "New week plan" ([[Bug - Wrong button name in instructions]]) |
| 16 | "make the UI cooler, simpler, unique, with motion" / "can't see changes" | Week redesign; auto-update ([[Bug - UI changes not showing on phone]]) |
| 17 | "UI too basic, better animations, more user friendly" + "update README and everything remaining" | App-wide redesign ([[Design System]]) |
| 18 | "supabase preview failing" + "background blur image" | Migration check fixed; blurred background |
| 19 | "does this look impressive?" | ~8/10 advanced ([[Project Assessment]]) |
| 20 | "connect my Obsidian vault, upload all project data and bugs" | This vault section 🙂 |
