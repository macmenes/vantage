# Changelog

All notable changes to **Vantage** are documented here.
This project adheres to [Semantic Versioning](https://semver.org).

## [0.2.1] — 2026-06-16

### Added — sample report for every pack
- Shipped a full, self-contained HTML sample for each Build pack, all on one fictional brand
  (**Northpeak**) so the teardown and the marketing it produces read as one story:
  `sample-messaging-house.html`, `sample-campaign-concepts.html`, `sample-content-plan.html`,
  `sample-lifecycle-flows.html`. Each is also bundled as the skill's `references/report-example.html`.
- README now links all five samples in a **Sample reports** gallery.

## [0.2.0] — 2026-06-16

Vantage becomes a hub: "analyze the field" **and** "build your marketing."

### Added — four marketing creation packs (HTML deliverable each)
- **Positioning Studio** (`vantage-messaging`) — Dunford-style positioning, messaging house, value prop & one-liners, 3 hero-copy variants, voice/tone, narrative → `MESSAGING-HOUSE.html`.
- **Paid-Media Lab** (`vantage-ad-lab`) — angle matrix, hook bank, full ad variants (Meta / Google RSA / LinkedIn / video), creative briefs, LP outline, test plan → `CAMPAIGN-CONCEPTS.html`.
- **Content Engine** (`vantage-content-plan`) — pillar/cluster map, prioritized topic backlog, full content briefs, editorial calendar → `CONTENT-PLAN.html`.
- **Lifecycle & Email** (`vantage-lifecycle`) — lifecycle map, core sequences, full email copy, trigger/timing logic → `LIFECYCLE-FLOWS.html`.

### Changed
- Console menu now groups **🔍 Analyze** vs **🛠 Build**; the Build skills offer to pull from a prior teardown or run the analysis first.
- 13 skills across 5 packs. Manifests, README, commands, and roadmap updated.

## [0.1.0] — 2026-06-16

Initial public release.

### Added
- Umbrella `vantage` skill that orchestrates a full digital-marketing competitive teardown.
- 8 specialist skills: `vantage-discover`, `vantage-positioning`, `vantage-website`,
  `vantage-content`, `vantage-ads`, `vantage-social`, `vantage-battlecard`, `vantage-monitor`.
- **Digital Share-of-Voice (DSoV)** scoring framework across six channels with banding and
  evidence rules.
- Web-only data-source playbook (ad libraries, review sites, Wayback Machine) — no API keys.
- Public-source ethics & ToS guardrails.
- **Beautiful self-contained HTML report** as the primary deliverable (heatmap matrix, plotted
  2×2 positioning map, win/lose battlecards, sourced evidence log, print-ready), with the design
  system documented and a worked sample report (fictional data) shipped as the template.
- Claude Code plugin + marketplace manifests for one-command install.
