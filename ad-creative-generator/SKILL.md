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