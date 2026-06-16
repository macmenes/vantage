---
name: vantage-content-plan
description: >
  TRIGGER when the user wants to PLAN their own content / content strategy —
  "content strategy", "content plan", "what should we write", "topic ideas",
  "content calendar", "pillar pages", "content briefs", "blog plan". Part of the
  `vantage` (Vantage.os) Content Engine pack. Builds a pillar/cluster plan, a
  prioritized topic backlog, full content briefs, and an editorial calendar.
  DO NOT trigger for ANALYZING a competitor's content (use vantage-content), live
  keyword DATA (use seo-dataforseo), or writing the final article (use copywriting /
  seo-content-writer).
context: fork
---

# Vantage — Content Engine (your content plan)

Turns competitive content gaps + your positioning into a buildable content engine: a
**pillar/cluster map**, a **prioritized topic backlog**, **full content briefs**, and
an **editorial calendar**. Web-informed but strategy-first; it coordinates with the
`seo-*` skills for keyword/volume data rather than duplicating them.

Deliverable: **`CONTENT-PLAN.html`** (shared design system —
`../vantage/references/html-report.md`).

## Intake (one question at a time — see console rules in `../vantage/SKILL.md`)

1. **"What's your brand or website, and who's the audience?"**
2. **"What's the content goal?"** (organic traffic · leads/demand · authority/POV ·
   product education · all)
3. **"Which themes do you want to own?"** (or "find them for me")
4. **"Want me to scan competitor content gaps first?"** → run `vantage-content`; else
   work from the user's themes.
5. **"Publishing capacity?"** (posts/month, formats you can produce) — sets the calendar.

## Method

### 1. Pillar / cluster architecture
- **Pillars** = the 3–5 themes you can credibly own (tie to positioning + white space).
- **Clusters** = supporting topics that link up to each pillar.
- Map intent across the funnel: TOFU (educate) → MOFU (evaluate) → BOFU (decide).
Every cluster topic should ladder to a pillar and a business outcome.

### 2. Topic backlog (prioritized, web-only signals)
Build a backlog scored qualitatively (quantify later via `seo-dataforseo`):
| Field | How to judge web-only |
|-------|------------------------|
| Search intent | Inspect the SERP for the query — informational/commercial/transactional |
| Competition | Who ranks; can you do better/different? (from `vantage-content`) |
| Business value | How close to the buying decision / your offer |
| Effort | Format + depth required |
| Gap type | Uncontested · under-served · saturated (from the content teardown) |
**Priority = business value × gap opportunity ÷ effort.** Surface the top 10–15.

### 3. Content briefs (the buildable unit)
Full brief per priority topic:
- Working title + target query + search intent
- Angle / POV (how yours differs — anti-generic)
- Audience + funnel stage + the CTA/offer it ladders to
- Outline (H2/H3s), key points to cover, questions to answer
- Original element (data, example, template, tool) that earns links/citations
- Internal links (to pillar + related clusters), suggested format & length
- Hand-off: "quantify keywords/difficulty with `seo-dataforseo`"

### 4. Editorial calendar
Sequence the backlog against capacity: what to publish in what order, cadence, and a
mix of pillar vs cluster vs distribution-friendly pieces. 8–12 weeks mapped.

## Output — `CONTENT-PLAN.html`

Clone the design system. Sections:
1. **Strategy snapshot** — audience, goal, pillars, the bet (which gaps you're taking)
2. **Pillar/cluster map** — visual hub-and-spoke per pillar
3. **Prioritized backlog** — table (topic · intent · funnel · gap · value · effort · priority)
4. **Content briefs** — 3–5 full briefs as cards (clone the rest to the same template)
5. **Editorial calendar** — 8–12 week schedule
6. **Hand-offs** — `seo-dataforseo` (volume/difficulty), `seo` (on-page), `seo-geo` (AI citation)

Then `open` it. Offer: "Want me to draft the first brief into a full article
(`seo-content-writer` / copywriting)?"

## Principles
- Strategy before keywords — own **themes**, not scattered posts.
- Every piece has a **distinct POV and an original element**; generic SEO filler loses.
- Each topic ladders to a **pillar and a business outcome** — no orphan traffic.
- Hand keyword/difficulty/backlink quantification to the `seo-*` skills.
