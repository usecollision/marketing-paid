---
name: linkedin-ads
category: paid
description: Plan, launch, and optimize LinkedIn Ads for B2B lead generation and account-based marketing.
triggers:
  - "LinkedIn ads"
  - "LinkedIn campaign"
  - "B2B lead generation ads"
  - "ABM advertising"
  - "Sponsored Content LinkedIn"
  - "LinkedIn lead gen forms"
inputs:
  - product_context
  - icp
  - target_account_list
  - budget
  - creative_assets
  - lead_routing_setup
outputs:
  - audience_architecture
  - campaign_structure
  - format_recommendations
  - lead_gen_plan
  - measurement_plan
related_skills:
  - paid-strategy
  - media-planning
  - performance-reporting
  - marketing-intelligence/icp-builder
  - marketing-intelligence/account-intelligence
  - marketing-messaging/case-study-builder
  - marketing-channels/linkedin-content
required_context:
  - .context/product-marketing.md
allowed_tools:
  - none
version: 1.0.0
---

## When to Use

Invoke when:
- Launching LinkedIn Ads for B2B lead generation
- Building account-based marketing (ABM) campaigns
- Scaling a B2B brand beyond one ad format
- LinkedIn cost per lead is rising and needs diagnosis
- Planning Thought Leader Ads or Conversation Ads
- Aligning LinkedIn measurement with CRM reality

## Workflow

### Step 1: Tracking & Objective Setup
- [ ] Insight Tag installed on all pages
- [ ] Conversions API configured for server-side events
- [ ] Conversion rules defined (lead form submit, demo booked, qualified lead via offline conversions)
- [ ] Lead Gen Forms synced to CRM (native integrations or webhook/Zapier) - routing matters more than the form itself
- [ ] Conversion window set consistent with the sales cycle

**Gate:** Conversions fire, forms route into CRM, offline conversions flow back.

### Step 2: Targeting Architecture
Layer targeting like a Venn diagram - company x persona x behavior:
- **Company layer** - ABM account lists (uploaded, max ~300k), company size, industry, company growth
- **Persona layer** - job title, job function, seniority, member skills, member groups
- **Matched Audiences** - website retargeting, contact lists (match-rate caveat - expect partial matches, heuristics only), company lists, lookalikes
- **ABM tiers** - Tier 1 named accounts (contact + account lists), Tier 2 lookalikes of customers, Tier 3 broad ICP attributes
- Audience size sanity check - too small (roughly under ~50k, heuristic) overpays for CPMs; too broad wastes spend. Layer multiple attributes to hit the sweet spot
- Exclusions - current customers, your own company, recruiters, competitors

**Gate:** Target audience per campaign documented with size estimate and ICP rationale.

### Step 3: Format Selection
Match format to job:
- **Sponsored Content (single image/video/carousel)** - the workhorse; image for speed, video for consideration, carousel for storytelling
- **Thought Leader Ads** - boost posts from founders/execs' personal profiles; typically higher engagement than company posts (heuristic - validate with your own data); only with an active poster
- **Document Ads** - gated PDFs for deeper nurture and higher-quality leads
- **Conversation Ads (Message Ads)** - choose-your-own-path in LinkedIn inbox; high-intent hand-raisers, premium CPMs
- **Lead Gen Forms** - pre-filled, lowest-friction lead capture; expect volume with quality caveat

**Gate:** Format mapped per funnel stage with a rationale for each.

### Step 4: Campaign Structure
Separate by objective and audience tier:
- **Prospecting** - broad ICP attribute audiences; offer educational content, benchmarks, frameworks
- **Retargeting** - website visitors, engagers, video viewers; offer case studies, demos, trials
- **ABM** - named account lists with vertical-personalized messaging
- One objective per campaign; no prospecting and retargeting mixed
- Naming: `[Tier]-[Stage]-[Offer]-[Date]`

**Gate:** Campaign map covers prospecting, retargeting, and ABM tiers separately.

### Step 5: Bidding & Budget
- Auction basics - LinkedIn is a second-price auction; set bids high enough to actually enter
- Start with automated bidding (max delivery) or manual CPM/CPC to learn; move to cost cap once you have lead targets
- Budget heuristics - validate every number against your account history; LinkedIn minimums and viable test budgets vary by region and audience size
- Pacing - LinkedIn serves heavily during business hours; expect weekday concentration
- Bid floor reality - underbidding on a premium B2B audience gets you nothing, not cheap traffic

