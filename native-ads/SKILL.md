---
name: native-ads
category: paid
description: Plan native advertising on Taboola and Outbrain with headline-driven creative testing, traffic quality assessment, and native vs display economics.
triggers:
  - "native ads"
  - "Taboola"
  - "Outbrain"
  - "content recommendation ads"
  - "native advertising"
  - "sponsored content ads"
  - "traffic quality native"
inputs:
  - product_context
  - content_assets
  - budget
  - conversion_data
  - target_metrics
outputs:
  - channel_fit_assessment
  - platform_selection
  - campaign_structure
  - headline_testing_plan
  - traffic_quality_plan
  - measurement_plan
related_skills:
  - paid-strategy
  - media-planning
  - creative-testing
  - performance-reporting
  - hook-frameworks
  - ad-creative-generator
  - marketing-messaging/content-strategy
required_context:
  - .context/product-marketing.md
allowed_tools:
  - none
version: 1.0.0
---

## When to Use

Invoke when:
- Buying native placements on Taboola, Outbrain, or similar content-recommendation networks
- Scaling content distribution to article-level traffic at economics below premium display (heuristic - verify per publisher mix)
- Testing headline-driven creative where the headline is most of the ad
- Building top-of-funnel volume for content marketing or lead magnets
- Assessing whether native traffic quality justifies the spend

## Workflow

### Step 1: Economics - Native vs Display
- [ ] Understand the trade - native recommendation inventory is cheaper per click than premium display, more abundant, and lower-intent (heuristic - validate per network and publisher blocklist)
- [ ] Frame expectations - native is a top-of-funnel volume engine, not a mid-funnel converter
- [ ] Pick the right KPI - CPM/CPC for reach, but cost-per-qualified-visitor or cost-per-lead for performance
- [ ] Decide the offer - content, lead magnets, or list building work; direct sales pages usually underperform on native (heuristic)

**Gate:** Economics modeled with explicit traffic-quality assumptions.

### Step 2: Platform Selection
- **Taboola** - largest publisher network, broad reach, strong in news and entertainment publishers
- **Outbrain** - similar network, strong in premium news and editorial contexts
- **Others** - Yahoo native, Revcontent, MGID (lower quality tiers - verify inventory before spend)
- Selection criteria - publisher list quality, blocklist control, brand safety verification, and self-serve UI maturity
- Run a head-to-head test if budget allows - same creatives, both networks, one winner

**Gate:** Platform chosen with publisher-quality rationale; blocklists planned.

### Step 3: Creative - Headline-Driven CTR
Native creative is a headline contest first, image second:
- [ ] Write 10-20 headline variants per offer - the headline is most of the CTR (heuristic - test to confirm per campaign)
- [ ] Use proven headline patterns - curiosity gaps, numbered lists, contrarian takes, specificity over superlatives (heuristic patterns - validate with your own tests)
- [ ] Match the thumbnail - image and headline must promise the same thing or CTR collapses
- [ ] Keep landing continuity - the ad promise must survive the click; native users bounce hard on bait-and-switch
- [ ] Rotate aggressively - fatigue on recommendation feeds is fast; refresh headlines weekly at scale

**Gate:** Headline matrix (10+ variants per offer) with thumbnail pairing and landing-continuity check.

### Step 4: Campaign Setup & Targeting
- [ ] Publisher-level targeting - blocklist low-quality sites from day one
- [ ] Contextual/interest targeting - topic categories and page-level context
- [ ] Retargeting - site visitors via network pixels for lower-funnel native
- [ ] Geo, device, and daypart basics - mobile dominates recommendation feeds; set mobile-first bids (heuristic - verify per campaign)
- [ ] Frequency caps - recommendation feeds repeat; cap to avoid fatigue

**Gate:** Campaign live with publisher blocklist applied and mobile bid adjustments set.

### Step 5: Traffic Quality Assessment
- [ ] Define quality signals - bounce rate, time on page, pages per session, and conversion depth, measured in your analytics
- [ ] Compare by publisher - export placement-level reports; the same creative converts wildly differently by site (heuristic)
- [ ] Build and grow the blocklist - kill placements that send high-bounce, zero-conversion traffic
- [ ] Watch for bot patterns - suspicious session consistency, impossible behavior, zero time on page
- [ ] Reconcile clicks vs sessions - network-reported clicks and your analytics sessions should roughly align; large gaps mean quality problems
- [ ] Re-evaluate monthly - traffic quality decays as networks rotate inventory

**Gate:** Placement-level quality dashboard live; blocklist maintenance cadence scheduled.

### Step 6: Scaling & Optimization
- [ ] Scale by headline winners - reallocate budget to top CTR/CVR variants, not blanket budget raises
- [ ] Expand placements - whitelist the publishers that deliver quality, then raise their share
- [ ] Layer retargeting - native top-of-funnel feeds retargeting pools on Meta/Google
- [ ] Test new offers - native audiences respond to fresh content; rotate the content library
- [ ] Watch economics quarterly - native CPM/CPC creeps up as you exhaust the quality inventory slice (heuristic)

