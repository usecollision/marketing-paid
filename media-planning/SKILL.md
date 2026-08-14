---
name: media-planning
category: paid
description: Allocate a paid media budget across channels with channel mix design, budget math, and incrementality checks.
triggers:
  - "where should I spend my ad budget"
  - "media plan"
  - "channel mix"
  - "budget allocation"
  - "media buying plan"
  - "which platforms for my budget"
inputs:
  - budget
  - icp
  - goals
  - historical_performance
  - product_context
outputs:
  - channel_mix
  - budget_allocation_table
  - testing_plan
  - kpi_targets
  - reallocation_rules
related_skills:
  - paid-strategy
  - performance-reporting
  - creative-testing
  - google-ads
  - meta-ads
  - marketing-optimize/metrics-framework
  - marketing-optimize/mmm-incrementality
required_context:
  - .context/product-marketing.md
allowed_tools:
  - none
version: 1.0.0
---

## When to Use

Invoke when:
- Answering "I have $X budget, where do I spend it"
- Reallocating budget across platforms quarterly
- Entering a new channel or scaling an existing one
- Planning a launch budget
- Performance has plateaued and the mix needs rethinking

## Workflow

### Step 1: Define Goals & Constraints
Before any channel math:
- Primary KPI (purchases, leads, signups) with a numeric target
- CAC/CPA ceiling derived from unit economics (LTV, margin, payback period)
- Budget total, plus minimum viable thresholds per channel
- Timeline and seasonality (launch windows, sales cycles)
- Creative production capacity - channels live or die on creative supply
- Measurement maturity - per-channel attribution, or blended-only

**Gate:** Single north-star KPI with a numeric target and a CAC ceiling.

### Step 2: Score Candidate Channels
Rate each channel 1-5 on: ICP presence, intent level, expected cost efficiency (your data first; cautious industry heuristics second), creative requirements, measurement quality, learning speed.
Weight scores by goal type:
- Demand capture (Search, Amazon) - high intent score
- Demand creation (Meta, TikTok, YouTube) - high reach and creative-scale score
- Niche B2B (LinkedIn, Reddit) - high ICP precision score
Score honestly - a channel you can't produce creative for is a channel you can't run.

**Gate:** Every candidate channel scored with a written rationale, not vibes.

### Step 3: Budget Math
Work backwards from the target:
- Required conversions = spend target / CAC ceiling
- Per channel - expected conversions = channel budget / expected CPA (from your data or labeled heuristics)
- Allocation shape - 60-70% proven channels, 20-30% scaling channels, 10% experiments
- Every channel must clear its minimum viable budget (heuristic - a sub-minimum channel never exits learning; label the threshold per platform)
- Funnel coverage - roughly 50-60% demand capture, 30-40% demand creation, ~10% retention/defense (framework - adjust per business)
- Sanity-check the math both directions - top-down allocation vs bottom-up conversion needs must reconcile

**Gate:** Budget table adds up, minimums met per channel, experiment budget reserved.

### Step 4: The "I Have X Budget" Framework
Tier the answer by budget size (all tiers are heuristics - the real constraint is conversions per channel per week, not dollars):
- **Small (roughly under ~$3k/mo)** - one channel only, usually search or Meta; spreading kills learning
- **Medium (~$3-10k/mo)** - one primary plus one retargeting/experiment channel
- **Growth (~$10-50k/mo)** - 2-3 channels with full funnel coverage and structured creative testing
- **Scale ($50k+/mo)** - full-funnel multi-channel plus incrementality testing
A channel needs enough conversions to optimize, not enough dollars to spend - always convert budget into expected conversion counts before comparing.

**Gate:** Budget tier identified; the recommended channel set matches the tier.

### Step 5: Funnel Coverage Map
For each channel, map: funnel stage, audience, job to be done, KPI, and its handoff to the next stage:
- Search/Amazon capture existing demand
- Meta/TikTok/YouTube create demand and feed retargeting pools
- Retargeting converts warm traffic everywhere
- A mix without demand creation starves the funnel over time; a mix without capture wastes created demand
- Every channel needs a stated job - "scale" is not a job

**Gate:** Funnel map complete with handoffs between stages defined.

### Step 6: Incrementality & Diminishing Returns
- Track MER (total revenue / total ad spend) at the business level - if MER holds while spend rises, keep scaling
- Watch diminishing returns - rising blended CPA as spend grows signals saturation
- Run geo-lift or holdout tests on scaling channels (see mmm-incrementality)
- Ask per channel - would these conversions have happened anyway (brand search, retargeting)?
- Reallocate from saturated channels before adding net-new budget

**Gate:** MER baseline set; a holdout test planned for the largest scaling channel.

### Step 7: Milestones & Reallocation Rules
- Review cadence - 2-week check-ins, 30-day reallocation, quarterly mix rethink
- Kill criteria per channel - fails the CAC ceiling after sufficient data (see creative-testing for volume thresholds)
- Scale criteria - hits target at volume, MER stable, incrementality test passed
- Reallocation rule - move budget in 20-30% steps, never wholesale flips
- Always protect the 10% experiment budget - that's the next channel being born

**Gate:** Milestone calendar set with kill/scale/reallocation criteria written down.

## Evaluation & QA

### Common Failure Modes
- Spreading a small budget across five channels - none exit learning
- Allocating by industry averages instead of your own funnel data
- No demand-creation layer - capture-only plans stall as demand plateaus
- Ignoring creative capacity - channels without an asset pipeline underperform
- Reallocating too fast - judging channels before they exit learning
- No incrementality checks - scaling channels that just steal organic demand
