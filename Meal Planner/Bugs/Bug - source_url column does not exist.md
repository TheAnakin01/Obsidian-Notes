---
type: bug
status: fixed
severity: low
area: database
date: 2026-09-27
step: 11
found_by: owner
tags: [meal-planner, bug, database]
---
# "column source_url does not exist" (migration 0002)

- **Symptom:** Running `0002_saved_recipes_spoonacular.sql` failed.
- **Cause:** Same as 0001 — the GitHub integration had already applied 0002, so the column was already removed.
- **Fix:** Checked the table shape was right; no action needed.
- **Lesson:** Same root cause as [[Bug - profiles already exists when running migration 0001]] and
  [[Bug - Supabase Preview check failing]].

Related: [[Database]] · [[Bugs]]
