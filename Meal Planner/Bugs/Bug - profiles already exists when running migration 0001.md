---
type: bug
status: fixed
severity: low
area: database
date: 2026-09-27
step: 5
found_by: owner
tags: [meal-planner, bug, database]
---
# "relation profiles already exists" when running migration 0001

- **Symptom:** Running `0001_init.sql` in the SQL Editor failed: table `profiles` already exists.
- **Cause (found later):** The Supabase GitHub integration had already applied the file automatically on push.
- **Fix:** Verified the tables were correct and continued. Root cause fully understood only in
  [[Bug - Supabase Preview check failing]].
- **Lesson:** When something "already exists", find out *who* created it before re-running anything.

Related: [[Database]] · [[Bugs]]
