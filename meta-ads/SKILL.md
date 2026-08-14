---
name: meta-ads
category: paid
description: Set up, structure, and optimize Meta (Facebook/Instagram) ad campaigns from scratch.
triggers:
  - "Meta ads"
  - "Facebook ads"
  - "Instagram ads"
  - "run ads on Facebook"
  - "Meta campaign"
inputs:
  - product_context
  - icp
  - budget
  - creative_assets
  - landing_page_url
outputs:
  - campaign_structure
  - audience_setup
  - ad_specs
  - optimization_plan
related_skills:
  - paid-strategy
  - marketing-paid/ad-creative-generator
  - marketing-optimize/landing-page-optimization
  - marketing-optimize/analytics-setup
required_context:
  - .context/product-marketing.md
allowed_tools:
  - mcp:meta-ads
version: 1.0.0
---

## When to Use

Invoke when:
- Setting up first Meta ad campaigns
- Restructuring underperforming Meta account
- Launching a new product/offer on Meta
- Scaling Meta ads to new audiences
- Auditing existing Meta campaigns

## Workflow

### Step 1: Pixel & Tracking Setup
Before running any ads:
- [ ] Meta Pixel installed and firing on all pages
- [ ] Conversions API (CAPI) configured for server-side tracking
- [ ] Standard events configured (ViewContent, AddToCart, Purchase, Lead, etc.)
- [ ] Custom conversions for specific goals if needed
- [ ] Domain verification complete
- [ ] Aggregated Event Measurement priority set (iOS tracking)
- [ ] UTM parameters standardized

**Gate:** Pixel firing correctly, key events tracked, attribution window set.

### Step 2: Campaign Structure
Set up campaigns following best practices:

**For lead gen/SaaS:**
`
Campaign 1: Prospecting (Conversions/Leads objective)
  Ad Set 1: Lookalike 1% of customers
  Ad Set 2: Lookalike 1% of high-value actions
  Ad Set 3: Interest stack (3-5 interests)
  Ad Set 4: Broad/Advantage+ (let Meta optimize)

Campaign 2: Retargeting (Conversions objective)
  Ad Set 1: Website visitors 1-7 days (hot)
  Ad Set 2: Website visitors 8-30 days (warm)
  Ad Set 3: Video viewers 75%+ / Engaged
  Ad Set 4: Email list / abandoned signups
`

**For DTC/ecommerce:**
`
Campaign 1: Advantage+ Shopping Campaign (ASC)
  (Let Meta handle audience, focus on creative)

Campaign 2: Prospecting Manual
  Ad Set 1: Lookalike 1% purchasers
  Ad Set 2: Interest-based audiences

Campaign 3: Retargeting
  Ad Set 1: Viewed product, didn't buy (1-7d)
  Ad Set 2: Added to cart, didn't buy (1-14d)
  Ad Set 3: Past purchasers (upsell/cross-sell)
`

**Gate:** Campaign structure matches business model with clear audience segmentation.

### Step 3: Audience Setup
Build audiences in layers:

**Custom Audiences (retargeting):**
- Website visitors (1d, 7d, 14d, 30d, 90d, 180d)
- Specific page visitors (pricing, product, checkout)
- Email/CRM lists (customers, leads, high-value)
- Video viewers (25%, 50%, 75%, 95%)
- Social engagers (page, profile, ad interactions)

**Lookalike Audiences (prospecting):**
- 1% of purchasers/customers (highest quality)
- 1% of high-value customers (LTV-optimized)
- 1% of leads/signups
- 1-3% expansion for scale

**Interest/Behavioral (prospecting):**
- Stack 3-5 related interests per ad set
- Combine with demographic/behavioral filters
- Use Advantage+ for broader reach

**Gate:** Audience pyramid built from narrow/hot to broad/cold.

### Step 4: Creative Strategy
Plan creative following Meta best practices:
- 3-5 ad variants per ad set minimum
- Mix formats: static images, video (15-30s), carousel, UGC
- Test angles: pain-focused, benefit-focused, social proof, curiosity
- Creative refresh every 2-4 weeks or when frequency > 3

