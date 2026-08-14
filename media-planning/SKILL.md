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

## Practitioner Grounding

This skill's decision layer is built from the IPA effectiveness research (Binet & Field), Ehrenberg-Bass laws (Byron Sharp), two-speed planning (Mark Ritson), ad-economics/incrementality (Eric Seufert), and lean-team budget practice (Spike, Stackmatix). Full research: practitioner-intelligence/syntheses/paid-strategy.md.

- **Binet & Field (T1)**: no universal brand:activation ratio — aggregate optimum ~62:38; **rational/high-consideration categories need MORE brand**, online-first businesses need MORE brand; long-term brand ~2x profit of short-term-only; whole-market targeting ~3x of existing-customer targeting.
- **Byron Sharp (T1)**: growth comes from penetration — the brand stream must reach category buyers broadly; never think small/low-reach even on limited budgets; double jeopardy means loyalty work doesn't grow brands.
- **Mark Ritson (T1)**: plan in 12-month increments: diagnosis → strategy → tactics. Segmentation = market map; targeting = strategy. Brand stream = whole market, activation stream = selected segments. Hold the split for years.
- **Eric Seufert (T1)**: allocate against incremental contribution (iROAS/MMM), not attributed ROAS; macro measurement (MMM/MER) monthly/quarterly, micro optimization weekly; payback window by cash position.
- **Spike (T2)**: lean-team split — 60-70% primary channel / 20-30% compounding / ≤10% experiments, all above minimum viable spend thresholds; "underfunded tests are the #1 reason channel strategies fail."

## Decision Rules

1. IF budget < minimum viable spend for the medium THEN do not spread — one primary channel (usually search or Meta), and shift the brand job to cheap brand assets instead of paid reach (Spike; Sharp — HEURISTIC/EMPIRICAL, T2/T1).
2. IF designing the mix THEN allocate by expected conversion counts per channel per week, not dollars — a channel needs enough conversions to optimize, not enough dollars to spend (Spike — HEURISTIC, T2).
3. IF the business is established with 3+ year payback tolerance THEN set brand:activation near 62:38; IF high-consideration/rational category or online-first THEN raise brand share; IF low-consideration/emotional THEN lower (Binet & Field — EMPIRICAL, T1).
4. IF the brand stream is being planned THEN target whole-market/category buyers with reach, never existing-customer segments (Sharp; Binet & Field — EMPIRICAL, T1).
5. IF a channel fails the CAC ceiling after sufficient data (see creative-testing volume thresholds) THEN kill; IF MER holds while spend rises THEN keep scaling; IF blended CPA rises as spend grows THEN reallocate before adding net-new budget (media-planning heuristics + Seufert — T1/T2).
6. IF a scaling channel has no incrementality evidence THEN test it (geo-lift or ghost ads) before budget increases; brand search and retargeting are the two channels most likely to be over-credited (Seufert; AdSights — EMPIRICAL, T1/T2).
7. IF reallocating THEN move budget in 20-30% steps, never wholesale flips; review split annually against stage, not quarterly on ROI swings (Ritson; Francois — HEURISTIC, T1/T2).
8. IF MER drifts >10% between periods THEN investigate overlap/retargeting inflation before trusting platform reports (AdMaxxer — EMPIRICAL vendor, T2).

## Metrics

- **MER at P&L level**: total revenue ÷ total ad spend; target ≈ 1.3 ÷ contribution margin (AdMaxxer — EMPIRICAL vendor, T2). Primary budget-health metric.
- **Platform ROAS**: creative/optimization decisions only — overlap inflates it 1.4-1.8x vs true MER (AdMaxxer — T2).
- **iROAS**: budget decisions. Directional benchmarks: brand search iROAS ~0.10-0.25x reported, retargeting ~0.20-0.35x (AdSights/Metricuno — T2).
- **Brand stream**: mental availability / distinctive asset recognition, share of search, branded query volume — never dollar ROI (Ritson — FRAMEWORK, T1).
- **Incrementality test minimums**: 5-15k users per arm (digital lift), 6-8 matched geos with pre-test baseline (geo) (AdSights/Metricuno — EMPIRICAL vendor, T2).

## Sources

1. Binet & Field, *Effectiveness in Context* (2022), IPA | downloads.ctfassets.net | tier 1 | 2026-08-14
2. Binet & Field, *The Long and the Short of It* (2013), Thinkbox summary | thinkbox.tv | tier 1 | 2026-08-14
3. Byron Sharp / Ehrenberg-Bass, "Mental availability is not awareness"; "What causes the Double Jeopardy law?" | marketingscience.info | tier 1 | 2026-08-14
4. Mark Ritson, "Planning for marketing planning: 14 steps to an effective presentation"; "Can you achieve long and short at the same time? Usually, no" | marketingweek.com | tier 1 | 2026-08-14
5. Eric Seufert, "Media mix models are the future of mobile advertising" | mobiledevmemo.com | tier 1 | 2026-08-14
6. AdMaxxer, "Blended MER vs ROAS: When Each Breaks" | admaxxer.com | tier 3 (vendor) | 2026-08-14
7. AdSights / Metricuno incrementality guides | vendor blogs | tier 3 | 2026-08-14

## Evaluation & QA

### Common Failure Modes
- Spreading a small budget across five channels - none exit learning
- Allocating by industry averages instead of your own funnel data
- No demand-creation layer - capture-only plans stall as demand plateaus
- Ignoring creative capacity - channels without an asset pipeline underperform
- Reallocating too fast - judging channels before they exit learning
- No incrementality checks - scaling channels that just steal organic demand
