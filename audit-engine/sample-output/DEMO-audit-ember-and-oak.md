# Ember & Oak Candle Co. — Conversion Audit
**Prepared for Maya · July 2026 · by ShiftLift**

> ⚠️ **DEMO SAMPLE.** "Ember & Oak" is a realistic composite of common small candle-store
> patterns, created to demonstrate report quality and voice. It is not a real client.
> Real audits cite only verified, screenshotted findings — see `dry-run-runbook.md`.

---

## Your score: 58/100 — Leaking

Your product photography and brand voice are better than 80% of candle stores we see — but
your product page hides the two things buyers need most (shipping cost and reviews), and
your mobile buy button disappears the moment someone scrolls. Fixing the top 3 items below
is conservatively worth **$540–$1,350/month** at your current traffic (assumptions in
"The math"). Bottom line: you don't have a traffic problem, you have a leaky bucket.

| Area | Score | Status |
|------|-------|--------|
| Product page | 45/100 | 🔴 Priority |
| Cart & checkout | 50/100 | 🔴 Priority |
| Mobile | 50/100 | 🔴 Priority |
| First impression & hero | 67/100 | 🟡 |
| Retention & capture | 50/100 | 🟡 |
| Offer & pricing | 63/100 | 🟡 |
| Navigation | 80/100 | 🟢 |
| Trust | 80/100 | 🟢 |

---

## Your top 3 fixes (do these first)

### 1. Your mobile add-to-cart button vanishes on scroll
- **What we found:** On `/products/cedar-smoke-8oz`, the Add to Cart button sits below
  4 images and your (great) scent description. On a phone, it's 2.5 screens down — and
  there's no sticky ATC bar. 71% of your traffic is mobile (your analytics screenshot).
- **Why it costs you money:** Mobile shoppers who are ready to buy have to scroll back
  and hunt. Every extra action sheds buyers; sticky ATC exists because this is one of
  the most-measured mobile leaks in e-commerce.
- **Exactly what to do:** Theme editor → Product pages → enable "sticky add to cart"
  (your theme, Dawn 12.0, has it built in — Settings → Product page → check
  "Enable sticky add-to-cart bar"). Zero cost, ~5 minutes.
- **Estimated impact:** typical range +2–5% mobile conversion → **$180–$450/mo** on your
  numbers (assumptions below).
- **Effort:** 5 minutes, DIY.

### 2. Shipping cost is a checkout surprise
- **What we found:** No shipping information anywhere on product pages or cart. A buyer
  learns shipping is $6.95 only at checkout step 2. Your cart also has no free-shipping
  threshold, though your AOV ($34) sits just under a natural $45 threshold.
- **Why it costs you money:** "Unexpected shipping cost" is the #1 self-reported cart
  abandonment reason across every major checkout study. You're triggering it on 100% of
  orders.
- **Exactly what to do:** (a) Add "Free U.S. shipping over $45 — otherwise $6.95 flat"
  under the price on product pages (theme editor → Product page → text block, 10 min).
  (b) Set the free-shipping rate: Settings → Shipping → add condition ≥ $45. (c) Add a
  cart progress bar ("You're $11 from free shipping!") — your theme supports this
  natively in cart settings.
- **Estimated impact:** threshold set just above AOV typically lifts AOV +8–15% AND cuts
  abandonment → conservatively **$250–$600/mo** combined.
- **Effort:** ~45 minutes, DIY.

### 3. 214 reviews exist — and zero are visible near the buy box
- **What we found:** Judge.me is installed and has collected 214 reviews (4.7★) but the
  widget renders only at the very bottom of product pages, below the fold ×4. No star
  rating appears near the product title.
- **Why it costs you money:** Social proof works at the moment of decision, not three
  screens later. Right now a first-time visitor evaluating $28 candles sees no evidence
  anyone has ever bought one.
- **Exactly what to do:** Judge.me app → Widgets → enable "Star rating badge" on product
  title; move the review widget block directly under the description block in the theme
  editor (drag, 2 minutes). Turn on "review carousel" for the homepage.
- **Estimated impact:** visible ratings near title typically +1–3% CR → **$110–$300/mo**.
- **Effort:** 15 minutes, DIY.

---

## Full findings (14 issues, prioritized)

**Product page** — title says "Cedar Smoke №4" (no benefit/use language) · no
compare-at price on the bundle SKU · scent notes buried in an accordion · return policy
link absent from buy box area (it exists in footer).
**Cart & checkout** — no express pay above the fold in cart (Shop Pay enabled but Apple
Pay off in Payments settings) · discount field prominent in cart (invites coupon-hunting;
inline it) · no cart upsell (wick trimmer at $12 is the obvious one-tap add).
**Hero** — headline "Welcome to our store" on mobile variant (default text left in a
theme section) · email popup fires at 3 seconds (move to exit-intent/30s).
**Retention** — abandoned-cart flow inactive (Klaviyo installed, flow in draft — turn it
on) · thank-you page has no offer.
**Offer** — no bundle for a consumable product people buy 2–3 of (create "any 3 for $75").

---

## Quick wins (under 1 hour each)
- Enable sticky ATC (5 min) · Turn on Apple Pay (2 min) · Publish the drafted Klaviyo
  abandoned-cart flow (10 min) · Fix "Welcome to our store" mobile hero text (5 min) ·
  Star badge near title (15 min) · Move popup to exit-intent (10 min).

## What you're already doing right
- Photography is genuinely excellent — in-use lifestyle shots on every product.
- About page tells a real founder story; this is retention fuel most stores lack.
- Navigation is clean: 5 items, customer-language collection names.
- Policies are real and humane (30-day returns, plainly worded).

## What we'd verify next
Checkout flow internals (needs a test order) · email flow content quality · post-purchase
survey data · paid traffic landing-page match. This is what the monthly optimization
retainer covers.

## The math
Your inputs: ~5,400 sessions/mo · 1.6% CR · $34 AOV → ≈ $2,940/mo revenue.
Top-3 fixes, conservative bounds only: +0.4pp blended CR and +$3 AOV
→ ≈ $3,480–$4,290/mo → **+$540–$1,350/mo**. Assumptions: mobile share 71%, fix effects
at the LOW end of published ranges, no traffic growth assumed.

---
*Questions? Reply to the delivery email — one round of clarification is included.
Want us to implement the top 3 for you? That's the Fix Sprint.*
