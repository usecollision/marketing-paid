---
name: programmatic-ctv
category: paid
description: Buy programmatic display and CTV with DSP selection, open exchange vs PMP trade-offs, CTV targeting and measurement, and B2B IP-targeting plays.
triggers:
  - "programmatic advertising"
  - "DSP selection"
  - "CTV ads"
  - "connected TV advertising"
  - "open exchange vs PMP"
  - "programmatic display"
  - "IP targeting B2B"
inputs:
  - product_context
  - icp
  - budget
  - audience_data
  - creative_assets
  - measurement_requirements
outputs:
  - channel_fit_assessment
  - dsp_selection
  - inventory_strategy
  - targeting_plan
  - ctv_measurement_plan
  - retargeting_plan
  - b2b_ip_targeting_plan
related_skills:
  - paid-strategy
  - media-planning
  - performance-reporting
  - native-ads
  - linkedin-ads
  - marketing-optimize/attribution-model-selection
  - marketing-optimize/analytics-setup
required_context:
  - .context/product-marketing.md
allowed_tools:
  - none
version: 1.0.0
---

## When to Use

Invoke when:
- Building or auditing a programmatic display program
- Choosing or switching a DSP
- Launching CTV campaigns
- Deciding between open exchange and PMP inventory
- Planning retargeting at scale
- Running B2B account-based campaigns via IP targeting

## Workflow

### Step 1: Objectives & Channel Fit
- [ ] Define the job - awareness (reach/frequency), consideration (retargeting, mid-funnel), or performance (programmatic rarely wins on strict last-click ROAS - heuristic)
- [ ] Match format to job - display for retargeting and prospecting, CTV for high-attention reach and brand, native for content distribution
- [ ] Set measurement expectations - viewability, reach, and assisted conversions; agree before launch
- [ ] Size the budget - DSP, data, and verification fees can eat 15-30% of media spend on small budgets (heuristic - model your own tech stack)

**Gate:** Objectives, formats, and measurement expectations documented.

### Step 2: DSP Selection
- **Major self-serve DSPs** - Google DV360, The Trade Desk, Amazon DSP (retail data), Xandr/Microsoft Invest, plus vertical specialists
- Selection criteria - inventory access (CTV partners, publisher direct deals), data integrations (first-party, retail, B2B), fees and minimums, UI and support quality, measurement integrations
- Ask for a pilot - most DSPs offer tests; run the same campaign brief across two DSPs before committing
- Self-serve vs managed - managed services cost more but skip the learning curve; self-serve pays off at scale (heuristic)

**Gate:** Shortlist evaluated on inventory, data, and fees; pilot planned.

### Step 3: Inventory - Open Exchange vs PMP vs Programmatic Guaranteed
- **Open exchange (RTB)** - largest pool, cheapest CPMs, lowest transparency; quality and brand safety risk
- **PMP (private marketplace)** - curated publisher deals at negotiated CPMs; the quality sweet spot
- **Programmatic guaranteed** - direct deals executed programmatically; premium but fixed
- Decision rules - open exchange for performance and retargeting with strict blocklists; PMP for brand and CTV quality; guaranteed for flagship placements
- Blocklist and whitelist discipline applies at every tier

**Gate:** Inventory mix per campaign objective with quality controls defined.

### Step 4: Targeting & Data Strategy
- **First-party data** - onboard CRM/email lists (via DMP/CDP or DSP onboarding) for retargeting and suppression
- **Contextual** - page and content signals; the cookieless-safe default
- **Third-party segments** - shrinking in usefulness as identifiers deprecate; verify segment freshness before buying
- **Lookalikes** - modeled from first-party seeds
- **Frequency and recency** - cap per user per day; programmatic reach burns fast without caps
- Plan for identifier deprecation - contextual plus first-party should be the default architecture now

**Gate:** Targeting architecture per audience with caps; cookieless plan explicit.

### Step 5: CTV Planning & Measurement
- [ ] Formats - 15-30s non-skippable video as the core; 6s for frequency extensions
- [ ] Targeting - household-level, not person-level; audience segments, context, and geography
- [ ] Measurement - impressions served to TVs are not clicks; measure reach, frequency, and completion
- [ ] Use incrementality or brand-lift studies for impact, not last-click attribution
- [ ] Connect to search/social - CTV drives branded search and site visits; measure assisted conversions and search lift during flights
- [ ] Beware double-counting - TV and digital attribution overlap; agree on the read before launch

**Gate:** CTV measurement plan includes completion, reach/frequency, and a brand-lift or search-lift readout.

### Step 6: Retargeting Strategies
- [ ] Build audience pools - site visitors by recency and page depth, cart abandoners, content engagers
- [ ] Layer recency tiers - 1-3 day, 4-7 day, 8-14 day pools with different bids (heuristic tiers - adjust per funnel length)
- [ ] Frequency caps - 5-10 per user per day on display, lower on CTV (heuristic - validate per brand)
- [ ] Burn pools fast - 30-60 day windows lose relevance; refresh constantly
- [ ] Suppress customers - exclude converters to stop remarketing waste

**Gate:** Retargeting architecture with recency tiers, caps, and suppression rules.

### Step 7: B2B via IP Targeting
- [ ] Match IP ranges to companies - B2B data vendors map IPs to named accounts and industries
- [ ] Use account lists - target the building, not the person; ideal for ABM when combined with company-size and industry filters
- [ ] Layer with display and CTV - the same account list can run on both formats
- [ ] Know the caveats - WFH blurs home-vs-office IPs, and IP data has false positives; verify match quality with the vendor before scaling (request match-rate reports)
- [ ] Combine with LinkedIn Ads - programmatic IP covers the account broadly, LinkedIn covers the named roles
- [ ] Measure at account level - impressions per account, site visits from target accounts, pipeline influence

**Gate:** IP-targeted account list live with match-quality report reviewed; ABM measurement defined.

### Step 8: Quality, Optimization & Reporting
- [ ] Run viewability and brand-safety verification from day one
- [ ] Review weekly - spend by placement, blocklist additions, frequency violations
- [ ] Optimize quarterly - rebalance inventory mix, refresh segments, renegotiate PMP CPMs
- [ ] Report on reach, frequency, viewability, and assisted conversions - never raw impressions alone

**Gate:** Verification live; reporting structure matches pre-agreed measurement expectations.

## Evaluation & QA

### Common Failure Modes
- Buying open-exchange inventory with no blocklists - brand safety and fraud exposure
- Measuring CTV on clicks - the format doesn't generate them; wrong read
- Retargeting everyone forever - no suppression, no recency tiers, burned budget
- Trusting third-party segments blindly as identifiers deprecate
- Paying managed-service fees on tiny budgets where self-serve would do
- Treating IP targeting as precise - it is account-level, not person-level
- Reporting impressions without viewability and frequency context
