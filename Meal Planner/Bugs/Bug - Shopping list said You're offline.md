---
type: bug
status: fixed
severity: high
area: offline
date: 2026-09-27
step: 25
found_by: owner
tags: [meal-planner, bug, pwa]
---
# Shopping list said "You're offline"

- **Symptom:** Reopening the app offline and going to the shopping list showed "You're offline" instead of the list.
- **Cause:** Pages opened by tapping links inside the app never load as whole pages, so the service worker never saved them.
- **Fix:** On every page change the app asks the service worker to save the current page, Today, Week, Shopping and
  linked recipe pages (at most once a minute each). Owner confirmed it syncs on Android.
- **Lesson:** Test offline mode by *navigating inside the app*, not just by opening pages directly.

Related: [[Offline & PWA]] · [[Decision - Hand-written service worker instead of Serwist]] · [[Bugs]]
