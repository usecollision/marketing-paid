---
name: apple-search-ads
category: paid
description: Run Apple Search Ads for App Store growth with keyword bidding, basic vs advanced campaign selection, keyword discovery, and TTR-CR optimization loops.
triggers:
  - "Apple Search Ads"
  - "App Store ads"
  - "ASA campaign"
  - "app install ads"
  - "Search tab ads"
  - "App Store keyword bidding"
inputs:
  - app_context
  - app_store_listing
  - conversion_events
  - budget
  - existing_keyword_data
  - mmp_data
outputs:
  - campaign_structure
  - keyword_plan
  - bidding_plan
  - negative_keyword_list
  - custom_product_page_plan
  - optimization_cadence
related_skills:
  - google-ads
  - paid-strategy
  - media-planning
  - creative-testing
  - performance-reporting
  - marketing-channels/keyword-research
  - marketing-optimize/metrics-framework
required_context:
  - .context/product-marketing.md
allowed_tools:
  - none
version: 1.0.0
---

## When to Use

Invoke when:
- Launching or scaling an iOS app's user acquisition
- Capturing high-intent App Store search demand
- Defending brand searches in the App Store from competitors
- Testing App Store keyword demand before ASO investment
- Building a search-to-install loop alongside ASO and referral programs
- Running app marketing where the store listing is the landing page

## Workflow

### Step 1: Foundations - Tracking & Store Readiness
ASA optimizes against post-install events; nothing else matters until this works:
- [ ] Verify MMP integration (AppsFlyer, Adjust, Branch) and SKAdNetwork setup
- [ ] Define the primary optimization event - install, registration, first purchase, or trial start
- [ ] Audit the App Store listing first - title, subtitle, keywords field; ASA and ASO share the same keyword relevance signals
- [ ] Fix the product page before buying traffic - a weak page burns budget regardless of bidding

**Gate:** Conversion events verified firing; listing relevance audited.

### Step 2: Choose Basic vs Advanced
- **Basic** - Apple manages everything; pay per install; no keyword control; simple but expensive at scale
- **Advanced** - manual keyword and bid control, audience refinement, custom product pages; the real platform
- Decision rule - Basic for first-time testers with small budgets and no MMP setup; Advanced for anyone serious about CPA control (heuristic)
- Advanced unlocks - exact match, broad match, search match, negative keywords, per-keyword bids

**Gate:** Campaign type chosen with rationale tied to tracking maturity and budget.

### Step 3: Keyword Discovery
- [ ] Start with brand terms - own-brand searches convert cheapest; competitor brand terms go in a separate campaign
- [ ] Mine ASA search match data after launch - real query data beats speculation
- [ ] Run ASO keyword research (keyword-research skill) - App Store keyword field and title analysis
- [ ] Use Apple's suggested keywords in the console as a starting point only
- [ ] Structure - exact match ad groups for proven terms; search match on a separate group for discovery
- [ ] Add negatives aggressively - search match surfaces irrelevant queries; negate weekly

**Gate:** Keyword map tiered brand, non-brand exact, and discovery (search match) with negatives live.

### Step 4: Bidding & Budget
- [ ] Use manual CPT (cost per tap) bids per keyword to start; treat Apple's suggested bid ranges as a ceiling reference, not a target
- [ ] Back into bids from value - estimate per-keyword install value, then derive a max CPT
- [ ] Brand keywords - bid to win; they are cheap and defense matters
- [ ] Scale by CPA - start small, raise budget on keywords that hit CPA targets after enough installs for a stable read
- [ ] Watch auction volatility - App Store auctions shift; check bid competitiveness weekly

**Gate:** Per-keyword max CPT set from an install-value model; brand terms fully defended.

### Step 5: TTR and CR Optimization Loop
- **TTR (tap-through rate)** - impressions to taps; the creative/relevance dial
- **CR (conversion rate)** - taps to installs; the listing-quality dial
- Diagnose low TTR - weak screenshot set, irrelevant keyword-to-page match, or low rating visibility
- Diagnose low CR - the product page fails to justify the tap; test custom product pages per keyword theme
- Custom product pages - assign themed pages (feature X for keyword theme X) to lift both metrics
- Loop cadence - review TTR/CR per keyword weekly; act when a keyword has volume and both metrics lag peers

**Gate:** TTR and CR dashboards per keyword theme; at least one custom product page test live.

### Step 6: Scale, Refresh & Reporting
- [ ] Scale winners by raising budgets on CPA-hitting keywords before adding new keywords
- [ ] Refresh keyword lists monthly from search match data and new ASO research
- [ ] Sync with ASO - install velocity lifts keyword rankings; feed ASA winners into ASO strategy
- [ ] Report with MMP data - ASA console numbers stop at the tap; post-install value lives in the MMP
- [ ] Watch seasonality - App Store demand shifts with device cycles and app events

**Gate:** Scaling rules defined; ASA-to-ASO feedback loop documented.

## Evaluation & QA

### Common Failure Modes
- Optimizing to impressions or taps instead of post-install events
- Running Advanced campaigns with zero negative keywords - search match burns budget
- Bidding competitor brand terms in the same campaign as own-brand terms
- Ignoring custom product pages - the only ASA-native creative lever
- Judging performance in the ASA console alone - misses post-install revenue in the MMP
- Scaling bids without an install-value model
- Treating ASA and ASO as separate projects - they compound or they cancel