Ad structure per creative:
- Primary text (125 chars above fold, 3 variants)
- Headline (40 chars, clear value or CTA)
- Description (optional, social proof or urgency)
- CTA button (most relevant: Learn More, Sign Up, Shop Now)
- Media (1080x1080 for feed, 1080x1920 for stories/reels)

**Gate:** 4+ creative variants planned across formats and angles.

### Step 5: Optimization Cadence
Daily/weekly optimization routine:

**Daily (5 min):**
- Check for disapproved ads or account issues
- Monitor spend pacing

**Every 3 days:**
- Review ad-level metrics (CTR, CPC, CPM)
- Pause underperforming creatives (<50% of avg CTR after 2x target CPA spend)

**Weekly:**
- Review campaign-level CAC/ROAS
- Shift budget (winners get more, losers get less)
- Check frequency (>3 = audience fatigue)
- Review audience performance

**Bi-weekly:**
- Launch new creative variants
- Test new audiences
- Review funnel metrics (landing page → conversion)

**Gate:** Optimization schedule defined with specific decision triggers.

## Practitioner Grounding & Decision Rules

Built from Jon Loomer (Meta ads deep practice), Nick Shackelford (creative-led structure), Dara Denney (creative fatigue), Ezra Firestone (DTC Meta). Full research: practitioner-intelligence/syntheses/paid-strategy.md.

- **Creative iteration velocity > targeting optimization** (Shackelford/Denney — HEURISTIC, T1): in the 2020s Meta, account structure and audiences matter less than creative supply; the account that feeds the algorithm more distinct creatives wins.
- **Fatigue is the silent killer** (Denney — EMPIRICAL, T1): frequency creep + same-creative saturation degrade results before CPA alarms fire; refresh on fatigue signals, not dates alone.
- **Platform ROAS is over-credited** (Seufert/AdMaxxer — EMPIRICAL, T1): Meta-reported ROAS includes overlap and last-click bias — validate with MER/iROAS before budget decisions (see performance-reporting).

Decision rules:
1. IF creative volume is low (1-3 per ad set) THEN add creative supply before touching targeting — creative is the highest-leverage variable (Shackelford — HEURISTIC, T1).
2. IF frequency exceeds ~2-3/week on a creative THEN prepare refresh — fatigue precedes CPA degradation (Denney — EMPIRICAL, T1).
3. IF scaling THEN increase budgets 20-30% steps, never more — algorithm shock resets learning (existing + Shackelford — HEURISTIC, T1).
4. IF a campaign wins on platform ROAS BUT MER is flat THEN treat the win as attribution shift, not growth (Seufert — EMPIRICAL, T1).
5. IF launching new structure THEN keep the test simple: one variable per ad set (audience vs creative vs placement), never all three (Loomer — FRAMEWORK, T1).

## Metrics

- **Creative supply rate** (new distinct creatives per ad set per week) (Shackelford — HEURISTIC, T1).
- **Frequency + fatigue signals** per creative (Denney — EMPIRICAL, T1).
- **MER / iROAS** as the truth layer alongside platform ROAS (Seufert — EMPIRICAL, T1).

## Sources

1. Jon Loomer, Meta ads deep practice | jonloomer.com | tier 1 | 2026-08-15
2. Nick Shackelford, creative-led account structure | Structured Agency | tier 2 | 2026-08-15
3. Dara Denney, creative fatigue + testing cadence | her podcast/essays | tier 1 | 2026-08-15
4. Eric Seufert, attribution/incrementality | mobiledevmemo.com | tier 1 | 2026-08-15
5. AdMaxxer, MER vs ROAS | admaxxer.com | tier 3 | 2026-08-15

## Evaluation & QA

### Common Failure Modes
- No Conversions API (losing 20-30% of data to iOS privacy)
- Too many ad sets splitting budget (consolidate for better learning)
- Judging creative too early (need 50+ conversions per ad set for learning)
- Not refreshing creative (fatigue is the #1 performance killer)
- Broad targeting without strong creative (creative IS the targeting)
- Optimizing for clicks instead of conversions