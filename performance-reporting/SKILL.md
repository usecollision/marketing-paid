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

## Evaluation & QA

### Common Failure Modes
- Treating platform-reported conversions as truth (double-counting across platforms)
- Blending last-click numbers and calling it incrementality
- Ignoring MER while platform ROAS looks great - creative accounting
- No UTM standard - every platform reports differently, nothing reconciles
- Optimizing to a report instead of to revenue - reporting-induced behavior
- Diagnosing anomalies by instinct instead of running the checklist
