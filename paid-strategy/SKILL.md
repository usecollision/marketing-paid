---
name: paid-strategy
category: paid
description: Build a multi-platform paid media strategy with budget allocation, platform selection, and funnel design.
triggers:
  - "paid strategy"
  - "ads strategy"
  - "media buying plan"
  - "ad budget"
  - "which platforms to advertise on"
  - "paid acquisition plan"
inputs:
  - product_context
  - icp
  - budget
  - goals
outputs:
  - platform_selection
  - budget_allocation
  - funnel_architecture
  - kpi_targets
  - testing_plan
related_skills:
  - meta-ads
  - google-ads
  - media-planning
  - marketing-paid/ad-creative-generator
  - marketing-optimize/metrics-framework
  - marketing-optimize/attribution-model-selection
required_context:
  - .context/product-marketing.md
  - .context/project-context.md
allowed_tools:
  - mcp:ads-platforms
version: 1.0.0
---

## When to Use

Invoke when:
- Launching paid ads for the first time
- Scaling from one platform to multi-platform
- Budget planning and reallocation
- Performance has plateaued on current platform
- Need to determine optimal channel mix

## Workflow

### Step 1: Platform Selection
Match platforms to your ICP and goals:

| Platform | Best For | Avg CAC | Min Budget | Targeting | Funnel Stage |
|----------|---------|---------|-----------|-----------|-------------|
| Meta (FB/IG) | B2C, DTC, broad audiences | Variable | /mo | Interest/behavior/lookalike | Full funnel |
| Google Search | High-intent buyers | -500 | /mo | Keyword intent | Bottom funnel |
| Google Display | Retargeting, awareness | -50 | /mo | Audiences/placements | Top/mid funnel |
| LinkedIn | B2B, enterprise, SaaS | -200 | /mo | Title/company/industry | Mid/bottom |
| X/Twitter | Tech, creators, news | -100 | /mo | Interest/follower lookalike | Top/mid |
| Reddit | Niche communities, tech | -80 | /mo | Subreddit/interest | Top/mid |
| TikTok | Gen Z, B2C, awareness | -30 | /mo | Interest/behavior | Top funnel |
| YouTube | Education, consideration | -50 | /mo | Intent/affinity | Mid funnel |

**Selection criteria:**
1. Where does your ICP spend time? (confirmed by research)
2. What funnel stage are you optimizing for?
3. Does your budget meet minimum thresholds?
4. Do you have creative assets for this platform?

**Gate:** 2-3 platforms selected with clear rationale tied to ICP and budget.

### Step 2: Budget Allocation
Distribute budget across platforms and funnel stages:

**Budget framework:**
- 60-70% → Primary platform (highest confidence)
- 20-30% → Secondary platform (testing/diversifying)
- 10% → Experimentation (new platforms, creative tests)

**Funnel allocation:**
- Prospecting (cold): 50-60% of budget
- Retargeting (warm): 20-30% of budget
- Retention/upsell (hot): 10-20% of budget

| Platform | Monthly Budget | Prospecting | Retargeting | Testing |
|----------|---------------|-------------|-------------|---------|
| [Platform 1] | $ | $ | $ | $ |
| [Platform 2] | $ | $ | $ | $ |
| Experimentation | $ | | | $ |
| **Total** | $ | | | |

**Gate:** Budget adds up, minimums met per platform, testing budget reserved.

### Step 3: Funnel Architecture
Design the ad funnel per platform:

`
TOFU (Awareness/Prospecting)
├── Audiences: Broad interests, lookalikes, competitor audiences
├── Creative: Educational content, hooks, brand awareness
├── Goal: Clicks, video views, engagement
├── Metric: CPM, CTR, CPC
│
MOFU (Consideration/Retargeting)
├── Audiences: Website visitors, engagers, video viewers
├── Creative: Case studies, demos, social proof, offers
├── Goal: Leads, signups, demo requests
├── Metric: CPL, conversion rate
│
BOFU (Decision/Conversion)
├── Audiences: High-intent visitors, cart abandoners, free trial users
├── Creative: Testimonials, urgency, direct offer, comparison
├── Goal: Purchases, paid conversions
├── Metric: CPA, ROAS
`

**Gate:** Full funnel designed with audiences, creative needs, and metrics per stage.

### Step 4: KPI Targets & Tracking
Set specific targets:

| Metric | Target | Benchmark | Measurement |
|--------|--------|-----------|-------------|
| CPC | $ | Industry avg | Platform reporting |
| CTR | X% | 1-3% | Platform reporting |
| CPL/CPA | $ | Based on LTV/CAC math | Attribution |
| ROAS | Xx | Break-even + margin | Revenue / Spend |
| Frequency | <X | 2-3 per week | Platform reporting |

