---
type: decision
status: accepted
area: allergens
date: 2026-09-27
step: 9
tags: [meal-planner, decision, safety]
---
# Two-layer allergen checks

- **Context:** A real API test leaked dairy recipes ([[Bug - Spoonacular let dairy recipes through]]).
- **Decision:** Every recipe must pass **two independent checks** — allergen tags/flags *and* a keyword scan — and
  if either says "maybe", it's hidden. Applied everywhere: planner, swaps, barcode scans, AI replies.
- **Consequences:** Occasionally hides a safe recipe (acceptable); never shows an unsafe one.

Related: [[Allergen Safety]] · [[Decisions]]
