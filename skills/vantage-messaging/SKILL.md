---
name: vantage-messaging
description: >
  TRIGGER when the user wants to build or sharpen THEIR OWN positioning &
  messaging — "our positioning", "messaging house", "value proposition", "our
  one-liner", "homepage copy", "how should we position", "messaging framework",
  "what's our narrative". Part of the `vantage` (Vantage.os) Positioning Studio
  pack. Produces a positioning statement, messaging house, hero copy, and narrative.
  DO NOT trigger for analyzing a COMPETITOR's positioning (use vantage-positioning)
  or writing long-form content (use vantage-content-plan / copywriting).
context: fork
---

# Vantage — Positioning Studio (your messaging house)

The "now what" after a competitive teardown: turn the white space you found into
**your own** positioning and a complete messaging house. This is a *creation* skill —
it builds the brand's strategic messaging, ideally informed by a prior Vantage
competitive run (the white space, the shared clichés to avoid, the rivals' claims).

Deliverable: **`MESSAGING-HOUSE.html`** (shared design system —
`../vantage/references/html-report.md`; Vantage-purple accent permitted on this
"build" deliverable). Working frameworks below.

## Intake (one question at a time — see the console rules in `../vantage/SKILL.md`)

Ask each as its own message, waiting between each. Skip anything already known from a
prior Vantage run or the user's input.
1. **"What's your brand or website?"**
2. **"In one breath, what do you sell and to whom?"**
3. **"Who's the ideal customer — and what do they use today instead of you?"**
   (the *competitive alternative*, incl. "do nothing / spreadsheets")
4. **"What can you do that the alternatives can't?"** (unique attributes)
5. **"What does that let the customer achieve?"** (the value/outcome)
6. **"Any non-negotiables?"** — words to own, words to avoid, tone (optional)

If a competitive teardown exists, pull white space + rivals' one-liners + shared
clichés from it instead of re-asking.

## Method

### 1. Positioning (Dunford "Obviously Awesome" sequence)
Work in this order — positioning is *derived*, not declared:
1. **Competitive alternatives** — what the customer would use without you.
2. **Unique attributes** — what only you have (features, model, data, focus).
3. **Value** — the outcome those attributes enable, that customers care about.
4. **Target segment** — who cares most about that value (be specific).
5. **Market category** — the frame that makes your value obvious. Owning or naming a
   category beats fighting in a generic one.
6. **(Optional) Trend** — the "why now" that makes the category urgent.

### 2. Positioning statement (internal)
`For [target segment] who [need/trigger], [brand] is the [category] that [unique
value]. Unlike [alternative], we [key differentiator] — [proof].`

### 3. Value proposition & one-liner (external)
- **One-liner** (5–9 words, outcome-led, plain language, no clichés).
- 2–3 alternative one-liners across different angles (outcome / category / contrarian).
- Run the **cliché filter**: kill "all-in-one," "powerful," "AI-powered,"
  "seamless," "platform," "next-gen," "supercharge" unless backed by specifics.

### 4. Messaging house
- **Roof** = the positioning one-liner.
- **3 pillars** = the value themes you compete on (not features — outcomes).
- Under each pillar: **2–4 proof points** (RTBs — features, stats, customers, demos)
  and the *message* (how to say it).
- **Foundation** = voice, tone, and the words you own vs avoid.

### 5. Hero copy (apply it)
Three homepage hero directions, each: eyebrow, H1, subhead, primary CTA, secondary
CTA — written to the one-liner, differentiated from the rivals' heroes in the teardown.

### 6. Narrative / POV
The short "manifesto" version: the shift in the world (why now) → the problem with the
old way → your view → the better way. 120–180 words. This is the founder-letter / sales
narrative spine.

## Output — `MESSAGING-HOUSE.html`

Clone the design system from `../vantage/references/report-example.html` (same CSS,
components, print-ready). Sections:
1. **Positioning statement** (the internal north star, in a dark scorecard-style card)
2. **The messaging house** — a visual: roof (one-liner) → 3 pillars → proof under each
3. **Value prop & one-liners** — recommended + alternatives, with the cliché-kill list
4. **Hero copy** — 3 variants as cards (eyebrow/H1/subhead/CTAs)
5. **Voice & tone** — own / avoid word lists, sample rewrites (before → after)
6. **Narrative / POV** — the manifesto block
7. **Differentiation vs the set** — how each pillar beats a named rival (if teardown exists)

Then `open` it. Offer: "Want hero copy shipped as a page (`seo-competitor-pages` /
copywriting), or ad concepts from this positioning (`vantage-ad-lab`)?"

## Principles
- Positioning is **earned from the market**, not invented — derive it from alternatives
  and real attributes, never aspirational fluff.
- Every claim needs a **proof point**, or it's a wish. Flag unproven claims.
- Differentiate from the **actual** competitive set (use the teardown), not a strawman.
- Plain language beats jargon every time.
