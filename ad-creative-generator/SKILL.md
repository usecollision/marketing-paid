---
name: ad-creative-generator
category: ad-creative
description: Generate high-performing ad creative concepts across angles, formats, and platforms.
triggers:
  - "ad creative"
  - "write ads"
  - "ad concepts"
  - "creative brief"
  - "ad angles"
  - "UGC script"
inputs:
  - product_context
  - icp
  - platform
  - creative_format
  - pain_points
outputs:
  - creative_concepts
  - ad_copy_variants
  - hook_options
  - visual_direction
  - creative_brief
related_skills:
  - hook-frameworks
  - creative-testing
  - marketing-messaging/conversion-copywriting
  - marketing-paid/meta-ads
required_context:
  - .context/product-marketing.md
allowed_tools:
  - mcp:image-generation
version: 1.0.0
---

## When to Use

Invoke when:
- Need fresh ad creative for campaigns
- Current ads fatiguing (CTR dropping, frequency rising)
- Launching new campaigns or testing new angles
- Expanding to new platforms that need native creative
- Building a creative testing pipeline

## Workflow

### Step 1: Angle Mining
Identify creative angles from research:

**Angle categories:**
| Angle Type | Description | Example |
|-----------|-------------|---------|
| Pain-focused | Lead with the frustration | "Tired of [pain]?" |
| Outcome-focused | Show the end result | "Imagine [desired state]" |
| Social proof | Others validate | "[X] companies switched in [month]" |
| Curiosity | Create information gap | "The [industry] secret that..." |
| Authority | Expert positioning | "[Expert/data] says..." |
| Contrast | Before/after or vs | "Still doing [old way]? vs [new way]" |
| Urgency | Time pressure | "Before [event/deadline]..." |
| Story | Narrative hook | "3 months ago, [character] was..." |
| UGC/testimonial | Real person experience | "I was skeptical until..." |
| Demo/how-it-works | Show the product | "Watch how [brand] does [thing]" |

Generate 5-10 angles minimum per campaign.

**Gate:** 5+ unique angles identified, each tied to a specific ICP pain/desire.

### Step 2: Format Selection
Match formats to platform and angle:

| Format | Best Platforms | Best Angles | Specs |
|--------|--------------|-------------|-------|
| Static image | Meta, LinkedIn, Reddit | Pain, outcome, social proof | 1080x1080, 1200x628 |
| Short video (15s) | TikTok, Reels, Stories | Hook, demo, UGC | 1080x1920, 9:16 |
| Medium video (30-60s) | Meta feed, YouTube | Story, demo, testimonial | 1080x1080 or 16:9 |
| Carousel | Meta, LinkedIn | Step-by-step, features, before/after | 1080x1080 x 3-10 |
| UGC-style | TikTok, Meta, IG | Testimonial, review, unboxing | 1080x1920, raw feel |
| Meme/native | Reddit, X, TikTok | Humor, relatability | Platform-native |

**Gate:** 2-3 formats selected per angle with platform-specific specs.

### Step 3: Copy Production
For each angle x format combination, write:

**Static ads:**
- Primary text (3 variants: short/medium/long)
- Headline (5 options)
- Description
- CTA selection

**Video ads:**
- Hook (first 3 seconds - the most critical part)
- Body (problem → solution → proof)
- CTA (verbal + visual)
- Captions/text overlays

**UGC scripts:**
- Setup (who is speaking, why should I care)
- Problem (relatable frustration)
- Discovery (how they found the solution)
- Result (specific outcome)
- CTA (direct recommendation)

**Gate:** Each concept has complete copy ready for production.

### Step 4: Visual Direction
For each creative, specify:
- Key visual element (product shot, person, screen recording, illustration)
- Color palette (brand vs. native/organic feel)
- Text overlay placement and style
- Thumbnail/first-frame strategy (for video)
- Mood/energy level (calm/educational vs. energetic/urgent)

**Gate:** Visual direction specific enough for a designer/producer to execute.

### Step 5: Testing Plan
Organize creatives into a testing framework:
- Test one variable at a time (angle OR format OR copy, not all)
- Minimum 3 variants per test
- Define success metric before launching (CTR for awareness, CPA for conversion)
- Required spend before judgment (typically 2-3x target CPA per variant)

| Test | Variable | Variants | Success Metric | Budget | Duration |
|------|----------|----------|---------------|--------|----------|

**Gate:** Testing plan with clear hypotheses, variants, and decision criteria.

## Practitioner Grounding

- **Dara Denney** — creative is the highest-leverage paid variable; test creatives, not audiences; budget-scaled supply rate (1–3 new creatives/week at $5k–30k/mo, cap ~10 live); iterate winners 10 ways. (EMPIRICAL, T2)
- **Nick Shackelford** — "creative is the new targeting"; structure testing budget between proven winners and fresh creative; production volume (50+ videos/day at his agency) is the scaling constraint. (HEURISTIC, T2)
- **Alex Hormozi** — angle/claim before asset; ~80% of resources reskin winners; hook-splice proven first-3s onto new bodies for 10–50x yield. (HEURISTIC, T2/T3)
- **Eugene Schwartz** — claim type must match market sophistication: direct → differentiated → mechanism → named mechanism → identity. (FRAMEWORK, T2)
- **hawky/AdGenz/AdManage 2026 operator consensus** — angle matrix (pains×proofs, scored on evidence/saturation/proof); 2–4 genuinely distinct concepts/week at meaningful spend; 3–5 variants per batch; one variable per test, offer last; rotate every 7–10 days. (HEURISTIC, T3)
- **AppsFlyer** — ad fatigue (one ad) vs creative fatigue (same KIND of ad): different remedies. (EMPIRICAL, T2)

