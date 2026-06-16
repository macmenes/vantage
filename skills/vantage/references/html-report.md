# HTML Report — Standard Deliverable

The suite's **primary deliverable is a single, self-contained, beautiful HTML
file** (`COMPETITIVE-LANDSCAPE.html`). Markdown is kept only as the working draft /
data layer; the HTML is what gets shared. The canonical, fully-worked template ships
with this skill at **`references/report-example.html`** (a fully-worked sample) —
**clone its structure and CSS verbatim**, then swap in the new analysis. Do not
redesign per run. (LLMs reproduce a worked example more reliably than a placeholder
skeleton, so the example *is* the template.)

## Non-negotiables

1. **Self-contained.** One `.html` file. All CSS inline in a `<style>` block. No
   build step, no JS framework. Google Fonts via `<link>` is allowed (degrades
   gracefully to the system stack offline).
2. **Logo included, real, inlined.** Fetch the subject brand's actual mark and embed
   it — never a placeholder. See "Logo acquisition" below. Recolor it to sit on the
   report's ink/paper palette if needed.
3. **Restrained, premium chrome; color only in data.** The page chrome is
   monochrome (ink on warm paper). Color appears **only** in the score heatmap,
   priority tags, and win/lose blocks. Do not theme the whole report in the brand's
   color just because the brand uses it — match the brand's *level of taste*, not its
   hue. (e.g. a design-forward AI tool → sleek monochrome chrome, not a literal wash of the brand color.)
4. **Every number is evidence-backed.** The Evidence Log `<details>` is mandatory and
   must carry a row per quantitative claim with source link + capture date.
5. **Print-ready.** Keep the `@media print` block so the report exports cleanly to PDF.

## Design system (tokens — keep these exact)

- **Fonts:** `Inter` (UI/body) + `Fraunces` (display serif for the big DSoV number,
  section numerals, battlecard accents). System fallbacks required.
- **Palette:** `--ink:#0c0d10` · `--ink-2:#3a3d44` · `--ink-3:#73767e` ·
  `--paper:#fbfaf7` · `--card:#fff` · hairline `--line:#e7e5e0`.
- **Heatmap bands** (the only saturated colors): Dominant `#0f5c3f`/bg`#e4f0ea` ·
  Strong `#2f7d54`/`#ebf3ee` · Credible `#9a7b1f`/`#f6f0dd` · Thin `#b5631f`/`#f7e9dd`
  · Absent `#9a3b34`/`#f5e2e0`. Priority: Critical = Absent red, High = Credible
  amber, Medium = slate `#41515f`.
- **Radius** 14px cards / 18–20px feature cards; soft layered `--shadow`.
- **Accent = ink** by default (monochrome). Only override `--accent` if the brand's
  identity genuinely calls for one restrained accent — never a loud one.

## Required sections (in order)

Sticky nav → Hero (logo lockup + title + meta chips + dark **scorecard** with the
DSoV number, rank, strongest/weakest channel) → 01 Executive Summary (threat +
white-space cards + numbered moves) → 02 Competitive Set (tiered table) → 03 **DSoV
Matrix** (heatmap table, subject row highlighted, band legend) → 04 **Positioning
Map** (CSS 2×2 with plotted dots; subject dot larger/ink; name the empty quadrant) →
05 Channel Findings (one block per channel with a band pill + "so what" callout) →
06 White Space & Threats (two columns) → 07 Action Plan (priority-tagged table) →
08 Battlecards (win/lose two-column, steelman, landmines, objection table, do/don't)
→ 09 Evidence & Hand-offs (`<details>` evidence log + skill hand-offs).

## Component cheatsheet

- **Score cell:** `<span class="score strong">75</span>` — class = band name.
- **Subject row:** `<tr class="subject">` (left ink rule + tint).
- **Positioning dot:** `<div class="pt" style="left:62%;top:36%">` — X = solo→team,
  Y top = canvas / bottom = single surface. Subject gets `class="pt us"`.
- **So-what callout:** `<p class="callout so-what"><span class="tag">So what</span>…`.
- **Priority tag:** `<span class="prio p-crit|p-high|p-med">`.
- **Battlecard:** `.bcard` → `.steel` (steelman) → `.winlose` (`.wl.win` / `.wl.lose`)
  → `.landmines` → objection `<table>` → `.dodont`.

## Logo acquisition (web-only, in priority order)

1. Fetch the homepage; read `<link rel="icon">` (often a crisp **SVG** — inline it
   directly, recolor fills to `--ink`/`#fff` for the badge), `apple-touch-icon`, and
   `og:image`.
2. Look for a brand asset path (`/brand/logo*.svg|png`, `media.<domain>/brand/…`).
3. Fallback: `https://www.google.com/s2/favicons?domain=<domain>&sz=256` (base64-embed).
4. Last resort: a monogram badge — the brand's initial in `Fraunces` on an ink
   rounded square. Never ship a broken image.

Inline SVG marks are best (scalable, recolorable, tiny). Base64-embed raster logos so
the file stays self-contained.

## Generation flow

1. Produce/collect the analysis (markdown working draft is fine).
2. Acquire + inline the logo.
3. Clone `references/report-example.html`, replace content section by section, keep
   all CSS.
4. Write `COMPETITIVE-LANDSCAPE.html`; offer to open it (`open <file>`) and to
   export PDF (print dialog) or stand up `vantage-monitor`.
