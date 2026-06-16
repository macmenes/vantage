---
name: vantage-positioning
description: >
  TRIGGER when the user wants a competitor messaging / positioning teardown —
  "how do they position", "messaging analysis", "positioning matrix", "what's
  their value prop", "how do we differentiate", "messaging map". Part of the
  `vantage` suite. Produces a messaging matrix, positioning map, and white-space
  read.
  DO NOT trigger for writing the user's OWN copy (use copywriting) or on-page SEO
  (use seo-page).
context: fork
---

# Vantage-Positioning — Messaging & Differentiation Teardown

How each competitor stakes its claim to the buyer's mind — and where the
uncontested ground is. This is the channel that most directly drives the
marketing/growth deliverable: it produces the **positioning map** and **messaging
matrix**, and feeds the battlecard's "their pitch / why we win."

Web-only. Score with `../vantage/references/scoring-framework.md` §1; template B in
`../vantage/references/deliverable-templates.md`.

## What to read (per competitor)

1. **Hero** (homepage H1 + subhead + primary CTA) — the one-liner promise.
2. **Category stance** — do they own/name a category, or hide behind
   "platform/solution/all-in-one"?
3. **Named ICP** — who do they explicitly say it's for? (`/customers`, headlines)
4. **Differentiator** — the concrete, ideally hard-to-copy claim. Distinguish a
   *real* edge from a me-too feature list.
5. **Proof adjacency** — is there specific proof (stat, outcome, name) next to the
   promise, or unsupported adjectives?
6. **Message consistency** — compare home vs ads (Meta Ad Library) vs social bios.
   Inconsistency is a weakness *and* an opening.
7. **Evolution** — Wayback the hero across 1–3 years. A recent pivot signals strategy
   shift (and often a vulnerability while messaging is unsettled).

## Frameworks to apply

- **One-liner test** (April Dunford-style): `[For ICP] who [need], [brand] is the
  [category] that [differentiated value], unlike [alternative].` Reconstruct each
  competitor's implied one-liner; gaps in it = weak spots.
- **Value-prop ladder:** feature → benefit → outcome → identity. Where does each
  competitor stop? Most stop at "benefit"; whoever reaches "outcome/identity" wins
  the high ground.
- **Cliché audit:** list phrases everyone in the set uses ("powerful," "all-in-one,"
  "AI-powered," "trusted by teams"). Shared clichés are dead positioning — the
  subject brand must avoid them.

## Positioning map

Choose **two axes that actually divide this market** (not generic). Examples:
self-serve ↔ enterprise, point-solution ↔ suite, price-led ↔ premium, horizontal ↔
vertical. Place every brand from evidence. **The empty quadrant is the headline** —
name it as white space (if it's empty because it's worthless, say that too).

## Output

```markdown
# Positioning Teardown — [set]
*Prepared [date]*

## Messaging matrix
[Template B: one-liner / category / ICP / differentiator / proof / CTA / tone per brand]

## Positioning map
[2×2 with chosen axes; brands placed; empty-quadrant call-out]

## Shared clichés (avoid)
- …

## Uncontested ground (white space)
- [A true, ownable claim no competitor is making.]

## Differentiation recommendation for [subject]
- **Claim to own:** …
- **Proof we'd need:** …
- **What to stop saying:** [our current clichés]

## So what (sales)
[Their pitch to our buyer + the one reframe that beats it — feeds the battlecard.]
```
