---
type: decision
status: accepted
area: pwa
date: 2026-09-27
step: 25
tags: [meal-planner, decision, pwa]
---
# Hand-written service worker instead of Serwist

- **Context:** The spec planned the Serwist library + IndexedDB for offline support.
- **Decision:** A small hand-written `public/sw.js` with exact rules (what to save, what never to save) and a tiny
  localStorage "outbox" for offline shopping ticks.
- **Why:** Less to maintain, full control (e.g. never cache Spoonacular data or admin pages), easy to unit test.
- **Consequences:** Needed a fix for in-app navigation ([[Bug - Shopping list said You're offline]]) and later an
  update strategy ([[Bug - UI changes not showing on phone]]).

Related: [[Offline & PWA]] · [[Decisions]]
