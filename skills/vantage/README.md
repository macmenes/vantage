# Vantage — Digital-Marketing Competitive Landscape Suite

A self-contained competitive-intelligence skill suite for **marketing/growth and
sales** teams. Maps the full digital-marketing surface of a competitive set and
rolls it into a **Digital Share-of-Voice (DSoV) index**, a **positioning map**, a
**competitive matrix**, and **sales battlecards** — using **WebSearch + WebFetch
only**. No API keys required.

**The deliverable is a single, self-contained, beautiful HTML report** —
`COMPETITIVE-LANDSCAPE.html`, with the subject brand's real logo embedded, a dark
DSoV scorecard, a heatmap matrix, a plotted 2×2 positioning map, win/lose
battlecards, and a collapsible evidence log. Print-ready (exports cleanly to PDF).
See `references/html-report.md` and the worked sample report in `references/report-example.html`.

## Why this exists

Most "competitive analysis" tools either dump data (rank trackers, ad-spy tools) or
stay generic. This suite is opinionated about turning **public evidence** into
**decisions**: every section ends in a move, every claim cites a dated source, and
the same evidence always yields the same score. It is deliberately **complementary**
to the `seo-*` skills — it's marketing intelligence, not an SEO audit, and it hands
off to those skills for keyword/backlink/technical depth.

## Install / location

Skills live in `~/.claude/skills/`. This suite is:

```
vantage/                 ← umbrella orchestrator (+ shared references/)
vantage-discover/        ← build & tier the competitor set
vantage-positioning/     ← messaging & differentiation
vantage-website/         ← website & conversion path
vantage-content/         ← content engine & organic footprint
vantage-ads/             ← paid-media & ad-creative intelligence
vantage-social/          ← social presence & share-of-voice
vantage-battlecard/      ← sales battlecards & win/loss
vantage-monitor/         ← recurring competitive watch
```

## Usage

| Command | Output |
|---------|--------|
| `/vantage <your-domain>` | Full landscape: discover → all channels → DSoV matrix, positioning map, battlecards |
| `/vantage <your-domain> vs <comp1>,<comp2>` | Same with a supplied set |
| `/vantage discover <domain>` | Tiered competitor set |
| `/vantage positioning <domains>` | Messaging matrix + positioning map |
| `/vantage website <domains>` | Funnel & offer teardown |
| `/vantage content <domains>` | Content engine & share-of-search |
| `/vantage ads <domains>` | Ad-library creative & offer intelligence |
| `/vantage social <domains>` | Social & share-of-voice |
| `/vantage battlecard <competitor>` | Rep-ready sales battlecard |
| `/vantage monitor <domains>` | Stand up recurring watch (pairs with `/schedule`) |

The umbrella auto-orchestrates the sub-skills; you can also invoke any sub-skill
directly.

## The DSoV index

`DSoV = 0.20·Positioning + 0.20·Content + 0.15·Website + 0.15·Paid + 0.15·Social + 0.15·Reputation`

Each competitor **and the subject brand** are scored 0–100 per channel, so every
number reads as a gap. Rubrics: `references/scoring-framework.md`.

## Reference library (`vantage/references/`)

- `scoring-framework.md` — DSoV rubrics, per-channel signals, banding, honesty rules
- `data-sources.md` — Web-only intelligence map: where every signal lives + query patterns
- `deliverable-templates.md` — Report, matrix, positioning map, battlecard, monitoring templates
- `ethics-and-tos.md` — Public-source-only CI: what's allowed, what's not, citation discipline

## Operating principles

1. **Evidence over assertion** — every claim cites a dated, public source; estimates are labeled.
2. **Public sources only** — ad libraries, transparency centers, reviews, Wayback, public pages. No impersonation, no breaching auth, no scraping gated data.
3. **Decisions, not data dumps** — every section ends in a "so what" tuned to the audience (growth → positioning/channel moves; sales → battlecard ammo).
4. **Freshness** — competitive facts decay; stamp captures with dates and re-verify.

## Relationship to `seo-*` skills

| Need | Use |
|------|-----|
| Deep on-page / technical / schema SEO | `seo`, `seo-technical`, `seo-page` |
| Build an actual "X vs Y" comparison page | `seo-competitor-pages` |
| Live keyword ranking data | `seo-dataforseo`, `seo-geo-claude-skills:competitor-analysis` |
| Backlink profile deep-dive | `backlink-analyzer` |
| AI-search / GEO visibility | `seo-geo` |
