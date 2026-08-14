---
name: shopping-feeds
category: paid
description: Build and optimize product feeds for Google Merchant Center with feed schema, health checks, title structure, and supplement feeds for Shopping and PMax.
triggers:
  - "shopping feed"
  - "product feed"
  - "Google Merchant Center"
  - "feed optimization"
  - "PMax feed issues"
  - "product disapprovals"
  - "supplement feed"
inputs:
  - product_catalog_export
  - google_ads_account_context
  - margin_data
  - category_taxonomy
outputs:
  - feed_setup_plan
  - title_optimization_rules
  - merchant_center_health_report
  - supplement_feed_plan
  - feed_optimization_roadmap
related_skills:
  - google-ads
  - retail-media
  - marketplace-expansion
  - amazon-ads
  - performance-reporting
  - marketing-channels/keyword-research
required_context:
  - .context/product-marketing.md
allowed_tools:
  - none
version: 1.0.0
---

## When to Use

Invoke when:
- Setting up Google Merchant Center for the first time
- Diagnosing disapprovals and feed errors
- Optimizing product titles for Shopping and Performance Max
- Building supplement feeds or feed rules
- Improving Shopping campaign performance through feed quality

## Workflow

### Step 1: Feed Strategy & Source of Truth
- [ ] Decide primary feed source - platform export (Shopify, WooCommerce), scheduled fetch, or manual upload
- [ ] One source of truth - the feed mirrors the store; the store is the master
- [ ] Choose fetch method - scheduled fetch from a URL beats manual CSV uploads (heuristic - manually uploaded feeds go stale immediately)
- [ ] Set refresh cadence - daily for active catalogs, more often for price-sensitive inventory
- [ ] Inventory scope - decide which SKUs belong in the feed at all (exclude out-of-stock, non-shippable, restricted)

**Gate:** Primary feed source, method, and cadence decided and documented.

### Step 2: Feed Schema & Required Fields
- [ ] Required attributes - id, title, description, link, image_link, price, availability, condition (plus GTIN/MPN/brand where applicable)
- [ ] GTIN/MPN discipline - identifier mismatches are a top disapproval source; fix at catalog level, not feed level
- [ ] Price and availability must match the landing page exactly - mismatches trigger account-level warnings (heuristic - the most common health issue in Merchant Center)
- [ ] Link validation - every product link lands on a working page showing the same product
- [ ] Image specs - white background, minimum resolution, no watermarks or promo text
- [ ] Additional attributes worth filling - product_type, google_product_category, custom_labels, sale_price windows

**Gate:** Schema complete for all SKUs; zero missing required attributes in diagnostics.

### Step 3: Merchant Center Health & Disapprovals
- [ ] Review Diagnostics weekly - account-level, feed-level, and item-level issues
- [ ] Disapproval triage - policy issues need business fixes; data-quality issues need feed fixes
- [ ] Fix at source, then re-fetch - patching inside Merchant Center leaves the store broken
- [ ] Watch account health - repeated policy violations can suspend the account, and Shopping spend is collateral damage
- [ ] Set up alerts - email notifications for new disapprovals

**Gate:** Zero critical disapprovals; weekly health review scheduled.

### Step 4: Product Title Structure
- [ ] Front-load keywords - the opening characters carry the most weight in matching and CTR (heuristic - Google truncates long titles)
- [ ] Title formula per product type - Brand + Product Type + Key Attributes + Variant (adapt the formula to your category)
- [ ] Include what shoppers actually search - mine search-term and query data for attribute language
- [ ] Mind the character limit (heuristic - Google shows roughly 70-150 characters depending on surface; keep titles under ~150)
- [ ] Remove noise - no promo text, no internal codes, no ALL CAPS
- [ ] Scale with rules - rule-based title generation for large catalogs, hand-tuned titles for hero SKUs

**Gate:** Title formula documented per product type; hero SKUs hand-tuned.

### Step 5: Feed Optimization for Shopping & PMax
- [ ] Custom labels - tag SKUs by margin, season, bestseller, and promo status; use as campaign structure and bid levers
- [ ] product_type taxonomy - build your own consistent taxonomy, not the store's loose tags
- [ ] Image quality - the thumbnail is the ad; test lifestyle vs white-background where the surface allows
- [ ] Description hygiene - the first sentence carries the snippet; keyword-relevant but readable
- [ ] Availability and price competitiveness - Shopping is a price-comparison surface; track competitor price gaps for hero SKUs (heuristic)
- [ ] PMax specifics - the feed plus creative assets power PMax; weak feed data means weak PMax performance; segment by custom labels for reporting

**Gate:** Custom labels and taxonomy live; hero SKU feed attributes audited.

### Step 6: Supplement Feeds & Rules
- [ ] Supplement feeds - overlay data without touching the primary feed - promotions, custom labels, seasonal overrides, localized titles
- [ ] Feed rules - transform primary feed data inside Merchant Center (append brand to titles, remap categories) - use sparingly; rules obscure the source of truth
- [ ] Promotions - sale_price and promotion feeds power badge treatments; keep windows accurate or face mismatches
- [ ] Local inventory feeds - for store-fulfilled channels where relevant
- [ ] Multi-country feeds - currency, language, and availability per target country

**Gate:** Supplement feed architecture defined; rules documented with owners.

### Step 7: Feed Hygiene & Ongoing Ops
- [ ] Weekly - diagnostics review, new-SKU feed status, price/availability spot checks
- [ ] Monthly - title and keyword refresh from search-term data, custom label audit, stale SKU cleanup
- [ ] Quarterly - taxonomy review, image refresh, competitive price-gap analysis
- [ ] Tie feed quality to campaign performance - when Shopping ROAS dips, check the feed before touching bids (heuristic - feed issues masquerade as bid issues)

**Gate:** Hygiene cadence documented; feed-first triage rule adopted in the optimization workflow.

## Evaluation & QA

### Common Failure Modes
- Price or availability mismatch between feed and landing page - silent account-level damage
- Editing feeds in Merchant Center instead of fixing the store - fixes evaporate on the next fetch
- Keyword-stuffed titles that read as spam - CTR and compliance both suffer
- Ignoring GTIN/MPN - a top disapproval cause and an easy catalog-level fix
- No custom labels - PMax and Shopping run blind without margin and promo structure
- Letting rules accumulate - a web of feed rules nobody can untangle
- Treating feed quality as one-time setup - it decays with every catalog change
