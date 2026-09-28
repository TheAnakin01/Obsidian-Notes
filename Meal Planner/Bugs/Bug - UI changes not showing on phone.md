---
type: bug
status: fixed
severity: high
area: pwa
date: 2026-09-27
step: 36
found_by: owner
tags: [meal-planner, bug, pwa, deploy]
---
# UI changes not showing on the phone

- **Symptom:** After the Week redesign went live, the owner still saw the old design in the installed app.
- **Cause:** An installed app left open keeps the old code in memory until it's fully closed.
- **Fix:** `/api/version` reports the live version; when the app comes back on screen it compares and reloads once
  if a newer version exists (never while you're typing).
- **Lesson:** Installed web apps need an update strategy.

Related: [[Offline & PWA]] · [[Updating the app]] · [[Bugs]]
