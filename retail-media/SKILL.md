---
name: retail-media
category: paid
description: Plan retail media across Amazon DSP, Walmart Connect, and Instacart with first-party data targeting and incrementality-based measurement.
triggers:
  - "retail media"
  - "Amazon DSP"
  - "Walmart Connect"
  - "Instacart Ads"
  - "retail media network"
  - "first-party retail data"
  - "shopper marketing"
inputs:
  - product_context
  - budget
  - retailer_relationships
  - first_party_data_assets
  - measurement_requirements
outputs:
  - network_selection
  - campaign_architecture
  - audience_strategy
  - measurement_plan
  - budget_allocation
related_skills:
  - amazon-ads
  - shopping-feeds
  - marketplace-expansion
  - paid-strategy
  - media-planning
  - performance-reporting
  - programmatic-ctv
  - marketing-optimize/mmm-incrementality
required_context:
  - .context/product-marketing.md
allowed_tools:
  - none
version: 1.0.0
---

## When to Use

Invoke when:
- Evaluating retail media networks for a CPG or consumer brand
- Planning Amazon DSP, Walmart Connect, or Instacart campaigns
- Building targeting from retailer first-party purchase data
- Measuring retail media beyond last-click ROAS
- Negotiating retailer trade budgets that include media

## Workflow

### Step 1: The Retail Media Landscape & Channel Fit
- [ ] Understand the terrain - retailer-owned ad platforms selling both on-site placements and off-site audiences built from purchase data
- **Network types** - marketplaces (Amazon Ads), mass retail (Walmart Connect, Target Roundel), grocery (Instacart, Kroger), specialty (Ulta, Home Depot)
- [ ] Fit check - retail media fits brands whose products are sold at the retailer, especially CPG and consumables where purchase data is the differentiator
- [ ] Why it works - closed-loop measurement (ad view to in-store or online purchase) and first-party purchase audiences; the pitch is deterministic attribution, not reach
- [ ] Set expectations - retail media is expensive per impression but measured on sales lift, not cheap CPMs (heuristic)

**Gate:** Network landscape mapped; channel fit written for your brand.

### Step 2: Network Selection
- [ ] Selection criteria - where the product is actually sold, audience match, data quality, measurement capability, fees and minimums, self-serve maturity
- **Amazon** - the largest; DSP buys both on-Amazon and off-site (Twitch, Fire TV, third-party inventory) with Amazon audiences
- **Walmart Connect** - Walmart.com search and sponsored placements plus off-site; strong omnichannel data story (store plus online)
- **Instacart Ads** - sponsored products in-app plus display; the grocery-trip audience with direct-to-cart mechanics
- [ ] Start where the shopper is - one network done well beats three done thinly (heuristic - minimums and learning curves are real)
- [ ] Check fee transparency - platform fees and managed-service layers erode working media on small budgets (heuristic - model before committing)

**Gate:** 1-2 networks selected with fee and minimum reality check.

### Step 3: Campaign Architecture & Formats
- [ ] On-site sponsored placements - search and browse placements inside the retailer's app or site; the performance layer (closest analogue to classic retail search ads)
- [ ] Off-site programmatic - the retailer's audiences applied to display, video, and CTV off-platform; the brand layer
- [ ] Structure - separate on-site performance and off-site brand campaigns; different objectives, different measurement
- [ ] Tie to availability - never drive demand for out-of-stock SKUs; retail media amplifies supply problems
- [ ] Coordinate with the trade team - shopper marketing, promo calendars, and in-store merchandising should align with paid flights

**Gate:** On-site/off-site split defined per objective; availability check process in place.

### Step 4: First-Party Data Targeting
- [ ] Retailer audience segments - category buyers, lapsed buyers, brand switchers, basket affinities, loyalty-tier segments
- [ ] Lapsed and competitive conquest - the highest-value retail media audiences (heuristic - winning back your own lapsed buyers usually beats cold prospecting)
- [ ] Your own first-party data - onboard CRM lists into the network where supported, for retargeting and suppression
- [ ] Suppress current buyers where the goal is acquisition - or target them for replenishment and upsell instead
- [ ] Data caveats - segments are retailer-defined and refreshed on their schedule; ask how segments are built before trusting them
- [ ] Cookieless resilience - purchase-based audiences are the durable alternative to third-party cookies

**Gate:** Audience map per campaign with segment definitions and sourcing verified.

### Step 5: Measurement & Incrementality
- [ ] Platform ROAS - deterministic on-site (ad-attributed purchases); useful but overstates by ignoring baseline sales (heuristic - treat as directional)
- [ ] Retail sales lift - compare exposed vs control groups; the retail media gold standard
- [ ] Incrementality tests - holdout-based tests that isolate true lift from what would have sold anyway
- [ ] New-to-brand rate - how much spend reaches genuinely new buyers; key for CPG
- [ ] Halo metrics - impact on total category share and in-store sales, not just the advertised SKU
- [ ] Coordinate with MMM - retail media belongs in the marketing mix model alongside everything else (see marketing-optimize/mmm-incrementality)
- [ ] Agree the read before launch - platform dashboards and finance's read must be the same read

**Gate:** Measurement plan includes an incrementality or lift component, not dashboard ROAS alone.

### Step 6: Budgeting, Bidding & Trade
- [ ] Budget sources - retail media often pulls from trade marketing budgets, not just digital; align internally first
- [ ] Minimums and flight pacing - networks carry minimums; continuous flighting beats bursty dips for retail data learning (heuristic)
- [ ] Bid strategy - start with the platform's target-ROAS or max-bid options; shift to manual once conversion data accumulates
- [ ] Seasonal alignment - retail media flexes with category seasonality and retailer promo events
- [ ] Trade negotiation - joint business planning with the retailer can unlock media credits, placement priority, and better data access

**Gate:** Budget source agreed; flight plan aligned to the trade calendar.

### Step 7: Reporting & Optimization
- [ ] Report on - platform ROAS, incrementality readouts, new-to-brand, sales lift, category share
- [ ] Optimize cadence - on-site weekly (bids, placements, search terms); off-site monthly (audiences, creative, frequency)
- [ ] Creative for retail media - retail-native creative (price, offer, product clarity) differs from brand creative
- [ ] Watch cannibalization - on-site sponsored ads on your own branded terms may just tax organic sales; test the difference
- [ ] Quarterly review - rebalance networks, refresh audiences, renegotiate commitments

**Gate:** Reporting structure mirrors the agreed measurement read; optimization cadence scheduled.

## Evaluation & QA

### Common Failure Modes
- Judging retail media on platform ROAS alone - baseline sales inflate the read
- Running off-site brand campaigns with on-site performance expectations
- Advertising out-of-stock SKUs - paid demand for product that cannot be bought
- Ignoring the trade team - retail media lives inside retailer relationships
- Buying audiences without asking how segments are built and refreshed
- Treating all networks as interchangeable - each has different data, fees, and formats
- No incrementality or holdout design - the entire measurement story is missing
