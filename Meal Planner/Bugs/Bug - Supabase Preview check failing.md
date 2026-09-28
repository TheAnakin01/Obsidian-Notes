---
type: bug
status: fixed
severity: medium
area: database
date: 2026-09-27
step: 37
found_by: owner
tags: [meal-planner, bug, ci, database]
---
# "Supabase Preview" check failing on every push

- **Symptom:** GitHub showed a red "Supabase Preview" check: `column "diet_type" of relation "profiles" already exists`.
- **Cause:** The Supabase GitHub integration auto-applies migration files on push. It had applied 0001–0002 itself,
  but the owner ran 0003–0013 by hand, so it retried 0003 on every push and failed. No data was harmed (it stops at
  the first statement).
- **Fix:** Owner ran a one-off SQL marking 0001–0013 as applied; an empty commit re-ran the check → green (commit b620025).
- **Lesson:** Know which tool owns your database changes. From now on: push the migration file only.

Related: [[Decision - Migrations applied by Supabase GitHub integration]] · [[Database]] · [[Bugs]]
