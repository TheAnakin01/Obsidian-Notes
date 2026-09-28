---
type: bug
status: fixed
severity: high
area: legal
date: 2026-09-27
step: 11
found_by: claude
tags: [meal-planner, bug, terms]
---
# Spoonacular terms forbid caching and storing

- **Symptom:** The app cached recipe results for an hour and saved full recipe details.
- **Cause:** Reading the terms: caching needs written permission; only recipe id, title and image may be stored.
- **Fix:** Removed caching (`no-store`); migration 0002 trimmed saved recipes to id / title / image; added the
  required "Recipes powered by spoonacular" backlink.
- **Lesson:** Read API terms, not just docs. This is also why we built our own recipe library.

Related: [[Decision - Own recipe library with USDA nutrition]] · [[Bug - source_url column does not exist]] · [[Bugs]]
