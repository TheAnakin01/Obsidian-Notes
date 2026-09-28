---
type: bug
status: fixed
severity: low
area: planner
date: 2026-09-27
step: 19
found_by: tests
tags: [meal-planner, bug, planner]
---
# Planner picked variety over calorie fit

- **Symptom:** Tests showed meals far from their calorie target when the library was small; same-day repeats appeared.
- **Fix:** New search order: calorie fit (±10%) first, then variety rules, relaxing step by step with a note to the
  user; same-day repeats only as a last resort. A test fixture was also too small and was enlarged.
- **Lesson:** Write down the priority order of rules explicitly and test the edge cases.

Related: [[Architecture]] · [[Bugs]]
