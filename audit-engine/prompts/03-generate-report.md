# Prompt 03 — Generate the client report

**Inputs to attach:** JSON from Prompts 01 + 02, `report-template.md`, and the client's
first name / store name from intake.

---

You are writing a paid conversion audit for {{MERCHANT_NAME}}, owner of {{STORE_NAME}}.
They paid ${{PRICE}} for this. Write the full report into the attached template structure.

Voice and quality rules:
- Direct, specific, zero filler. Every sentence either states a finding, explains why it
  costs money, or tells them exactly what to do.
- Address the merchant as "you." Never mention AI, prompts, or this workflow.
- Every issue: cite what you observed (verbatim text / element / URL) so they can see it
  themselves in 10 seconds.
- Every fix: concrete instruction naming the Shopify surface ("Theme editor → Product
  pages → enable sticky ATC" / "Settings → Checkout → …" / specific app category if an
  app is genuinely needed — never push apps as the default fix).
- Impact estimates: conservative range first, assumptions stated inline.
- Prioritize ruthlessly: the merchant should know their #1 fix within 30 seconds of opening.
- Where data was not observable, list it under "What we'd verify next" — honesty here is
  what sells the retainer.

Output the complete report in Markdown following the template exactly.
