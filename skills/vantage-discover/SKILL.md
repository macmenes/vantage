---
name: vantage-discover
description: >
  TRIGGER when the user needs to identify and tier the real competitor set for a
  brand/domain — "who are our competitors", "find our competitors", "build a
  competitor list", "competitive set", "who else is in this market". Part of the
  `vantage` suite. Produces a tiered, evidence-backed competitor set.
  DO NOT trigger for analyzing competitors already named (use the relevant
  vantage-* channel skill) or keyword-ranking rivals only (use seo-dataforseo).
context: fork
---

# Vantage-Discover — Build the Real Competitor Set

The most common failure in competitive analysis is analyzing the **wrong set** —
the competitors leadership *names* instead of the ones the *buyer actually
considers*. This skill builds the set from market evidence, tiers it, and caps the
deep-dive to a workable size.

Web-only. See `../vantage/references/data-sources.md` for sourcing patterns.

## Method

1. **Anchor on the subject brand.** WebFetch its homepage; extract category, ICP,
   and the buyer problem it solves. The set is "who else solves this for this buyer."
2. **Cast the net across five lenses** (each surfaces a different rival type):
   - **SERP rivals** — run 5–10 buyer queries for the category; collect domains that
     repeat on page 1. These are who the buyer sees.
   - **"Alternatives / vs" mining** — `"<brand>" alternatives`, `"<brand>" vs`,
     `best <category> 2026`. Read the listicles and G2 "compare" tabs.
   - **Review-site neighbors** — on G2/Capterra, the "competitors" and "compare"
     modules name the considered set directly.
   - **Ad rivals** — who bids on the brand term (Google Ads Transparency) and who
     runs ads on the same angles (Meta Ad Library keyword search).
   - **Emerging/funded** — `<category> startup funding 2025 2026`; catch entrants
     before they're obvious.
3. **De-dupe and classify** each candidate into a tier (below).
4. **Tier and cap.** Keep the **top 5–7** for deep-dive by relevance to the
   subject's actual buyer; list the long tail so nothing's lost.

## Tiering model

| Tier | Definition | Treatment |
|------|-----------|-----------|
| **Direct** | Same buyer, same problem, substitutable | Full deep-dive |
| **Adjacent** | Overlapping buyer or partial-solution overlap | Deep-dive if it appears in deals/SERPs often |
| **Aspirational** | The category leader / who everyone benchmarks | Analyze for positioning even if "out of league" |
| **Emerging** | New/funded entrant changing the rules | Watch; analyze if momentum is real |
| **Indirect** | The status quo / DIY / "do nothing" / spreadsheets | Name it — often the real competitor for budget |

Don't forget the **indirect** tier. For many growth/sales motions the biggest
competitor is "the buyer keeps doing it manually," and the messaging must beat that.

## Relevance scoring (to pick the deep-dive set)

Score each candidate 0–3 on: buyer overlap, problem overlap, how often it co-appears
(SERP/reviews/deals), and momentum. Sum → rank → take the top 5–7. Show the scores
so the cut is defensible.

## Output

```markdown
# Competitor Set — [Subject Brand]
*Category: [category] · Buyer: [ICP] · Prepared [date]*

## Deep-dive set (top N by relevance)
| Competitor | Tier | Buyer overlap | Why in set | Relevance |
|-----------|------|---------------|-----------|-----------|

## Long tail (named, not deep-dived)
[list with one-line each]

## Notable absences / blind spots
[markets/segments we couldn't see; sources that blocked fetching]

## Recommended deep-dive set → hand to /vantage
[the 5–7 to run channel teardowns on]
```

Then offer: "Run the full `/vantage` teardown on this set?"
