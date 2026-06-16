---
name: vantage
description: >
  TRIGGER when the user runs `/vantage`, or asks for competitive landscape /
  competitive intelligence work, or says "competitive analysis", "competitor
  teardown", "competitive landscape", "size up our competitors", "how do we stack
  up", "share of voice", "competitive matrix", "build a battlecard". This is the
  Vantage launcher — it shows the menu of marketing-intelligence skills, runs a
  short guided intake, then dispatches to the right specialist.
  DO NOT trigger for: pure technical/on-page SEO audits (use seo / seo-* skills),
  single "X vs Y" comparison PAGE creation (use seo-competitor-pages), backlink
  profiles only (use backlink-analyzer), or live keyword data lookups.
context: fork
---

# Vantage — Marketing-Intelligence Skills Launcher

`/vantage` is the front door to a growing pack of marketing skills. Today it ships
the **Competitive Analysis** pack: full-funnel digital-marketing teardowns for
marketing/growth and sales, scored into a **Digital Share-of-Voice (DSoV) index**,
a **positioning map**, a **competitive matrix**, and **sales battlecards** —
delivered as a single beautiful self-contained **HTML report**. Web-only, no API keys.

## When invoked — the launcher flow

Follow these steps in order. Keep it snappy and friendly; this is a branded experience.

### Step 1 — Show the splash

Print this banner **verbatim**, inside a plain fenced code block so it renders in
monospace (do not alter the spacing):

```
        ▲              ▲          ▲
       ╱ ╲      ▲     ╱ ╲        ╱ ╲
      ╱   ╲    ╱ ╲   ╱   ╲      ╱   ╲
   ▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔▔

   █   █  ███  █   █ █████  ███   ████ █████
   █   █ █   █ ██  █   █   █   █ █     █
   █   █ █████ █ █ █   █   █████ █  ██ ████
    █ █  █   █ █  ██   █   █   █ █   █ █
     █   █   █ █   █   █   █   █  ████ █████

   S E E   T H E   W H O L E   F I E L D
```

Then one line: **"Vantage — marketing intelligence for Claude Code."**

### Step 2 — Route or show the menu

- If the user already gave clear intent (a domain, or a sub-command like
  `battlecard <competitor>`, `ads <domain>`, `positioning <domains>`), **skip the
  menu** and go straight to Step 3 for that skill.
- Otherwise present the menu below (use `AskUserQuestion`, header "Skill"). List the
  **available** Competitive Analysis skills as selectable options, and mention the
  **coming-soon** packs in one line so the roadmap is visible.

**Competitive Analysis pack (available now):**

| # | Skill | What it does |
|---|-------|--------------|
| 1 | **Full landscape** | Discover the set → analyze every channel → DSoV matrix, positioning map, battlecards (the headline deliverable) |
| 2 | Discover competitors | Identify & tier the real competitor set |
| 3 | Positioning & messaging | Messaging matrix + positioning 2×2 + white space |
| 4 | Website & conversion | Funnel, offers, pricing, proof, lead capture |
| 5 | Content engine | Cadence, topics, share-of-search, content gaps |
| 6 | Paid media | Ad-library creative & offer intelligence |
| 7 | Social & share-of-voice | Platforms, scale, engagement, themes |
| 8 | Sales battlecard | Rep-ready battlecard for one competitor |
| 9 | Monitor | Stand up a recurring competitive watch |

**Coming soon (roadmap — mention, don't offer):** Positioning Studio · Content
Engine · Paid-Media Lab · Lifecycle & Email · Brand & PR. Vantage is built as a hub;
more marketing packs slot in here over time.

### Step 3 — Guided intake (pre-questions)

Before running, gather just enough to do it well. Ask only what's missing. Prefer
`AskUserQuestion` for the structured choices; ask for the domain in plain text.

For a **Full landscape** (the common path):
1. **Your brand / domain** — plain text if not already given.
2. **Competitor set** — "Auto-discover them, or do you have a list?" (if a list,
   collect it).
3. **Audience emphasis** — Growth/marketing · Sales · Both. (Shapes whether the
   "so what" leans positioning/channel moves vs battlecard ammo.)
4. **Depth** — Quick (top 3, headlines) · Standard (5–7, full) · Deep (7+, exhaustive).
5. **Any specific angle?** — optional (a segment, a launch, a rival to focus on).

For a single-skill pick, ask only that skill's essentials (e.g. battlecard → which
competitor + your brand; ads → which domains).

