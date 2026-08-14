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

## Practitioner Grounding & Decision Rules

Built from Melissa Mackey (Head of Paid Search, Compound Growth Marketing; ex-JumpFly; Bing Champion 2018/19), Lisa Raehsler (Big Click Co), LSEO. Full research: practitioner-intelligence/syntheses/paid-longtail.md. Cross-ref: google-ads skill (Mackey verified for Google too).

- **"In general Bing outperforms Google, both in higher conversion rates and lower CPCs"** — not true for every client, but common (Mackey — EMPIRICAL/HEURISTIC, T1). Case: new client's cost per conversion on Bing was ¼ that of Google (Mackey — EMPIRICAL, T1).
- **Bing's audience is different, not a clone**: better-educated, higher household income (Microsoft's Rik van der Kooi via Mackey — T2); skews older + Windows/Office/LinkedIn ecosystem.
- **"Importing AdWords campaigns to Bing — many advertisers don't realize their job has just started with the import"** (Mackey — FRAMEWORK, T1): bids, negatives, extensions, geo, devices all need Bing-native re-tuning post-import (Mackey/Raehsler — CONSENSUS).
- **Bing "feels like a second language"**: ad-group-level targeting available; targeting sometimes doesn't import cleanly; negative matching has fewer options (no negative broad match) (Mackey — EMPIRICAL, T1).
- **Microsoft Audience Network placements "aren't search"** — can't exclude sites or set per-site ads; manage via bid modifiers with separate expectations (Mackey — HEURISTIC, T1).
- Automation is more manual in Microsoft Ads — plan for more hands-on management (LSEO — T3).

Decision rules:
1. IF a Google Ads account exists THEN import to Microsoft Ads, then treat the import as a starting point: re-check bids, negatives (no negative broad), extensions, geo and device targets (Mackey/Raehsler — FRAMEWORK, T1).
2. IF the ICP skews older, higher-income, or Windows/Office/LinkedIn-adjacent THEN prioritize Microsoft Ads — the audience differs from Google's (Mackey/Microsoft — EMPIRICAL, T2).
3. IF comparing platforms THEN compare cost-per-conversion and conversion rate, not CPC — Bing often wins both (Mackey — EMPIRICAL, T1).
4. IF running Microsoft Audience Network placements THEN manage with bid modifiers and separate performance expectations — native ≠ search (Mackey — HEURISTIC, T1).
5. IF a campaign underperforms on Bing but wins on Google THEN check match-type nuances and bid calibration before killing (LSEO/Mackey — HEURISTIC, T2).
6. IF re-optimizing Google THEN re-import to Microsoft Ads on a schedule to propagate improvements (LSEO — HEURISTIC, T3).

## Metrics

- **Cost per conversion + conversion rate vs Google** as primary comparison (Mackey — EMPIRICAL, T1).
- **Post-import audit completeness** (bids, negatives, extensions, geo, devices) as a pre-flight gate (Raehsler — HEURISTIC, T2).
- **Audience Network performance separated** from search metrics (Mackey — HEURISTIC, T1).
- **Guardrail**: import-and-forget is the #1 failure; copy-paste Google bids without calibration (Mackey — HEURISTIC, T1).
- **Timebox**: 30-60 days post-import to re-tune and judge.

## Sources

1. Melissa Mackey, Where Bing Ads Are Beating Google | beyondthepaid.com | tier 1 | 2026-08-15
2. Melissa Mackey, Importing AdWords Campaigns to Bing Ads: The Guide | beyondthepaid.com | tier 1 | 2026-08-15
3. Melissa Mackey, Bing Ads feels like a second language | beyondthepaid.com | tier 1 | 2026-08-15
4. Melissa Mackey profile (Bing Champion, JumpFly) | paidsearch.org/team/melissa-mackey | tier 2 | 2026-08-15
5. Lisa Raehsler, Optimizing Bing Ads after import (via Mackey) | bigclickco.com | tier 2 | 2026-08-15
6. LSEO, How to Import Google Ads into Microsoft Ads | lseo.com | tier 3 | 2026-08-15

## Evaluation & QA

### Common Failure Modes
- Importing Google campaigns without fixing tracking first - blind bidding from day one
- Cloning Google budgets 1-to-1 - Microsoft inventory is smaller; overspend saturates fast
- Judging Microsoft on CPC while conversion quality lags
- Letting imported negatives go stale - the two platforms' query pools drift apart
- Over-restricting with LinkedIn layers until campaigns can't deliver
- Ignoring brand vs non-brand separation on a platform where brand is especially cheap
- Never mining the search term report - variance is higher on the smaller pool
