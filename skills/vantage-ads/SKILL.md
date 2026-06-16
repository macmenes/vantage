---
name: vantage-ads
description: >
  TRIGGER when the user wants competitor paid-media / ad-creative intelligence —
  "what ads are they running", "Meta Ad Library", "ad creative analysis",
  "competitor ads", "their offers", "paid media teardown", "ad spy". Part of the
  `vantage` suite. Reads public ad libraries to map creatives, offers, and spend
  posture.
  DO NOT trigger for running the user's OWN ads or pure keyword bid data (use
  seo-dataforseo).
context: fork
---

# Vantage-Ads — Paid-Media & Ad-Creative Intelligence

Public ad libraries are the **single highest-signal competitive source** — they
reveal a competitor's actual offers, hooks, audiences, and (via ad longevity) what's
working. This skill turns them into messaging and offer intelligence.

Web-only, all public. Sourcing in `../vantage/references/data-sources.md`; score with
`scoring-framework.md` §4.

## Sources (check all that apply)

| Channel | Source | What you get |
|---------|--------|--------------|
| Meta/Instagram | **Meta Ad Library** `facebook.com/ads/library` | Active creatives, full copy, "started running" date, variants, # active |
| Google/YouTube/Display | **Google Ads Transparency Center** `adstransparency.google.com` | Formats, creative, regions, date ranges |
| LinkedIn | Company Page → **Posts → Ads** tab | B2B ad creative & copy |
| TikTok | **TikTok Creative Center** Top Ads | Format/hook trends (region-limited) |

**Blind spots (always disclose):** Google *Search text ads* and several networks
aren't fully visible. "No ads found" = not visible here, **not** "not advertising."

## What to extract (per competitor)

1. **Spend posture** — roughly how many active ads, across how many platforms?
   (footprint, not exact spend). Heavy + multi-platform = serious paid motion.
2. **Creative volume & iteration** — many concepts and fresh dates = a real testing
   engine. A handful of stale ads = low investment.
3. **Winners (longevity proxy)** — ads running **many months** are almost certainly
   profitable. Catalog these — they're the competitor's proven messages.
4. **Hooks & angles** — categorize the opening lines (pain, outcome, social proof,
   comparison, fear/FOMO, curiosity, offer-led). Which angle dominates?
5. **Offers** — free trial, demo, discount, lead magnet, webinar, tool. The offer is
   the conversion mechanism — note strength and friction.
6. **Audience signals** — copy/imagery imply the targeted segment, role, region.
7. **Landing-page match** — click through: dedicated, message-matched LP vs dumping
   to homepage. Mismatch = a beatable weakness.

## Analysis frames

- **Angle distribution** — tally angles across the set. An over-served angle is
  crowded; an under-served, resonant angle is an opening for the subject brand.
- **Proven-message library** — the long-running ads across competitors are a
  pre-validated swipe file of what converts *this buyer*. Highest-value output.
- **Offer escalation** — is anyone out-offering the set (better trial, stronger
  magnet)? Match or beat, or differentiate on something other than offer.

## Output

```markdown
# Paid-Media Teardown — [set]
*Captured [date] · Sources: Meta Ad Library, Google ATC, [others]*

## Spend posture (footprint)
| Competitor | Meta active | Google formats | LinkedIn | Est. investment | Notes |
|-----------|------------:|---------------|---------|-----------------|-------|

## Proven messages (long-running ads = likely winners)
| Competitor | Hook | Angle | Offer | Running since | LP |
|-----------|------|-------|-------|---------------|----|

## Angle distribution across the set
[which angles are saturated vs open]

## Offer comparison
[trial/demo/discount/magnet strength per competitor]

## So what
- **Swipe-worthy proven angles** to test: …
- **Under-served angle / offer** the subject brand should own: …
- **Beatable weaknesses** (LP mismatch, stale creative): …
- **Blind spots:** [channels not publicly visible].
```