### Step 4 — Dispatch & deliver

- Load the matching specialist skill and run it with the gathered inputs:
  Full landscape → orchestrate all (see "Orchestration" below); else →
  `vantage-discover` · `vantage-positioning` · `vantage-website` · `vantage-content`
  · `vantage-ads` · `vantage-social` · `vantage-battlecard` · `vantage-monitor`.
- Produce the **HTML report** (see `references/html-report.md`), `open` it, and offer
  to stand up `vantage-monitor`.

## Orchestration (Full landscape)

1. **Frame**: confirm subject brand, category, audience.
2. **Discover & tier** the set (`vantage-discover`) if not supplied; cap the deep-dive
   at top 5–7 by relevance (Quick=3, Deep=7+).
3. **Fan out** across channels in parallel (one subagent per competitor-channel where
   practical): `vantage-positioning`, `vantage-website`, `vantage-content`,
   `vantage-ads`, `vantage-social`.
4. **Score** each competitor + the subject brand per channel (0–100) using
   `references/scoring-framework.md`; roll up to the **DSoV index**.
5. **Synthesize**: positioning map, competitive matrix, white-space & threats, then
   battlecards (`vantage-battlecard`) for the 2–3 most contested competitors.
6. **Deliver** a single self-contained beautiful **`COMPETITIVE-LANDSCAPE.html`** —
   clone the design system and structure from `references/html-report.md` and the
   bundled sample at `references/report-example.html`. Embed the subject brand's real
   logo. Then `open` it and offer `vantage-monitor`.

## The DSoV Index (signature scoring)

| Channel | Weight | Skill |
|---------|--------|-------|
| Positioning & Differentiation | 20% | vantage-positioning |
| Organic / Content Engine | 20% | vantage-content |
| Website & Conversion | 15% | vantage-website |
| Paid Media | 15% | vantage-ads |
| Social & Community | 15% | vantage-social |
| Reputation & Proof | 15% | vantage-positioning + vantage-website (reviews, proof) |

Rubrics and how to score from web-only evidence: **`references/scoring-framework.md`**.

## Reference Files (load on demand — do NOT load all at startup)

- `references/html-report.md` — **Primary deliverable**: the beautiful self-contained HTML report (design system, components, logo embedding). Clone the bundled `report-example.html`.
- `references/scoring-framework.md` — DSoV rubrics, per-channel signals, banding
- `references/data-sources.md` — Where every signal lives, web-only (free tools, URLs, query patterns)
- `references/deliverable-templates.md` — Markdown working/data templates that feed the HTML
- `references/ethics-and-tos.md` — Public-source-only CI: ToS, no impersonation/scraping gated data, citation discipline

## Operating Principles

- **Evidence over assertion.** Every claim cites a dated, public source (URL + capture date). No fabricated metrics; label estimates and show the basis. Read `references/ethics-and-tos.md`.
- **Public sources only.** Ad libraries, transparency centers, review sites, the Wayback Machine, public pages. No login, no scraping gated data, no impersonation.
- **Decisions, not data dumps.** Each section ends with a "so what" — a move the subject brand should make.
- **Freshness matters.** Stamp every finding with a date; prefer current captures.

## Relationship to other skills

| Need | Use |
|------|-----|
| Deep on-page / technical / schema SEO | `seo`, `seo-technical`, `seo-page` |
| Build an actual "X vs Y" comparison page | `seo-competitor-pages` |
| Keyword-level competitor ranking data (live) | `seo-dataforseo` |
| Backlink profile deep-dive | `backlink-analyzer` |
| AI-search / GEO visibility | `seo-geo` |

## Sub-Skills

1. **vantage-discover** — Build & tier the real competitor set
2. **vantage-positioning** — Messaging, ICP, category, differentiation matrix
3. **vantage-website** — Website & conversion-path teardown
4. **vantage-content** — Content engine & organic footprint (marketing read)
5. **vantage-ads** — Paid-media & ad-creative intelligence
6. **vantage-social** — Social presence & share-of-voice
7. **vantage-battlecard** — Sales battlecards & win/loss
8. **vantage-monitor** — Recurring competitive monitoring
