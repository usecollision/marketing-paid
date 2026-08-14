---
name: reddit-ads
category: paid
description: Plan and run Reddit ads with community-native creative, subreddit targeting, and karma-aware copy.
triggers:
  - "Reddit ads"
  - "advertise on Reddit"
  - "subreddit targeting"
  - "Reddit campaign"
  - "community-native ads"
inputs:
  - product_context
  - icp
  - community_research
  - budget
  - creative_assets
outputs:
  - community_targeting_plan
  - creative_angles
  - campaign_structure
  - comment_management_plan
  - measurement_plan
related_skills:
  - paid-strategy
  - ad-creative-generator
  - creative-testing
  - marketing-intelligence/reddit-research
  - marketing-channels/reddit-engagement
  - marketing-messaging/conversion-copywriting
required_context:
  - .context/product-marketing.md
allowed_tools:
  - none
version: 1.0.0
---

## When to Use

Invoke when:
- Testing Reddit as an ad channel
- Reaching technical or niche audiences at scale
- Building campaigns that need community credibility
- Advertising to researchers and early adopters
- Launching with a small budget on a new platform

## Workflow

### Step 1: Community & Fit Research
Reddit punishes advertisers who skip homework:
- [ ] Use reddit-research to identify relevant subreddits
- [ ] Lurk each community for 2+ weeks - learn the language, inside jokes, taboos
- [ ] Check rules - some subreddits ban promotion outright
- [ ] Assess audience size and engagement - niche but active beats huge but dead
- [ ] Study top posts - what earns upvotes in this community
- [ ] Mine threads for recurring pain points and objections

**Gate:** Shortlist of 5-15 communities with language and objection notes per community.

### Step 2: Targeting Strategy
- **Subreddit targeting** - direct placement in chosen communities; start here for relevance
- **Interest targeting** - Reddit's algorithm expands across related communities; scale later
- **Custom/retargeting** - site visitors and engagers; the mid-funnel layer
- Layering - subreddit + interest + device when volumes allow
- Avoid hyper-targeting - Reddit audiences are small; too many layers kills delivery
- Respect context - an ad that fits r/woodworking doesn't fit r/fitness

**Gate:** Targeting plan per community with delivery sanity check on audience size.

### Step 3: Community-Native Creative
Redditors smell marketing from the headline:
- Write like a Redditor, not a brand - specific, honest, direct, zero corporate voice
- Karma-aware copy - value-first posts, transparent that it's a promoted post
- Angles that work - "I built X and here's what I learned", "Am I crazy or...", honest founder stories, data and benchmarks, contrarian takes
- Avoid - emojis, ALL CAPS clickbait, salesy CTAs, stock photos, "Hey Reddit!" pandering
- Match the visual language of the subreddit - screenshots, memes, plain text over polished studio assets
- One creative per community persona - never one generic ad everywhere
- Be prepared for scrutiny - comments will fact-check every claim

**Gate:** Creative angle per community, written in that community's voice.

### Step 4: Formats & Placements
- **Free-form ads** - text-heavy, community-style; great for tech and product subreddits
- **Image ads** - subtle, native-feeling imagery
- **Video ads** - UGC-style; first 2 seconds decide everything
- **Conversation placement** (thread-level) - smaller inventory, deep engagement
- **AMAs and takeovers** - big budgets, mature brands, high-effort formats
- Start with feed + conversation placements, then review where engagement lands

**Gate:** Format per community chosen; placement split planned.

### Step 5: Bidding & Budget
- CPC or CPM bidding available; CPC often better for direct response
- Reddit minimums are low - viable for small-budget pilots (heuristic - validate with a controlled test)
- Expect lower CTRs than other platforms (heuristic) - but clicks skew research-driven and deliberate
- Pilot design - few communities, modest daily budget, 2-4 weeks, one variable
- Don't judge the channel on a pilot smaller than the community's active audience

**Gate:** Pilot budget and duration set with a pre-registered verdict date.

### Step 6: Comment Management (the hidden feature)
- Comments on your ads are public, blunt, and gold
- Enable and read comments on every ad; respond quickly and honestly
- Founder responses beat brand-account responses
- Objections in comments = free qualitative research - feed the insights into messaging
- Delete only spam; never delete criticism (it escalates publicly)
- Active comment sections improve trust and engagement signals

**Gate:** Comment monitoring assigned with response guidelines and an insights log.

