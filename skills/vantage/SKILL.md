---
name: vantage
description: >
  TRIGGER when the user runs `/vantage`, or asks for competitive landscape /
  competitive intelligence / marketing-intelligence work, or says "competitive
  analysis", "competitor teardown", "competitive landscape", "size up our
  competitors", "how do we stack up", "share of voice", "competitive matrix",
  "build a battlecard". This is Vantage — a Marketing Intelligence OS. It opens a
  guided console, asks what the user wants one question at a time, then runs it.
  DO NOT trigger for: pure technical/on-page SEO audits (use seo / seo-* skills),
  single "X vs Y" comparison PAGE creation (use seo-competitor-pages), backlink
  profiles only (use backlink-analyzer), or live keyword data lookups.
context: fork
---

# Vantage.os — Marketing Intelligence OS

**Vantage.os** is a marketing-intelligence operating system that lives **inside your
agent** — the marketing brain inside your coding agent. `/vantage` opens a guided
console: it greets the user, asks what they want to do, and walks them there **one
question at a time**.

It runs in **Claude Code today** and is built to port to any agentic coding
environment (Codex and others) — the experience is the same everywhere. Today it
ships the **Competitive Analysis** pack: full-funnel digital-marketing teardowns
scored into a **Digital Share-of-Voice (DSoV) index**, a **positioning map**, a
**competitive matrix**, and **sales battlecards**, delivered as a single beautiful
self-contained **HTML report**. Web-only, no API keys. Vantage is a **hub** — more
marketing packs slot in over time.

---

## When invoked — the console flow

### Step 1 — Splash

Print this banner **verbatim**, inside a plain fenced code block (monospace):

```
██     ██    ███    ██    ██ ████████    ███     ██████   ████████      ███████   ██████
██     ██   ██ ██   ███   ██    ██      ██ ██   ██    ██  ██           ██     ██ ██    ██
██     ██  ██   ██  ████  ██    ██     ██   ██  ██        ██           ██     ██ ██
██     ██ ██     ██ ██ ██ ██    ██    ██     ██ ██   ████ ██████       ██     ██  ██████
 ██   ██  █████████ ██  ████    ██    █████████ ██    ██  ██           ██     ██       ██
  ██ ██   ██     ██ ██   ███    ██    ██     ██ ██    ██  ██       ███ ██     ██ ██    ██
   ███    ██     ██ ██    ██    ██    ██     ██  ██████   ████████ ███  ███████   ██████
```

Then exactly two lines:
- **Vantage.os — Marketing Intelligence OS**
- _marketing brain inside your agent_

### Step 2 — The interview (THIS IS THE CORE UX)

**WIZARD RULES — follow exactly:**
- Ask **exactly ONE question per message.** Then **STOP and wait** for the user's
  reply. Never put two questions in one message. Never pre-list all the questions.
- Ask in **plain conversational text.** Do **not** depend on the AskUserQuestion
  tool — it may be unavailable. (If it happens to be available, you may use it for a
  single question, but the one-at-a-time rule still holds.)
- For a question with a few sensible choices, offer them inline as a short lettered
  list **for that one question only** — but keep it light and human, not a form.
- Acknowledge each answer in a few words, then ask the next question. Keep momentum.
- If the user already supplied something in their `/vantage` input (a domain, a
  sub-command), **skip that question** and confirm it instead of re-asking.
- Let the user say "skip", "you decide", or "just run it" at any point — take a
  sensible default and move on. Don't interrogate.

**Question 1 — always start here, on its own:**

> **What are you looking to do today?**

Then, briefly, orient them with what Vantage can do (a light menu — this is still the
single Q1, not a dump of intake questions):

- **Full competitive landscape** — the complete teardown + report (most popular)
- **Find my competitors** — discover & tier the real set
- **Positioning & messaging** — how rivals position, where the white space is
- **Website / paid ads / content / social** — a single-channel teardown
- **Sales battlecard** — how to beat one specific competitor
- **Monitor** — keep watch on competitors over time

Wait for their answer, then route to the matching skill and continue the interview.

### Step 3 — Follow-up questions (one at a time, only what's needed)

Branch on what they chose. Ask each as its **own message**, waiting between each.
For the **Full competitive landscape** (the common path), ask in this order:

1. **"What's your brand or website?"** (the subject to analyze)
2. **"Who are your main competitors — or want me to find them for you?"**
   (if they have a list, take it; else plan to run `vantage-discover`)
3. **"Who's this for — marketing/growth, sales, or both?"**
   (shapes whether the "so what" leans positioning moves vs battlecard ammo)
4. **"How deep should I go — quick scan (top 3), standard (5–7), or deep dive (7+)?"**
5. **"Anything specific you want me to zero in on?"** (optional — a segment, a launch,
   a rival; accept "nope")

For a single-skill pick, ask only that skill's essentials (e.g. battlecard → which
competitor + your brand; ads → which domains). Always one question per message.

### Step 4 — Confirm, run, deliver

- Give a one-line recap of what you're about to do ("Got it — full landscape on
  ACME vs 5 competitors, sales-focused, standard depth. Running now.") and go.
- Execute (see Orchestration). Produce the **HTML report** (`references/html-report.md`),
  `open` it, and offer to stand up `vantage-monitor`.

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
