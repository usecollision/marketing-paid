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

## Practitioner Grounding

- **AdTribes** (feed tool vendor): diagnostics triage is top-down — account-level → feed-level → item-level; within items: errors (won't show) → warnings (performance suffers) → notifications (informational) (HEURISTIC, T2).
- **Elite Brands** (agency): ~80% of account issues are warnings/limited-performance flags on non-core products; the damage is the ~20% hard disapprovals on revenue SKUs; account-suspension warnings are all-hands emergencies (HEURISTIC, T2).
- **GetFeeder** (feed vendor): technical error taxonomy — malformed XML, units required on shipping_weight ("1.5 kg" not "1.5"), 4GB compressed feed limit, promo language belongs in the promotions feed (FACT, T1).
- **Shoparize** (CSS partner): data-quality issues are the fastest wins — missing attributes/formatting resolve in hours with fast re-approval; set up disapproval notifications (HEURISTIC, T2).
- **MBA Digital Ventures** (agency): feed management tools (Feedonomics, DataFeedWatch) add error alerting before disapproval; useful at catalog scale (HEURISTIC, T3).
- **Shopify/WordPress community field reports**: category-taxonomy mismatches spike disapprovals across hundreds of SKUs; "all products disapproved despite valid feed" patterns usually trace to account/taxonomy-level changes, not per-item issues (T3).
- Existing shopping-feeds skill validated against all of the above (price/availability mismatch as the top recurring health issue; fix at source).

## Decision Rules

- IF an account-suspension warning is present THEN stop all other work; remediate the root cause immediately (Elite Brands; HEURISTIC; T1)
- THEN resolve account-level → feed-level → item-level issues; within item-level: errors before warnings before notifications (AdTribes; HEURISTIC; T2)
- IF hard disapprovals exist on core revenue SKUs THEN fix those before high-volume warnings on non-core SKUs (80/20 rule) (Elite Brands; HEURISTIC; T2)
- IF price/availability/GTIN mismatch THEN fix at the catalog source, never in Merchant Center or a supplement feed (existing skill; AdTribes; T1/T2)
- IF Shopping/PMax ROAS dips THEN check diagnostics before touching bids; only move to bid/asset optimization when the feed is clean (existing skill; HEURISTIC; T2)
- IF catalog > ~1,000 SKUs THEN use rule-based title generation with hand-tuned hero SKUs; document rule owners and audit quarterly (existing skill; MBA Digital; HEURISTIC; T2)
- IF >100 products are suddenly disapproved at once THEN suspect an account/taxonomy-level change before debugging per-item issues (community reports; T3)
- IF using promotions THEN put promotional language in the promotions feed, never in titles/descriptions (GetFeeder; FACT; T1)
- IF shipping_weight is rejected THEN add units (kg/lb) — numeric-only values fail (GetFeeder; FACT; T1)

## Metrics

- **Primary**: % of items disapproved, weighted by revenue (core SKUs at zero errors) (Elite Brands; HEURISTIC; T2)
- **Guardrails**: account-health warnings count (rising = early signal), re-approval latency after fixes, feed vs landing-page price/availability mismatch count
- **Performance proxies**: Shopping CTR (title/image quality), ROAS by custom label (margin/promo structure)
- **Cadence**: weekly diagnostics review + new-SKU feed status; monthly title refresh from search-term data; quarterly taxonomy/custom-label audit (existing skill)
- **Stop-and-remeasure**: if a fix disappears on the next fetch, it was edited in Merchant Center — stop and fix the source (existing skill; AdTribes)

## Sources

1. AdTribes — Google Merchant Center Diagnostics: Fix WooCommerce Feed Errors & Avoid Suspension | adtribes.io/google-merchant-center-diagnostics | T2 | 2026-08-15
2. Elite Brands — Not All Google Merchant Center Disapprovals Are Bad (80/20 + suspension triage) | elitebrands.org/blog | T2 | 2026-08-15
3. GetFeeder — Google Shopping Disapprovals: Fix Every Error Type | getfeeder.co/blog/google-shopping-disapprovals | T2 | 2026-08-15
4. Shoparize — How Do You Fix Google Shopping Disapprovals | partner.shoparize.com | T3 | 2026-08-15
5. MBA Digital Ventures — Debugging Merchant Center Feed Errors & Disapprovals (2026) | mbadv.agency | T3 | 2026-08-15
6. Shopify Community — Why does my Google Shopping feed keep getting disapproved (category mapping) | community.shopify.com | T3 | 2026-08-15
7. WordPress.org — All products disapproved despite valid feed (account/taxonomy-level pattern) | wordpress.org/support | T3 | 2026-08-15
8. Synthesis: practitioner-intelligence/syntheses/feeds.md | T1-T3 | 2026-08-15

## Evaluation & QA

### Common Failure Modes
- Price or availability mismatch between feed and landing page - silent account-level damage
- Editing feeds in Merchant Center instead of fixing the store - fixes evaporate on the next fetch
- Keyword-stuffed titles that read as spam - CTR and compliance both suffer
- Ignoring GTIN/MPN - a top disapproval cause and an easy catalog-level fix
- No custom labels - PMax and Shopping run blind without margin and promo structure
- Letting rules accumulate - a web of feed rules nobody can untangle
- Treating feed quality as one-time setup - it decays with every catalog change
- Debugging item-level errors first when the cause is account- or taxonomy-level - wasted hours (AdTribes; community reports; T2/T3)
- Ignoring account-suspension warnings while polishing individual products - the account dies while you fix items (Elite Brands; T2)
- Promo language in titles/descriptions instead of the promotions feed - policy risk + spam look (GetFeeder; T1)