**Gate:** Bid strategy chosen per campaign with a test-budget rationale.

### Step 6: Creative & Offer Strategy
- B2B creative rules - quantify value in the headline, show a face, use charts/customer logos, no stock-photo corporate cliches
- Angle testing - pain, outcome, ROI, social proof, contrarian take
- Offer ladder - educational content (prospecting) > case study/demo (retargeting) > consultation (ABM)
- Lead magnets that earn B2B attention - benchmarks, calculators, teardowns, frameworks, templates
- The ad's job is the click; the landing page closes (see marketing-optimize/landing-page-optimization)

**Gate:** At least 3 angles and an offer mapped per funnel stage.

### Step 7: Lead Gen Forms & Follow-Up
- Form fields - minimize; pre-filled from the profile; one qualifying question max
- Hidden fields - capture campaign, ad, and audience for attribution
- Speed-to-lead - route leads to CRM within minutes; set an explicit follow-up SLA
- Define MQL criteria up front - a LinkedIn lead is not a pipeline deal
- A/B test form vs landing page - forms lower friction, landing pages pre-qualify

**Gate:** Lead routing live, SLA agreed, MQL criteria written down.

### Step 8: Measurement & Attribution
- Reconcile platform CPL against CRM truth monthly - pipeline and closed-won, not just leads
- Push offline conversions back so LinkedIn optimizes toward revenue
- View-through caveat - LinkedIn credits impressions-driven conversions; compare against last-click before believing uplift claims
- Measure per campaign: leads, MQL rate, pipeline, revenue; a high-CPL campaign with strong pipeline can beat a cheap-CPL campaign
- Expect CPL inflation as audiences saturate - creative refresh is the main lever, not bid games

**Gate:** Platform-to-CRM reconciliation process running; deal-stage metrics per campaign.

## Practitioner Grounding & Decision Rules

Built from AJ Wilcox (B2Linked), Richard van der Blom (LinkedIn data). Full research: practitioner-intelligence/syntheses/paid-strategy.md.

- **LinkedIn is B2B ABM's best precision channel — at a price premium** (Wilcox — FRAMEWORK, T1): justify the CPM with ICP precision; it fails when audiences are broad.
- **Data decays; refresh audience lists** (van der Blom — EMPIRICAL, T1): LinkedIn match rates and intent data degrade; company lists need quarterly refresh.

Decision rules:
1. IF the target list is broad (industry-wide) THEN LinkedIn is likely the wrong buy — precision is the only premium justification (Wilcox — FRAMEWORK, T1).
2. IF running ABM THEN use company lists + job-title overlays; refresh lists quarterly (van der Blom — EMPIRICAL, T1).
3. IF measuring success THEN use pipeline-influenced and MQL quality, not CTR — LinkedIn clicks convert poorly on average but the good ones close (Wilcox — HEURISTIC, T1).
4. IF creative is static (no Sponsored Content variety) THEN add message variety — LinkedIn rewards fresh angles and penalizes repetition (van der Blom — EMPIRICAL, T1).

## Metrics

- **MQL/pipeline per ICP account** — the ABM truth layer (Wilcox — FRAMEWORK, T1).
- **List match rate + refresh cadence** (van der Blom — EMPIRICAL, T1).

## Sources

1. AJ Wilcox, LinkedIn Ads practice (B2Linked) | b2linked.com | tier 1 | 2026-08-15
2. Richard van der Blom, LinkedIn algorithm/ad data | his research | tier 1 | 2026-08-15

## Evaluation & QA

### Common Failure Modes
- Targeting too narrow (tiny audiences, spiked CPMs, no delivery)
- Too many targeting layers excluding qualified buyers
- Lead Gen Forms without CRM routing - dead leads
- Judging campaigns on CPL alone while pipeline quality varies wildly
- No retargeting layer - LinkedIn clicks are expensive; capture the intent
- Thought Leader Ads from inactive or ghost member profiles
- Comparing LinkedIn CPL to Meta CPL directly - different funnel roles
