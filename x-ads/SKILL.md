---
name: x-ads
category: paid
description: Plan and run X Ads with promoted post formats, follower-lookalike-keyword targeting, creator co-branding, and B2B-tech audience plays.
triggers:
  - "X Ads"
  - "Twitter Ads"
  - "promoted posts on X"
  - "X campaign"
  - "follower lookalike targeting"
  - "advertise on X"
  - "X ads for B2B"
inputs:
  - product_context
  - icp
  - budget
  - creative_assets
  - account_data
  - creator_partners
outputs:
  - channel_fit_assessment
  - campaign_structure
  - ad_format_plan
  - targeting_plan
  - creator_briefs
  - measurement_plan
related_skills:
  - paid-strategy
  - ad-creative-generator
  - creative-testing
  - media-planning
  - linkedin-ads
  - marketing-messaging/brand-voice
  - marketing-channels/social-strategy
required_context:
  - .context/product-marketing.md
allowed_tools:
  - none
version: 1.0.0
---

## When to Use

Invoke when:
- Testing X as a paid channel for B2B tech or developer products
- Promoting content, launches, or thought leadership on X
- Reaching founders, engineers, and tech press who live on the feed
- Running creator or influencer co-branded campaigns
- Capturing real-time topical demand (events, launches, news moments)
- Adding a low-cost awareness layer next to LinkedIn and Google

## Workflow

### Step 1: Channel Fit & Objective
- [ ] Define the objective first - X works best for awareness, content amplification, and community building; direct-response performance is weaker than search/social incumbents (heuristic - validate with your own tests)
- [ ] Check ICP presence - is your audience actually active on X? Verify with follower-graph research before spending
- [ ] Pick the KPI that matches the objective - profile visits, link clicks, engagement rate, video views, or assisted conversions
- [ ] Frame the budget - X is usually a test-and-learn or brand layer, not the performance backbone

**Gate:** Objective, ICP presence evidence, and KPI agreed before any campaign build.

### Step 2: Ad Formats
- **Promoted posts** - boost organic-feeling posts; the native unit people actually engage with
- **Video ads** - in-feed video; keep it under 30 seconds, the first frame carries the hook
- **Amplify pre-roll** - brand-safe video against premium publisher content; awareness play
- **Vertical video** - full-screen unit; matches mobile feed behavior
- **Carousel and moment ads** - for storytelling and multi-product showcases
- Default recommendation - promote existing organic posts that already earned engagement (heuristic)

**Gate:** Format per objective chosen; at least one organic post with proof of resonance picked for promotion.

### Step 3: Targeting
- **Follower lookalikes** - target followers of specific accounts (competitors, media, thought leaders); the highest-signal X audience for tech
- **Keyword targeting** - catch real-time topical conversations; pair with exclusions to control noise
- **Engagement retargeting** - people who engaged with your posts or videos
- **Custom audiences** - email lists, site visitors via the X pixel
- **Interest and behavior segments** - broader reach, weaker signal
- Layering rule - combine 2-3 signals max; X's active base is small and heavy layering kills delivery

**Gate:** Targeting plan per ad group with audience-size sanity check and excluded noise keywords.

### Step 4: Creative for the X Feed
- [ ] Write like a human on X - short, opinionated, zero corporate tone; match the timeline's voice
- [ ] Lead with the take, not the product - strong opinions and data earn the click
- [ ] Keep threads and context - link to a thread or long-form post, not a bare landing page, for technical audiences
- [ ] Use memes and screenshots - native X formats beat polished brand assets (heuristic)
- [ ] Iterate fast - X creative fatigue is real; refresh hooks weekly during active campaigns
- [ ] Enable replies carefully - community replies can amplify or derail; have a moderation plan

**Gate:** Creative set written in X-native voice with a weekly refresh plan.

### Step 5: Creator Co-Branding
- [ ] Identify creators your ICP already follows - use follower-graph overlap, not vanity metrics
- [ ] Choose the structure - branded content posts or creator-led takeovers, with disclosure
- [ ] Let the creator write it - pre-written brand copy from a creator account converts worse (heuristic)
- [ ] Compensate fairly and disclose - paid partnership tags keep it compliant
- [ ] Amplify creator posts with paid - the compounding play: creator earns organic reach, you buy the distribution

