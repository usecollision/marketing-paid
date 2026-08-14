---
name: pinterest-ads
category: paid
description: Plan Pinterest Ads for DTC discovery with pin formats, shopping campaigns, seasonal planning, and interest-and-stage audience targeting.
triggers:
  - "Pinterest Ads"
  - "promoted pins"
  - "shopping ads on Pinterest"
  - "Pinterest campaign"
  - "Pinterest seasonal planning"
  - "Pinterest audience targeting"
  - "advertise on Pinterest"
inputs:
  - product_context
  - icp
  - catalog_data
  - seasonal_calendar
  - creative_assets
  - budget
outputs:
  - channel_fit_assessment
  - campaign_structure
  - pin_format_plan
  - shopping_setup_plan
  - audience_targeting_plan
  - seasonal_calendar_plan
  - measurement_plan
related_skills:
  - paid-strategy
  - meta-ads
  - shopify-marketing-audit
  - ad-creative-generator
  - creative-testing
  - media-planning
  - marketing-intelligence/trend-detection
required_context:
  - .context/product-marketing.md
allowed_tools:
  - none
version: 1.0.0
---

## When to Use

Invoke when:
- Launching Pinterest Ads for a DTC or retail brand
- Capturing discovery-stage demand for visual, lifestyle products
- Building a shopping ads program from a product catalog
- Planning campaigns around seasonal moments (gifts, holidays, life events)
- Reaching planners and researchers before they reach the purchase moment
- Extending Meta/Google winners to a cheaper, lower-competition discovery layer

## Workflow

### Step 1: Channel Fit Assessment
Pinterest is a planning engine, not an impulse machine:
- [ ] Confirm product fit - visual, aspirational, lifestyle products with strong imagery work best; utility software does not (heuristic)
- [ ] Check ICP presence - Pinterest skews female and planning-oriented; verify your audience is actually there before budgeting
- [ ] Understand the mindset - users plan purchases weeks out; expect longer paths and lower CTRs than Meta (heuristic - validate with your own tests)
- [ ] Frame the KPI - traffic, saves, adds-to-cart, and assisted conversions over immediate ROAS
- [ ] Frame the budget - Pinterest is usually an incremental discovery layer, not the backbone

**Gate:** Fit assessment documented with product-category and audience rationale.

### Step 2: Pin Formats & Creative
- **Standard pins** - static image; the workhorse
- **Video pins** - 6-15 second loop-friendly clips; test against static
- **Idea pins** - multi-page, creator-style; engagement-first, weaker direct response
- **Carousel pins** - multi-image storytelling
- **Collection ads** - hero image plus product thumbnails; the discovery-to-shop bridge
- Creative rules - vertical 2:3, text overlay on every pin, warm lifestyle imagery over studio shots, brand name visible early (heuristic - test against your own data)

**Gate:** Format mix per funnel stage; creative set produced in Pinterest-native specs.

### Step 3: Shopping Ads & Catalog Setup
- [ ] Ingest the product catalog (via the Shopify app or a feed) - titles, images, prices, availability
- [ ] Fix feed quality first - Pinterest ads are catalog-driven; clean titles and lifestyle images lift everything downstream
- [ ] Enable automatic bidding options once the catalog has traffic history
- [ ] Use rich product data - price and availability info drive clicks
- [ ] Connect the Pinterest tag for conversion tracking before scaling

**Gate:** Catalog live and healthy; conversion tag firing.

### Step 4: Audience Targeting by Interest & Stage
- [ ] Start with interest + keyword targeting - Pinterest's interests are explicit and strong for discovery
- [ ] Use act-alike audiences once you have seed lists (site visitors, engagers, customers)
- [ ] Stage-based layering - broad interest for cold discovery, act-alike for warm, retargeting for hot (site visitors, cart abandoners)
- [ ] Use keyword targeting - Pinterest search intent is real; match keywords to pin themes
- [ ] Avoid hyper-layering - Pinterest audiences are smaller; too many filters stall delivery

**Gate:** Audience plan mapped by funnel stage with delivery sanity checks.

### Step 5: Seasonal Planning
Pinterest demand is calendar-driven - users plan months ahead:
- [ ] Build a seasonal calendar - holidays, gifting moments, back-to-school, wedding season, home refresh cycles
- [ ] Launch 4-8 weeks BEFORE the peak - Pinterest is a planning tool; late launches miss the research window (heuristic)
- [ ] Pre-seed seasonal boards and pins - organic presence before paid amplification
- [ ] Refresh seasonal creative each year - recycled assets fatigue fast
- [ ] Align budget to planning windows - front-load around research peaks, not purchase peaks

**Gate:** Seasonal calendar with launch dates 4-8 weeks ahead of each peak and budget mapped.