### Step 7: Measurement & Iteration
- Reddit users research heavily - expect multi-touch journeys; last-click undercounts
- Track assisted conversions and branded search lift during campaigns
- Retarget Reddit engagers on Meta/Google - they're warm researchers
- Iterate creative weekly based on comment sentiment plus engagement metrics
- Scale - double budget on winning communities, expand to interest targeting, consider broader placements later
- Watch for the honeymoon cliff - early cheap clicks from a new audience segment often normalize

**Gate:** Measurement plan includes assisted conversions; iteration cadence scheduled.

## Practitioner Grounding & Decision Rules

Built from Dāvis Lejnieks (Undecided Agency), Matt Pru/Adam Tanguay (Stackmatix), Cole Furrh (Interteam), AdBacklog benchmarks, Reddit Business case studies. Full research: practitioner-intelligence/syntheses/paid-longtail.md.

- **Reddit is a consideration/research channel, not a click channel** (Lejnieks — EMPIRICAL, T2): pausing Reddit campaigns drops revenue 3-4x within 3-4 days while dashboard attribution shows little; last-click undercounts.
- **Unit economics are cheap but CTR is low** (Stackmatix/AdBacklog — HEURISTIC, T2/T3): CPM $2-5, median CPC ~$1.25, CTR 0.3-0.8%, ROAS 2.3-4.7x typical; B2B SaaS CPL $50-100, consumer ecom CPA $5-15 (vendor tables, directional).
- **Community intent beats interest targeting** (Lejnieks — EMPIRICAL, T2): subreddit targeting is the moat; interest expansion dilutes.
- **Reddit Max is a multiplier, not a magic button** (Lejnieks — EMPIRICAL, T2): requires ~$10k/month conversion volume; manual ads remain better for spicy creatives and specific communities.
- **CAPI halves CPA** (Lejnieks — EMPIRICAL, T2): conversion API installation alone cut CPA ~50% in his account.
- **Biggest mistake: reacting to a bad CPA without decomposing CPM/CTR/CVR** (AdBacklog — HEURISTIC, T3).

Decision rules:
1. IF budget < $10k/month THEN run manual community-targeted campaigns, NOT Reddit Max (Lejnieks — HEURISTIC, T2).
2. IF CPA looks bad THEN decompose CPM vs CTR vs CVR to find the broken stage before touching bids (AdBacklog — HEURISTIC, T3).
3. IF scaling THEN double budget on winning subreddits and only then expand to interest targeting after 2-4 weeks of community validation (Stackmatix/Lejnieks — HEURISTIC, T2).
4. IF judging the channel THEN require CAPI + a 30-60 day window + assisted-conversion view; dashboard ROAS alone is a lie (Lejnieks — EMPIRICAL, T2).
5. IF a subreddit's active audience is smaller than the pilot requires THEN don't run there — hyper-targeting kills delivery (Stackmatix — HEURISTIC, T3).
6. IF negative comment chains appear THEN respond honestly in-account; never delete criticism — backlash ranks in search (Stackmatix — HEURISTIC, T2).

## Metrics

- **CAPI-enabled conversions** as primary CPA/ROAS layer (Lejnieks — EMPIRICAL, T2).
- **Assisted conversions + branded search lift** during flight — the halo probe (Lejnieks/Stackmatix — HEURISTIC, T2).
- **Decomposed funnel**: CPM → CTR → CVR → CPA; fix the broken stage, not the bid (AdBacklog — HEURISTIC, T3).
- **Timebox**: verdict at 30-60 days per community; watch for honeymoon cliff (early cheap clicks normalize).
- **Guardrail**: don't judge one creative in one subreddit; comment sentiment is qualitative KPI.

## Sources

1. Dāvis Lejnieks, Reddit Max case study | undecided.agency/post/reddit-max-case-study | tier 1 | 2026-08-15
2. Matt Pru, Advertising on Reddit: Pros and Cons | stackmatix.com/blog | tier 2 | 2026-08-15
3. Stackmatix, Reddit Ads CPC/CPM benchmarks | stackmatix.com | tier 2 | 2026-08-15
4. AdBacklog, Reddit Ads Benchmarks per Industry | adbacklog.com | tier 3 | 2026-08-15
5. Reddit Business, DocMorris success story | business.reddit.com | tier 2 | 2026-08-15
6. Cole Furrh (Interteam), Reddit case studies | interteammarketing.com | tier 2 | 2026-08-15

## Evaluation & QA

### Common Failure Modes
- Repurposing polished Meta creative - instant downvotes
- Targeting dead or tiny subreddits
- Pitching in the first sentence instead of adding value
- Ignoring comments, or disabling them - a red flag to the community
- Judging the channel on one creative in one community
- Expecting Meta-level CTR benchmarks on day one
