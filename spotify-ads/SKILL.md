---
name: spotify-ads
category: paid
description: Plan and run Spotify Ads with audio ad formats, mood-and-music-taste targeting, companion banners, and streaming-specific measurement.
triggers:
  - "Spotify ads"
  - "audio advertising"
  - "streaming audio ads"
  - "Spotify Ad Studio"
  - "music taste targeting"
  - "audio ad creative"
  - "companion banner"
inputs:
  - product_context
  - icp
  - budget
  - brand_voice_assets
  - audio_script_or_vo
  - landing_page_url
outputs:
  - channel_fit_assessment
  - audio_ad_scripts
  - targeting_plan
  - campaign_setup_plan
  - companion_banner_specs
  - measurement_plan
related_skills:
  - paid-strategy
  - media-planning
  - performance-reporting
  - programmatic-ctv
  - podcast-newsletter-ads
  - ad-creative-generator
  - hook-frameworks
  - marketing-optimize/mmm-incrementality
required_context:
  - .context/product-marketing.md
allowed_tools:
  - none
version: 1.0.0
---

## When to Use

Invoke when:
- Planning a brand or upper-funnel audio campaign
- Testing Spotify as a new paid channel
- Building audio ad creative and needing format guidance
- Wanting to target listeners by music taste, mood, or playlist context
- Launching companion display banners alongside audio spots
- Measuring a streaming audio campaign without click-based KPIs
- Comparing audio against other upper-funnel channels like CTV or podcasts

## Workflow

### Step 1: Channel Fit & Objectives
- [ ] Define the job - awareness, reach, and consideration; audio rarely wins on last-click ROAS (heuristic - treat as brand media, not direct response)
- [ ] Fit check - is the audience a streaming listener? Free-tier listeners hear ads; premium subscribers mostly don't
- [ ] Set expectations - measure reach, frequency, completion rate, ad recall, and branded search lift, not clicks
- [ ] Budget floor - audio CPMs are modest but testing needs enough impressions to read results (heuristic - validate against current platform minimums)
- [ ] Confirm audio actually fits - products with sound associations (music, focus, mood, food delivery) carry an edge

**Gate:** Objective and non-click KPIs agreed before creative starts.

### Step 2: Formats & Creative Production
- **Core formats** - audio ads (15-30s) with optional companion banner, video takeover, sponsored sessions, playlist sponsorships
- [ ] 15s vs 30s - 30s carries more message; 15s is cheaper to rotate; test both (heuristic - category-dependent)
- [ ] Script - the first 3 seconds matter more than in video because there is nothing to watch; say the brand early and often
- [ ] Voice - conversational reads outperform announcer reads on streaming (heuristic - validate per brand)
- [ ] Music bed - licensed or simple bed; match the mood of the playlists you target
- [ ] Companion banner - square or wide format per current Ad Studio spec (verify live specs before exporting), clear CTA, landing page URL
- [ ] Native sound design - no radio-style jingles or hard-sell reads; the format rewards restraint

**Gate:** 15s and 30s scripts written plus one companion banner per ad.

### Step 3: Targeting by Music & Context
- **Music taste and genre targeting** - serve ads inside specific genres (fitness, focus, pop, chill)
- **Mood and playlist targeting** - target by playlist and activity context (workout, sleep, cooking, party)
- [ ] Match product to context - energy drinks on workout playlists, meal kits on cooking, focus apps on study playlists
- **Demographic and geo layers** - age, gender, location on top of context
- [ ] Build 3-5 audience-context pairings per campaign instead of one broad audio buy
- Contextual relevance is the channel's targeting advantage - it lifts recall (heuristic - validate with brand-lift data)

**Gate:** At least 3 context-audience pairings defined with matched creative.

### Step 4: Campaign Setup in Ad Studio
- [ ] Structure - campaign per objective; ad set per targeting pairing; 1-3 ads per ad set
- [ ] Budget and schedule - daily budgets; daypart around listening peaks (commute, evening - heuristic; validate with your own reporting)
- [ ] Frequency - cap per listener per week; audio cannot be scrolled past, so annoyance compounds fast
- [ ] Destination - URL for companion banner click-through; UTM-tag every flight
- [ ] Self-serve via Ad Studio is the entry point; large buys may route through Spotify direct sales (heuristic - depends on budget tier)
- [ ] Start with 2-3 campaigns, learn, then scale winning pairings

**Gate:** Campaign architecture mirrors targeting pairings; frequency caps set.

