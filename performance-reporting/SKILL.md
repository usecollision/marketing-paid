---
name: performance-reporting
category: paid
description: Build cross-platform paid reporting with blended CAC and ROAS, MER, rollup structure, and anomaly diagnosis.
triggers:
  - "blended CAC"
  - "ROAS report"
  - "MER reporting"
  - "cross-platform performance report"
  - "anomaly diagnosis"
  - "paid media reporting"
inputs:
  - platform_exports
  - revenue_data
  - spend_data
  - kpi_targets
outputs:
  - metric_definitions
  - rollup_structure
  - report_templates
  - anomaly_diagnosis
  - action_log
related_skills:
  - media-planning
  - google-ads
  - meta-ads
  - creative-testing
  - marketing-optimize/metrics-framework
  - marketing-optimize/attribution-model-selection
  - marketing-optimize/mmm-incrementality
required_context:
  - .context/product-marketing.md
allowed_tools:
  - none
version: 1.0.0
---

## When to Use

Invoke when:
- Building a cross-platform reporting system
- Reconciling platform numbers with business revenue
- Diagnosing a sudden performance drop or spike
- Setting up blended CAC/ROAS tracking
- Preparing investor or executive reporting

## Workflow

### Step 1: Define Metrics & Formulas
Agree on definitions before building anything:
- **Spend** - media spend plus fees (platform, tools); write down what's included
- **Blended CAC** = total ad spend / total new customers attributed to ads
- **Platform CAC** = platform spend / platform-attributed new customers
- **ROAS** = revenue / spend; blended ROAS = total ad-attributed revenue / total spend
- **MER** = total business revenue / total ad spend (the truth metric - attribution-independent)
- **Contribution margin after ads** = gross margin - ad spend
- Qualified-cost metrics (nCPA, cost per MQL) where lead quality varies
- Write one formula per metric in plain language - definitional disagreement is the top cause of reporting fights

**Gate:** Metric dictionary written with one plain-language formula per metric.

### Step 2: Data Infrastructure
- Standardize UTMs across all platforms (source/medium/campaign/content)
- Export schedule - pull platform data on a fixed cadence via API or scheduled exports
- Connect revenue (Shopify, CRM, Stripe) - revenue lives outside the ad platforms
- Build a source-of-truth spreadsheet/BI with raw tabs plus rollup - never hand-edit raw data
- Store cohort columns - when the customer was acquired, not just when revenue landed
- Annotate events (tracking fixes, launch days, outages) in the data, not in Slack

**Gate:** Data pipeline runs on schedule; revenue joined to ad data.

### Step 3: Rollup Structure
Design the rollup so anyone can read it in 60 seconds:
- Tabs - daily raw, weekly rollup, monthly rollup, cohort view
- Per platform block - spend, impressions, clicks, CTR, CPM, CPC, conversions, CPA, ROAS
- Cross-platform rows - totals, blended CAC, blended ROAS, MER, contribution margin
- Funnel stage columns - demand capture vs creation vs retention
- MoM/WoW deltas plus target variance on every KPI row
- Anomaly flag column (threshold-based, with a notes field)

**Gate:** Rollup built; every KPI row carries deltas, targets, and variance.

### Step 4: Reporting Cadence & Audiences
- **Daily (operator)** - spend, pacing, platform health flags; a 5-minute scan
- **Weekly (team)** - CPA/ROAS vs targets, creative verdicts, actions from the week
- **Monthly (exec)** - blended metrics, MER, cohort trends, channel mix
- **Quarterly (investor/board)** - efficiency, payback, incrementality findings
- Each audience gets one page, three numbers, and the single decision needed from them

**Gate:** Cadence calendar set with a template per audience tier.

### Step 5: Anomaly Diagnosis Framework
When blended CPA/ROAS moves beyond the threshold (set X% per business), run the checklist in order:
1. **Tracking** - pixels/tags firing? UTM changes? platform outage? (most common cause)
2. **Spend/mix** - budget shifted? new campaign launched? bid changes?
3. **Conversion path** - landing page changed? checkout broken? site speed regression?
4. **Creative** - fatigue on a big-spend creative?
5. **Market** - competitor launch, seasonality, holidays, news cycle
6. **Audience** - saturation, frequency spike
- Document every anomaly - cause, evidence, fix, resolution date; the log compounds into a playbook

**Gate:** Threshold set; checklist run and documented for every flagged anomaly.

