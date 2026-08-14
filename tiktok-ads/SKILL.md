---
name: tiktok-ads
category: paid
description: Launch and scale TikTok Ads with a creative-first system for ecommerce and consumer brands.
triggers:
  - "TikTok ads"
  - "Spark Ads"
  - "TikTok Shop ads"
  - "TikTok campaign setup"
  - "TikTok ad creative"
inputs:
  - product_context
  - icp
  - budget
  - creative_assets
  - shop_setup
outputs:
  - campaign_structure
  - creative_plan
  - bidding_strategy
  - shop_ads_plan
  - testing_plan
related_skills:
  - paid-strategy
  - ad-creative-generator
  - hook-frameworks
  - creative-testing
  - media-planning
  - shopify-marketing-audit
  - marketing-messaging/video-scripts
required_context:
  - .context/product-marketing.md
allowed_tools:
  - none
version: 1.0.0
---

## When to Use

Invoke when:
- Launching TikTok ads for DTC/ecommerce
- Setting up TikTok Shop ads
- Driving consumer app installs
- Scaling beyond Meta/Google into a new audience
- Creative performance declining and needing a refresh system

## Workflow

### Step 1: Foundations - Pixel, Events, Shop
- [ ] TikTok Pixel installed and firing
- [ ] Events API configured for server-side signals (mobile privacy makes this mandatory, not optional)
- [ ] Complete event mapping - ViewContent, AddToCart, InitiateCheckout, CompletePayment
- [ ] TikTok Shop connected if selling natively (catalog sync)
- [ ] UTM parameters standardized to match other channels

**Gate:** Events verified in TikTok Events Manager; Shop catalog synced.

### Step 2: Creative-First System
TikTok is a creative marketplace - the asset matters more than targeting:
- Native-first - UGC-style, phone-shot, lo-fi beats studio polish
- Hook in the first 1-2 seconds - pattern interrupt, open loop, or bold claim
- Formats - 15-30s native video, Spark Ads (boost organic posts from your account or creators), carousels for stills
- Spark Ads - organic posts keep comments and social proof; whitelist creators for authentic voices
- Volume expectation - TikTok demands a high creative velocity (heuristic - plan 10+ new creatives per month at scale; validate per account)
- Organic wins - promote what performs organically; the loop runs both directions

**Gate:** Creative pipeline defined with velocity target and native-style specs.

### Step 3: Campaign Structure
- **Smart+ campaigns** (Smart+ Shopping for ecommerce) - broad targeting, TikTok optimizes; the default for scale
- **Manual campaigns** - when you need control over audience, budget, or placement split
- Ad group = audience + budget; keep one audience per ad group
- Structure: `[Objective]-[Product/Theme]-[Audience]`
- Separate retargeting (engaged viewers, site visitors) from prospecting

**Gate:** Campaign map separates prospecting from retargeting with clear objectives.

### Step 4: Targeting
- **Broad-first** - TikTok's strength is its algorithm; start with broad/auto targeting
- Interest targeting - only to seed learning when you need a narrower start
- Custom audiences - site visitors, engagers, app users for retargeting
- Lookalikes of purchasers once conversion volume exists
- Age gating when the product requires it (never as a lazy default)

**Gate:** Targeting plan documented - default broad with explicit exceptions.

### Step 5: Bidding & Optimization
- Lowest cost to learn; cost cap to control CPA; target CPA once stable
- Value-Based Optimization (VBO) for ecommerce once purchase volume supports it
- Budget heuristics - per-ad-group budget high enough to exit the learning phase (rough guide - aim for enough budget for 20+ conversions in the learning window; validate per account)
- Don't touch budgets mid-learning-phase; let the campaign exit learning before judging
- Expect CPA volatility in the first days of any new campaign

**Gate:** Bidding ladder defined per campaign stage with learning-phase rules.

### Step 6: TikTok Shop Commerce
- **Product Shopping Ads** - catalog-driven from Shop listings
- **LIVE shopping ads** - amplify live streams to viewers
- **Affiliate creators** - commission-based video generation; the cheapest way to scale creative supply (heuristic - validate commission rates per category)
- **Video Shopping Ads with creators** - third-party endorsement in native format
- Shop ads require clean product listings - fix listings before scaling spend

**Gate:** Shop ad type chosen per product with listing quality checked.

### Step 7: Funnel Role & Cross-Platform Synergy
- TikTok is usually top-of-funnel - attribute accordingly (view-through, assisted conversions)
- Feed TikTok engagers into Meta/Google retargeting pools
- Expect lower in-platform ROAS; measure contribution at the blended level (see performance-reporting)
- Branded search lift is a leading indicator of TikTok's halo effect
- TikTok Shop orders don't replace DTC - track them as a separate revenue line

**Gate:** TikTok's funnel role stated, cross-platform handoff configured.

### Step 8: Creative Testing & Refresh Cadence
- Fast fatigue - TikTok creative decays faster than Meta (heuristic - calibrate with your own frequency and CPA-creep data)
- Weekly creative reviews; kill underperformers at pre-registered thresholds (see creative-testing)
- Iterate winners - remix the hook, swap the creator, change the opening scene
- Maintain the pipeline - brief, shoot, iterate on a calendar, never ad hoc
- Watch comments on Spark Ads - engagement signals boost delivery and reveal objections

**Gate:** Refresh cadence scheduled; kill/iterate rules pre-registered.

## Practitioner Grounding & Decision Rules

Built from Dara Denney, Chase Chappell, Nik Sharma (TikTok/DTC practice). Full research: practitioner-intelligence/syntheses/paid-strategy.md.

- **TikTok is creative-supply-constrained** (Denney/Chappell — HEURISTIC, T1): you need volume of distinct creatives (Spark/UGC native), not iteration on one.
- **Native beats polished** (Chappell — EMPIRICAL, T1): creator-native formats (Spark Ads, UGC) outperform studio polish for most DTC offers; the feed punishes ad-ness.

Decision rules:
1. IF creative supply is <5 distinct native-style creatives per test cell THEN add supply before judging (Denney/Chappell — HEURISTIC, T1).
2. IF using studio/static creative THEN test Spark/UGC variants — native wins most offers (Chappell — EMPIRICAL, T1).
3. IF frequency rises toward ~2-3/week THEN rotate — fatigue on TikTok is faster than Meta (Denney — EMPIRICAL, T1).
4. IF measuring TikTok results THEN use MER/contribution, not platform-reported ROAS alone (Seufert — EMPIRICAL, T1).

## Metrics

- **Creative supply + native share** per campaign (Chappell — HEURISTIC, T1).
- **Fatigue signals** (frequency, CTR decay) (Denney — EMPIRICAL, T1).
- **MER/contribution** as the truth layer (Seufert — EMPIRICAL, T1).

## Sources

1. Dara Denney, TikTok creative practice | her podcast/essays | tier 1 | 2026-08-15
2. Chase Chappell, TikTok ads + UGC | his essays | tier 2 | 2026-08-15
3. Eric Seufert, attribution | mobiledevmemo.com | tier 1 | 2026-08-15

## Evaluation & QA

### Common Failure Modes
- Repurposing polished Meta ads without native hooks
- Judging TikTok on last-click ROAS alone - undercounts top-of-funnel contribution
- Too few creatives - one winner is not a strategy
- Over-targeting - fighting the algorithm with narrow audiences
- Budget too low to exit learning - constant churn, no data ever accumulates
- Ignoring comments on Spark Ads - the community response is the feedback loop
