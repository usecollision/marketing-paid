---
name: google-ads
category: paid
description: Build, audit, and optimize Google Ads accounts across Search, Shopping, Performance Max, Display, and YouTube.
triggers:
  - "Google Ads"
  - "Google Ads audit"
  - "search ads campaign"
  - "shopping ads"
  - "Performance Max"
  - "PMax campaign"
  - "Google keywords and bidding"
inputs:
  - product_context
  - icp
  - budget
  - conversion_data
  - existing_account_export
outputs:
  - account_structure
  - keyword_plan
  - negative_keyword_list
  - bidding_strategy
  - campaign_playbooks
  - audit_report
related_skills:
  - paid-strategy
  - media-planning
  - performance-reporting
  - creative-testing
  - marketing-channels/keyword-research
  - marketing-optimize/analytics-setup
  - marketing-optimize/attribution-model-selection
required_context:
  - .context/product-marketing.md
allowed_tools:
  - none
version: 1.0.0
---

## When to Use

Invoke when:
- Launching Google Ads for the first time
- Auditing an existing Google Ads account for wasted spend
- Restructuring campaigns around modern formats (PMax, broad match + Smart Bidding)
- Building Shopping/feed campaigns for ecommerce
- Fixing rising CPA or falling conversion volume
- Expanding beyond Search into Display, YouTube, or Performance Max

## Workflow

### Step 1: Conversion Tracking & Foundations
Google Ads optimizes against the conversion data you feed it - everything else is secondary:
- [ ] Define the primary conversion action (purchase, lead, call, qualified lead)
- [ ] Set up the conversion tag (Google tag + event snippets) or import from GA4
- [ ] Enable enhanced conversions (hashed first-party data)
- [ ] Upload offline conversions (CRM sales/qualified leads) when the sales cycle is long
- [ ] Exclude spam conversions (page-load fires, bot forms)
- [ ] Verify the attribution window matches the business cycle
- [ ] Standardize UTM parameters and the account-level tracking template

**Gate:** Primary conversion fires correctly, enhanced/offline data flows, spam filtered out.

### Step 2: Account Architecture
Map campaign types to funnel stage and intent:

| Campaign type | Best for | Typical role |
|---|---|---|
| Search | High-intent buyers | Bottom funnel, demand capture |
| Shopping / PMax | Ecommerce product feeds | Mid/bottom funnel, product demand |
| Performance Max | Cross-inventory scaling | Full funnel, asset-driven |
| Display | Retargeting, awareness | Top/mid funnel |
| YouTube | Consideration, education | Top/mid funnel |

Structure rules:
- One campaign per objective and geography (budget follows objective)
- Separate brand vs non-brand campaigns (brand is defense - measure it separately)
- Retargeting in its own campaign, never mixed with prospecting
- Naming convention: `[Type]-[Geo]-[Funnel]-[Offer]`

**Gate:** Every campaign has a single clear objective; brand and non-brand separated.

### Step 3: Keyword Strategy
Build keyword sets by intent tier:
- **Brand terms** - own campaign, cheapest conversions, measure brand CPC separately
- **High-intent non-brand** (buy/comparison language) - primary spend target
- **Mid-intent research terms** - smaller budget, feeds the retargeting pool
- **Competitor terms** - separate campaign, usually poor efficiency, monitor closely

Match type playbook:
- Exact match on proven terms (from prior data or keyword research)
- Phrase match for mid-intent expansion
- Broad match only with Smart Bidding + strong negative lists + enough conversion volume for the algorithm to learn (heuristic - validate per account)
- Group 5-15 tightly themed keywords per ad group so ads mirror the query

**Gate:** Keyword map tiered by intent with a match type assigned per tier.

### Step 4: Negative Keywords
Negatives are where wasted spend actually dies:
- [ ] Build a master negative list from the search term report (last 90 days)
- [ ] Add "free", "jobs", "careers", "salary", "training", "download", "torrent", "example" unless relevant to the business
- [ ] Negate competitor brand names (unless running a competitor campaign)
- [ ] Exclude geographies you don't serve (location exclusions)
- [ ] Apply account-level negatives for universal exclusions, campaign-level for per-campaign rules
- [ ] Schedule search term mining weekly for the first 60 days, monthly after

**Gate:** Master negative list built and applied; mining cadence scheduled.

### Step 5: Bidding Strategy
Match the bid strategy to data volume (heuristic thresholds - validate per account):
- **No/low conversion data** - Maximize Clicks or Manual CPC to gather data
- **Steady conversion volume** - switch to Maximize Conversions
- **Stable CPA target** - target CPA once average CPA has stabilized
- **Ecommerce with margin data** - target ROAS once purchase values are reliable
- Never move tCPA more than ~20-30% below current average CPA in one step (algorithm shock)
- Seasonal accounts - plan bid adjustments in advance, don't fight the algorithm daily

**Gate:** Bid strategy assigned per campaign with explicit data-volume rationale.

### Step 6: Quality Score & Ad Rank
Quality Score (QS) is a diagnostic, not a KPI. Improve each component:
- **Expected CTR** - write ads that mirror query language; test 3+ RSAs per ad group with distinct headlines
- **Ad relevance** - tight ad-group themes; get the keyword into the headline
- **Landing page experience** - load speed, mobile, content that matches the query promise
- Low QS keywords - diagnose with the QS columns before touching bids
- Ad Rank = bid x QS x context - a high-QS ad can beat higher bids

**Gate:** Every low-QS keyword has a diagnosed cause and a fix in progress.

### Step 7: Campaign-Type Playbooks
- **Search** - 3 RSAs per ad group (mix of pinned/unpinned), sitelinks, callouts, structured snippets, image assets
- **Shopping** - fix feed quality first (titles, GTIN, product types); ads are feed-driven. Segment campaigns by product margin
- **PMax** - asset groups per theme, add search themes to steer, exclude brand unless it converts well, asset quality matters more than any setting
- **Display** - audience-first (remarketing lists, custom segments, in-market), block mobile app placements via exclusions
- **YouTube** - 15-30s video-first, audience targeting over keywords, measure view-through conversions separately

**Gate:** Playbook applied per live campaign type with feed and assets checked.

### Step 8: Audit & Optimization Cadence
- **Weekly (30 min)** - search term mining, negative adds, manual bid adjustments, paused-asset check
- **Monthly** - QS review, budget reallocation by CPA/ROAS contribution, ad copy refresh, placement exclusions
- **Quarterly** - full account audit: structure, tracking health, new campaign types, audience refreshes
- Audit checklist: 1) tracking intact? 2) spend by objective correct? 3) wasted-spend report (zero-conversion keywords) 4) impression share on brand terms 5) feed health 6) negative coverage

**Gate:** Cadence calendar set with an owner per task; audit produced a ranked fix list.

## Evaluation & QA

### Common Failure Modes
- Launching PMax with zero conversion data and thin asset groups
- Broad match without negatives - paying for irrelevant queries
- Brand and non-brand mixed - inflated ROAS hides bad prospecting
- Changing bids too often - Smart Bidding never converges
- Judging PMax too early (the algorithm needs time and data)
- Ignoring the search term report - the highest-leverage report in the account
- Optimizing toward micro-conversions that don't predict revenue
