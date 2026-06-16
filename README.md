<div align="center">

<!-- BRANDING TODO: replace this block with assets/logo.png once re-dropped -->
```
██     ██    ███    ██    ██ ████████    ███     ██████   ████████      ███████   ██████
██     ██   ██ ██   ███   ██    ██      ██ ██   ██    ██  ██           ██     ██ ██    ██
██     ██  ██   ██  ████  ██    ██     ██   ██  ██        ██           ██     ██ ██
██     ██ ██     ██ ██ ██ ██    ██    ██     ██ ██   ████ ██████       ██     ██  ██████
 ██   ██  █████████ ██  ████    ██    █████████ ██    ██  ██           ██     ██       ██
  ██ ██   ██     ██ ██   ███    ██    ██     ██ ██    ██  ██       ███ ██     ██ ██    ██
   ███    ██     ██ ██    ██    ██    ██     ██  ██████   ████████ ███  ███████   ██████

                     marketing brain inside your agent
```

# Vantage.os — Marketing Intelligence OS

### The marketing brain inside your agent. Run `/vantage`, answer a few questions, and get a beautiful, evidence-backed competitive teardown.

Vantage maps the full digital-marketing surface of your rivals — positioning, content, website,
paid, social, reputation — scores it into one **Digital Share-of-Voice** index, plots a
**positioning map**, builds a **competitive matrix**, and writes rep-ready **sales battlecards**.
The deliverable is a single, gorgeous, self-contained **HTML report**.

**Lives inside your coding agent · Web search + fetch only · No API keys · Free & open source.**

