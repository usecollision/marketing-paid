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

## Practitioner Grounding

- **Marketplace Pulse** (Juozas Kaziukenas / Ben Donovan, 2025-2026 data): the "Great Compression" — 165k new Amazon sellers in 2025 (−44% YoY), Amazon now ~60% services/40% retail, advertising "evolved from optional to unavoidable", fees + tariffs squeeze margins, GMV concentrating among capitalized survivors; Walmart marketplace grew ~50% in one quarter (2026) (EMPIRICAL, T1).
- **Chris McCabe** (ecommerceChris, ex-Amazon Seller Performance): account health is an operational asset — policy violations (review inserts, third-party actions) suspend accounts with funds frozen; audit every customer-facing touchpoint before scaling (EMPIRICAL, T2).
- **Feedvisor 2022 brand survey** (n=1,000+, Zogby): e-marketplaces = top-priority selling channel for brands; self-reported 7x Amazon ad ROAS (vendor-commissioned, directional) (T3).
- **Community field intel** (r/FulfillmentByAmazon 143k members, r/AmazonSeller): dominant themes are advice requests and pain/anger (suspensions, reviews, PPC costs); thin listings can win temporarily on price but die without review depth (T3).
- **Existing marketplace-expansion skill** validated: per-marketplace landed-margin math, 1-2 marketplaces at a time, FBA/FBM per SKU, price-parity rules, offboarding criteria.

## Decision Rules

- IF per-SKU landed margin (price − COGS − referral − fulfillment − realistic ad allocation) is negative on a marketplace THEN kill that SKU there before entry, not after scaling (existing skill; HEURISTIC; T1)
- IF the business lacks capital reserves to absorb fee increases, tariffs, or margin compression THEN treat marketplace entry as a capital decision, not a channel test (Marketplace Pulse; EMPIRICAL; T1)
- IF already operating 2+ marketplaces without monthly per-marketplace P&L THEN fix operations before adding more (existing skill; HEURISTIC; T1)
- IF packaging or customer communications include review-request inserts THEN remove them or document control before launch (McCabe/SellerSprite; EMPIRICAL; T2)
- IF entering Walmart THEN price competitiveness and fast shipping (WFS or two-day) are prerequisites for visibility, and Walmart Connect ads come only after listings mature (existing skill; Eva Commerce; HEURISTIC; T2)
- IF a marketplace shows no path to break-even within ~2 quarters of realistic ad allocation THEN cut it (existing skill offboarding rule; HEURISTIC; T2)
- IF the category is gated/restricted or review depth cannot reach parity THEN deprioritize that marketplace (existing skill; HEURISTIC; T2)
- IF expansion target is international (e.g., Flipkart/India) THEN entity/tax readiness (GST, brand authorization) gates everything else (existing skill; FACT; T1)

## Metrics

- **Primary**: landed margin % per SKU per marketplace (computed pre-entry, re-measured monthly) (existing skill; T1)
- **Guardrails**: per-marketplace P&L (monthly), channel-mix share vs core store, review depth vs category parity, account health (seller metrics/ODR), ad allocation % of revenue (10-20% benchmark, Keywords.am)
- **Cadence**: monthly per-marketplace P&L; quarterly channel-mix review vs the 1-2-marketplace commitment rule; annual re-entry decision for markets previously cut
- **Stop-and-remeasure**: after fee-schedule changes or tariff shifts, re-run the landed-margin model before reallocating inventory (Marketplace Pulse data shows these hit without warning)

## Sources

1. Marketplace Pulse — Amazon New Seller Numbers Hit Decade Low in 2025 (Great Compression, 165k sellers, 60/40 services/retail) | marketplacepulse.com/articles/amazon-seller-registrations-hit-decade-low-in-2025 | T1 | 2026-08-15
2. Marketplace Pulse — Walmart Marketplace Growth Reaches Fastest Pace in Years (2026) | marketplacepulse.com | T1 | 2026-08-15
3. McCabe — ecommerceChris bio + AM/PM Podcast #379 (compliance, suspensions, appeals) | ecommercechris.com; ampmpodcast.com | T1/T2 | 2026-08-15
4. SellerSprite — Amazon Review Manipulation Suspensions 2026 (insert/velocity cases, $28k frozen funds) | sellersprite.com | T3 | 2026-08-15
5. Feedvisor — Brands Report Seven Times Return from Amazon Advertising (2022 survey) | businesswire.com | T3 | 2026-08-15
6. Keywords.am — TACoS sizing and budget benchmarks (10-20% of revenue) | keywords.am/blog/amazon-advertising-budget | T2 | 2026-08-15
7. Eva Commerce — How to Sell on Walmart Marketplace (2025 guide) + Walmart Connect guide | eva.guru | T3 | 2026-08-15
8. r/FulfillmentByAmazon community analysis (143k members; themes: suspensions, reviews, PPC costs) | gummysearch.com/r/FulfillmentByAmazon; thehiveindex.com | T3 | 2026-08-15
9. Synthesis: practitioner-intelligence/syntheses/amazon.md + retail-media.md | T1-T3 | 2026-08-15

## Evaluation & QA

### Common Failure Modes
- Copying the Shopify catalog into five marketplaces without per-marketplace listing work
- Ignoring fee models - negative landed margin discovered after scaling
- Treating marketplaces as free demand - ad costs and Buy Box dynamics eat margin
- FBA everything - storage fees on slow movers erase the margin FBA was meant to protect
- No inventory ring-fencing - overselling across channels
- Chasing every marketplace at once - operational load kills the core store
- Ignoring marketplace-specific review economics - launching without a review plan
- Entering marketplaces without capital for fee/tariff shocks - the Great Compression punishes undercapitalized entrants (Marketplace Pulse; T1)
- Scaling ads or inventory while account-health violations are unresolved - suspension freezes funds and kills the channel (McCabe; SellerSprite; T2)
- Assuming thin listings can't win - they can, temporarily, on price; without review depth and parity the win evaporates (r/FBA field report; T3)
