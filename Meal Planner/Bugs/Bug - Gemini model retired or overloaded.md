---
type: bug
status: fixed
severity: medium
area: ai
date: 2026-09-27
step: 18
found_by: claude
tags: [meal-planner, bug, ai]
---
# Gemini model retired or overloaded

- **Symptom:** AI recipe drafts failed — one model was retired, the newest one often answered "503 high demand" on the
  free tier. A draft takes 20–25 s.
- **Fix:** Try a list of Flash models in order until one answers; one shared ~75 s deadline; pages allow up to 120 s.
- **Lesson:** Free AI tiers are busy — always have fallbacks and timeouts.

Related: [[AI Coach]] · [[Decision - Gemini free tier for AI]] · [[Bugs]]