### Step 5: Measurement & Optimization
- [ ] Track impressions, reach, frequency, and completion rate (quartile data)
- [ ] Companion banner CTR is a secondary signal, not the KPI - expect low rates by design
- [ ] Measure lift - branded search, direct site traffic during flight, promo codes or dedicated landing pages
- [ ] Brand-lift study or incrementality test when budget justifies (heuristic - worth it at scale)
- [ ] Compare audio against other upper-funnel channels on cost-per-recall or lift-per-dollar, not impressions alone (heuristic - read your own studies before trusting cross-channel benchmarks)
- [ ] Optimize - rotate ads by completion rate; kill ads losing listeners in the first 10 seconds; rebalance budgets to best context pairings
- [ ] Accept streaming measurement limits - in-app attribution is limited, so landing pages and UTMs do the heavy lifting

**Gate:** Measurement plan includes completion and a lift metric, not clicks alone.

## Practitioner Grounding & Decision Rules

Built from Orbis Agency, ATTN Agency (DTC growth), Esteban Largaespada (Online Optimism), Spotify Advertising docs (Brand Lift, Pixel). Full research: practitioner-intelligence/syntheses/paid-longtail.md.

- **Spotify is a brand recall/reach channel, not direct response** — "the strength of Spotify Ads is in brand recall and reach, not in direct click-to-purchase sales. If you expect an audio ad to generate immediate, trackable sales the way a Google search campaign would, you're going to be frustrated" (Orbis — OPINION, T2).
- **Audio CTR is structurally low (0.1-0.5%) but intent is higher** than display (ATTN — HEURISTIC, T2).
- **The performance path is indirect**: audio exposure → branded search → conversion elsewhere. Pair flights with a branded-search bid bump + visual retargeting of listeners (ATTN — FRAMEWORK, T2).
- **Measurement is Brand Lift + search lift, not platform CPA**: Spotify Brand Lift randomizes test/control with in-app polls ≤48h post-exposure; Koodo example: +23pt ad recall (Spotify docs — EMPIRICAL, T1/T2).
- **Spotify Pixel + website-traffic objective** now exist for performance-minded buyers, but operator consensus: still a brand/consideration channel (Largaespada — T2).
- **Start with display ads as a low-risk entry** before producing audio creative (Largaespada — HEURISTIC, T2).
- Opt-in video ads (now-playing view) reach a self-selecting engaged audience (Largaespada — T2).
- Targeted audio ads achieve ~24% higher brand recall than non-targeted (R-Advertising cited study — T3).

Decision rules:
1. IF the objective is direct-response ROAS THEN don't lead with Spotify audio; use it only as a brand/consideration layer (Orbis — OPINION, T2).
2. IF running Spotify THEN pair with: branded-search bid bump + visual retargeting of listeners during flight (ATTN — FRAMEWORK, T2).
3. IF measuring Spotify THEN require Brand Lift or branded-search-volume lift — dashboard CTR is not the verdict (Spotify docs/ATTN — FRAMEWORK, T2).
4. IF testing Spotify for the first time THEN start with display before investing in audio creative (Largaespada — HEURISTIC, T2).
5. IF writing audio creative THEN one message per 30s spot; never cram (ATTN — HEURISTIC, T2).
6. IF budget is below minimum viable reach for the target audience THEN skip — underfunded audio is untestable noise (Orbis/ATTN synthesis — HEURISTIC, T3).

## Metrics

- **Brand Lift (recall/consideration)** + **branded search volume** during/after flight (Spotify docs/ATTN — FRAMEWORK, T2).
- **Completed listens / frequency / reach** as delivery metrics (Orbis — HEURISTIC, T2).
- **Delayed and cross-device conversions** with extended attribution windows (ATTN — HEURISTIC, T2).
- **Guardrail**: an agency that can't explain how it will measure the effect "is your first warning sign" (Orbis — OPINION, T2).
- **Timebox**: brand effects measured over the flight + post-period; not a 7-day ROAS channel.

## Sources

1. Orbis Agency, Spotify Ads | orbis.agency | tier 2 | 2026-08-15
2. ATTN Agency, Spotify & Audio Ads for Ecommerce | attnagency.com | tier 2 | 2026-08-15
3. Online Optimism, Spotify's push into performance marketing | onlineoptimism.com | tier 2 | 2026-08-15
4. Spotify Ads, Ad Measurement docs | ads.spotify.com | tier 1 | 2026-08-15
5. New Digital Age, Spotify launches Brand Lift (Koodo) | newdigitalage.co | tier 2 | 2026-08-15

## Evaluation & QA

### Common Failure Modes
- Measuring audio on CTR - companion banners see low click rates by design
- Generic creative that ignores playlist context - the targeting advantage is wasted
- Too much frequency - audio cannot be scrolled past; annoyance turns reach negative
- Skipping the companion banner - loses the only clickable surface
- Announcer-style scripts that sound like radio ads - fit the platform voice
- Expecting direct-response economics from an upper-funnel format
