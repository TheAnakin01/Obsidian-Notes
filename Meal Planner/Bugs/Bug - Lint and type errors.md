---
type: bug
status: fixed
severity: low
area: code-quality
date: 2026-09-27
step: 29
found_by: tests
tags: [meal-planner, bug, tooling]
---
# Lint and type errors

Small issues caught by the automatic checks before they reached users:
- `useLatestWeightAction` looked like a React hook to the linter → renamed `applyLatestWeightAction`.
- Setting React state directly inside an effect (count-up animation) → rewritten to update inside animation frames.
- A Supabase RPC typing error → fixed with an explicit type.
- Missing route types → always run `npm run build` before the type check.
- Unused imports after the redesign → removed.

**Lesson:** Run tests, lint, type check and build before every push — they're a free safety net.

Related: [[Updating the app]] · [[Bugs]]
