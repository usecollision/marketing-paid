---
name: microsoft-ads
category: paid
description: Build and optimize Microsoft Advertising search campaigns with Google imports, LinkedIn profile targeting, and lower-CPC efficiency plays.
triggers:
  - "Microsoft Ads"
  - "Bing Ads"
  - "Microsoft Advertising"
  - "import Google Ads to Microsoft"
  - "LinkedIn profile targeting"
  - "search ads on Bing"
  - "cheaper search ads than Google"
inputs:
  - product_context
  - icp
  - budget
  - google_ads_export
  - conversion_data
  - audience_data
outputs:
  - channel_fit_assessment
  - import_plan
  - account_structure
  - keyword_plan
  - negative_keyword_list
  - audience_targeting_plan
  - bidding_strategy
  - audit_report
related_skills:
  - google-ads
  - paid-strategy
  - linkedin-ads
  - media-planning
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
- Launching Microsoft Advertising (Bing) search campaigns
- Importing an existing Google Ads account into Microsoft
- Seeking lower CPCs than Google on the same keywords (heuristic - validate per account)
- Reaching an audience that skews older, desktop-first, and often higher-income (Bing/Edge/Windows defaults - verify with your own data)
- Layering LinkedIn profile data onto search audiences for B2B
- Extending brand-term defense beyond Google
- Auditing an existing Microsoft account for wasted spend

## Workflow

### Step 1: Channel Fit Assessment
- [ ] Estimate the search share available - Microsoft powers Bing, Yahoo, AOL, and DuckDuckGo ads; share varies sharply by market (verify per geo before budgeting)
- [ ] Check demographic fit - Microsoft search skews older and desktop-first (heuristic - validate with your own audience data)
- [ ] Confirm market coverage - US and UK are strongest; coverage is thinner elsewhere
- [ ] Size the prize - in most accounts Microsoft is a 10-30% of Google increment, not a replacement (heuristic)
- [ ] Decide brand-only vs full portfolio - brand defense on Microsoft is usually cheap and worth doing first

**Gate:** Documented decision on whether Microsoft gets budget, and at what share.

### Step 2: Import from Google Ads
- [ ] Use the built-in Import tool instead of rebuilding - imports campaigns, ad groups, keywords, negatives, and bids
- [ ] Set up the UET tag and conversion tracking BEFORE import - bidding signals must work from day one
- [ ] Choose what to import - start with high-intent Search campaigns; skip Performance Max (no direct equivalent)
- [ ] Configure a recurring import schedule (daily or weekly) so Google wins keep flowing over
- [ ] Post-import checklist - re-enable paused items deliberately, review bid strategies (some Google bid types have no Microsoft equivalent), fix device and geo settings that reset to defaults
- [ ] Audit match types - imported broad match is riskier on Microsoft's smaller query pool

**Gate:** Import completed, conversion tracking live, post-import audit log of every changed setting.

### Step 3: Account & Campaign Architecture
Mirror Google structure, but don't clone it blindly:
- Separate brand vs non-brand campaigns (same defense logic as Google)
- One campaign per objective and geography
- Retargeting in its own campaign, never mixed with prospecting
- Naming convention - `[Type]-[Geo]-[Funnel]-[Offer]`
- Microsoft-only opportunities - Bing shopping campaigns for ecommerce, Microsoft Audience Ads (native placements) as a cheap add-on, LinkedIn profile targeting on search audiences

**Gate:** Structure documented with a rationale for every campaign's existence.

### Step 4: Keyword & Negative Strategy
- [ ] Start from the Google keyword set, then expand - search term data on Microsoft differs from Google's
- [ ] Run Microsoft's own keyword planner for platform-specific volume
- [ ] Import negatives with the keyword import; keep the master list synced across platforms
- [ ] Mine the search term report weekly at launch - a smaller query pool means more variance in matches
- [ ] Add the same universal negatives as Google (free, jobs, careers, salary, torrent, example) unless relevant to the business

**Gate:** Keyword map synced with Google plus platform-specific additions; negative lists live.

### Step 5: Audience Targeting with LinkedIn Profile Data
The differentiator other search engines don't have:
- [ ] Create audiences from LinkedIn profile fields - company, industry, and job function are available on search campaigns
- [ ] Layer combinations - e.g. job function = marketing AND company size = 200-500 employees
- [ ] Use bid-only audiences first (observe) before target-only (restrict)
- [ ] Try company targeting for ABM - search campaigns restricted to a named-company list
- [ ] Test in-market audiences - Microsoft's segments reach searchers whose behavior signals purchase intent
- [ ] Beware over-restriction - small LinkedIn layers on small search pools kill delivery; check audience estimates before restricting

**Gate:** At least one LinkedIn-profile audience live with bid modifiers; one ABM test planned.

### Step 6: Bidding & Budget
- [ ] Start with Enhanced CPC or Maximize Clicks while volume builds; move to automated strategies as conversion data accrues (same data-volume logic as Google)
- [ ] Expect lower CPCs - identical keywords often cost less than Google (heuristic - differences vary by vertical and market; verify with your own auction data)
- [ ] Don't assume lower CPC means free money - conversion rates and volume differ; judge on CPA and ROAS, not CPC
- [ ] Scale winners with care - Microsoft inventory is smaller; aggressive scaling saturates fast
- [ ] Measure brand CPCs separately - brand efficiency should never be diluted by non-brand

**Gate:** Bid strategy per campaign with data-volume rationale; success judged on CPA/ROAS, not CPC.

### Step 7: Optimization Cadence
- Weekly (30 min) - search term mining, negative adds, bid adjustments
- Monthly - keyword expansion from Microsoft-specific query data, audience bid review, budget reallocation by CPA contribution
- Quarterly - full audit, import sync health, new Microsoft-only features (Audience Ads, shopping, audience layers)
- Cross-platform rule - never judge Microsoft on Google's benchmarks; set platform-specific targets from its own history

**Gate:** Cadence calendar set; platform-specific targets defined.

## Evaluation & QA

### Common Failure Modes
- Importing Google campaigns without fixing tracking first - blind bidding from day one
- Cloning Google budgets 1-to-1 - Microsoft inventory is smaller; overspend saturates fast
- Judging Microsoft on CPC while conversion quality lags
- Letting imported negatives go stale - the two platforms' query pools drift apart
- Over-restricting with LinkedIn layers until campaigns can't deliver
- Ignoring brand vs non-brand separation on a platform where brand is especially cheap
- Never mining the search term report - variance is higher on the smaller pool
