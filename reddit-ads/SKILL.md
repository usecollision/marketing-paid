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

## Evaluation & QA

### Common Failure Modes
- Repurposing polished Meta creative - instant downvotes
- Targeting dead or tiny subreddits
- Pitching in the first sentence instead of adding value
- Ignoring comments, or disabling them - a red flag to the community
- Judging the channel on one creative in one community
- Expecting Meta-level CTR benchmarks on day one
