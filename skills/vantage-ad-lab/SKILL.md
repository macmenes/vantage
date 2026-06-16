---
name: vantage-ad-lab
description: >
  TRIGGER when the user wants to CREATE their own paid ads / campaign concepts —
  "write ad copy", "ad concepts", "campaign ideas", "Meta ad variants", "Google
  RSA", "ad angles", "creative brief", "hooks for ads". Part of the `vantage`
  (Vantage.os) Paid-Media Lab pack. Turns competitive ad intelligence + positioning
  into ready-to-test ad concepts.
  DO NOT trigger for ANALYZING competitor ads (use vantage-ads) or organic content
  (use vantage-content-plan).
context: fork
---

# Vantage — Paid-Media Lab (your campaign concepts)

Turns what's working in the market (competitor ad intelligence) plus your positioning
into **ready-to-test ad concepts** — angles, hooks, full copy per channel, creative
briefs, and a test plan. Pairs with `vantage-ads` (which reads the ad libraries) and
`vantage-messaging` (which sets the positioning).

Deliverable: **`CAMPAIGN-CONCEPTS.html`** (shared design system —
`../vantage/references/html-report.md`).

## Intake (one question at a time — see console rules in `../vantage/SKILL.md`)

1. **"What are you advertising — product/offer and the page it points to?"**
2. **"Who's the target, and what's the one action you want?"** (objective: awareness /
   leads / trials / sales)
3. **"Which channels?"** (Meta/Instagram · Google Search · LinkedIn · YouTube · TikTok)
4. **"Want me to pull competitor ad intel first?"** → run `vantage-ads`; else use any
   insights the user has.
5. **"Anything to push or avoid?"** (offer, proof points, brand guardrails — optional)

## Method

### 1. Angle strategy
Map concepts across proven **angles** — and deliberately pick angles the competitor
set is *under-using* (from `vantage-ads`):

| Angle | Lead with |
|-------|-----------|
| Pain / problem | The cost of the status quo |
| Outcome / desire | The after-state, vividly |
| Social proof | Customers, numbers, logos |
| Comparison | Us vs the old way / a named alternative |
| Authority / data | Original stat, expertise |
| Curiosity / pattern-break | An unexpected hook |
| Urgency / FOMO | A real reason to act now |
| Offer-led | The deal itself |

### 2. Hook bank
10–15 scroll-stoppers (first line / first 3 seconds). Hooks do the heavy lifting —
specific, concrete, tension-led. No "Introducing…". Tie each to an angle.

### 3. Full ad variants (channel-correct specs)
Write complete, ready-to-paste ads:
- **Meta/Instagram** — Primary text (hook + body), Headline (≤40 char), Description,
  CTA button. 3–5 variants across angles.
- **Google Search (RSA)** — 12–15 Headlines (≤30 char), 4 Descriptions (≤90 char),
  organized so any combination reads well; reflect the keyword intent.
- **LinkedIn** — Intro text (B2B tone), Headline, CTA. 2–3 variants.
- **YouTube/TikTok (optional)** — a 15–30s script with hook-on-frame.

Match every ad to the landing page's promise (message match).

### 4. Creative briefs
For the top 3 concepts: visual idea, format (static/carousel/video/UGC), the
hook-on-frame text, and what the thumbnail must communicate in 1 second.

### 5. Landing-page outline
A message-matched LP skeleton for the lead offer: hero (mirrors the winning ad),
proof, how-it-works, objection handling, CTA.

### 6. Test plan
What to test first (angle > hook > creative > audience), a simple structure (e.g. 3
angles × 2 hooks), the metric that decides, and the kill/scale rule.

## Output — `CAMPAIGN-CONCEPTS.html`

Clone the design system. Sections:
1. **Strategy snapshot** — objective, target, channels, angle bets (with which are
   under-served by the competitive set)
2. **Angle matrix** — angles × which to prioritize and why
3. **Hook bank** — the 10–15 hooks, tagged by angle
4. **Ad variants** — channel-grouped cards (Meta / Google RSA / LinkedIn / video script)
5. **Creative briefs** — top 3 concept cards
6. **Landing-page outline**
7. **Test plan** — first test, structure, decision metric

Then `open` it. Offer: "Want the landing page built, or a competitive ad refresh
(`vantage-ads`) before launch?"

## Principles
- Concept from **what's proven in-market** (competitor long-running ads = validated
  messages) — then differentiate the angle, don't copy.
- Hooks win or lose the ad — over-invest there.
- Respect channel specs and **message match** ad → LP.
- Honest claims only; no fabricated stats or fake urgency. (See `../vantage/references/ethics-and-tos.md`.)
