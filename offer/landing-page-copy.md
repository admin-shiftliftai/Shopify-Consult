# Offer site — one page, full copy

Build on Carrd ($19/yr), Framer free tier, or a single Next.js page. One page only.
Brand: pick a studio-style handle (suggestions: **StoreSurgeon**, **AuditKit**,
**LiftAudit** — operate as a DBA under ShiftLift LLC). Placeholder below: `STORESURGEON`.

---

## Hero

**Your Shopify store is leaking sales. We'll show you exactly where — in 48 hours.**

A conversion audit that scores your store against 47 revenue checkpoints and hands you a
prioritized fix list — what's broken, why it's costing you money, and exactly what to do
about it. Fixed price. No calls required. No retainer pitch disguised as a report.

[**Get your audit → $297**]   [See a real sample report ↓]

*Trusted process: every finding screenshotted from YOUR store. If we can't find at least
5 meaningful issues, you get a full refund.*

---

## The problem (agitate, brief)

You're driving traffic — from ads, TikTok, wherever — and watching 98% of it leave
without buying. More traffic isn't the fix. A leaky bucket doesn't need more water.

---

## What you get

- **Scored report (0–100)** across 8 areas: product page, checkout, mobile, trust, offer…
- **Your top 3 fixes, step-by-step** — most take under an hour, named to the exact
  Shopify setting
- **Every finding screenshotted** from your actual store — see it yourself in seconds
- **The math**: what fixing the leaks is conservatively worth per month, assumptions shown
- **Delivered in 48 hours** as a PDF you'll actually read

## Tiers

| | **Core — $297** | **Deep — $597** | **Fix Sprint — $997** |
|---|---|---|---|
| 47-point scored audit | ✅ | ✅ | ✅ |
| Top-10 prioritized fixes | ✅ | ✅ | ✅ |
| Email + abandoned-cart flow review | | ✅ | ✅ |
| 15-min Loom walkthrough | | ✅ | ✅ |
| **We implement your top 3 fixes** | | | ✅ |

## Sample report
[Embed 2–3 pages of the demo report — the score table and fix #1. Watermark "SAMPLE".]

## FAQ

**Is this AI-generated?** Our analysis engine is AI-assisted — that's how we deliver in
48 hours at this price — and every single finding is human-verified against your live
store before it ships. Nothing goes in the report that we haven't seen with our own eyes.

**What do you need from me?** Your store URL and 5 minutes on an intake form. Analytics
screenshots make the audit sharper but aren't required.

**What if my store is already good?** Then the report says so, tells you what to test
next — and if we can't find 5 meaningful issues, you get a refund.

**Do I need to get on a call?** No. That's the point.

**Who is this for?** Stores doing roughly $1k–$100k/mo who want more out of the traffic
they already have. Pre-launch stores: wait until you have 30 days of real traffic.

---

## Footer
STORESURGEON is a ShiftLift LLC service · contact@… · Terms · Privacy

---
---

# Stripe + delivery setup (60–90 min, one time)

1. **Stripe** (stripe.com, under ShiftLift LLC — EIN + business bank account):
   Products → create "Core Audit $297", "Deep Audit $597", "Fix Sprint $997" as one-time
   prices → generate a **Payment Link** for each (no code needed).
2. **Post-purchase redirect:** each Payment Link → Settings → after payment → redirect to
   your intake form (Tally/Typeform, built from `audit-engine/intake-form.md`).
3. **Intake notification** → your email. That's the trigger to run the audit engine.
4. **Delivery:** export report to PDF (Markdown → PDF via Typora/pandoc, or a Notion
   share link). Send from a branded email (Google Workspace, $7/mo).
5. **Later (Phase 2):** swap Payment Links for Stripe Checkout on your own domain, add
   the retainer as a Stripe subscription product.

Total stack cost to start: **≈ $30–50** (domain + Carrd + Workspace). Everything else free tier.
