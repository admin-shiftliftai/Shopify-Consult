# Dry-run runbook — real store, ~15 minutes

Run this from your own machine (the cloud sandbox blocks outbound fetches to stores).
Do 2–3 practice stores before charging anyone.

## 1. Pick a store (2 min)
Small/mid independent store, ideally one you found via hashtag browsing (#shopifystore,
niche hashtags) or a store that's running ads (they have traffic → audits matter more).

## 2. Collect signals (8 min)
- `https://STORE.com/products.json` → save the JSON (public on nearly every Shopify store;
  append `?limit=250` for more)
- Homepage: save full-page screenshot (mobile width too — Chrome DevTools device mode)
- Their top product page: full-page screenshot, mobile + desktop
- View-source the product page and save the HTML (catches apps installed, theme name)
- Optional: run the homepage through PageSpeed Insights, screenshot the mobile score

## 3. Run the chain (5 min)
In Claude (claude.ai or API):
1. Paste `prompts/01-extract-signals.md` + attach the materials → get signals JSON
2. Paste `prompts/02-score-checklist.md` + signals JSON + `checklist.md` → get scores
3. Paste `prompts/03-generate-report.md` + both JSONs + `report-template.md` → get report

## 4. QA (the part that makes it worth $297+)
- Open the store side-by-side; verify EVERY cited finding is really there. Delete
  anything you can't see with your own eyes.
- Screenshot each top-3 finding for the report.
- Sanity-check the math section's assumptions.
- Add one insight the AI missed — there's always one, and it's usually the thing the
  merchant remembers.

## 5. For unpaid practice runs
Turn the best one into your first teardown content (anonymize the store), and consider
sending the merchant the free mini version (3 issues) — that's outreach and portfolio
in one move.
