# Deliverable Templates

Copy-ready structures for every output the suite produces. Fill brackets, keep the
section order, and never ship a section without cited evidence.

> **The primary deliverable is a self-contained HTML file** — see
> `html-report.md` and clone `vantage/COMPETITIVE-LANDSCAPE.html`. The markdown
> structures below are the **working/data layer** that feeds the HTML (and a fine
> fallback when the user explicitly wants markdown). Same section order, same
> evidence rules, same DSoV scoring — just rendered beautifully in HTML.

---

## A. Full landscape report — `COMPETITIVE-LANDSCAPE.md`

```markdown
# Competitive Landscape — [Subject Brand]
*Category: [category] · Prepared [date] · Audience: [growth / sales]*

## 1. Executive Summary
- **The set:** [N direct, M emerging] competitors analyzed.
- **Where we stand:** DSoV [score]/100 — rank [k] of [N+1].
- **Biggest threat:** [competitor] — [one line why].
- **Biggest opening (white space):** [the gap no one owns].
- **Top 3 moves:** 1) … 2) … 3) …

## 2. The Competitive Set
| Tier | Competitor | Why they're in the set | DSoV |
|------|-----------|------------------------|------|
| Direct | … | … | …/100 |
| Direct | … | … | …/100 |
| Emerging | … | … | …/100 |
*Long tail (not deep-dived): [list].*

## 3. DSoV Matrix
| Brand | Pos. | Content | Website | Paid | Social | Rep. | **DSoV** |
|-------|-----:|-------:|-------:|----:|------:|----:|--------:|
| **[Us]** | | | | | | | |
| [Comp A] | | | | | | | |
*Band key: Dominant 85+ · Strong 70–84 · Credible 50–69 · Thin 30–49 · Absent <30.*

## 4. Positioning Map
[2×2 — axes chosen for this market, e.g. Price × Breadth, or
Self-serve × Enterprise. Place each brand. Call out the empty quadrant.]

## 5. Channel Findings
### Positioning & Messaging
[Messaging matrix + so-what]
### Content Engine
[Cadence, themes, share of search + so-what]
### Website & Conversion
[Funnel, offers, proof + so-what]
### Paid Media
[Active creatives, offers, spend posture + so-what]
### Social & Community
[Platforms, scale, engagement + so-what]
### Reputation & Proof
[Review themes, sentiment + so-what]

## 6. White Space & Threats
- **White space:** [positioning/channel/segment no competitor owns].
- **Threats:** [moves a rival is making that endanger us].

## 7. Prioritized Action Plan
| # | Move | Channel | Why now | Effort | Priority |
|---|------|---------|---------|--------|----------|
| 1 | … | … | … | … | Critical |

## 8. Battlecards
[Link to / embed per-competitor battlecards for top 2–3 — see template D.]

## Appendix: Evidence Log
| Claim | Source URL | Captured |
|-------|-----------|----------|
```

---

## B. Messaging matrix (positioning sub-skill)

| Element | Us | Comp A | Comp B |
|---------|----|--------|--------|
| One-liner | | | |
| Category they claim | | | |
| Named ICP | | | |
| Core differentiator | | | |
| Primary proof | | | |
| Primary CTA | | | |
| Tone | | | |

End with: **shared clichés** (what everyone says — avoid), and **uncontested
ground** (a true claim no one is making).

---

## C. Feature / offer comparison (website + content)

| Dimension | Us | Comp A | Comp B |
|-----------|----|--------|--------|
| Pricing model | | | |
| Entry price / free tier | | | |
| Primary offer (trial/demo/tool) | | | |
| Lead magnets | | | |
| Proof density (logos/reviews) | | | |
| Notable gaps | | | |

---

## D. Sales battlecard — one per competitor

```markdown
# Battlecard: [Competitor]  ·  Updated [date]
**Quick take:** [1–2 sentences: who they are, when we meet them, how we win.]

## Their pitch (steelman)
[How they position to OUR buyer — accurate, not strawman.]

## Why WE win  (lead with these)
- [Proof-backed advantage] — *evidence: [source]*
- …

## Where THEY win  (be honest)
- [Their real strength] — **our response:** [reframe / mitigant]

## Landmines to set  (questions that expose their weakness)
- "Ask them about [X]…" — surfaces [their gap].

## Objection handling
| They'll say | We respond |
|-------------|-----------|
| "[claim]" | "[reframe + proof]" |

## Pricing & packaging
[Public pricing, gotchas, where we're better value.]

## Proof points to cite
- [Customer / stat / G2 theme they lack and we have.]

## Do / Don't
- ✅ [trap-setting move]   ❌ [trash-talking — never]
```
*Sourcing: build "why they win/lose" from review-site themes + public pricing.
Never disparage; reframe with evidence. See `ethics-and-tos.md`.*

---

## E. Monitoring brief (vantage-monitor)

```markdown
# Competitive Watch — [date range]
## Changes since last check
| Competitor | What changed | Channel | Source | So what |
|-----------|--------------|---------|--------|---------|
## New entrants / exits
## Recommended responses
```

## Formatting rules
- Lead every section with the conclusion, then the evidence.
- Every quantitative claim → Evidence Log row (URL + date).
- Keep matrices to ≤7 competitors; tier the rest.
- Color bands in prose where tables can't render color (e.g. "Strong (78)").
