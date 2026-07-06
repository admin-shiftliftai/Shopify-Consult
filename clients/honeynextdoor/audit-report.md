# Honey Next Door — Conversion Audit
**honeynextdoor.com · July 2026 · by ShiftLift (practice audit #1)**

> Basis: desktop homepage screenshot, full catalog page screenshot, complete
> `/products.json` (20 products). NOT observed: product-page layout, mobile, cart,
> checkout, email — those areas are scored N/A and listed under "What we'd verify next."

---

## Score: 53/100 — Leaking (from observable areas only)

Your brand is genuinely charming — "unheated, unfiltered, and generally not messed with"
is better copy than most agencies write — and your differentiator (honey from the buyer's
own neighborhood) is one of the strongest we've ever seen on a small store. But the store
buries that differentiator inside a variant dropdown, a quarter of the catalog is sold-out
dead weight, and one listing carries a legal-risk health claim plus a leftover eBay
tracking pixel. The top three fixes below are brand-defining, not just conversion tweaks.

| Area | Score | Basis |
|------|-------|-------|
| Product/catalog data | 45/100 | 🔴 full products.json |
| First impression & hero | 55/100 | 🟡 homepage screenshot |
| Offer & pricing | 50/100 | 🔴 catalog data |
| Trust & compliance | 55/100 | 🟡 partial + one red flag |
| Navigation | 65/100 | 🟢 screenshots |
| Cart & checkout | N/A | not observable |
| Mobile | N/A | not observable |
| Retention & capture | N/A | not observable |

---

## Top 3 fixes

### 1. Your best idea in the world is hidden in a dropdown
- **What we found:** Neighborhood honey — Buckhead, Inman Park, Grant Park, 12 in all —
  exists only as *variants* of generic products ("1 lb. Pure Raw Atlanta Honey"). Worse,
  the variant option is literally mislabeled: on the 1lb and 2lb jars the option NAME is
  "1lb"/"2lbs" and the *values* are the neighborhoods. Variants get no Google pages, no
  individual photos (only Oakhurst/Candler/Inman images exist), no way to link someone
  straight to "Buckhead honey."
- **Why it costs money:** "Honey from YOUR street" is the whole brand ("A Neighborhood
  Honey Company" is the tagline!) — and a shopper landing on the site can't see it, search
  engines can't index it, and gift-buyers can't share it. This is the Savannah-Bee-scale
  asset in the catalog, invisible.
- **Exactly what to do (phased):**
  (a) Today: rename the variant option from "1lb"/"2lbs" to "Neighborhood" (Products →
  edit → Variants) — 10 minutes.
  (b) This month: create a "Shop by Neighborhood" collection page + homepage block
  ("Find your neighborhood's honey"), with a labeled jar photo per neighborhood.
  (c) For SEO/gifting: split the flagship into per-neighborhood products or landing pages
  ("Buckhead Raw Honey") so each neighborhood ranks and links.
- **Impact:** direction, not a range we can honestly quantify without analytics — but it
  compounds into SEO, gifting, and the realtor/corporate channels in the growth brief.
- **Effort:** (a) minutes · (b) an afternoon · (c) a weekend.

### 2. A quarter of the catalog is dead weight
- **What we found (all verifiable in products.json):** Tumblers — all 7 variants sold out,
  listed since 2020. Truffle Honey — sold out. Gallberry — sold out. Sourwood — all 4
  variants sold out (copy still says "this year is easily the finest Sourwood we've ever
  made" — written 2019). Soap — 7 of 8 scents sold out. That's 5 of 20 products a shopper
  can click and can't buy, shown right in the main grid.
- **Why it costs money:** every dead click is a bounce, and a grid full of "Sold out"
  teaches visitors the store is inactive — poison for a first-time buyer's trust.
- **Exactly what to do:** unpublish the tumblers (or make them a waitlist); for seasonal
  honeys (Sourwood/Gallberry/Truffle) add a "back in season — get notified" email capture
  instead of a dead Sold Out card, and push them to the bottom of collections (Shopify
  collection sort or a "Coming back" collection). Refresh the stale vintage copy.
- **Impact:** typical range for removing dead-end PDPs and adding back-in-stock capture:
  +1–3% CR plus an owned email list from your scarcest (most desired) products.
- **Effort:** ~1 hour, DIY.

### 3. The Elderberry Syrup listing is a legal and technical liability
- **What we found:** the product description contains (a) explicit medical claims —
  "Clinically shown to help boost your immune system… will lessen the severity and length
  of your illness" — and (b) a leftover eBay tracking pixel
  (`<img src="//rover.ebay.com/roversync/…">`) pasted into the HTML from an old eBay
  listing, firing a third-party tracker on your page.
- **Why it costs money:** disease-treatment claims on a food product are FDA/FTC
  warning-letter territory — a real risk, not a conversion tweak. The eBay pixel leaks
  visitor data to a marketplace you don't even sell on and can trigger browser security
  warnings.
- **Exactly what to do:** edit the description (Products → Elderberry Syrup → edit HTML):
  delete the `<img>` tag, and replace the medical sentences with compliant framing
  ("made with organic elderberries, traditionally used to support wellness" — no illness
  claims). 15 minutes.
- **Impact:** risk removal — worth more than any CR gain on this list.
- **Effort:** 15 minutes, DIY. Do this one first.

---

## Full findings (prioritized within groups)

**Catalog & product data**
- Generic product titles: "Soap", "Candles", "Organic Lip Balm" — no benefit, no keywords
  (compare: "Sweet Clover Honey" copy, which is excellent).
- Most products have exactly ONE photo; the Tunisian candle has 32 variants (4 colors × 8
  fragrances) and a single photo — buyers can't see what they're choosing.
- No reviews visible anywhere (no stars on any product card in either screenshot). If you
  have happy repeat customers (you clearly do), that proof is invisible.
- 1-gallon jars say "AVAILABLE FOR PICKUP ONLY" in the description, but every gallon
  variant has `requires_shipping: true` — checkout will happily sell a $124–$170 gallon
  to someone in Oregon and create a refund headache. Configure real local-pickup-only.
- Copy inconsistency: "130 hives / twelve apiaries" (2lb jar) vs "150 hives / fifteen
  apiaries" (1lb, 3oz, gallon) — pick the current number everywhere.
- Product-type/tag chaos: Pure Beeswax and the ceramic candle have product_type "Honey";
  soap is tagged "Honey" — automated collections and search filters will misfire.
- "Scratch and Dent Honey" is a *great* offer hiding under a clearance name — reframe as
  "Ugly Jar Club" or similar and it's a content asset.

**Hero & first impression**
- Hero image is blurry (out-of-focus jar close-up) on a carousel; your product shots on
  white are crisp — use one, kill the carousel, keep the single SHOP NOW CTA.
- No announcement bar offer (shipping threshold / farmers-market schedule / seasonal drop).
- "Hive Removal" (a service) sits mid-nav in a retail store — move it under About or FAQ;
  add a "Best Sellers" or "Shop by Neighborhood" link instead.

**Offer & pricing**
- Zero bundles or gift sets in a 20-product catalog made for gifting (honey + candle +
  lip balm = "Taste of [Neighborhood]" box; "any 3 for $X" on 3oz jars). Biggest AOV lever.
- No compare-at anchoring except one sold-out product; gallon jars do anchor well.
- Tupelo scarcity copy ("get it while you can") is honest urgency — good; apologizing for
  the price increase in the description is not — state the shortage, drop the apology.

**What you're doing right**
- Brand voice ("generally not messed with", the cease-and-desist tumbler joke) is a moat.
- Neighborhood concept + hive-removal-to-honey story = authenticity most brands fake.
- Sweet Clover "Honey on the Side" farm-partnership program is smart line expansion with
  honest provenance framing.
- Price laddering within products (3oz → 1lb → 2lb → gallon) is already there.

---

## What we'd verify next (not observable in this run)
Mobile product page (sticky ATC, tap targets) · cart/checkout (express pay, guest
checkout, shipping surprise) · email capture + abandoned-cart flow · policies/footer ·
PageSpeed · the homepage title tag (Google indexes it as "…Local Atlanta Bees - Tupelo
Honey" — looks misconfigured) · a price mismatch to check: catalog feed says Bourbon
Barrel $12 while the storefront grid shows $17 — one of them is stale.

## The math (placeholder assumptions — replace with real analytics)
IF ~3,000 sessions/mo at 1.5% CR and $26 AOV ≈ $1,170/mo online. Conservative effects of
fixes 1–2 + a gift bundle (+0.5pp CR, +$4 AOV) ≈ $1,800–2,100/mo → **+$600–900/mo**, before
any SEO upside from neighborhood pages. Assumptions are stated, not known — the first
retainer task would be pulling real numbers.
