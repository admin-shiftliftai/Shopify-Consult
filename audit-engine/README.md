# ShiftLift Audit Engine — AI Shopify Conversion Audit

Productized-service workflow: merchant submits their store → AI drafts a prioritized
conversion audit → you QA (~30–60 min) → send branded report. Sold at $297–$997 fixed price.

## How a single audit runs, end to end

```
Intake form (intake-form.md)
        │
        ▼
STEP 1 · Signal collection (~10 min, mechanical)
  - Store URL, /products.json, homepage + top product page (screenshots or HTML)
  - Optional: merchant-provided analytics screenshots (traffic, conversion, AOV)
        │
        ▼
STEP 2 · AI prompt chain (prompts/01→03, ~5 min of runtime)
  01-extract-signals.md   → structured JSON of observable store facts
  02-score-checklist.md   → scores the store against checklist.md (0–100 + per-area)
  03-generate-report.md   → drafts full report into report-template.md format
        │
        ▼
STEP 3 · Human QA (30–60 min early, <30 min once practiced)
  - Verify every claim is actually true on the store (no hallucinated issues)
  - Sharpen the top-3 fixes; add 1–2 insights only a human spots
  - Estimate $ impact honestly (ranges, stated assumptions)
        │
        ▼
STEP 4 · Deliver
  - Export to branded PDF (or Notion share link), send + 15-min Loom walkthrough (optional upsell)
```

## Pricing ladder

| Tier | Price | What they get |
|------|-------|---------------|
| Mini teardown (lead magnet) | Free | 3 issues, delivered publicly or via DM |
| Core audit | $297 | Full scored report, top-10 prioritized fixes |
| Deep audit | $597 | Core + email/checkout flow review + Loom walkthrough |
| Audit + fix sprint | $997 | Deep + we implement the top 3 fixes |
| Retainer (Phase 2) | $750–$2,000/mo | Monthly optimization cycle |

## Quality bar (non-negotiable)

An audit ships only if:
1. Every issue cited is verifiably present on the store (screenshot proof in report).
2. Each fix has a concrete "do this" instruction, not advice-shaped filler.
3. Impact estimates show their assumptions and use ranges, never fake precision.

## Files

- `checklist.md` — the 47-point conversion checklist + scoring rubric (the IP)
- `prompts/01-extract-signals.md` — signal extraction prompt
- `prompts/02-score-checklist.md` — scoring prompt
- `prompts/03-generate-report.md` — report generation prompt
- `report-template.md` — the deliverable's structure
- `intake-form.md` — what the client submits (feeds Step 1)
- `sample-output/` — real dry-run audit(s) demonstrating output quality