## Decision Rules

1. IF no angle evidence exists THEN build a pains×desires × proof-points matrix and scan competitor ad libraries (Meta Ad Library / Google Transparency) for saturation BEFORE producing assets (hawky, FRAMEWORK, T3).
2. IF budget is $5k–30k/mo THEN generate 1–3 distinct creatives/week and cap ~10 live; scale supply only with budget (Denney, EMPIRICAL, T2).
3. IF market sophistication is stage 3+ THEN lead claims with mechanism/proof, not outcome promises; stage 1–2 markets take direct claims (Schwartz, FRAMEWORK, T2).
4. IF testing THEN one variable per batch (hook → format → angle → offer last), equal budget/audience, ≥1–2x target CPA or 3–7 days before any verdict (AdGenz/hawky, HEURISTIC, T3).
5. IF a creative wins THEN iterate/reskin it 10 ways before testing net-new concepts (Denney/Hormozi, HEURISTIC, T2).
6. IF CTR/CPA decays as frequency rises THEN rotate in fresh variants (7–10 day cadence) before touching targeting or budget (Denney/AdManage/AppsFlyer, HEURISTIC, T2).
7. IF producing UGC-style creative THEN brief angle + emotional beats, not full scripts (Pixis, HEURISTIC, T3).

## Metrics

- Primary: hook rate/thumb-stop (30–50% = good on Meta, T3), 3s hold %, CTR, CPA per creative; creative-level ROAS.
- Guardrails: live-creative cap vs budget; supply rate (distinct concepts/week); fatigue curve (frequency × CPA trend); taxonomy coverage (every creative tagged `[Platform]-[Campaign]-[Angle]-[Format]-[Version]` so winners compound into a library).
- Timebox: judge at 1–2x target CPA or 3–7 days, whichever comes last; re-measure on rotation (7–10 days) and on any frequency spike.

## Sources

1. Denney panel | domains/messaging-longtail/dara-denney.md (practitioner-intelligence) | tier 1 | 2026-08-15
2. hawky.ai Creative Strategy for Performance Marketing 2026 | https://hawky.ai/blog/creative-strategy-performance-marketing | tier 3 | 2026-08-15
3. AdGenz Facebook Ad Creative Testing 2026 | https://www.adgenz.ai/blog/facebook-ad-creative-testing-framework-2026 | tier 3 | 2026-08-15
4. Shackelford — Open Residency Ep.08 | https://openresidency.com/nick-shackelford | tier 2 | 2026-08-15
5. Hormozi hook/reskin doctrine | usegavel.com/alex-hormozi/hook-meat-cta + github.com/claes-work/alex-hormozi-clone | tier 2/3 | 2026-08-15
6. AppsFlyer — creative fatigue vs ad fatigue | https://www.appsflyer.com/blog/tips-strategy/creative-fatigue | tier 2 | 2026-08-15
7. Schwartz sophistication (messaging.md exegesis) | practitioner-intelligence/syntheses/messaging.md | tier 1 | 2026-08-15

## Evaluation & QA

### Creative Scoring
| Criteria | Score 1 | Score 3 | Score 5 |
|----------|---------|---------|---------|
| Hook strength | Generic/boring | Interesting | Impossible to scroll past |
| Angle clarity | Unclear message | Decent angle | Crystal clear, specific pain/outcome |
| Platform nativeness | Looks like an ad | Somewhat native | Indistinguishable from organic |
| CTA clarity | Vague/missing | Present | Compelling + low friction |
| Scroll-stop potential | Blends in | Stands out slightly | Thumb-stopping |

### Common Failure Modes
- All creatives look/sound the same (need angle diversity)
- Too polished for platforms that reward raw/authentic (TikTok, Reddit)
- No clear hook in first 3 seconds of video (you lose 50% by second 3)
- Feature-heavy instead of outcome/emotion-driven
- Not enough variants to achieve statistical significance in testing
- Testing variations instead of concepts — ten crops of the same ad is one test; Meta clusters similar creatives (hawky, HEURISTIC, T3)
- Leading with features instead of the buyer's pain — "almost nobody scrolls past a feature list" (Hormozi, HEURISTIC, T2)
- Ignoring creative fatigue (same KIND of ad feeling repetitive) while chasing ad fatigue — frequency caps + supply rotation, not just new targeting (AppsFlyer/Denney, EMPIRICAL, T2)
- No creative taxonomy — untagged ads can't compound into a winning-element library (ORCA/scalable.ad, HEURISTIC, T3)