**Gate:** Creator shortlist with follower-overlap rationale; at least one co-branded post live with paid support.

### Step 6: Bidding, Budget & Measurement
- [ ] Start with automatic bidding on engagement or views while learning; switch to conversions only with volume
- [ ] Pilot design - small daily budget, 2-4 weeks, one variable (audience or format)
- [ ] Measure beyond last-click - X touchpoints rarely close deals directly; track assisted conversions and branded search lift
- [ ] Watch quality - engagement rate and profile visits are leading indicators; low-quality clicks happen
- [ ] Expect CPM variance - topical moments spike demand; schedule around launches, not against them

**Gate:** Pilot launched with pre-registered verdict criteria and a quality-check cadence.

## Practitioner Grounding & Decision Rules

Built from Directive Consulting (B2B X retargeting practice), Coinis (2026 X ads mechanics), Upgrow (X agency), Affiliate World Forums operator reports. Full research: practitioner-intelligence/syntheses/paid-longtail.md. NOTE: X has no famous practitioner layer — evidence is operator/agency content, confidence T3; treat all numbers as directional.

- **X's strongest B2B application is retargeting, not prospecting** (Directive — FRAMEWORK, T2): sequence familiarity (video/image, upper funnel) → retargeting with conversion objective (demos, gated content).
- **Prospecting must feed the retargeting layer; a retargeting campaign without replenishment loses efficiency fast** (Directive — HEURISTIC, T2).
- **Self-serve practical floor is ~$20-50/day** for Promoted Posts; below that delivery is patchy (Coinis — HEURISTIC, T3). Trend/Timeline takeovers are 5-6-figure daily minimums, managed service.
- **Vertical fit**: B2B SaaS, crypto, finance, live events still perform; mass-market ecommerce performs better on Meta/TikTok (Coinis — T3).
- **Measure against pipeline, not platform metrics** (Directive — FRAMEWORK, T2).
- **Brand-safety objection is fair but often outdated** — governed adjacency + first-party audiences make X an efficient revenue-influence layer (Directive — OPINION, T2).
- Curiosity/emotional CTAs roughly double CTR on X placements (Affiliate World operator — T3, community intel).

Decision rules:
1. IF B2B AND budget < $50/day THEN use X only as a governed retargeting layer fed by other channels — never prospecting (Directive — HEURISTIC, T2).
2. IF running X for conversions THEN sequence: familiarity campaign first, retargeting campaign second (Directive — FRAMEWORK, T2).
3. IF measuring X THEN use pipeline (SQLs/demos/qualified traffic), never CTR or engagement (Directive — FRAMEWORK, T2).
4. IF mass-market ecommerce THEN skip X; the audience profile isn't there (Coinis — T3).
5. IF considering takeovers THEN require 5-6-figure daily budgets or decline (Coinis — HEURISTIC, T3).
6. IF evaluating the channel on a <$20/day test THEN discard the result — the campaign never delivered (Coinis — HEURISTIC, T3).

## Metrics

- **Pipeline/qualified leads** as primary (Directive — FRAMEWORK, T2).
- **Retargeting-layer efficiency**: cost per demo/lead vs other channels, replenishment ratio.
- **Guardrail**: engagement/CTR metrics are vanity here — do not optimize to them.
- **Timebox**: 30-60 days with real delivery; if delivery is patchy, raise budget or stop (Coinis — T3).

## Sources

1. Directive Consulting, Twitter Ads Manager: B2B Retargeting on X | directiveconsulting.com | tier 2 | 2026-08-15
2. Coinis, X Ads (Twitter Ads) 2026 glossary | coinis.com | tier 3 | 2026-08-15
3. Upgrow, X Ads agency | upgrow.io | tier 3 | 2026-08-15
4. Affiliate World Forums, Twitter monetization case study | affiliateworldforums.com | tier 5 | 2026-08-15

## Evaluation & QA

### Common Failure Modes
- Copy-pasting LinkedIn or Meta creative into the X feed - instant scroll-past
- Targeting only interests while ignoring follower lookalikes - the strongest X signal for tech
- Judging X on last-click conversions alone - undercounts a channel that seeds discovery
- Letting replies run unmoderated, or disabling them - both cost credibility
- Over-layering targeting until nothing delivers
- Measuring impressions alone - cheap reach with no engagement is a vanity win
