---
type: overview
tags: [meal-planner, design, ui]
---
# Design System

Back to [[Meal Planner Home]]

- **App shell:** sticky blurred header; on phones a floating bottom tab bar — Today · Week · Shopping · Diary · More.
  "More" slides up a sheet with Progress, AI coach, Household, Discover, Saved, Profile, Recipe library (admin), Sign out.
- **Background:** soft blurred colour pictures (`public/bg/light.webp`, `dark.webp`, ~8 KB each).
- **Shared styles** (`globals.css`): `card`, `btn` + `btn-primary` / `btn-secondary` / `btn-dark`, `chip`, `input`, `page`, `muted`.
- **Motion:** fade-up, slide, pop, sheet-up, float, staggered lists, page fade-in, count-up numbers, calorie rings
  that draw themselves. All off when the phone asks for "reduce motion".
- **Meal colours:** breakfast amber 🌅, lunch green ☀️, dinner indigo 🌙 — decoration only; text keeps high contrast.
- **Quality bar:** 0 accessibility issues (axe) in light and dark mode; works at 360 px wide with no sideways scrolling.

History: v1 basic look → Week redesign → app-wide redesign → blurred background ([[Build Log]]).
Bugs met here: [[Bug - Page animation trapped the tab bar]] · [[Bug - Chart text tiny on phones]] · [[Bug - Low colour contrast]]
