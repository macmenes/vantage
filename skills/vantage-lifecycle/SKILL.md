---
name: vantage-lifecycle
description: >
  TRIGGER when the user wants to build email / lifecycle / nurture flows — "email
  sequence", "welcome series", "onboarding emails", "nurture flow", "drip
  campaign", "winback", "lifecycle marketing", "trial conversion emails", "write our
  emails". Part of the `vantage` (Vantage.os) Lifecycle & Email pack. Produces a
  lifecycle map, sequence designs, full email copy, and trigger/timing logic.
  DO NOT trigger for one-off broadcast/newsletter copy only (use copywriting) or
  paid ads (use vantage-ad-lab).
context: fork
---

# Vantage — Lifecycle & Email (your flows)

Designs the brand's lifecycle program and writes the emails: a **lifecycle map**, the
**core sequences**, **full email copy** (subject, preview, body, CTA), and the
**trigger/timing logic** to run them. ESP-agnostic — the logic ports to any tool.

Deliverable: **`LIFECYCLE-FLOWS.html`** (shared design system —
`../vantage/references/html-report.md`).

## Intake (one question at a time — see console rules in `../vantage/SKILL.md`)

1. **"What's the product, and the pricing/model?"** (free trial · freemium · demo/sales
   · ecommerce · subscription)
2. **"What's the ONE conversion event that matters most?"** (e.g. activate, upgrade,
   first purchase, booked call)
3. **"Where do most people drop off today?"** (the leak to plug first)
4. **"Which flows do you want?"** — or "recommend the highest-leverage ones"
5. **"Brand voice / sender, and any offer you can use?"** (optional)

## Method

### 1. Lifecycle map
Plot the customer across stages and name the goal + risk at each:
`Subscribe → Activate → Onboard → Engage → Convert → Retain → Expand → Win-back → Refer.`
Identify where the biggest leak is and prioritize the flow that plugs it.

### 2. Core sequences (pick by model)
- **Welcome / onboarding** — set expectations, drive the first value moment (activation).
- **Lead nurture** — educate the not-yet-ready; tie to content + offers.
- **Trial / freemium conversion** — value recap → proof → urgency → upgrade.
- **Abandoned cart / browse** (ecommerce) — reminder → objection → incentive.
- **Post-purchase / onboarding** — reduce regret, drive adoption, set up expansion.
- **Win-back** — re-engage dormant users; "is this goodbye?" pattern.
Design each as a flow: number of emails, the job of each, timing, and exit/branch logic.

### 3. Trigger & timing logic
For each flow: entry trigger, send delays, branch conditions (opened/clicked/converted),
exit criteria, and suppression rules. Keep it ESP-agnostic (works in any tool).

### 4. Full email copy
Write each priority email complete:
- **Subject line** (+1–2 A/B alternates) and **preview text**
- **Body** — one idea, one CTA, skimmable, value-led not feature-led
- **CTA** — single, specific, action-oriented
Apply best practices: lead with the reader's outcome, short paragraphs, plain voice, a
clear single action; avoid spam-trigger fluff.

### 5. Measurement
Per flow: the metric that matters (activation rate, trial→paid, reactivation), and the
one thing to A/B first (usually subject or the core offer/angle).

## Output — `LIFECYCLE-FLOWS.html`

Clone the design system. Sections:
1. **Lifecycle map** — stages with goal/risk, the prioritized leak
2. **Flow index** — the sequences, each with purpose + email count + timing
3. **Sequence diagrams** — per flow: emails in order, timing, branch/exit logic
4. **Email copy** — every priority email as a card (subject · preview · body · CTA · A/B)
5. **Trigger & timing table** — entry/delay/branch/exit per flow
6. **Measurement** — KPI + first A/B per flow

Then `open` it. Offer: "Want ad concepts to feed the top of this funnel
(`vantage-ad-lab`), or a content plan to fuel nurture (`vantage-content-plan`)?"

## Principles
- Map the **leak** before writing emails — fix the highest-leverage stage first.
- One email, one idea, one CTA — value before feature.
- Timing and triggers are part of the copy; design the **flow**, not just the messages.
- Honest urgency and real offers only; never fake scarcity.
