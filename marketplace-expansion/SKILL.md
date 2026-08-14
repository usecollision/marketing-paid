---
name: marketplace-expansion
category: ecommerce
description: Expand DTC brands beyond Shopify across Amazon, Walmart, eBay, Etsy, and Flipkart with per-marketplace listings, fulfillment, and fee economics.
triggers:
  - "marketplace expansion"
  - "sell on Amazon"
  - "Walmart marketplace"
  - "eBay or Etsy selling"
  - "Flipkart India"
  - "FBA vs FBM"
  - "multi-marketplace strategy"
inputs:
  - product_catalog
  - margin_data
  - current_channel_mix
  - target_geographies
  - fulfillment_capacity
outputs:
  - marketplace_prioritization
  - fee_model_per_marketplace
  - listing_optimization_plan
  - fulfillment_strategy
  - pricing_and_catalog_plan
related_skills:
  - amazon-ads
  - shopify-marketing-audit
  - shopping-feeds
  - retail-media
  - paid-strategy
  - performance-reporting
  - marketing-intelligence/market-sizing
  - marketing-intelligence/pricing-intelligence
  - marketing-intelligence/competitor-battlecards
required_context:
  - .context/product-marketing.md
allowed_tools:
  - none
version: 1.0.0
---

## When to Use

Invoke when:
- Evaluating which marketplaces to add beyond a Shopify store
- Modeling whether Amazon, Walmart, eBay, Etsy, or Flipkart economics work
- Choosing between FBA, merchant-fulfilled, and 3PL
- Building per-marketplace listing strategies
- Planning a multi-marketplace expansion roadmap

## Workflow

### Step 1: Marketplace Selection Criteria
Score each marketplace on:
- [ ] Audience fit - Amazon is intent-rich generalist; Etsy is handmade/vintage/creative; eBay skews deal-seekers and secondhand; Walmart is price-sensitive mass retail; Flipkart is Indian mass market
- [ ] Category fit - some categories are dominated, gated, or restricted per marketplace
- [ ] Competitive intensity - count competing listings, review depth, and price compression
- [ ] Fee economics - model referral fees plus fulfillment costs against margin (Step 2)
- [ ] Operational load - catalog, support, returns, and tax obligations per marketplace
- [ ] Brand control - marketplaces trade brand control for demand access; decide what you give up
- Prioritize 1-2 new marketplaces at a time - each one is a full operational commitment (heuristic)

**Gate:** Scorecard completed; 1-2 marketplaces selected with written rationale.

### Step 2: Fee Economics Model
- [ ] Model per marketplace - referral or commission rate by category, fulfillment fees, subscription fees, and the ad spend required to be competitive
- [ ] Referral fees vary widely by marketplace and category (heuristic - always pull current fee schedules; never rely on remembered numbers)
- [ ] FBA adds fulfillment, storage, removal, and long-term-storage risk - model the worst case
- [ ] Compute landed margin per SKU per marketplace - price minus COGS, referral, fulfillment, and a realistic ad allocation
- [ ] Kill SKUs that go negative - some products simply do not work on some marketplaces
- [ ] Note price parity rules - marketplaces punish external undercutting; map-pricing awareness is required

**Gate:** Landed margin computed per SKU per marketplace; negative-margin SKUs flagged.

### Step 3: Amazon - Seller Central & FBA
- [ ] Account type - individual vs professional plan; professional is needed for scale
- [ ] FBA vs FBM per SKU - FBA wins the Buy Box and Prime badge, adds fees; FBM protects margin on slow movers
- [ ] Listing requirements - UPC/GTIN or exemption, category approvals, Brand Registry for protection and A+ content
- [ ] Buy Box dynamics - price, fulfillment method, and seller metrics all factor; stabilize the Buy Box before ads
- [ ] Pair with amazon-ads only after listings convert on their own

**Gate:** FBA/FBM decision per SKU; Brand Registry applied where eligible.

