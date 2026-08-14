---
name: snapchat-ads
category: paid
description: Launch Snapchat Ads for young audiences with AR Lens creative, full-screen ad formats, and separate ecommerce and brand campaign playbooks.
triggers:
  - "Snapchat Ads"
  - "Snap ad campaign"
  - "AR Lens ads"
  - "Snapchat ecommerce"
  - "Gen Z advertising"
  - "advertise on Snapchat"
  - "Snapchat audience targeting"
inputs:
  - product_context
  - icp
  - age_data
  - creative_assets
  - budget
  - conversion_data
outputs:
  - channel_fit_assessment
  - campaign_structure
  - ad_format_plan
  - lens_creative_briefs
  - targeting_plan
  - measurement_plan
related_skills:
  - paid-strategy
  - tiktok-ads
  - ad-creative-generator
  - hook-frameworks
  - creative-testing
  - media-planning
required_context:
  - .context/product-marketing.md
allowed_tools:
  - none
version: 1.0.0
---

## When to Use

Invoke when:
- Reaching a 13-34 demographic at scale, especially under-25 (heuristic - verify current platform demographics before planning)
- Launching AR Lens experiences for brand engagement
- Running ecommerce campaigns for Gen Z-focused DTC products
- Building brand campaigns where immersive, full-screen creative matters
- Testing Snapchat as a cheaper complement to TikTok/Meta for young audiences
- Activating around moments (events, launches, campus life)

## Workflow

### Step 1: Channel Fit & Audience Reality Check
- [ ] Verify your ICP's actual presence - Snapchat's core skews young, toward under-25 in many markets (check current platform data rather than assuming)
- [ ] Decide the job - Snapchat is stronger for brand engagement and cheap reach than for mature direct response (heuristic - validate per vertical)
- [ ] Check creative capacity - Snapchat demands native vertical video and AR; if you can't produce it, the channel won't work
- [ ] Frame the KPI - engagement, lens plays, video views, or assisted conversions over strict ROAS
- [ ] Frame the budget - test-and-learn or brand layer, rarely the performance backbone

**Gate:** Fit assessment with audience evidence and creative capacity check.

### Step 2: Ad Formats
- **Snap Ads** - full-screen vertical video; the core unit
- **Story Ads** - branded tile in the Discover feed leading to a collection
- **Collection Ads** - four-product showcase for ecommerce
- **Commercials** - 6-second, non-skippable, premium placement
- **AR Lenses** - sponsored filters; the engagement machine
- **Dynamic Product Ads** - catalog-driven retargeting for ecommerce
- Default rule - Snap Ads with a 3-second hook for direct response; Lenses for brand engagement

**Gate:** Format per objective; ecommerce accounts have catalog ads planned.

### Step 3: Lens & AR Creative
- [ ] Design for the camera, not the ad - Lenses are played with, not watched; utility and delight win
- [ ] Keep interactions instant - a user should get the payoff in 2-3 seconds (heuristic)
- [ ] Brand subtly - logo inside the Lens experience, not the opening frame
- [ ] Plan for shareability - Lenses compound through organic shares; measure plays and shares, not clicks
- [ ] Budget realistically - Lenses cost more to produce; reserve for brand moments or tentpoles, not always-on

**Gate:** Lens concept with interaction design and shareability rationale before production spend.

### Step 4: Targeting & Placement
- [ ] Age and location - the basic dials; Snapchat age buckets are coarse
- [ ] Lifestyle categories and Snapchat Life Stages - platform-native interest segments
- [ ] Lookalikes - from engagers, site visitors, customers
- [ ] Retargeting - site visitors and video viewers via the Snap Pixel
- [ ] Keep targeting loose - Snapchat's auction needs volume; heavy layering kills delivery on a smaller platform

**Gate:** Targeting plan per ad set with audience-size estimates.

### Step 5: Ecommerce Playbook
- [ ] Install the Snap Pixel first - conversions, retargeting, and lookalikes all depend on it
- [ ] Run Dynamic Product Ads for retargeting once catalog data flows
- [ ] Creative - UGC-style vertical video with the hook in frame one; native Snapchat energy, not repurposed TV
- [ ] Start with purchase-optimized Snap Ads, layer Collection Ads for browsing
- [ ] Expect lower volume than Meta - treat Snapchat as an incremental channel and judge it on marginal CAC (heuristic)

**Gate:** Pixel live, catalog connected, UGC-style creative set produced.

### Step 6: Brand Campaign Playbook
- [ ] Objective - awareness and engagement, measured by reach, video views, and lens plays
- [ ] Use Commercials for guaranteed-reach moments; Snap Ads for always-on
- [ ] Anchor campaigns to Lenses - they are the platform's differentiated brand format
- [ ] Measure brand lift with Snapchat's brand-lift studies or third-party equivalents
- [ ] Don't force direct-response KPIs on brand campaigns - agree on the metric before launch

**Gate:** Brand campaign KPI agreed; at least one differentiated Snapchat-native format (Lens or Commercial) in plan.

