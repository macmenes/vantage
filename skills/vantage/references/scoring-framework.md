# DSoV Scoring Framework

How to turn web-only evidence into defensible 0–100 scores. Read this before
scoring any competitor. The goal is **consistency** (the same evidence yields the
same score across competitors) and **decision-usefulness** (scores map to moves).

## The index

`DSoV = 0.20·Positioning + 0.20·Content + 0.15·Website + 0.15·Paid + 0.15·Social + 0.15·Reputation`

Score the **subject brand on the identical rubric** so every cell is a gap, not an
absolute. Round to nearest 5 — these are judgments, not measurements; false
precision erodes trust.

## Banding (applies to every channel)

| Band | Score | Meaning |
|------|-------|---------|
| Dominant | 85–100 | Sets the standard in the set; others react to them |
| Strong | 70–84 | Clearly above set average; few gaps |
| Credible | 50–69 | In the game; visible weaknesses |
| Thin | 30–49 | Present but underinvested / incoherent |
| Absent | 0–29 | Effectively not competing on this channel |

Never score a channel without **≥3 cited signals**. Fewer than 3 → score the
channel "Insufficient evidence" and say what you'd need, rather than guessing.

---

## 1. Positioning & Differentiation (20%)

What you can read from the homepage, /about, category pages, and headlines.

| Signal | Where | Scores up |
|--------|-------|-----------|
| Value-prop clarity | Hero H1/subhead | One sentence, specific outcome, names the ICP |
| Category stance | Hero, nav, /product | Owns or names a category vs generic "platform/solution" |
| Differentiation | Throughout | Concrete, hard-to-copy claim vs me-too feature lists |
| ICP precision | Headlines, /customers | Names a buyer/segment vs "for everyone" |
| Message consistency | Home vs ads vs social | Same core promise across surfaces |
| Proof of claim | Hero proximity | Specific outcome/stat near the promise, not vague |

Deductions: jargon-only hero, "all-in-one" with no edge, contradictory messages
across channels, claims with zero proof.

## 2. Organic / Content Engine (20%)

Marketing-level read of the content machine (hand depth to `seo-*`).

| Signal | Where | Scores up |
|--------|-------|-----------|
| Publishing cadence | /blog, /resources, sitemap dates | Consistent, recent (last post < 30d) |
| Topical depth | Blog taxonomy, hubs | Clear pillar/cluster structure, owns themes |
| Format range | Resources nav | Guides, tools, templates, video, original data |
| Share of search | SERP for category terms | Appears repeatedly on page 1 for buyer queries |
| Distinct POV | Content tone | A thesis/voice vs SEO filler |
| Conversion intent | CTAs in content | Content tied to offers, not orphaned |

Estimate cadence from sitemap `lastmod`, visible post dates, and Wayback diffs.
Estimate share of search by running 5–10 category queries and counting appearances.

## 3. Website & Conversion (15%)

| Signal | Where | Scores up |
|--------|-------|-----------|
| Funnel clarity | Nav → CTA path | Obvious primary action; low-friction next step |
| Offer strength | Hero/pricing CTA | Compelling, specific (free trial, demo, tool) |
| Pricing transparency | /pricing | Public tiers/anchors vs "contact us" only |
| Social proof density | Throughout | Logos, named testimonials, quantified results, ratings |
| Lead capture | Forms, magnets | Multiple low-friction captures; valuable magnets |
| Trust & polish | Whole site | Fast, modern, credible; no broken/dated UX |

## 4. Paid Media (15%)

From **Meta Ad Library** and **Google Ads Transparency Center** (public).

| Signal | Where | Scores up |
|--------|-------|-----------|
| Active spend footprint | Ad libraries | Many active ads across platforms |
| Creative volume/variety | Ad library | Many concepts/angles, ongoing iteration |
| Longevity (proxy for ROAS) | Ad "running since" dates | Ads running months = likely winners |
| Offer & angle clarity | Ad copy | Strong hooks, clear offers, distinct angles |
| Landing-page match | Ad → LP | Dedicated, message-matched LPs |
| Channel breadth | Across libraries | Meta + Google + (LinkedIn/YouTube where visible) |

Absence of ads ≠ no spend (search ads & some channels are less visible) — note the
blind spots. See `data-sources.md`.

## 5. Social & Community (15%)

| Signal | Where | Scores up |
|--------|-------|-----------|
| Platform fit | Their profiles | Present where their ICP actually is |
| Audience scale | Profile counts | Followers relative to set (context, not vanity) |
| Engagement rate | Recent posts | Real comments/shares vs follower count |
| Content quality | Feed | Native, on-brand, distinct vs reposted filler |
| Cadence | Post dates | Consistent and recent |
| Community/owned | LinkedIn, communities, newsletter | Owned audience (community, Slack, newsletter) |

Engagement rate >> follower count. A 5k-follower account with 3% engagement beats a
50k account with 0.1%.

## 6. Reputation & Proof (15%)

From review sites (G2, Capterra, TrustRadius, Trustpilot), testimonials, press.

| Signal | Where | Scores up |
|--------|-------|-----------|
| Review volume & rating | G2/Capterra/Trustpilot | High count + high rating (both matter) |
| Recency | Review dates | Steady recent reviews, not stale |
| Sentiment themes | Review text | Consistent praise themes; few repeated complaints |
| Named proof | Site testimonials, case studies | Real names/logos, quantified outcomes |
| Third-party validation | Press, awards, analyst | Independent coverage/recognition |
| Response posture | Review replies | Vendor engages, resolves complaints |

Mine review *themes* — they are the raw material for battlecard "why they win / why
they lose" and for positioning white space.

---

## Rolling up

1. Score each competitor + the subject brand per channel (cite ≥3 signals each).
2. Compute weighted DSoV per brand.
3. Build the matrix (brands × channels, color-banded).
4. **Read the gaps**: where is the subject brand behind, and where is there
   *white space* no competitor owns (highest-leverage opportunity).
5. Translate each gap into one prioritized move (Critical / High / Medium).

## Honesty rules

- No invented metrics. Follower counts, review counts, ad counts = cite the source
  and capture date. Anything inferred = label "estimate" + show the basis.
- If the subject brand wins a channel, say so plainly — this isn't an exercise in
  flattering the competition.
- Distinguish *can't tell* from *weak*. Hidden ≠ absent.
