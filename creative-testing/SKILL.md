---
name: creative-testing
category: ad-creative
description: Run structured creative tests with volume planning, scoring, fatigue detection, and kill-scale rules.
triggers:
  - "creative testing"
  - "test ad creatives"
  - "ad fatigue"
  - "scale winning ads"
  - "creative volume matrix"
  - "kill or scale creative"
inputs:
  - campaign_data
  - creative_assets
  - budget
  - kpi_targets
outputs:
  - test_design
  - volume_matrix
  - scoring_framework
  - kill_scale_rules
  - creative_insight_library
related_skills:
  - ad-creative-generator
  - hook-frameworks
  - media-planning
  - performance-reporting
  - meta-ads
  - tiktok-ads
  - marketing-optimize/ab-testing
required_context:
  - .context/product-marketing.md
allowed_tools:
  - none
version: 1.0.0
---

## When to Use

Invoke when:
- CPA/ROAS has plateaued and needs a creative lever
- Setting up a systematic creative testing program
- Detecting ad fatigue and planning refreshes
- Deciding whether to kill or scale a creative
- Building a learning loop from ad results into new briefs

## Workflow

### Step 1: Test Strategy & Hypotheses
- State the hypothesis before the test - "audience X responds to angle Y because Z"
- Test at the right level - angle tests (problem vs solution vs social proof) before element tests (hook vs headline vs CTA)
- One variable per test cell - if testing hooks, change the hook only
- Prioritize by expected leverage - hooks and angles usually move results more than colors or buttons (heuristic)
- Log every test in a shared doc - hypothesis, design, verdict, insight

**Gate:** Each test has a written hypothesis and a single isolated variable.

### Step 2: Test Design
- Structure - control plus 2-4 variants per test; platform-native formats only
- Naming convention - `[angle]-[format]-[variant]-[date]`
- Platform learning requirements - each variant needs enough conversions within the platform's learning window (thresholds vary per platform - see meta-ads and tiktok-ads)
- Isolation - run variants in the same campaign/ad set environment with equal budgets
- Pre-register the decision date and criteria - no peeking, no mid-test edits

**Gate:** Test design documented with pre-registered decision criteria.

### Step 3: Volume & Budget Matrix
Plan spend so every variant gets a fair shot:
- Per-variant budget = target CPA x conversions needed to judge (heuristic - e.g. 20-50 conversions per variant; validate per platform)
- Total test budget = variants x per-variant budget x safety margin
- If the budget can't fund the matrix, test fewer variants - two properly funded variants beat six underfunded ones
- Map the test calendar - weekly launches, bi-weekly verdicts
- Respect platform learning phases - a test chopped up by budget edits teaches nothing

**Gate:** Volume matrix funded; test calendar laid out against budget.

### Step 4: Scoring Framework
Score every creative on a weighted scorecard (set weights per business):
- Hook rate (3s/2s holds) - attention
- Hold rate / average watch time - retention
- CTR - click interest
- CVR - landing alignment
- CPA/ROAS - the economic vote (highest weight)
- Statistical caution - score on direction plus magnitude, not tiny differences; one day of data is not a verdict
- Record qualitative signals too - comment sentiment, saves, shares

**Gate:** Scorecard weights agreed; qualitative capture wired into the process.

### Step 5: Fatigue Detection
- Frequency rising while CTR/CPA decay = fatigue (watch per-platform frequency)
- CPA creep - CPA up consistently for 3+ consecutive reporting periods
- Engagement decay - same creative, falling hook and hold rates
- Set fatigue thresholds per platform (TikTok decays faster than Search - heuristics; calibrate to your own data)
- Act before the cliff - refresh at the first signal, not at full failure
- Separate fatigue from seasonality - compare against the same period's baseline

**Gate:** Fatigue thresholds set per platform with a refresh trigger documented.

### Step 6: Kill / Scale / Iterate Rules
- **Kill** - below the scoring bar after sufficient volume (pre-registered threshold, e.g. 2x target CPA with enough conversions)
- **Iterate** - promising secondary metrics (great hook rate, weak CVR) - remix the weak element, don't discard the angle
- **Scale** - hits target at volume - scale in 20-30% budget steps with 2-3 days of observation between steps
- **Hold** - within range of target - leave untouched; don't optimize noise
- Kill rules protect budget; scale rules protect account stability
- Every verdict recorded - killed, scaled, iterated, held - with the reason

**Gate:** Decision thresholds written down and applied consistently across tests.

### Step 7: Learning Capture
- After every verdict - write one insight (what did the audience tell us) plus one brief implication
- Maintain an insight library - winning angles, hooks, formats, surfaced objections
- Feed insights into ad-creative-generator briefs and landing page copy
- Quarterly pattern review - which angles keep winning across tests
- The library compounds - testing without capture is just expensive content production

**Gate:** Insight library maintained; every test closes with an insight entry.

## Evaluation & QA

### Common Failure Modes
- Changing multiple variables at once - unreadable results
- Killing variants too early - before the conversion threshold
- Scaling too fast - algorithm shock, performance collapse
- Testing elements before angles - optimizing buttons while the premise is wrong
- No control group or pre-registered criteria - post-hoc storytelling
- Ignoring fatigue signals until CPA spikes