[Install](#install) · [The experience](#the-experience) · [What you get](#what-you-get) · [Commands](#commands) · [How it works](#how-it-works) · [Sample report](examples/sample-competitive-landscape.html)

<!-- BRANDING TODO: drop a hero logo + screenshot of a generated report here -->

</div>

---

## The experience

`/vantage` isn't a one-shot command — it's a console that interviews you, **one question at a time**:

```
$ /vantage

   V A N T A G E . O S  ·  Marketing Intelligence OS
   marketing brain inside your agent

   ▸ What are you looking to do today?
     · Full competitive landscape   · Find my competitors
     · Positioning & messaging      · Website / ads / content / social
     · Sales battlecard             · Monitor competitors

   you ▸ full landscape

   ▸ What's your brand or website?
   you ▸ acme.com

   ▸ Who are your main competitors — or want me to find them?
   you ▸ find them for me

   ▸ Who's this for — marketing, sales, or both?
   you ▸ both

   ▸ How deep should I go — quick, standard, or deep dive?
   you ▸ standard

   → Running… → COMPETITIVE-LANDSCAPE.html opens in your browser.
```

Already know what you want? Skip the interview — `/vantage acme.com` or
`/vantage battlecard <competitor>` jumps straight in.

## Runs inside any coding agent

Vantage is a **marketing-intelligence OS that lives inside your coding agent**, not a
single-vendor tool. It ships for **Claude Code** today and is built to port to other agentic
coding environments (Codex and beyond) — same console, same reports, wherever you work.

## Why Vantage

Most "competitive analysis" tools either dump data (rank trackers, ad-spy dashboards) or stay
generic. **Vantage turns public evidence into decisions.** Every section ends in a move, every
number cites a dated source, and the same evidence always yields the same score — output you can
hand straight to a founder, a growth lead, or a sales rep.

- 🎯 **Built for marketing & sales**, not SEO audits. Positioning, messaging, offers, share-of-voice, and battlecards — the things that move pipeline.
- 🧮 **A real scoring model.** The Digital Share-of-Voice (DSoV) index scores every competitor *and you* 0–100 across six channels, so every cell reads as a gap.
- 🌐 **Web-only, no keys.** Runs entirely on `WebSearch` + `WebFetch`. Uses public ad libraries, review sites, and the Wayback Machine.
- 📄 **A deliverable you'll want to send.** One self-contained HTML file — your competitor's real logo, a heatmap matrix, a plotted 2×2 map, win/lose battlecards, a sourced evidence log. Print-to-PDF ready.
- 🤝 **Plays well with others.** Hands off cleanly to SEO/backlink skills for keyword-level depth instead of reinventing them.

## What you get

| Deliverable | Description |
|-------------|-------------|
| **Digital Share-of-Voice index** | Weighted 0–100 score per competitor across Positioning, Content, Website, Paid, Social, Reputation |
| **Competitive matrix** | Color-banded heatmap of every brand × channel, with you highlighted |
| **Positioning map** | A 2×2 plotted from evidence — see exactly where the white space is |
| **Channel teardowns** | Messaging matrix, conversion/offer comparison, content engine, ad-creative intelligence, social share-of-voice, review-sentiment themes |
| **Sales battlecards** | Per-competitor: steelman, why-we-win, where-they-win, landmines, objection handling, do/don't |
| **Action plan** | Prioritized (Critical → High → Medium) moves tied to the gaps |
| **Evidence log** | Every claim linked to a public source with a capture date |

👉 **[See a full sample report (fictional data) → Northpeak vs. its market](examples/sample-competitive-landscape.html)** *(open in a browser)*

## Install

**Claude Code (reference implementation):**

```
/plugin marketplace add macmenes/vantage
/plugin install vantage@vantage
```

**Manually (drop-in skills):**

```bash
git clone https://github.com/macmenes/vantage.git
cp -R vantage/skills/* ~/.claude/skills/
```

Then just type `/vantage`.

## Commands

| Command | What it does |
|---------|-------------|
| `/vantage` | Open the console — it interviews you, then runs |
| `/vantage <your-domain>` | Jump straight to a full landscape teardown |
| `/vantage <your-domain> vs <a>,<b>` | Full landscape with the competitor set supplied |
| `/vantage discover <domain>` | Identify & tier the real competitor set |
| `/vantage positioning <domains>` | Messaging & positioning teardown + matrix |
| `/vantage website <domains>` | Website & conversion-path teardown |
| `/vantage content <domains>` | Content engine & share-of-search |
| `/vantage ads <domains>` | Paid-media & ad-creative intelligence (Meta Ad Library, Google ATC) |
| `/vantage social <domains>` | Social presence & share-of-voice |
| `/vantage battlecard <competitor>` | Rep-ready sales battlecard |
| `/vantage monitor <domains>` | Stand up recurring competitive monitoring |

## How it works

The `vantage` console fans out to 8 specialists, scores each on web-only evidence, and
synthesizes the result.

```
                         /vantage <your-domain>
                                  │
                   ┌──────────────┴───────────────┐
                   ▼                               ▼
            vantage-discover                  (your brand,
         build & tier the set              scored on the same rubric)
                   │
   ┌───────┬───────┼────────┬────────┬─────────┐
   ▼       ▼       ▼        ▼        ▼         ▼
positioning content website  ads    social  reputation
   └───────┴───────┴────────┴────────┴─────────┘
                   │  score each 0–100 → DSoV
                   ▼
        positioning map · matrix · white space
                   ▼
           vantage-battlecard  →  beautiful HTML report
                   ▼
            vantage-monitor (optional recurring watch)
```

### The DSoV index

```
DSoV = 0.20·Positioning + 0.20·Content + 0.15·Website
     + 0.15·Paid + 0.15·Social + 0.15·Reputation
```

Bands: **Dominant** 85+ · **Strong** 70–84 · **Credible** 50–69 · **Thin** 30–49 · **Absent** <30.
No channel is scored without ≥3 cited signals. Full rubrics live in
[`skills/vantage/references/scoring-framework.md`](skills/vantage/references/scoring-framework.md).

## The skills

| Skill | Role |
|-------|------|
| `vantage` | The console — splash, interview, dispatch + shared reference frameworks |
| `vantage-discover` | Build & tier the real competitor set (incl. the "do-nothing" indirect tier) |
| `vantage-positioning` | Messaging matrix, positioning 2×2, differentiation white space |
| `vantage-website` | Funnel, CTAs, pricing presentation, proof, lead capture |
| `vantage-content` | Content engine, share-of-search, content gaps |
| `vantage-ads` | Ad-library creative & offer intelligence |
| `vantage-social` | Social & share-of-voice (engagement > follower vanity) |
| `vantage-battlecard` | Honest, evidence-backed sales battlecards |
| `vantage-monitor` | Diff-since-last-check competitive watch |

## Responsible by design

Vantage uses **public sources only** — ad transparency libraries, review sites, the Wayback
Machine, and public pages. No impersonation, no breaching auth or paywalls, no scraping gated data,
no disparagement in battlecards (it steelmans rivals, then counters with evidence). Every
quantitative claim is cited with a capture date. See
[`skills/vantage/references/ethics-and-tos.md`](skills/vantage/references/ethics-and-tos.md).

## Roadmap

Vantage is built as an **OS / hub**: `/vantage` is the front door to a growing pack of marketing skills.

- [x] **Competitive Analysis** pack (this release)
- [ ] Hero logo + screenshot + short demo GIF
- [ ] Ports for other coding agents (Codex and beyond)
- [ ] **Positioning Studio** — messaging & narrative development
- [ ] **Content Engine** — content strategy, briefs, calendars
- [ ] **Paid-Media Lab** — ad concepting from competitive intelligence
- [ ] **Lifecycle & Email** · **Brand & PR**
- [ ] Optional connectors (DataForSEO / SerpAPI / SimilarWeb) as opt-in power-ups

## Contributing

Issues and PRs welcome. The design system for the HTML report is documented in
[`skills/vantage/references/html-report.md`](skills/vantage/references/html-report.md).

## License

MIT © macmenes. Free to use, modify, and share.
