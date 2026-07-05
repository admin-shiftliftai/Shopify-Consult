# Prompt 01 — Extract store signals

**Inputs to attach:** homepage HTML/screenshot, top product page HTML/screenshot,
`/products.json` output (first 250 products), any analytics screenshots from intake.

---

You are a meticulous e-commerce analyst. From the attached materials for the Shopify store
{{STORE_URL}}, extract ONLY directly observable facts. Do not evaluate, score, or recommend yet.

Return JSON exactly in this shape:

```json
{
  "store": {
    "url": "", "niche": "", "estimated_sku_count": 0,
    "price_range": {"min": 0, "max": 0, "currency": ""},
    "apparent_positioning": ""
  },
  "hero": {
    "headline_text": "", "subheadline_text": "", "cta_count_above_fold": 0,
    "primary_cta_text": "", "hero_media_type": "image|video|carousel|none",
    "shows_product_in_use": null, "announcement_bar_text": "", "popup_observed": null
  },
  "navigation": {
    "top_level_items": [], "search_visible": null, "bestseller_collection_linked": null,
    "footer_trust_pages": []
  },
  "product_page": {
    "example_url": "", "title": "", "title_states_benefit": null,
    "image_count": 0, "first_image_type": "", "price_visible_above_fold": null,
    "compare_at_shown": null, "atc_above_fold_mobile": null,
    "shipping_info_near_atc": null, "review_count_visible": null, "review_average": null,
    "variant_ux_notes": "", "cross_sell_present": null, "return_policy_link_near_buybox": null,
    "urgency_elements": ""
  },
  "trust": {
    "about_page_has_story": null, "contact_method": "", "policies_customized": null,
    "powered_by_shopify_visible": null
  },
  "cart_checkout": {
    "cart_type": "slideout|page|unknown", "free_shipping_bar": null,
    "express_pay_options": [], "guest_checkout": null, "discount_field_prominent": null,
    "cart_upsell_present": null
  },
  "offer": {
    "bundles_or_volume_discounts": null, "free_shipping_threshold": "",
    "guarantee_stated": null, "email_capture_incentive": ""
  },
  "catalog_observations": {
    "top_products_by_position": [], "pricing_pattern_notes": "",
    "products_missing_images": 0, "products_with_thin_descriptions": 0
  },
  "analytics_provided": {
    "monthly_sessions": null, "conversion_rate": null, "aov": null, "notes": ""
  },
  "not_observable": ["list every checklist area you could NOT verify from the materials"]
}
```

Rules:
- `null` means "could not observe" — never guess.
- Quote text fields verbatim from the store.
- `not_observable` must be complete; downstream scoring marks those N/A, and the
  human reviewer checks them manually.