**LTV/CAC math:**
- Target CAC = LTV x (1 / payback months) x margin %
- Break-even ROAS = 1 / margin %
- Target ROAS = Break-even x target multiplier

**Gate:** Every metric has a specific target backed by unit economics.

### Step 5: Testing Plan
Structure initial tests:

**Week 1-2:** Platform and audience validation
- 3-5 audience variants per platform
- Same creative across audiences (isolate audience variable)
- -100/day per audience minimum

**Week 3-4:** Creative testing
- Winner audiences from Week 1-2
- 3-5 creative variants (different hooks, angles, formats)
- Isolate creative variable

**Ongoing:**
- Kill losers at 2x target CPA with statistical significance
- Scale winners by 20-30% budget increases (not more)
- Refresh creative every 2-4 weeks (before fatigue)

**Gate:** Testing plan with clear variables, sample sizes, and decision criteria.

## Practitioner Grounding

This skill's decision layer is built from the IPA effectiveness research (Binet & Field), Ehrenberg-Bass laws (Byron Sharp), two-speed planning (Mark Ritson), ad-economics/incrementality (Eric Seufert), and B2B budget practice (Chris Walker/Refine Labs, Stackmatix, Spike). Full research: practitioner-intelligence/syntheses/paid-strategy.md.

- **Binet & Field (researchers, T1)**: brand and activation are complementary; the aggregate optimum brand:activation split is now ~62:38 and varies by sector — there is NO universal ratio. Their most counterintuitive empirical finding: **when brand building is hard (high-consideration/rational categories), spend MORE on brand, not more on activation.** Long-term brand investment delivers ~2x the profit of short-term-only; whole-market targeting ~3x the effect of existing-customer targeting; emotional creative ~2x as efficient as rational.
- **Byron Sharp (researcher, T1)**: growth comes from penetration, not loyalty. Double jeopardy law: bigger brands have more buyers AND slightly higher loyalty. Brand media should reach category buyers broadly — never think small/low-reach even on limited budgets. Mental availability (memory structure) ≠ awareness.
- **Mark Ritson (educator, T1)**: plan in 12-month increments: diagnosis → strategy → tactics. Brand stream = whole market; activation stream = selected segments. Hold the split for years, not quarters. Stop measuring brand with dollar-ROI estimates — use brand-effect metrics.
- **Eric Seufert (analyst, T1)**: multi-channel spend guarantees redundant (overlapping) spend — platform attribution is a "veneer of control". Allocate against incremental contribution (iROAS/MMM), not attributed ROAS. Run macro measurement (MMM/MER, monthly/quarterly) and micro optimization (weekly) as separate cadences. Set payback window by cash position, not product potential.
- **Chris Walker / Refine Labs (practitioner, T2)**: B2B working model — Brand 20-30% / Demand 50-60% / Expand 10-20%; founder-led organic content counts as brand at low cost. Diagnose with the "budget truth" audit: map the last 2 quarters of inbound revenue to real source and compare to budget split.
- **Francois/Stackmatix (practitioner, T2)**: stage-based ratios — pre-PMF/early stage runs 30/70-20/80 (brand/activation); 60/40 is "roughly wrong" until channels, positioning, and measurement are validated. Review the split annually, not quarterly.

## Decision Rules

1. IF pre-PMF / cash-constrained / <12-18 months runway THEN set brand ceiling at 20-30% of budget, run performance-led, and set the payback window by cash position (Seufert; Francois — HEURISTIC, T2).
2. IF established brand with validated channels and 3+ year payback tolerance THEN start at ~62:38 brand:activation; IF high-consideration/rational category OR online-first business THEN RAISE brand share; IF low-consideration/emotional or travel-like category THEN lower it (Binet & Field — EMPIRICAL, T1).
3. IF B2B THEN baseline 46% brand / 54% activation (Binet & Field — EMPIRICAL, T1), or working model Brand 20-30% / Demand 50-60% / Expand 10-20% with founder-led organic counted as brand (Walker — HEURISTIC, T2). Condition: sales-cycle length and whether sales covers the activation job.
4. IF budget is below the minimum viable spend for paid reach in the medium THEN do NOT force paid brand reach — shift the brand job to cheap brand assets (founder narrative, content, distinctive assets) (Sharp; Stackmatix — EMPIRICAL/HEURISTIC, T1/T2).
5. IF allocating the brand stream THEN target the whole market/category buyers, NOT existing customers or lookalike loyalty segments (Binet & Field 3x finding; Sharp penetration law — EMPIRICAL, T1).
6. IF deciding whether to cut a channel on platform ROAS THEN do not — never cut prospecting on reported ROAS alone; validate incrementality first (AdSights — EMPIRICAL vendor, T2).
7. IF a channel's iROAS falls below contribution-margin breakeven after a valid incrementality test THEN cut or reallocate (Seufert — FRAMEWORK, T1).
8. IF evaluating a scaling decision THEN use the 3-of-4 kill criteria: conversion volume insufficient, CAC > 2x target, declining marginal returns, team-time drain (Spike — HEURISTIC, T2).
9. IF revisiting the split THEN review annually against stage, never quarterly on ROI swings; long-term effects only show over 3+ years (Ritson; Francois — HEURISTIC, T1/T2).
10. IF the overlap tax (sum of platform ROAS×spend ÷ total revenue − 1) exceeds ~35% THEN platform ROAS is materially inflated — require iROAS/MMM before reallocating on reported numbers (AdMaxxer — EMPIRICAL vendor, T2).

