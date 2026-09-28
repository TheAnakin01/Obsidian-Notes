---
type: decision
status: accepted
area: database
date: 2026-09-27
step: 37
tags: [meal-planner, decision, database]
---
# Migrations applied by the Supabase GitHub integration

- **Context:** Migrations were being run by hand *and* auto-applied by the GitHub integration, causing clashes
  ([[Bug - Supabase Preview check failing]]).
- **Decision:** The integration owns database changes. Add a migration file, push, check the "Supabase Preview"
  result. Never also paste it into the SQL Editor.
- **Exceptions:** seed data and the secret reminder scheduler are still run by hand.

Related: [[Database]] · [[Updating the app]] · [[Decisions]]
