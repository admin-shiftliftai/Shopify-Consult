# Prompt 02 — Score against the checklist

**Inputs to attach:** the JSON from Prompt 01, plus the full text of `checklist.md`.

---

You are a conversion-rate optimization expert scoring a Shopify store. Using ONLY the
extracted signals JSON (attached) and the 47-point checklist (attached), score every point.

Rules:
- Score each point **Pass / Weak / Fail / N/A**.
- If the signal for a point is `null` or listed in `not_observable`, mark it **N/A** with
  reason "not verifiable from materials" — NEVER infer a Fail from missing data.
- Every Fail/Weak must cite the exact signal field that justifies it.
- Compute area scores and the weighted overall score using the formulas in the checklist.

Return JSON:

```json
{
  "scores": [
    {"point": 1, "area": "hero", "verdict": "Pass|Weak|Fail|N/A",
     "evidence": "signal field + observed value", "reason": ""}
  ],
  "area_scores": {"hero": 0, "navigation": 0, "product_page": 0, "trust": 0,
                   "cart_checkout": 0, "mobile": 0, "offer": 0, "retention": 0},
  "overall_score": 0,
  "verdict_band": "",
  "top_leaks": [
    {"point": 0, "why_it_matters": "", "estimated_impact": "conservative range with stated assumptions"}
  ],
  "quick_wins": ["fixes doable in <1 hour each"],
  "human_review_needed": ["N/A points the human must verify manually before the report ships"]
}
```

`top_leaks`: the 5–10 highest-impact failures, ordered by (revenue impact × ease of fix).
Impact estimates must follow the checklist's impact estimation rules — ranges, stated
assumptions, conservative bound first.