## Metrics

- **MER (media efficiency ratio)** at P&L level: total revenue ÷ total ad spend. Target ≈ 1.3 ÷ contribution margin. If MER holds while spend rises, keep scaling; a >10% MER drift jump signals overlap/retargeting problems (AdMaxxer — EMPIRICAL vendor, T2).
- **Platform ROAS**: optimization and creative decisions only — NOT budget allocation. Sum of platform ROAS is typically 1.4-1.8x true MER (overlap tax).
- **iROAS / incrementality**: budget allocation decisions. Benchmarks (directional): brand search iROAS ~0.10-0.25x reported; retargeting ~0.20-0.35x reported (AdSights/Metricuno — EMPIRICAL vendor, T2).
- **Brand effects** (for the brand stream): mental availability / distinctive asset recognition, share of search, branded query volume — not dollar ROI (Ritson — FRAMEWORK, T1).
- **Cadence**: macro (MMM/MER) monthly/quarterly; micro (creative, audiences) weekly — separate loops, separate owners (Seufert — FRAMEWORK, T1).

## Sources

1. Binet & Field, *Effectiveness in Context* (2022), IPA | downloads.ctfassets.net | primary report | tier 1 | 2026-08-14
2. Binet & Field, *The Long and the Short of It* (2013), Thinkbox summary | thinkbox.tv | tier 1 | 2026-08-14
3. IPA blog, "Three common mistakes in awards entries" | ipa.co.uk | tier 1 | 2026-08-14
4. Byron Sharp / Ehrenberg-Bass, "Mental availability is not awareness", "What causes the Double Jeopardy law?", "Answering critics" | marketingscience.info | tier 1 | 2026-08-14
5. Mark Ritson, "Can you achieve long and short at the same time? Usually, no"; "Planning for marketing planning: 14 steps"; "Three axioms and three questions that summarise all of brand strategy" | marketingweek.com | tier 1 | 2026-08-14
6. Eric Seufert, "Media mix models are the future of mobile advertising"; "The emerging marketing economist" | mobiledevmemo.com | tier 1 | 2026-08-14
7. Chris Walker / Refine Labs, "How to Budget Across Brand, Demand, and Expand" | refinelabs.com | tier 1 | 2026-08-14
8. AdMaxxer, "Blended MER vs ROAS: When Each Breaks" | admaxxer.com | tier 3 (vendor) | 2026-08-14
9. AdSights / Metricuno incrementality guides (sample sizes, iROAS benchmarks, ghost ads) | vendor blogs | tier 3 | 2026-08-14

## Evaluation & QA

### Common Failure Modes
- Spreading budget too thin across too many platforms
- No retargeting layer (losing warm traffic)
- Scaling too fast (algorithm shock)
- Not testing creative systematically (changing too many variables)
- Ignoring frequency/fatigue (burning out audiences)
- Optimizing for wrong metric (clicks instead of conversions)

### Practitioner-Sourced Failure Modes
- **Over-investing in bottom-funnel demand capture** beyond diminishing returns — e.g. scaling Google Ads to $1M/mo with a 36-month CAC payback (Walker, T2); redundant multi-channel spend is guaranteed once >1 channel runs without incrementality checks (Seufert, T1).
- **Brand starvation via the 12-month ROI trap**: under-investing in awareness because it doesn't show in quarterly ROI — online brands run 56% brand vs 62% optimum (Binet & Field, T1; Ritson, T1).
- **Attribution-driven misallocation**: cutting/keeping channels on platform ROAS when overlap inflates it 1.4-1.8x; brand search reporting 10x+ vs true iROAS of 1.5-3x (AdMaxxer/Metricuno, T2). Use the overlap-tax check (Rule 10).
- **Underfunded tests**: "underfunded tests are the #1 reason channel strategies fail" (Spike, T2); underpowered incrementality tests produce inconclusive CIs (AdSights, T2).
- **Fixed splits never revisited**: "fixed splits applied to changing businesses is how marketing investment quietly underperforms for years" (Francois, T2).
- **Loyalty-marketing-as-growth**: retention-heavy strategies have no empirical justification; growth comes from penetration (Sharp, T1; Binet & Field, T1).