---
type: home
project: GitHub Profile
status: live
started: 2026-09-28
repo: https://github.com/TheAnakin01/TheAnakin01
live_url: https://github.com/TheAnakin01
tags: [github-profile, home, javascript, automation]
---
# 👤 GitHub Profile — Home

Back to [[Projects]]

The special `TheAnakin01/TheAnakin01` repo: its README is shown at the top of my GitHub profile. It's animated:
a **contribution heatmap**, an **ASCII-art portrait**, and a **neofetch-style info card**, plus a link to
[[Meal Planner Home|Meal Planner]].

## 🔗 Links
- **See it live:** https://github.com/TheAnakin01
- **Code:** https://github.com/TheAnakin01/TheAnakin01

## ⚙️ How it works
| Piece | File | What it does |
|---|---|---|
| Portrait | `scripts/portrait.mjs` → `assets/portrait.svg` | Turns a photo into animated ASCII art using `sharp`. Run once by hand (`npm run portrait`) |
| Heatmap + info card | `scripts/heatmap.mjs` → `assets/live/heatmap-*.svg`, `info-*.svg` | Reads my public contribution calendar (no token needed) and draws an animated heatmap with active days, best day and streak |
| Daily refresh | `.github/workflows/heatmap.yml` | GitHub Action every day at **00:30 UTC (6:00 IST)**. Commits "Refresh heatmap [skip ci]" only if something changed |

## 💡 Lessons
- **GitHub caches README images.** Updating the same file name kept showing old pictures, so each refresh is saved
  under a **new time-stamped file name** (`heatmap-202610010615.svg`) and the README points to it (`9938f05`).
- Private contributions only count if *"Show private contributions"* is on in profile settings (heatmap showed 459 after that, `f11f035`).

## 📜 History (2026-09-28)
`f02b747` launch → `e4a9482` last-year count on info card → `f4b3c82` heatmap above portrait →
`ba9a0fc` active days / best day / streak → `cf3528d` + `9938f05` cache-busting file names.
Since then the bot refreshes it daily.

## 🔧 If it breaks
- Heatmap script errors with *"Only found N days"* → GitHub changed its page format; update the regexes in `heatmap.mjs`.
- To refresh by hand: repo → **Actions** → *Refresh contribution heatmap* → **Run workflow**.
