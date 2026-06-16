---
name: vantage-social
description: >
  TRIGGER when the user wants a competitor social & community / share-of-voice
  read — "their social presence", "share of voice", "engagement vs competitors",
  "what do they post", "their LinkedIn", "community strategy", "social
  benchmarking". Part of the `vantage` suite.
  DO NOT trigger for paid social ADS (use vantage-ads) or running the user's own
  social.
context: fork
---

# Vantage-Social — Social Presence & Share-of-Voice

Where each competitor shows up organically, how big and how *engaged* their audience
is, what they post, and whether they own a community. Engagement quality beats
follower vanity throughout.

Web-only, public profiles. Score with `scoring-framework.md` §5.

## Read each presence

1. **Platform fit** — which platforms are they actually on, and is it where their
   ICP is? (B2B → LinkedIn/X/YouTube; B2C/creator → Instagram/TikTok/YouTube.) Being
   big on the wrong platform doesn't count.
2. **Audience scale** — public follower counts per platform. Context only — compare
   within the set, never treat as the goal.
3. **Engagement rate** — eyeball the last ~10 posts: avg likes+comments+shares ÷
   followers. **This is the real signal.** 5k followers at 3% beats 50k at 0.1%.
4. **Content quality & themes** — native, on-brand, distinct content vs reposted
   filler. What 2–3 themes do they push? Any signature format (series, formats)?
5. **Cadence** — posting frequency and recency. Sporadic = underinvested.
6. **Owned audience / community** — newsletter, Slack/Discord/Circle community,
   forum, ambassador program. Owned > rented; a real community is a moat.
7. **Employee/founder amplification** — are execs/employees posting and getting
   reach? Founder-led distribution is hard to vantage with on ad budget alone.

## Share-of-voice frame

For the category, estimate each brand's relative organic mindshare from: audience
scale × engagement × cadence, plus mentions (`site:reddit.com <brand>`, X search,
community chatter). Express as a **relative** ranking with evidence — not a fake
precise percentage.

## Output

```markdown
# Social & Share-of-Voice — [set]
*Captured [date]*

## Presence comparison
| Competitor | Platforms (fit) | Largest audience | Est. engagement | Cadence | Owned community |
|-----------|-----------------|-----------------:|-----------------|---------|-----------------|

## Content themes & signature formats
| Competitor | Top themes | Signature format | Founder/employee amplification |
|-----------|-----------|------------------|--------------------------------|

## Share-of-voice (relative)
[Ranked, with the basis for each placement.]

## So what (growth)
- **Platform/format the subject brand should double down on:** …
- **Under-served platform or community white space:** …
- **Engagement tactics worth copying:** …
```
