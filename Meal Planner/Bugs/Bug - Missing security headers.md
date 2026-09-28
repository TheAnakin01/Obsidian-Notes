---
type: bug
status: fixed
severity: medium
area: security
date: 2026-09-27
step: 33
found_by: claude
tags: [meal-planner, bug, security]
---
# Missing browser security headers

- **Symptom:** The launch check found the site sent only one security header.
- **Fix:** Added no-sniff, no framing (clickjacking protection), referrer policy and a permissions policy that still
  allows the camera for the barcode scanner.
- **Lesson:** Security checklists catch things that "work fine" but aren't safe.

Related: [[Security & Privacy]] · [[Bugs]]
