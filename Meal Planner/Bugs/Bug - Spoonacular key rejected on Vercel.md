---
type: bug
status: fixed
severity: medium
area: config
date: 2026-09-27
step: 10
found_by: owner
tags: [meal-planner, bug, config]
---
# Spoonacular key rejected on Vercel (401)

- **Symptom:** Live site said "the recipe service didn't accept our key".
- **Cause:** The key pasted into Vercel had extra spaces/quotes (or a typo).
- **Fix:** The app now trims spaces and quotes from keys; the owner re-entered the key and redeployed.
- **Lesson:** After changing environment variables on Vercel you must **Redeploy**. Clean up pasted secrets in code.

Related: [[Maintenance & Troubleshooting]] · [[Bug - Reminders not set up yet]] · [[Bugs]]
