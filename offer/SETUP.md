# Launch setup — payment, intake, delivery, hosting

Everything to go from "assets in a repo" to "can take money." ~90 minutes, ~$0–50.
Do it in this order. Entity is ShiftLift LLC (GA), so nothing here is blocked.

## 1. Stripe — take payment (30 min, free)
1. Create/confirm a Stripe account at stripe.com under **ShiftLift LLC** (needs EIN +
   a business bank account for payouts).
2. **Products → Add product**, three one-time products:
   - Core Audit — $297
   - Deep Audit — $597
   - Fix Sprint — $997
3. For each, **Create payment link** (Stripe → Payment Links → New). No code needed.
4. On each payment link: **After payment → Redirect** → paste your intake form URL
   (step 2 below). Turn on **"Collect customer email."**
5. Copy the 3 payment-link URLs. In `offer/index.html`, replace the three
   `href="#" data-stripe="…"` on the pricing buttons with these URLs.

## 2. Intake form — collect the store (15 min, free)
1. Build a form in **Tally.so** or **Typeform** (free tier) from
   `../audit-engine/intake-form.md` — store URL, name/email, top products,
   optional analytics screenshots, and the consent line.
2. Turn on **email notification to yourself** on submit (Tally: Integrations → Email).
   That email is your signal to run the audit.
3. Use this form's public URL as the Stripe post-payment redirect (step 1.4).

## 3. Delivery (10 min, free–$7/mo)
1. Run the audit: `../audit-engine/prompts/00-one-shot-simple.md` + their screenshots.
2. Paste the finished report into the branded HTML template
   (`../audit-engine/report-template.html`) — or a Google Doc — and
   **File → Print → Save as PDF**.
3. Email it from a branded address (Google Workspace, ~$7/mo, or just
   admin@shiftliftai.com to start).

## 4. Host the offer page (15 min, ~$0–20/yr)
Pick one — `offer/index.html` is a single self-contained file, drop-in anywhere:
- **Netlify Drop** (netlify.com/drop): drag the file in, live in 30 seconds, free.
- **GitHub Pages**: repo Settings → Pages → deploy from `main` → `/offer` (free;
  URL like admin-shiftliftai.github.io/Shopify-Consult).
- **Carrd / Framer**: if you'd rather rebuild it in a visual editor.
- Point a domain at it later (e.g. audit.shiftliftai.com or a new one, ~$12/yr).

## 5. Go-live checklist
- [ ] 3 Stripe payment links created + pasted into `offer/index.html`
- [ ] Intake form live + notifying you + wired as the Stripe redirect
- [ ] Offer page hosted at a real URL
- [ ] Test purchase with a Stripe test card → confirm redirect + notification fire
- [ ] Sample-report link in the offer page points where you want (currently the
      Honey Next Door audit)
- [ ] Send the Honey Next Door email (`../clients/honeynextdoor/ready-to-send-email.md`)
- [ ] Post teardown #1 (`../clients/honeynextdoor/teardown-script.md`)

## Running cost to operate
Stripe takes ~2.9% + 30¢ per sale. Everything else free tier until volume justifies
Workspace ($7/mo) + a domain (~$12/yr). First audit pays for the year.
