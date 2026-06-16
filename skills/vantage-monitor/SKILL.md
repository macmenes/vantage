---
name: vantage-monitor
description: >
  TRIGGER when the user wants ONGOING competitive monitoring — "monitor our
  competitors", "watch competitor changes", "track competitor pricing/messaging",
  "competitive alerts", "keep tabs on", "recurring competitive watch". Part of the
  `vantage` suite. Establishes a repeatable watch and diff-since-last-check brief.
  DO NOT trigger for a one-time teardown (use /vantage) or rank tracking only (use
  rank-tracker).
context: fork
---

# Vantage-Monitor — Recurring Competitive Watch

Competitive facts decay. This skill stands up a **repeatable watch** over the set,
captures a baseline, and on each run reports only **what changed** and **what to do
about it** — so the landscape report and battlecards never go stale.

Web-only. Brief format = template E in `../vantage/references/deliverable-templates.md`.

## What to watch (per competitor)

| Signal | Source | Why it matters |
|--------|--------|----------------|
| Pricing & packaging | `/pricing` (+ Wayback diff) | Price moves = strategy shifts; battlecard-critical |
| Homepage hero / positioning | Homepage H1+subhead | Repositioning = vulnerability or new threat |
| New ad campaigns | Meta Ad Library, Google ATC | New offers/angles to counter or swipe |
| New content / launches | `/blog`, `/changelog`, `/news`, sitemap `lastmod` | Product & content momentum |
| Reviews & sentiment | G2/Capterra/Trustpilot counts + recent text | Emerging strengths/complaints for battlecards |
| Funding / M&A / news | WebSearch `<brand> news` | Resourcing, threat level, market moves |
| Social cadence shifts | Profile activity | Channel strategy changes |

## Method

1. **Baseline.** On first run, snapshot each watched signal with value + source URL
   + capture date into a `COMPETITIVE-WATCH-BASELINE.md` (or update the existing
   landscape report's Evidence Log).
2. **Diff.** On each subsequent run, re-fetch and compare to the last snapshot. Use
   the Wayback Machine to confirm *when* a change happened where the live page hides
   it.
3. **Report only deltas.** Produce the monitoring brief (template E): what changed,
   on which channel, the source, and the recommended response. No-change items get a
   one-line "no material change" — don't pad.
4. **Escalate.** Flag changes that invalidate a battlecard claim or the positioning
   map as **action-required**.
5. **Refresh artifacts.** Offer to update the affected battlecard / landscape section.

## Standing up the recurring run

This skill defines *what* to check. To actually run it on a cadence, use the
harness's scheduling — don't reinvent it:

- **`/schedule`** — a cloud cron agent (e.g. weekly) that re-runs this watch and
  reports deltas. Best for hands-off, runs-without-you monitoring.
- **`/loop`** — an in-session recurring run when you want to watch actively for a
  while.

Recommend a cadence by volatility: **weekly** for active markets / live deals,
**monthly** for stable categories, **ad-hoc** before a launch or big pitch. Suggest
the specific command, e.g. *"Want me to `/schedule` this competitive watch weekly on
Mondays?"* — and only offer if there's a real ongoing need.

## Output (each run)

```markdown
# Competitive Watch — [date]  (since [last date])
## Material changes
| Competitor | What changed | Channel | Source | When (Wayback) | So what |
|-----------|--------------|---------|--------|----------------|---------|
## Action required (invalidates a battlecard / map)
- …
## New entrants / exits
- …
## No material change
- [competitors with nothing notable]
## Recommended responses
1. …
```
