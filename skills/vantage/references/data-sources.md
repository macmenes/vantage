# Data Sources - Web-Only Intelligence Map

Every signal the suite needs, where it lives, and the query pattern to get it -
using **WebSearch + WebFetch only**. All public. No logins, no scraping gated data
(see `ethics-and-tos.md`). If paid tools (DataForSEO, SerpAPI, SimilarWeb API) are
present, prefer them for the items marked ⚡; otherwise the free path below works.

## Competitor discovery

| Goal | Source / pattern |
|------|------------------|
| Direct competitors | WebSearch: `"<brand>" alternatives`, `"<brand>" vs`, `best <category> tools 2026` |
| "Alternatives to" lists | WebFetch top results for `<brand> alternatives` (G2, listicles) |
| SERP rivals | Run 5–10 buyer queries for the category; collect repeat domains |
| Review-site co-listings | G2/Capterra "compare" + "competitors" tabs list rivals |
| Funded / emerging | WebSearch: `<category> startup funding 2025 2026`, Crunchbase result snippets |
| Who bids on the brand | Google Ads Transparency for the brand term; Meta Ad Library keyword search |

## Positioning & messaging

| Goal | Source |
|------|--------|
| Value prop / hero | WebFetch homepage; read H1, subhead, primary CTA |
| Category & ICP | /product, /solutions, /customers, /about |
| Message evolution | **Wayback Machine** `web.archive.org/web/*/<url>` - compare hero across years |
| Boilerplate / one-liner | /about, press releases, LinkedIn company "About", footer |

## Website & conversion

| Goal | Source |
|------|--------|
| Funnel & CTAs | WebFetch home + nav targets; map primary/secondary actions |
| Pricing | /pricing (or note "contact us only"); Wayback for pricing changes |
| Social proof | Logos, /customers, /case-studies, testimonial blocks |
| Lead magnets | /resources, gated assets, exit popups (visible in HTML/copy) |
| Tech stack ⚡ | BuiltWith.com `builtwith.com/<domain>`, Wappalyzer profiles |
| Traffic estimate ⚡ | SimilarWeb public page `similarweb.com/website/<domain>`; note it's an estimate |

## Content engine

| Goal | Source |
|------|--------|
| Cadence & topics | /blog, /resources; **sitemap.xml** `lastmod` dates; `/sitemap_index.xml` |
| Pillar/cluster structure | Blog category nav, hub pages |
| Share of search | Run category buyer queries; count domain appearances on page 1 |
| Content history | Wayback Machine snapshots of /blog index |
| Formats | Scan resources nav: guides, tools, templates, webinars, podcasts, video |
| Deep keyword/backlink data | **Hand off** to `seo-dataforseo`, `backlink-analyzer`, `seo` |

## Paid media (the highest-signal public source)

| Goal | Source |
|------|--------|
| Meta/Instagram ads | **Meta Ad Library** `facebook.com/ads/library` - search by brand; shows active creatives, copy, "started running" date, variations |
| Google/YouTube/Display ads | **Google Ads Transparency Center** `adstransparency.google.com` - search advertiser; shows formats, regions, time ranges |
| LinkedIn ads | LinkedIn company Page → **Posts → Ads** tab (public) |
| TikTok ads | **TikTok Creative Center** Top Ads (region-limited, public) |
| Offer/angle analysis | Read ad copy + click through to landing pages |
| Winner inference | Ads running many months = likely profitable; note longevity |

Blind spots to disclose: **Google Search text ads** and some networks aren't fully
visible; "no ads found" means *not visible here*, not *not advertising*.

## Social & community

| Goal | Source |
|------|--------|
| Profiles & scale | WebFetch their LinkedIn/X/Instagram/YouTube/TikTok profile pages (public follower counts) |
| Engagement | Eyeball recent posts: likes/comments/shares vs follower base |
| Themes & cadence | Scan last ~10 posts for topics + posting frequency |
| Owned community | Slack/Discord/Circle communities, newsletter signup, forum |
| Employee advocacy | LinkedIn: are execs/employees posting & getting reach? |
| Optional public X evidence | Xquik, when already configured or supplied by the user; capture public profile, search, post, and engagement snapshots with source post URLs or IDs |

## Reputation & proof

| Goal | Source |
|------|--------|
| Reviews | **G2**, **Capterra**, **TrustRadius**, **Trustpilot**, **Gartner Peer Insights**, app stores - counts, ratings, recent review text |
| Sentiment themes | Read 1★–2★ and 4★–5★ reviews; extract recurring pros/cons |
| Press & analyst | WebSearch: `<brand> news 2026`, `<brand> Gartner OR Forrester`, awards |
| Community sentiment | Reddit (`site:reddit.com <brand>`), Hacker News, niche forums |

## Pricing & packaging

| Goal | Source |
|------|--------|
| Current pricing | /pricing |
| Pricing history | Wayback Machine on /pricing - surface increases/repackaging |
| Discounts/promos | Ad copy, /deals, seasonal banners, affiliate pages |

## Capture discipline

For every fetched fact, record: **source URL + capture date (today)**. Competitive
facts decay fast; an undated claim is unusable in a battlecard. When using Wayback,
record the snapshot date, not today's date.
