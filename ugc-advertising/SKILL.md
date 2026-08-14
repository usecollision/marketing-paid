---
name: ugc-advertising
category: ad-creative
description: Run a UGC ad program with creator sourcing, briefing, usage licensing, UGC-vs-studio testing, and volume scaling.
triggers:
  - "UGC ads"
  - "user-generated content ads"
  - "creator ads"
  - "UGC creator sourcing"
  - "usage rights"
  - "UGC vs studio creative"
  - "whitelisting creators"
inputs:
  - product_context
  - icp
  - pain_points
  - budget
  - winning_angles
  - existing_creative_library
outputs:
  - ugc_program_plan
  - creator_briefs
  - licensing_checklist
  - testing_plan
  - scaling_roadmap
related_skills:
  - ad-creative-generator
  - hook-frameworks
  - creative-testing
  - tiktok-ads
  - meta-ads
  - media-planning
  - marketing-messaging/customer-language-bank
  - marketing-optimize/ab-testing
required_context:
  - .context/product-marketing.md
allowed_tools:
  - none
version: 1.0.0
---

## When to Use

Invoke when:
- Studio creative is fatiguing and CTR/CPA are degrading
- Launching paid social and needing native-feeling creative fast
- Building a repeatable UGC production pipeline
- Testing whether UGC outperforms studio-produced ads
- Scaling creator volume without losing quality control

## Workflow

### Step 1: Channel Fit & Expectations
- [ ] UGC fits best on native-feeling surfaces - TikTok, Reels, Stories - and often beats studio on hook rate and trust transfer (heuristic - validate per account; category and offer change the answer)
- [ ] Know what UGC is not - polished brand film; it wins on authenticity, not production value
- [ ] Set the bar - UGC works when the angle, hook, and creator are right; volume of mediocre UGC is still mediocre
- [ ] Decide the role - net-new prospecting creative, ad-fatigue reliever, or the full creative system
- [ ] Budget shape - small fixed cost per video (heuristic - creator fees typically run far below studio production; scale via volume, not per-asset cost)

**Gate:** Role of UGC in the creative mix defined with a success metric.

### Step 2: Creator Sourcing
- [ ] Sourcing channels - UGC marketplaces and platforms, creator networks, organic discovery (fans already posting about the product), seeding product to nano-creators
- [ ] Match criteria - creator's natural tone fits the brand, audience overlap with ICP, engagement quality over follower count
- [ ] Nano vs micro vs macro - nano creators are often better UGC actors than macro influencers (heuristic - UGC ads need relatable people, not reach)
- [ ] Vet with past work - ask for a portfolio or live examples in the relevant format
- [ ] Build a roster - a bench of 5-10 repeatable creators beats one-off hiring (heuristic - repeat creators internalize the brand voice)

**Gate:** Sourcing channels and creator roster criteria written; first bench assembled.

### Step 3: Briefing Creators
- [ ] Brief contents - product facts, target audience, problem-claim-offer, 2-3 angles to film, hook ideas, format specs, dos and don'ts
- [ ] Give hooks and angles, not full scripts - over-scripted creators sound stiff and the authenticity dies
- [ ] Ask for raw footage plus cutdowns - raw footage lets your editor make variants later
- [ ] Specify deliverable formats - 9:16, captions on, length variants (15/30/45s; adapt to platform)
- [ ] Include mandatory claims rules - what they can and cannot say; compliance first
- [ ] Set revision expectations up front - one paid revision round; avoid endless back-and-forth

**Gate:** Standard brief template exists; every creator gets it before filming.

### Step 4: Licensing & Usage Rights
- [ ] Secure paid-usage rights before running ads - organic permission is not ad permission
- [ ] Contract terms to fix - usage window (e.g. 30/90/365 days), platforms, channels (paid vs organic), exclusivity, and territory
- [ ] Whitelisting or Spark-style posting - running ads from the creator's handle with permission; often outperforms brand-handle posting (heuristic - validate per account)
- [ ] Re-licensing plan - rights expire; decide extension economics before the window lapses
- [ ] Archive everything - contracts, briefs, and approvals in one place; a rights audit should take minutes
- [ ] Know platform rules - branded content and disclosure requirements differ by platform

**Gate:** Rights and usage windows documented per video before launch.

### Step 5: Production Pipeline & QA
- [ ] Standard intake - brief out, footage in, editor cuts variants, internal review, rights check, export
- [ ] QA checklist - hook in the first 2 seconds, captions present, brand mention timing, audio quality, claim compliance
- [ ] Editing playbook - captions, pacing cuts, b-roll insertion, native platform styling
- [ ] Turnaround targets - keep the pipeline fast; UGC's advantage erodes if production drags (heuristic - aim for days, not weeks)
- [ ] Variant generation - one raw video becomes hook variants and length variants in the edit

**Gate:** Pipeline documented with QA checklist and turnaround targets.

### Step 6: Testing UGC vs Studio
- [ ] Run structured tests - same angle, UGC vs studio, matched budget and audience (use creative-testing methodology)
- [ ] Metrics that matter - hook rate and thumbstop, CTR, CPA, hold rate; do not judge on vanity likes
- [ ] Let statistical significance decide before declaring a winner - small budgets lie
- [ ] Read the pattern - UGC often wins prospecting; studio often wins retargeting and brand search (heuristic - test per account)
- [ ] Feed learnings back - winning UGC hooks become briefs for the next batch; losing angles get killed

**Gate:** At least one UGC-vs-studio test documented with a decision rule.

### Step 7: Scaling Volume
- [ ] Scale what works - double down on winning angle-creator combinations, not random volume
- [ ] Batch ordering - order 10-20 videos per angle wave to feed the testing cadence (heuristic - creative volume drives learning speed on paid social)
- [ ] Tier the roster - proven creators get repeat orders and higher rates; new creators fill the test bench
- [ ] Watch fatigue - UGC fatigues like any creative; refresh hooks before performance decays
- [ ] Guard quality at scale - briefs and QA checklists are what keep volume from becoming noise
- [ ] Rebalance mix monthly - UGC share of spend vs studio vs static, per platform

**Gate:** Volume plan tied to testing cadence; fatigue monitoring in place.

## Evaluation & QA

### Common Failure Modes
- Running creator content as ads without paid-usage rights - takedowns and platform strikes
- Over-scripting creators until the authenticity advantage disappears
- Judging UGC on production polish - the roughness is the format
- Ordering volume without angles - lots of videos, no hypotheses
- Ignoring rights expiry - creative dies mid-flight when the window lapses
- Comparing UGC vs studio on unmatched budgets or audiences
- No QA checklist - non-compliant or broken videos go live