**Gate:** Scaling rules based on quality-adjusted metrics; retargeting handoff configured.

## Practitioner Grounding & Decision Rules

Built from Marcel Sattler (native-advertising.net, $100M+ deployed), Fabien Schwartz (Schwartz Consulting), Joinative, OpenAdLibrary, Taboola/Outbrain case libraries. Full research: practitioner-intelligence/syntheses/paid-longtail.md.

- **The native CPA curve is INVERTED vs Facebook**: CPAs start high and fall over 2-4 weeks of manual optimization, then stabilize. Meta starts cheap, then explodes at scale (Sattler — EMPIRICAL, T1). "If someone sold you on Taboola or Outbrain going green in three days, they lied."
- **You need cash flow to survive convergence**; starting native when liquidity is short is always a bad decision (Sattler — HEURISTIC, T1).
- **Optimize three layers**: angle → ad → site; 3-5 editorials per angle (~15 in test); KPI-driven cuts only, never gut feeling (Sattler — FRAMEWORK, T1).
- **CTR is not a profitability metric** — app placements show high CTR/low CVR; judge CPA/ROAS on the full funnel (Schwartz — CONSENSUS with Sattler, T2).
- **Native feeds everything else**: clicks feed retargeting pools and lift other channels (halo) (Schwartz/Joinative/Outbrain — CONSENSUS, T2).
- **Headline must match content promise** — mismatch is a documented top mistake (Joinative — HEURISTIC, T2); durable formulas: curiosity + unresolved verdict + specific numbers (OpenAdLibrary — T3).
- **Don't trust max-conversion bidding before data exists** — budget burns for 1-2 leads (Schwartz — HEURISTIC, T2).
- **S2S (server-to-server) tracking is the key** to accurate native data (Schwartz — HEURISTIC, T2).

Decision rules:
1. IF running native THEN budget 2-4 weeks of runway at expected unprofitable CPAs before judging (Sattler — EMPIRICAL, T1).
2. IF CPA is high in week 1-2 THEN optimize angles/ads/sites — do NOT kill the campaign or cut budget (Sattler — EMPIRICAL, T1).
3. IF a campaign is still unprofitable after 4 weeks of structured testing THEN cut on KPI thresholds, never gut feel (Sattler — HEURISTIC, T1).
4. IF choosing a KPI THEN use CPA/ROAS; treat CTR as an early diagnostic only (Schwartz/Sattler — CONSENSUS, T2).
5. IF launching THEN test ≥3 angles x 3-5 editorials x 2-3 landing pages in parallel from day one (Sattler/Schwartz — FRAMEWORK, T2).
6. IF evaluating native's contribution THEN include assisted/halo impact and route clicks into retargeting — last-click-only makes native look ineffective (Joinative/Outbrain — HEURISTIC, T2).
7. IF cash-constrained THEN don't start native at all (Sattler — HEURISTIC, T1).

## Metrics

- **CPA / ROAS on final action** as primary (Sattler — FRAMEWORK, T1).
- **Editorial CTR + landing CTR** as early signals while conversion data is thin (Sattler — HEURISTIC, T1).
- **CPA trend curve**: high start → falling → stable = convergence; flat-high after 4 weeks = kill (Sattler — EMPIRICAL, T1).
- **S2S tracking completeness** as a pre-flight gate (Schwartz — HEURISTIC, T2).
- **Guardrail**: never optimize to CTR; app placements inflate it (Schwartz — HEURISTIC, T2).
- **Timebox**: verdict at end of week 4 of structured testing.

## Sources

1. Marcel Sattler, Profitable Native Ads on Taboola & Outbrain | native-advertising.net | tier 1 | 2026-08-15
2. Schwartz Consulting, How to boost online sales with Outbrain and Taboola | schwartzconsulting.co.uk | tier 2 | 2026-08-15
3. Joinative, 9 Native Advertising Mistakes | joinative.com | tier 2 | 2026-08-15
4. OpenAdLibrary, Native Ad Headlines: 12 Formulas | openadlibrary.com | tier 3 | 2026-08-15
5. Outbrain, Best of 2020 case studies (Domino's) | outbrain.com | tier 2 | 2026-08-15
6. Taboola, case studies (Kaspersky, Zazume) | taboola.com | tier 2 | 2026-08-15

## Evaluation & QA

### Common Failure Modes
- Running native traffic to a sales page - low-intent audience, immediate bounce
- Ignoring publisher-level reports - averages hide terrible placements
- Bait-and-switch headlines - high CTR, zero quality, brand damage
- Chasing CTR without a quality filter - native CTR is cheap to buy with garbage headlines
- Never refreshing creative on a fatigue-heavy feed
- Comparing native CPM to display without adjusting for intent
