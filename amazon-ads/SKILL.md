---
name: amazon-ads
category: paid
description: Structure and optimize Amazon Ads for marketplace growth - Sponsored Products, Brands, Display, and DSP.
triggers:
  - "Amazon ads"
  - "Sponsored Products"
  - "Sponsored Brands"
  - "Amazon PPC"
  - "ACoS optimization"
  - "Amazon advertising strategy"
inputs:
  - product_context
  - asin_list
  - margin_data
  - existing_campaign_export
  - listing_data
outputs:
  - campaign_architecture
  - keyword_harvesting_plan
  - acos_targets
  - listing_fix_list
  - dsp_assessment
related_skills:
  - paid-strategy
  - media-planning
  - performance-reporting
  - marketing-channels/keyword-research
  - marketing-intelligence/review-mining
  - marketing-optimize/cro-audit
  - shopify-marketing-audit
required_context:
  - .context/product-marketing.md
allowed_tools:
  - none
version: 1.0.0
---

## When to Use

Invoke when:
- Launching Amazon PPC for a product or catalog
- ACoS is rising and margin is shrinking
- Harvesting keywords from auto campaigns
- Scaling from Sponsored Products into Brands/Display/DSP
- Diagnosing why organic rank isn't following ad spend

## Workflow

### Step 1: Listing Readiness First
Ads amplify a listing - they cannot fix a weak one:
- [ ] Title, bullets, and A+ content optimized for main keywords
- [ ] High-quality main image (the click driver), 6+ images, video
- [ ] Review count at category parity (heuristic - match the top competitors' review depth before scaling spend)
- [ ] Price competitive; margins calculated per ASIN
- [ ] Buy Box ownership stable
If the listing doesn't convert organically, ad traffic just burns budget faster.

**Gate:** Listing meets category parity bar before scaling spend.

### Step 2: Campaign Architecture
Layer campaigns by objective:
- **Auto campaigns** - discovery, harvesting, rank seeding (one per ASIN or product theme)
- **Manual exact** - proven terms, scale spend where it works
- **Manual phrase/broad** - expansion at lower bids
- **Sponsored Brands** - brand defense plus category presence
- **Sponsored Display** - product targeting (competitor pages) plus retargeting
- Segment ASINs by margin tier - high-margin ASINs get more aggressive targets
- Naming convention: `[Type]-[ASIN/Theme]-[Targeting]-[Goal]`

**Gate:** Campaign map covers auto, manual, brand, and display layers per margin tier.

### Step 3: Keyword Harvesting Loop
The compounding engine of Amazon PPC:
1. Run auto + broad campaigns
2. Weekly - pull the Search Term Report
3. Terms with sales - promote to exact match in a manual campaign
4. Terms with clicks but no sales (past a threshold) - negate
5. Terms with high impressions but no clicks - negate (relevance waste)
6. Repeat weekly - this is the durable advantage
- Include ASIN targeting terms - competitor ASINs where you win the comparison
- Never harvest a term you haven't seen convert in the report

**Gate:** Harvesting loop scheduled weekly with promote/negate rules written down.

### Step 4: ACoS & TACoS Math
- **Break-even ACoS = margin %** (pre-ad contribution) - spending at break-even only makes sense if you're buying rank
- **Stage-based targets** (framework - set numbers from your own margin data):
  - Launch - at or above break-even (buy rank and reviews)
  - Growth - break-even minus a buffer
  - Harvest - well below break-even
- **TACoS** (total ad spend / total sales) is the north star - falling TACoS means ads are driving organic share, not just buying sales
- One target per ASIN stage, not one account-wide ACoS

**Gate:** Break-even ACoS computed per ASIN; stage-based targets assigned.

### Step 5: Bidding & Placements
- Start bids at the suggested range; adjust weekly (Amazon applies changes fast - no long learning phase like Meta)
- Placement modifiers - Top of Search multiplier for proven exact terms (brand defense and main keywords)
- Product page placements - often cheaper, lower competition, good for harvesting
- Bid by device only where data volume justifies it
- Dayparting only when the data clearly shows a pattern (rarely worth it early)

**Gate:** Bid baseline set with placement modifiers on proven terms only.

### Step 6: Sponsored Brands & Display
- **Sponsored Brands** - headline + 3 ASINs; defend your own brand terms, target category terms with a store spotlight
- **Sponsored Brands Video** - high CTR format (heuristic - validate in your category), test early
- **Sponsored Display offensive** - product targeting on competitor and adjacent detail pages
- **Sponsored Display defensive** - retarget your own viewers; appear on your own pages when competitors do
- Use brand campaigns as defense first - don't let competitors own your brand terms

**Gate:** Brand defense live; offensive product targeting mapped to competitor ASINs.

### Step 7: Listing Synergy & Organic Flywheel
- Ads on a keyword drive sales on that keyword; sales improve rank; rank grows organic share; TACoS falls
- Prioritize ad spend on keywords where you rank roughly 8-20 organically - ads can tip you onto page one
- Monitor organic vs paid share monthly; if organic share isn't growing, listing conversion is the issue, not ads
- Feed ad insights back into the listing - converting search terms belong in title/bullets

**Gate:** Monthly organic-share review scheduled; ad insights feeding listing updates.

### Step 8: DSP & Upper-Funnel Assessment
- DSP is awareness-scale display, video, and audio - minimum budgets are high (heuristic - typically meaningful only at larger monthly spend; validate against your category)
- Consider when - mature catalog, ACoS targets met, need brand halo or defense, New-to-Brand growth priority
- DSP audiences - in-market, lifestyle, remarketing, competitor viewers
- Measure DSP on - New-to-Brand metrics, branded search lift, assisted conversions; never direct ROAS
- DSP is a brand investment with marketplace-specific KPIs, not a second PPC tool

**Gate:** Written go/no-go on DSP with budget threshold and KPIs defined.

## Evaluation & QA

### Common Failure Modes
- Optimizing every keyword to the same ACoS regardless of margin or stage
- Harvesting without negatives - the same junk terms keep draining
- Ignoring TACoS - cutting ads that quietly drive organic rank
- Auto campaigns left on aggressive defaults without category logic
- Expecting DSP to deliver direct ROAS
- Scaling spend before listing conversion rate is proven
