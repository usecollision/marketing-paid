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

## Practitioner Grounding

- **Mike Zagare** (PPC Entourage): volume-tier campaign structure (single-keyword campaigns for top terms, 10-15 max per low-volume campaign), exact-match Top-of-Search for rank goals, weekly harvest/negate loop (HEURISTIC, T2).
- **Brent Zahradnik** (AMZ Pathfinder/SellerPlex): stage-appropriate ACoS (a 4-month-old brand at <90% ACoS is launch-acceptable if rank is building), negatives-vs-lower-bid judgment, event-day bid-vs-budget lever decisions (HEURISTIC, T2).
- **Ash Metry / Keywords.am**: lifecycle budget splits — launch 80/15/5 (SP/SB/SD), growth 60/25/15, mature 50/25/15/10-DSP, brand-under-attack 40/35/25; TACoS sizing 10-20% of revenue (HEURISTIC, T2).
- **AMALYZE / SalesDuo**: placement modifiers apply FIRST, dynamic bidding compounds SECOND ($1 bid × 900% ToS × up-and-down ≈ $20); up-and-down only on proven exact terms (EMPIRICAL, T2).
- **pcostudio**: ACoS = campaign metric, TACoS = business metric; ACoS rising + TACoS falling = healthy launch, not a problem (FRAMEWORK, T1).
- **SellerStack / Pattern**: ad-attributed ROAS inflates; NTB and halo (organic-rank lift, cross-SKU) are the missing truth; "when a branded campaign's ROAS looks great, distrust it" (EMPIRICAL, T1).
- **Darkroom Agency**: DSP is an upper-funnel/retargeting layer, premature below ~$50k/month sponsored spend (HEURISTIC, T2).
- **Chris McCabe / SellerSprite**: enforcement risk is operational risk — review velocity flags, packaging inserts, and third-party actions suspend accounts; document proportionality (EMPIRICAL, T2).

## Decision Rules

- IF listing doesn't convert organically at category parity THEN fix listing before scaling ads (Zagare; universal; HEURISTIC; T1)
- IF ad budget < $1.5k/month THEN SP-only, 80%+ of budget, single-keyword campaigns for top 5 high-volume terms (Zagare; Keywords.am; HEURISTIC; T2)
- IF stage = launch THEN ACoS target ≥ break-even, TACoS may run 20%+ and should decline within 8-12 weeks; do NOT cut on ACoS alone (pcostudio; Zahradnik; HEURISTIC; T2)
- IF stage = growth and 100+ reviews and branded search volume exists THEN move to ~60/25/15 split and enable SD retargeting (Keywords.am; HEURISTIC; T2)
- IF competitors bid your brand terms THEN prioritize SB brand defense over ACoS efficiency (Keywords.am; HEURISTIC; T2)
- IF using dynamic up-and-down bidding THEN only on proven exact terms with 30+ days conversion data; else use down-only; compute placement × dynamic compounding before setting modifiers (SalesDuo; AMALYZE; EMPIRICAL; T2)
- IF a branded campaign's ROAS looks excellent THEN distrust it; check NTB% and organic rank movement before scaling (SellerStack; EMPIRICAL; T1)
- IF sponsored spend < ~$50k/month or profitability inconsistent THEN no DSP; revisit at scale with AMC/holdout measurement (Darkroom; HEURISTIC; T2)
- IF review velocity spikes after a launch THEN proactively prepare proportionality documentation (sales data + campaign records) (SellerSprite; McCabe; EMPIRICAL; T2)
- IF TACoS is flat/rising while ACoS is stable THEN organic rank is not following — the listing is the problem, not bids (pcostudio; HEURISTIC; T2)

## Metrics

- **Primary**: TACoS (total ad spend / total sales) — business health; target by stage: launch 20%+ declining after 8-12 weeks, mature < 8-12% (Keywords.am; pcostudio; HEURISTIC; T2)
- **Campaign-level**: ACoS vs per-ASIN break-even ACoS (= contribution margin %); one target per ASIN stage, never account-wide (Zagare; universal; T1)
- **Guardrails**: NTB% on SB/SD (acquisition quality), organic share of sales (monthly), placement report CPC vs modifier expectations (AMALYZE)
- **Cadence**: weekly search-term harvest + bid review; monthly TACoS/organic-share review; quarterly budget-split review vs lifecycle stage (Zagare; Keywords.am)
- **Stop-and-remeasure**: after any bid-strategy switch, judge results only after 14 days; do not change bids during the switch (SalesDuo)

## Sources

1. Zagare — 6 Options for Determining Amazon Ad Campaign Starting Bids | blog.ppcentourage.com | T1 | 2026-08-15
2. Zagare — How to Optimize Amazon PPC (video transcript) | zonguru.com/blog/amazon-ppc-keyword-optimization | T1 | 2026-08-15
3. Zahradnik — QA Selling Online Podcast interviews (2020) | qasellingonline.com | T1 | 2026-08-15
4. Keywords.am — Best Amazon Advertising Budget Split by Stage (2026) | keywords.am/blog/amazon-advertising-budget | T2 | 2026-08-15
5. AMALYZE — Placement Bid Modifiers: cascade effect | amalyze.com/resources/sponsored-success/placement-bid-modifiers | T2 | 2026-08-15
6. SalesDuo — Amazon PPC Bidding Strategies (2026) | salesduo.com/blog/amazon-bidding-strategies-guide | T2 | 2026-08-15
7. pcostudio — Amazon ACoS & TACoS Explained (3 scenarios) | pcostudio.com/en/blog/amazon-acos-tacos | T2 | 2026-08-15
8. SellerStack — Incrementality and the Halo Effect in Amazon Ads | sellerstack.ai/glossary/incrementality | T2 | 2026-08-15
9. Darkroom — What Amazon DSP Actually Does and When Brands Should Use It | darkroomagency.com | T2 | 2026-08-15
10. SellerSprite — Amazon Review Manipulation Suspensions 2026 | sellersprite.com | T3 | 2026-08-15
11. AMZ Pathfinder — case studies (88% NTB, Viter Energy 3.25 ROAS) | amzpathfinder.com | T2 | 2026-08-15
12. Synthesis: practitioner-intelligence/syntheses/amazon.md | T1-T3 | 2026-08-15

## Evaluation & QA

### Common Failure Modes
- Optimizing every keyword to the same ACoS regardless of margin or stage
- Harvesting without negatives - the same junk terms keep draining
- Ignoring TACoS - cutting ads that quietly drive organic rank
- Auto campaigns left on aggressive defaults without category logic
- Expecting DSP to deliver direct ROAS
- Scaling spend before listing conversion rate is proven
- Pausing profitable high-reach keywords to push ACoS down - the campaign looks better while the business shrinks (pcostudio; T2)
- Trusting dynamic up-and-down on unproven campaigns - automation spends into the worst placements (r/FulfillmentByAmazon "127% ACoS" field report; T3)
- Judging launches by ACoS and pulling PPC at week 4-6 before rank forms (Zahradnik; ainfluencer; T2)
- Ignoring placement × dynamic-bidding compounding - surprise effective CPCs erase margin (AMALYZE; T2)
- Review manipulation or review-request inserts - suspension and frozen funds even from manufacturer-added cards (SellerSprite; McCabe; T2)
