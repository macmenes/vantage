---
name: vantage-battlecard
description: >
  TRIGGER when the user wants a SALES battlecard or win/loss material for a
  competitor — "build a battlecard", "how do we beat X", "why we win vs X",
  "objection handling for X", "competitor kill sheet", "sales enablement for
  competitor". Part of the `vantage` suite. Produces a rep-ready battlecard.
  DO NOT trigger for marketing positioning analysis (use vantage-positioning) or
  comparison PAGES (use seo-competitor-pages).
context: fork
---

# Vantage-Battlecard — Sales Battlecards & Win/Loss

A rep-ready, evidence-backed card for beating a specific competitor in a live deal.
Honest by design: it **steelmans** the competitor, then equips the rep to win with
proof — never with trash-talk. Disparagement loses deals and creates liability (see
`../vantage/references/ethics-and-tos.md`).

Web-only sourcing; output = template D in `deliverable-templates.md`.

## Inputs

- The competitor (and the subject brand).
- Ideally the outputs of `vantage-positioning` (their pitch), `vantage-website`
  (pricing/offer), and review-site themes (their real strengths/weaknesses). If
  those aren't available, gather the minimum below first.

## Build method

1. **Steelman their pitch.** From their homepage/ads, write how they position *to
   our buyer* — accurately. Reps must recognize it in the wild.
2. **Mine reviews for truth.** On G2/Capterra/TrustRadius/Trustpilot, read recent
   **1–2★** (their real weaknesses) and **4–5★** (their real strengths). These are
   the gold — actual customers stating where they win and lose. Pull recurring
   themes, not one-offs.
3. **Why WE win** — turn *their* weakness themes + *our* genuine strengths into
   proof-backed advantages. Each line needs evidence (a stat, a customer, a review
   theme they can't match). Lead the card with these.
4. **Where THEY win** — name their real strengths honestly, each paired with a
   **response** (reframe, mitigant, or "fair — here's the trade-off"). Reps who
   concede a true point keep credibility for the points that matter.
5. **Landmines** — questions the rep can pose that surface the competitor's weakness
   *for the buyer to discover themselves* ("ask them how onboarding actually works /
   what migration costs / how X is priced at renewal"). Most powerful when drawn from
   the competitor's own negative review themes.
6. **Objection handling** — for each "they'll say X," a crisp evidence-backed
   response. Anticipate the competitor's likely attacks on the subject brand too.
7. **Pricing & packaging** — public pricing, renewal/gotcha patterns, where the
   subject brand is better value or more transparent.
8. **Proof points** — specific customers, stats, review-rating advantages, awards
   the rep can cite.

## Quality bar

- Every "why we win" line cites evidence. No unsupported superiority claims.
- "Where they win" is genuinely honest — a battlecard that pretends the competitor
  has no strengths gets reps ambushed and ignored.
- **Never** instruct reps to lie, mislead, or disparage. Reframe with facts.
- Date the card; competitive facts (pricing, features, reviews) move fast.

## Output

Use template D from `deliverable-templates.md`:
Quick take · Their pitch (steelman) · Why WE win · Where THEY win + responses ·
Landmines · Objection-handling table · Pricing & packaging · Proof points · Do/Don't.

End with: "Stand up `vantage-monitor` to keep this card current as their pricing,
reviews, and messaging change?"