### Step 7: Measurement & Iteration
- [ ] Review weekly - hook rates (3-second view-through), engagement, and pixel conversions
- [ ] Kill creative fast - vertical video fatigue on Snapchat is real; refresh hooks every 1-2 weeks during scaling (heuristic)
- [ ] Compare against TikTok - same audience band, different algorithm; share learnings, not budgets
- [ ] Watch placement quality - exclude low-quality content categories for brand safety

**Gate:** Dashboard built; creative refresh cadence scheduled.

## Practitioner Grounding & Decision Rules

Built from Common Thread Collective (Snapchat-published Quay Sunglasses case + 4-brand portfolio), Measured (incrementality vendor), Affinco (small-budget benchmarks), Snap Ads API docs. Full research: practitioner-intelligence/syntheses/paid-longtail.md.

- **The open window: underpriced Gen-Z CPMs + mature Dynamic Product Ads** — "has a shelf life; once enough brands figure out the playbook, CPMs normalize" (CTC — OPINION/EMPIRICAL, T2).
- **DPA outperforms static**: Quay BFCM 2025: +40% ROAS vs non-dynamic, 2.86x CTR at 67% lower CPC, 131% lower cost per purchase; portfolio 8.7x blended ROAS (range 3.6-12.8x by vertical) (CTC/Snap — EMPIRICAL, T2).
- **Most brands fail by running Snap like a smaller Meta** — same creative, bidding, structure "almost never works"; Snap rewards native, product-forward content (CTC — CONSENSUS, T2).
- **Warm-up is mandatory**: ramp pre-peak so the algorithm arrives with context; cold Q4 launches underperform (CTC — HEURISTIC, T2).
- **Small budgets: broad targeting + auto-bid beats over-segmentation**; min daily spend ~$5 (Affinco — HEURISTIC, T3).
- **Attribution: 28-day click / 1-day view** windows; view-through inflates — judge click-through for small budgets (Affinco — HEURISTIC, T3).
- **AR Lenses are a brand format, not direct response**: billed per impression (second-price auction, swipe = impression), play-time/shares are the KPIs; premium lenses cost £450k+/day (Snap docs/Affinco — FRAMEWORK, T2).
- Third-party validation: median incremental ROAS on Snapchat grew 104% between Measured test periods (Snap Q1 2026 — T2).

Decision rules:
1. IF DTC fashion/beauty/accessories/lifestyle targeting Gen Z THEN test Snap with DPAs + native creative before writing it off (CTC — EMPIRICAL, T2).
2. IF launching Snap THEN warm up 3-6 weeks pre-peak; never cold-launch in Q4 (CTC — HEURISTIC, T2).
3. IF budget < $50/day THEN use broad targeting + auto-bid, one format at a time (Affinco — HEURISTIC, T3).
4. IF running direct response THEN use Dynamic Catalog Ads and measure click-through conversions (28-day), not view-through (CTC/Affinco — HEURISTIC, T2).
5. IF buying AR Lenses THEN fund from the brand/reach pool with play-time + shares + recall KPIs, never CPA targets (Snap docs/Affinco — FRAMEWORK, T2).
6. IF Snap ROAS < 3x after warm-up and native creative THEN the approach failed — fix approach, not budget (CTC — EMPIRICAL, T2).

## Metrics

- **DPA click-through ROAS (28-day)** as primary (CTC — HEURISTIC, T2).
- **Blended portfolio ROAS** 3.6-12.8x by vertical as sanity band (CTC — EMPIRICAL, T2).
- **Warm-up completion + learning-phase stability** before scaling.
- **Guardrail**: view-through conversions flagged as inflated; post-click landing page quality as conversion gate (Funnelish — T3).
- **Timebox**: verdict after warm-up + 4-6 weeks steady state.

## Sources

1. Common Thread Collective, Snapchat wrote a case study about our work (Quay) | commonthreadco.com | tier 1 | 2026-08-15
2. Snap for Business, Quay Sunglasses success story | forbusiness.snapchat.com | tier 2 | 2026-08-15
3. Snap Developers, AR Lenses Ads API docs | developers.snap.com | tier 1 | 2026-08-15
4. Affinco, Small Budget Snapchat Ads | affinco.com | tier 3 | 2026-08-15
5. Funnelish, Snapchat Ads worth it in 2026? | funnelish.com | tier 3 | 2026-08-15
6. Snap Q1 2026 earnings (Measured iROAS +104%) | finance.yahoo.com | tier 2 | 2026-08-15

## Evaluation & QA

### Common Failure Modes
- Repurposing TV or horizontal ads - full-screen vertical is non-negotiable
- Targeting too narrowly on a volume-thin platform
- Judging brand Lenses on clicks - the format's value is plays and shares
- Launching ecommerce without the Pixel - flying blind from day one
- Assuming Snapchat demographics without checking current data
- Expecting Meta-level purchase volume - measure marginal contribution instead
