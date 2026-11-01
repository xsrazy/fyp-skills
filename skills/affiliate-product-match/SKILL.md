---
name: affiliate-product-match
description: Match a short video or video stock item to the exact affiliate product listing it should link to, on TikTok Shop or Shopee, at variant level. Use when the user has a product video and candidate listings, or needs a product chosen for a video before posting. Produces a ranked match table and explicit HOLD cases. If the exact variant cannot be confirmed, the answer is HOLD, never a guess.
---

# Affiliate Product Match

A wrong basket link is worse than no basket link. If the video shows a red mahogany car handbrake cover and the link opens a listing where the buyer lands on a different color, a different model, or a random variant, the click dies and the platform learns the video misleads. Matching is a verification job, not a shopping job: prove the listing sells the exact thing on screen, or stop.

## Inputs to collect first

- What the video shows (required): product type, brand if visible, color, size, model, material, and any feature the camera clearly shows. Build this fingerprint from the video, not from the product title the user hopes is true.
- Platform (required): TikTok Shop, Shopee, or both. Rules and trust signals differ.
- Candidate listings, if the user has them: links or titles, store names, listed variants, price, commission, sales, and rating, exactly as shown on the platform.
- If candidates are missing, say what data is needed per listing instead of inventing it. Never invent a commission rate, a sales number, or a rating.

## The variant gate (read first, it outranks everything)

A listing passes only if the buyer can select the exact variant shown in the video:

- Same product type and same function.
- Same color, size, and model as shown, selectable as a named variant on the listing, not hidden in a photo.
- Same brand, or clearly the same unbranded product. A lookalike from a different brand does not pass.
- The video's key visible feature (a clasp shape, a port, a pattern, a handle) exists on that variant.

If any of these cannot be confirmed from the listing, the result is **HOLD**: stop, name the exact missing proof, and tell the user what would clear it (a variant list screenshot, the store's variant names, or a clearer product shot). Never downgrade a HOLD into a "close enough" match.

## Workflow

1. Write the video's product fingerprint in one short block: type, brand, color, size, model, material, key features.
2. Apply the variant gate to every candidate. Failures leave the ranking entirely and go to the HOLD or REJECT sections with a reason.
3. Score the survivors with the criteria below. Prefer single brand, single product listings; treat multi brand bundles and listings that mix unrelated products as suspect even when a variant name matches.
4. Rank, recommend one primary match, and name what the caption, basket title, and thumbnail must call the variant so the whole post agrees.

## Scoring criteria (survivors of the gate only)

Score each out of the points shown; total 100.

- **Variant certainty (gate, not points)**: pass or HOLD. No points compensate for a fail.
- **Commission (20)**: higher commission rate and higher absolute commission per sale both count. A big percentage on a near zero price is weak.
- **Sales proof (20)**: units sold and recent sales pace. Proven sellers convert better than identical listings with no history.
- **Rating (20)**: product rating and review count together. A 5.0 rating from 3 reviews scores below a 4.8 from thousands.
- **Shop trust (20)**: store rating, official or Mall or Star status where the platform shows it, response rate, return handling, and how long the store has sold this category.
- **Price and stock fit (20)**: price close to what the video implies (no bait variants priced far below the real variant), and the exact variant in stock, not only the cheap decoy variant.

## Rules

- Prefer single brand listings. Avoid multi brand listings where the variant menu mixes brands, because the variant the buyer lands on is often not the one in the video.
- Avoid listings where the cheapest variant is a different, smaller, or unrelated item used as a price hook.
- Avoid listings with "random color" or "mixed model" variant names entirely for video matching. They can never pass the gate.
- If two listings tie, pick the one with the stronger shop trust, then the stronger sales proof. Say that this was the tiebreak.
- Never promise earnings. Commission shown is the platform's stated rate, not a guarantee.
- The match must agree everywhere: the variant named here is the variant named in the caption, the basket, and the thumbnail brief.
- If no candidate survives the gate, the recommendation is to post without a basket or not post yet, stated plainly. Do not fill the slot with a guess to keep the schedule moving.

## HOLD and REJECT cases

List every non surviving candidate with one of these verdicts and a one line reason:

- **HOLD**: variant cannot be confirmed yet, but a specific missing proof could clear it. Name the proof.
- **REJECT**: wrong product, wrong variant with no matching option, multi brand ambiguity that cannot be resolved, bait pricing, dead listing, or out of stock on the shown variant.

## Output format

1. **Video fingerprint**: the short block from step 1.
2. **Ranked match table** with columns: Rank | Product (as titled on the listing) | Store | Variant match (exact variant name) | Commission | Sold | Rating | Shop trust | Score | Verdict (MATCH for the survivors in the ranking).
3. **Recommendation**: the single primary match, its score, the tiebreak if any, and the exact variant wording to reuse in the caption and basket.
4. **HOLD and REJECT cases**: every excluded candidate, verdict, and reason, including what proof would clear each HOLD.
5. **Missing data**: anything the ranking needed but the user has not provided yet, listed plainly, with no invented numbers anywhere in the table. Unknown values are written as "unknown".
