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

## Practitioner Grounding & Decision Rules

Built from Adapty (Victoria Kharlan), SearchAdsMaven, SEM Nexus, ASO Mobile, Admiral Media, SplitMetrics/AppRadar (Gabriel Kuriata). Full research: practitioner-intelligence/syntheses/paid-longtail.md.

- **Strongest intent in paid media, but the funnel ends at install**: "neither version reports what happens after the download" — post-install revenue is invisible to Apple (Adapty — CONSENSUS, T2).
- **Basic vs Advanced**: Basic = CPI pricing, one placement, Apple-managed (test/placeholder only); Advanced = CPT + target CPA, all four placements, manual/auto bidding. "Always work in Advanced mode. Every profitable campaign I've analyzed uses Advanced mode exclusively" (Adapty — OPINION/EMPIRICAL, T2).
- **The Basic trap**: budget decisions on download counts pause your best-subscriber keywords and scale duds — connect revenue attribution first (Adapty — EMPIRICAL, T2).
- **Keyword-level truth chain**: TTR (ad-query match) → CR (page quality) → CPT → CPA; CPA = CPT/CR; ASA is the only place with direct query→behavior links, usable for ASO (ASO Mobile — FRAMEWORK, T2).
- **Structure by campaign type** (Discovery/Brand/Competitor/General) with cross-campaign negatives to stop self-competition (ASO Mobile — FRAMEWORK, T2).
- **Auction is opaque** (second-price); "harder to tell how it works backstage" vs Google/Facebook (Moburst — OPINION, T2).
- **Organic uplift**: ASA drives organic installs indirectly; evaluating only by CPA misses it; reduce bids when organic rankings climb on a keyword (ASO Mobile — HEURISTIC, T2).
- **Competitor bidding: top 1-3 defensively only**; beyond that = high CPI, mediocre conversion (SEM Nexus — HEURISTIC, T2).
- Volume norms: 50-150 keywords at stage 1-2 (300+ large accounts); $5-10k/month minimum for meaningful optimization (Admiral), Advanced the only reasonable choice above ~$10k/mo (AppRadar).

Decision rules:
1. IF the app has subscription/in-app revenue AND budget >$10k/mo THEN run Advanced only, with revenue attribution (MMP/SKAdNetwork) — never Basic for optimization (Adapty/AppRadar — HEURISTIC, T2).
2. IF judging keywords THEN evaluate CPT→TTR→CR→CPA per keyword then cohort revenue, never install count alone (ASO Mobile/Adapty — FRAMEWORK, T2).
3. IF building the account THEN separate Discovery/Brand/Competitor/General campaigns and add cross-campaign negatives (ASO Mobile — FRAMEWORK, T2).
4. IF bidding on competitors THEN cap at top 1-3, defensive posture (SEM Nexus — HEURISTIC, T2).
5. IF organic ranking on a keyword is climbing THEN cut the paid bid on it (ASO Mobile — HEURISTIC, T2).
6. IF a keyword underperforms THEN run a discovery test (high CPT + low CPA target) before killing it (SearchAdsMaven — HEURISTIC, T2).
7. IF launch-stage with tiny budget THEN Basic as a placeholder is acceptable — but connect revenue attribution before scaling decisions (Adapty/AppRadar — HEURISTIC, T2).

## Metrics

- **Revenue-attributed ROAS per keyword** (MMP/SKAdNetwork) as primary — never installs (Adapty — EMPIRICAL, T2).
- **TTR / CR / CPT / CPA chain** per keyword for diagnosis (ASO Mobile — FRAMEWORK, T2).
- **Share of Voice + organic uplift** by keyword (ASO Mobile — HEURISTIC, T2).
- **Guardrail**: broad-match "let Apple learn" burns budget on irrelevant traffic (Adapty — HEURISTIC, T2); weak product page raises real CPT (ASO Mobile).
- **Timebox**: 90-day keyword evaluation windows; watch for the two-week-abandonment failure (Adapty).

## Sources

1. Adapty, Apple Search Ads 2026: cost, placements, bidding | adapty.io/blog | tier 2 | 2026-08-15
2. Adapty, Apple Ads best practices (Advanced-only) | adapty.io/blog/apple-ads-best-practices | tier 2 | 2026-08-15
3. SearchAdsMaven, Five mistakes on Apple Search Ads | searchadsmaven.com | tier 2 | 2026-08-15
4. SEM Nexus, ASA keyword bidding strategy | semnexus.com | tier 2 | 2026-08-15
5. ASO Mobile, Apple Search Ads and ASO | asomobile.net | tier 2 | 2026-08-15
6. AppRadar/SplitMetrics, ASA Advanced guide | appradar.com | tier 2 | 2026-08-15
7. Admiral Media, ASA benchmarks | admiral.media | tier 3 | 2026-08-15

## Evaluation & QA

### Common Failure Modes
- Optimizing to impressions or taps instead of post-install events
- Running Advanced campaigns with zero negative keywords - search match burns budget
- Bidding competitor brand terms in the same campaign as own-brand terms
- Ignoring custom product pages - the only ASA-native creative lever
- Judging performance in the ASA console alone - misses post-install revenue in the MMP
- Scaling bids without an install-value model
- Treating ASA and ASO as separate projects - they compound or they cancel
