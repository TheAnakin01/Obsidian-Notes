---
type: decision
status: accepted
area: shopping
date: 2026-09-27
step: 22
tags: [meal-planner, decision, shopping]
---
# Store deep links instead of checkout

- **Context:** "Buy ingredients online" for Indian users. Grocery apps have no free ordering APIs.
- **Decision:** One tap opens the item's **search page** on the user's preferred store (BigBasket, Blinkit, Zepto,
  Swiggy Instamart, Amazon.in, JioMart). No accounts, payments or affiliate tags. All links in one file
  (`src/lib/stores.ts`) so a changed URL is a one-line fix.
- **Consequences:** Free and simple; prices and delivery are up to the store.

Related: [[Features]] · [[Decisions]]
