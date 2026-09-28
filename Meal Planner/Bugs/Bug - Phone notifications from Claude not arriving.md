---
type: bug
status: workaround
severity: low
area: tooling
date: 2026-09-27
step: 19
found_by: owner
tags: [meal-planner, bug, tooling]
---
# Phone notifications from Claude not arriving

- **Symptom:** The owner asked to be notified on the phone when steps finished; notifications only appeared on the desktop.
- **Cause:** Mobile push is turned off in Claude Code's settings (`/config`), which Claude can't change itself.
- **Workaround:** Remote Control was turned on; the owner can enable mobile push in an interactive `claude` terminal.
- **Lesson:** Not an app bug — a tool setting. Tracked here so it isn't forgotten.

Related: [[Bugs]]
