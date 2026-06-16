---
name: vantage-content
description: >
  TRIGGER when the user wants a marketing-level read of a competitor's content
  engine & organic footprint — "their content strategy", "what do they blog
  about", "content cadence", "share of search", "content gaps vs competitors",
  "their resources". Part of the `vantage` suite.
  DO NOT trigger for deep keyword/backlink DATA (use seo-dataforseo,
  backlink-analyzer) or full SEO audits (use seo) — this skill HANDS OFF to those.
context: fork
---

# Vantage-Content — Content Engine & Organic Footprint

A marketing read on the content machine: how often they publish, what they own, how
visible they are in buyer search, and where the gaps are. This is **not** an SEO
audit — for keyword/backlink depth it hands off to `seo-dataforseo`,
`backlink-analyzer`, and `seo`.

Web-only. Score with `scoring-framework.md` §2.

## Read the engine (per competitor)

1. **Cadence** — pull `/sitemap.xml` (or `/sitemap_index.xml`) and read `lastmod`;
   cross-check visible post dates and Wayback snapshots of `/blog`. Estimate
   posts/month and recency (last post age). Consistency > bursts.
2. **Topical structure** — blog/resource taxonomy. Do they run **pillar/cluster**
   hubs that own a theme, or scattered one-offs? Name the themes they're claiming.
3. **Format range** — guides, original research/data, templates, free tools,
   calculators, webinars, podcasts, video, courses. Range and *depth* signal
   investment; original data and tools are the hardest to copy (and most linkable).
4. **Distinct POV** — is there a thesis/voice, or interchangeable SEO filler? A
   strong POV is defensible; filler is beatable with better filler.
5. **Conversion intent** — do articles tie to offers (CTAs, magnets), or are they
   orphaned traffic? Content without conversion is a beatable inefficiency.
6. **Share of search** — run **5–10 buyer queries** for the category; count where
   each competitor appears on page 1. This is the marketing proxy for organic
   strength without keyword tools.

## Content-gap method (web-only)

1. List the themes/buyer questions the *subject brand's* ICP cares about.
2. For each, search and note which competitor(s) own the result.
3. Three gap types:
   - **Uncontested** — a buyer-relevant theme **no one** covers well → highest
     leverage for the subject brand.
   - **Under-served** — covered shallowly → outdo with depth/data/format.
   - **Saturated** — everyone covers it well → don't fight here unless you have a
     genuine edge (original data, better format).
4. For volume/difficulty quantification, **hand off** to `seo-dataforseo` /
   `seo-geo-claude-skills:content-gap-analysis`.

## Output

```markdown
# Content Engine Teardown — [set]
*Captured [date]*

## Engine comparison
| Competitor | Posts/mo (est) | Last post | Pillar themes owned | Standout formats | POV |
|-----------|---------------:|-----------|---------------------|------------------|-----|

## Share of search (buyer queries)
| Query | Page-1 owners |
|-------|---------------|
*Method: [N] buyer queries run [date]; appearances counted.*

## Content gaps
- **Uncontested (own it):** …
- **Under-served (outdo):** …
- **Saturated (avoid / need an edge):** …

## So what (growth)
- **Topics to own** + format to win them: …
- **Hand-offs:** quantify with `seo-dataforseo`; link depth via `backlink-analyzer`.
```
