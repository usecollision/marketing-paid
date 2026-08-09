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
  - google-ads-audit
  - marketing-ad-creative/ad-creative-generator
  - marketing-analytics/metrics-framework
  - marketing-attribution/attribution-model-selection
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

## Evaluation & QA

### Common Failure Modes
- Spreading budget too thin across too many platforms
- No retargeting layer (losing warm traffic)
- Scaling too fast (algorithm shock)
- Not testing creative systematically (changing too many variables)
- Ignoring frequency/fatigue (burning out audiences)
- Optimizing for wrong metric (clicks instead of conversions)