### Step 6: Action Protocol
- Don't change anything until diagnosis completes - reactive changes obscure the cause
- Minor variance (within threshold) - log and ignore
- Tracking issue - fix tracking, annotate the data, restate metrics retroactively where possible
- Real performance shift - reallocate per media-planning rules, refresh creative per creative-testing
- Recurring anomaly - a structural fix is due (tracking hardening, creative pipeline, landing page)
- Review the anomaly log monthly - patterns are strategy inputs, not just noise

**Gate:** Action protocol written; anomaly log reviewed monthly.

## Practitioner Grounding

The measurement hierarchy here follows Eric Seufert (ad economics/incrementality), AdMaxxer/AdSights/Metricuno (MER vs ROAS diagnostics), and the IPA effectiveness researchers (Binet & Field). Full research: practitioner-intelligence/syntheses/paid-strategy.md.

- **Seufert (T1)**: platform attribution is a "veneer of control" — multi-channel spend guarantees redundant spend. Budget decisions belong on incremental contribution (iROAS/MMM); macro (MMM/MER) and micro (campaign) measurement run on separate cadences.
- **AdMaxxer (T2, vendor)**: sum of platform ROAS typically runs 1.4-1.8x true MER — the "overlap tax". Target MER ≈ 1.3 ÷ contribution margin. A >35% gap between summed platform ROAS and MER means platform numbers are fiction.
- **AdSights/Metricuno (T2, vendor)**: iROAS divergence benchmarks — brand search reports 10x+ but true iROAS is 1.5-3x (incrementality factor ~0.10-0.25x reported); retargeting ~0.20-0.35x. Creative A/B tests are not incrementality tests.

## Decision Rules

1. IF platform ROAS and MER diverge by >35% (overlap tax) THEN treat platform ROAS as inflated — report both, allocate on MER/iROAS, and schedule an incrementality test on the diverging channels (AdMaxxer — EMPIRICAL vendor, T2).
2. IF deciding whether to cut or scale a prospecting channel THEN never use reported ROAS alone — prospecting at 1.3x reported ROAS can feed 4.5x blended MER through downstream conversion; validate with iROAS first (AdSights — EMPIRICAL vendor, T2).
3. IF MER holds while spend rises THEN scaling is real; IF blended CPA rises while MER holds THEN the mix is shifting (retargeting-heavy) — rebalance, don't panic (Seufert — FRAMEWORK, T1).
4. IF a metric anomaly appears THEN run the Step 5 checklist in order — tracking first (most common cause), spend/mix, conversion path, creative, market, audience — before any action (performance-reporting practice, T1).
5. IF reporting to executives THEN lead with MER and contribution margin, not platform ROAS — platform numbers without the overlap check mislead allocation (Seufert; AdMaxxer — T1/T2).
6. IF a brand-search or retargeting channel claims high ROAS THEN assume over-crediting until tested: brand search iROAS ~0.10-0.25x reported, retargeting ~0.20-0.35x (AdSights/Metricuno — EMPIRICAL vendor, T2).

## Metrics

- **MER (the truth metric)**: total business revenue ÷ total ad spend. Target ≈ 1.3 ÷ contribution margin. Attribution-independent — this is the P&L-level number (AdMaxxer — T2).
- **Blended ROAS**: ad-attributed revenue ÷ spend — usable for trend, not for allocation.
- **Platform ROAS**: creative/optimization decisions only (overlap-inflated for allocation).
- **Overlap tax** = sum(platform ROAS × platform spend) ÷ total revenue − 1. >35% = platform fiction (AdMaxxer — T2).
- **iROAS** (when incrementality data exists): the only allocation-grade ROAS.
- **Qualified-cost metrics** (nCPA, cost per MQL) where lead quality varies (existing practice).

## Sources

1. Eric Seufert, "Media mix models are the future of mobile advertising"; "The emerging marketing economist" | mobiledevmemo.com | tier 1 | 2026-08-14
2. AdMaxxer, "Blended MER vs ROAS: When Each Breaks" | admaxxer.com | tier 3 (vendor) | 2026-08-14
3. AdSights / Metricuno incrementality guides (iROAS benchmarks, ghost ads, test design) | vendor blogs | tier 3 | 2026-08-14
4. Binet & Field, *Effectiveness in Context* (2022), IPA | downloads.ctfassets.net | tier 1 | 2026-08-14

## Evaluation & QA

### Common Failure Modes
- Treating platform-reported conversions as truth (double-counting across platforms)
- Blending last-click numbers and calling it incrementality
- Ignoring MER while platform ROAS looks great - creative accounting
- No UTM standard - every platform reports differently, nothing reconciles
- Optimizing to a report instead of to revenue - reporting-induced behavior
- Diagnosing anomalies by instinct instead of running the checklist
