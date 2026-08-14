---
name: hook-frameworks
category: ad-creative
description: Write scroll-stopping hooks for video ads, static ads, and organic content.
triggers:
  - "hooks"
  - "ad hooks"
  - "scroll stopping"
  - "first 3 seconds"
  - "attention grabbers"
inputs:
  - product_context
  - icp
  - pain_points
  - format
outputs:
  - hook_variants
  - hook_categories
  - platform_specific_hooks
related_skills:
  - ad-creative-generator
  - marketing-messaging/conversion-copywriting
  - marketing-channels/linkedin-content
required_context:
  - .context/product-marketing.md
allowed_tools: []
version: 1.0.0
---

## When to Use

Invoke when:
- Writing the first line/frame of any ad or content
- Video CTR is low (hook isn't working)
- Need fresh angles for existing messaging
- Creating thumb-stopping social content

## Workflow

### Step 1: Hook Category Selection
Choose from proven hook frameworks:

| Category | Pattern | Example |
|----------|---------|---------|
| Contrarian | Challenge a belief | "Everything you know about [X] is wrong" |
| Curiosity gap | Open a loop | "The [X] trick that [result] (most people miss this)" |
| Pain callout | Name the frustration | "If you're still [painful action], read this" |
| Result lead | Start with outcome | "How we went from [bad state] to [good state] in [time]" |
| Social proof | Leverage authority | "[X] companies just switched from [old] to [new]" |
| Question | Engage directly | "What would you do with [desirable outcome]?" |
| Pattern interrupt | Break expectations | "[Unexpected statement that relates to your message]" |
| Story open | Narrative hook | "6 months ago I was [relatable bad state]..." |
| Tutorial | Promise value | "Here's the exact [process/template] I use to [result]" |
| Controversial | Polarize | "Stop [common advice]. Here's what actually works." |

### Step 2: Generate 10+ Hook Variants
For your specific product/ICP, write hooks across 3-5 categories:

Rules for great hooks:
- Specific > generic (numbers, timeframes, named outcomes)
- Short (under 10 words for headlines, under 3 seconds for video)
- Create tension or curiosity that MUST be resolved
- Speak to ONE person, not an audience
- Use customer language, not marketing language
- Front-load the most interesting word

**Gate:** 10+ hooks across multiple categories, all specific to your ICP.

### Step 3: Platform Adaptation
Adapt top hooks per platform:

| Platform | Hook Style | Length | Format |
|----------|-----------|--------|--------|
| TikTok/Reels | Conversational, fast, surprising | 1-3 sec | Spoken + text overlay |
| Meta feed | Bold claim or question | <125 chars primary text | Text + image |
| LinkedIn | Professional insight or data | First line before "see more" | Text post |
| YouTube | Promise + timeframe | First 5 seconds | Spoken |
| X/Twitter | Hot take or data point | <50 chars ideal | Text |
| Reddit | Native, not salesy | Title format | Question or story |

**Gate:** Top 5 hooks adapted for 2-3 target platforms.

### Step 4: Rank & Select
Score hooks on:
- Specificity (1-5): Does it name a specific pain/outcome?
- Curiosity (1-5): Does it create an open loop?
- Relevance (1-5): Does the ICP immediately identify with it?
- Nativeness (1-5): Does it feel organic on the platform?

Top 3 go into production/testing.

**Gate:** Hooks ranked with clear winners for each platform/format.

## Practitioner Grounding

- **Alex Hormozi** — Hook-Meat-CTA: the hook names the buyer's pain in 3–4 words; "failed ads die at the hook, not the offer"; write 50 hooks before one ad; specificity beats cleverness. (HEURISTIC, T2)
- **Eugene Schwartz** — hook type must match awareness level: unaware → problem statement; problem-aware → pain callout; solution-aware → mechanism/contrast; most-aware → offer/direct close. (FRAMEWORK, T2)
- **Dara Denney** — conversational hooks that take a second to process ("Wait why is this…", "No because…") beat polished openings; 1.5s rule: the first 1.5 seconds decide retention. (EMPIRICAL/HEURISTIC, T2)
- **Short-form retention research (social.md)** — 50–70% of viewers leave in the first 1–2s; layered hooks (visual+audio+text) ~3x hold; core message in first 3s ≈ +60% total retention. (EMPIRICAL, T2)
- **vexub H-A-P** — every hook = pattern interrupt → audience call-out → promise; stack 2+ triggers; mirror the spoken hook in on-screen captions. (HEURISTIC, T3)
- **ORCA** — thumb-stop 30–50% is good on Meta; hook (0–3s) then context (3–5s, "if you run an ecommerce store…") then value. (HEURISTIC, T3)

## Decision Rules

1. IF the audience is unaware of the problem THEN open with the problem/frustration itself; IF problem-aware THEN name the specific pain; IF solution-aware THEN mechanism or contrast hook; IF most-aware (retargeting) THEN offer/close hook (Schwartz, FRAMEWORK, T2).
2. IF writing any ad hook THEN open with the buyer's pain in ≤4 words and never lead with a feature list (Hormozi, HEURISTIC, T2).
3. IF you need hooks THEN generate 50 options per angle and ship the top 3 — hook quality is a volume game (Hormozi, HEURISTIC, T2).
4. IF the format is short-form video THEN layer visual + audio + text hooks and caption-mirror the spoken line (social.md/vexub, EMPIRICAL/HEURISTIC, T2/T3).
5. IF retention drops hardest at ~1s THEN rebuild the pattern interrupt; IF at ~3s THEN strengthen the promise (vexub, HEURISTIC, T3).
6. IF the audience is new/cold THEN use conversational, problem-agitating hooks that take a second to process; IF warm/retargeting THEN lead with offer (Denney, HEURISTIC, T2).
7. IF a hook wins in testing THEN splice its first 3 seconds onto new bodies (10–50x creative yield) before inventing new hooks (Hormozi, TACTIC, T2/T3).

## Metrics

- Primary: thumb-stop / 3s watch rate (target 30–50% on Meta, T3), 15s watch rate, hook-level CTR and CPA.
- Guardrails: retention drop-point graph (1s vs 3s diagnosis); share of hooks that beat control per angle; platform-format fit (TikTok ~1s spoken+text vs LinkedIn first-line vs YouTube first-5s).
- Timebox: judge after 1–2x target CPA or 3–7 days; re-test hooks on every 7–10 day rotation and on any frequency-driven CTR decay.

## Sources

1. Gavel — Hormozi Hook-Meat-CTA (YouTube Ds_Qp2U5I8U @03:36) | https://usegavel.com/alex-hormozi/hook-meat-cta | tier 2 | 2026-08-15
2. Hormozi reskin/splicing doctrine | https://github.com/claes-work/alex-hormozi-clone/wiki/topics/marketing/paid-ads.md | tier 3 | 2026-08-15
3. Schwartz awareness/sophistication (messaging.md exegesis) | practitioner-intelligence/syntheses/messaging.md | tier 1 | 2026-08-15
4. Denney panel + short-form-hook-retention | practitioner-intelligence/domains/messaging-longtail/ | tier 1 | 2026-08-15
5. vexub — Hook Formula (H-A-P, 40 formulas, scorecard) | https://vexub.com/blog/hook-formula | tier 3 | 2026-08-15
6. ORCA — Video Ad Hooks That Convert | https://www.goorca.ai/blog/video_ad_hooks_guide | tier 3 | 2026-08-15
7. Social synthesis (1.5s/layered hooks) | practitioner-intelligence/syntheses/social.md | tier 1 | 2026-08-15

## Evaluation & QA

### Common Failure Modes
- Too clever/abstract (clarity beats creativity every time)
- No curiosity gap (nothing to resolve = no reason to keep watching)
- Generic hooks that could apply to any product
- Not matching platform energy (LinkedIn tone on TikTok)
- Burying the hook (should be first word/frame, not second sentence)
- Opening with a feature list — "almost nobody scrolls past a feature list" (Hormozi, HEURISTIC, T2)
- Ignoring the audience's awareness level — one hook for cold and retargeting audiences is a category error (Schwartz, FRAMEWORK, T2)
- Hooks without layered delivery on short-form video (spoken only, no text overlay) — audio+visual+text hooks hold ~3x longer (social.md, EMPIRICAL, T2)
- Judging hooks before minimum spend — 1–2x target CPA or 3–7 days, not first-day CTR (AdGenz/hawky, HEURISTIC, T3)