### Step 4: Walmart Marketplace
- [ ] Application and onboarding - gated approval; business and tax documentation required
- [ ] Listing setup - item setup by match or template; Walmart's algorithm rewards price competitiveness and fast shipping
- [ ] Fulfillment - Walmart Fulfillment Services (WFS) is the FBA analogue; two-day shipping badges lift conversion (heuristic)
- [ ] Pricing - Walmart's promise is everyday low price; margin expectations differ from Amazon
- [ ] Ads - Walmart Connect once listings mature (see retail-media)

**Gate:** Onboarding checklist complete; WFS vs 3PL decision made per SKU.

### Step 5: eBay
- [ ] Fit check - best for overstock, refurbished, niche parts, and price-comparison shoppers; weak for premium brand-building
- [ ] Listing formats - fixed price (default for DTC) vs auction; promoted listings are the paid lever
- [ ] Seller standards - metrics drive visibility; defect rate and late shipment matter
- [ ] Fees - insertion fees plus final value fees; store subscriptions reduce fees at volume (heuristic - pull the current schedule)
- [ ] Use for channel-clearing inventory and margin recovery, not flagship launches

**Gate:** eBay scoped as clearance/secondary channel with fee math done.

### Step 6: Etsy
- [ ] Fit check - handmade, vintage, craft supplies, and personalized goods; buyers expect a maker story
- [ ] Listing craft - story-first titles and tags, photography that shows craft process, personalization options
- [ ] Fees - listing, transaction, and payment processing fees stack; offsite ads fees apply to attributed sales (verify current terms before committing)
- [ ] SEO - tags and attributes drive Etsy search; the 13-tag discipline matters
- [ ] Seasonality - gift cycles dominate; plan inventory around holidays

**Gate:** Etsy fit validated against product type; tag and story strategy defined.

### Step 7: Flipkart (India)
- [ ] Market context - India's scale play; price sensitivity high; logistics handled by Flipkart's fulfillment network
- [ ] Onboarding - Indian entity, GST registration, brand authorization documents
- [ ] Listing - Hindi/English keywords, region-aware pricing, festival season planning (Diwali is the Q4 equivalent)
- [ ] Fulfillment - Flipkart Fulfillment handles delivery; returns run high (heuristic - plan inventory for it)
- [ ] Ads - Flipkart Ads platform once listings rank

**Gate:** Entity and tax readiness confirmed; festival calendar mapped.

### Step 8: Listing Optimization per Marketplace
- [ ] Titles - Amazon is keyword-dense within limits; Etsy is story-forward; eBay is specification-forward; Walmart mirrors Amazon; Flipkart mirrors Amazon with local keywords
- [ ] Backend keywords and attributes - fill every attribute field; marketplaces index them all
- [ ] Images - 6+ images, infographics, size and context shots; each marketplace has its own specs
- [ ] Reviews - every marketplace ranks and converts on review depth; seed reviews through compliant programs
- [ ] Pricing strategy per marketplace - avoid cross-marketplace price wars with yourself (map and parity rules)
- [ ] Catalog sync - one source of truth for SKU data; push per-marketplace transforms, never hand-edit in five places

**Gate:** Per-marketplace listing templates built from one source of truth.

### Step 9: Operations & Governance
- [ ] Inventory allocation - ring-fence stock per marketplace to avoid oversell
- [ ] Returns and support SLAs per marketplace - they differ, and violations cost visibility
- [ ] Tax and compliance - nexus, VAT/GST, and marketplace-collected vs seller-collected regimes
- [ ] Review cadence - monthly per-marketplace P&L, quarterly channel-mix review
- [ ] Offboarding criteria - define when a marketplace gets cut before you enter

**Gate:** Monthly P&L cadence and exit criteria documented.

## Evaluation & QA

### Common Failure Modes
- Copying the Shopify catalog into five marketplaces without per-marketplace listing work
- Ignoring fee models - negative landed margin discovered after scaling
- Treating marketplaces as free demand - ad costs and Buy Box dynamics eat margin
- FBA everything - storage fees on slow movers erase the margin FBA was meant to protect
- No inventory ring-fencing - overselling across channels
- Chasing every marketplace at once - operational load kills the core store
- Ignoring marketplace-specific review economics - launching without a review plan