### Step 6: Measurement & Optimization
- [ ] Track assisted conversions - Pinterest rarely wins last-click on the first visit
- [ ] Judge pins on saves and outbound clicks early, revenue later - the funnel is slow
- [ ] Kill low-CTR pins fast - imagery is the whole game; test 2-3 new images per theme weekly during scaling
- [ ] Scale winners by broadened interest and act-alike expansion, not budget blasting
- [ ] Compare Pinterest CAC to blended - discovery layers look bad solo, fine blended (heuristic - measure, don't assume)

**Gate:** Measurement plan includes saves, clicks, and assisted revenue; kill-scale rules defined.

## Practitioner Grounding & Decision Rules

Built from Md Sharifuzzaman (Pinterest Advertising Stuff / Decor Ads Pro, 343+ projects), Vixen Digital (Galvan London case), Pinterest Business official benchmarks. Full research: practitioner-intelligence/syntheses/paid-longtail.md.

- **Pinterest is a planning-intent catalog channel**: users save ideas 30-90 days before purchase; intent quality beats Meta cold audiences (Sharifuzzaman/Pinterest — CONSENSUS, T2).
- **Catalog quality is the single biggest lever**: category-first titles (brand keyword in title = +28% ROAS, pattern keyword +22% — Pinterest internal), lifestyle hero images, clean feed (Pinterest — EMPIRICAL, T2).
- **Always-on beats bursts**: campaigns 6+ months ≈ +25% ROAS; <3 months = −5-16% vs average; pausing resets learning (Pinterest internal — EMPIRICAL, T2).
- **Auto-targeting beats manual overlays** on catalog campaigns: a direct test saw ROAS drop 39x→31x for 6 weeks when interest overlays were added (Sharifuzzaman — EMPIRICAL, T2).
- **Scale ≤15-20%/month**; rapid increases reset optimization (Sharifuzzaman — HEURISTIC, T2).
- **Month 1-3 is below benchmark** — the algorithm builds conversion signal; early numbers are not the ceiling (Sharifuzzaman/Pinterest — CONSENSUS, T2).
- **CAPI + tag = 9% better CPA and 23.7% more attributed conversions** vs tag-only (Pinterest internal — EMPIRICAL, T2).
- Structure: one dominant catalog campaign (~80% spend) + collections + small retargeting; fragmented micro-campaigns starve the algorithm (Sharifuzzaman — HEURISTIC, T2).

Decision rules:
1. IF running shopping/catalog campaigns THEN keep them always-on year-round; never pause for events — rotate creative/promotions instead (Pinterest — EMPIRICAL, T2).
2. IF catalog underperforms THEN fix the feed first (titles, images, price accuracy) before touching bids (Sharifuzzaman/Pinterest — EMPIRICAL, T2).
3. IF using catalog auto-targeting THEN do NOT add interest/keyword overlays (Sharifuzzaman — EMPIRICAL, T2).
4. IF scaling THEN cap increases at 15-20%/month and wait for ROAS re-stabilization (Sharifuzzaman — HEURISTIC, T2).
5. IF evaluating Pinterest THEN require a 90-day window + CAPI tracking; compare to GA4/attribution gap, not dashboard ROAS alone (T2).
6. IF category is visual + high-AOV + planning-driven (furniture, decor, weddings, fashion) THEN Pinterest can beat Meta/Google on CPA; IF low-visual or B2B service THEN skip (Sharifuzzaman/Vixen — HEURISTIC, T2).

## Metrics

- **Catalog ROAS** (dashboard) + **GA4/attribution gap** — gap is expected; direction over magnitude (Sharifuzzaman — HEURISTIC, T2).
- **Earned impressions vs paid** (successful campaigns run 2-3x earned) (Dataslayer — T3).
- **Feed health** (title structure, image quality, price consistency) as pre-flight gate (Pinterest — EMPIRICAL, T2).
- **Timebox**: 90 days minimum before verdict; re-measure after every 15-20% budget step.

## Sources

1. Md Sharifuzzaman, 39.94x Pinterest catalog case study | pinterestadvertisingstuff.com | tier 2 | 2026-08-15
2. Pinterest Business, Shopping best practices checklist | business.pinterest.com/blog | tier 1 | 2026-08-15
3. Vixen Digital, Pinterest for ecommerce (Galvan London) | vixendigital.com | tier 2 | 2026-08-15
4. Social Media Today, Pinterest catalog advice | socialmediatoday.com | tier 2 | 2026-08-15
5. Dataslayer, Pinterest reporting mistakes | dataslayer.ai | tier 3 | 2026-08-15

## Evaluation & QA

### Common Failure Modes
- Repurposing horizontal Meta ads - wrong aspect ratio and wrong vibe
- Launching seasonal campaigns at the purchase peak instead of the planning peak
- Judging Pinterest on 7-day last-click ROAS - structurally undercounts a planning channel
- Ignoring saves - the leading indicator of a pin's compounding value
- Skipping catalog hygiene - shopping ads amplify bad feed data
- Over-targeting until delivery dies
