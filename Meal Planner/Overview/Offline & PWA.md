---
type: overview
tags: [meal-planner, pwa, offline]
---
# Offline & PWA

Back to [[Meal Planner Home]] · Why hand-written: [[Decision - Hand-written service worker instead of Serwist]]

- **Installable:** web manifest + icons; "Install app" prompt on Android, Share → Add to Home Screen on iPhone.
- **Service worker** (`public/sw.js`):
  - App files, icons and background pictures → saved once, served from the phone (fast).
  - Your own pages (Today, Week, Shopping, recipes, profile) → fresh from the internet, saved copy when offline.
  - Never saves Discover (Spoonacular terms) or admin pages. Sign-out wipes saved pages.
- **Offline ticks:** shopping-list ticks go into an "outbox" on the phone and sync when back online.
- **Auto-update:** the app checks `/api/version` when you come back to it and reloads once if a newer version is live.

Bugs met here: [[Bug - Shopping list said You're offline]] · [[Bug - UI changes not showing on phone]]
