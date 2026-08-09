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
  - marketing-ad-creative/ad-creative-generator
  - marketing-cro/landing-page-optimization
  - marketing-analytics/analytics-setup
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

## Evaluation & QA

### Common Failure Modes
- No Conversions API (losing 20-30% of data to iOS privacy)
- Too many ad sets splitting budget (consolidate for better learning)
- Judging creative too early (need 50+ conversions per ad set for learning)
- Not refreshing creative (fatigue is the #1 performance killer)
- Broad targeting without strong creative (creative IS the targeting)
- Optimizing for clicks instead of conversions