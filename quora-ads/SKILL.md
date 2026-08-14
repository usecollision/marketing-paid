---
name: quora-ads
category: paid
description: Run Quora Ads for intent capture with question and topic targeting, B2B lead generation plays, and lower-CPC test budgets.
triggers:
  - "Quora Ads"
  - "advertise on Quora"
  - "Quora B2B leads"
  - "question targeting"
  - "Quora topic targeting"
  - "Quora campaign"
  - "Quora lead gen"
inputs:
  - product_context
  - icp
  - competitor_research
  - budget
  - landing_pages
  - content_assets
outputs:
  - channel_fit_assessment
  - question_targeting_plan
  - campaign_structure
  - ad_copy_set
  - lead_gen_plan
  - measurement_plan
related_skills:
  - paid-strategy
  - google-ads
  - linkedin-ads
  - reddit-ads
  - media-planning
  - marketing-messaging/objection-handling
  - marketing-channels/keyword-research
required_context:
  - .context/product-marketing.md
allowed_tools:
  - none
version: 1.0.0
---

## When to Use

Invoke when:
- Capturing demand from people actively researching a problem your product solves
- Building B2B lead generation where questions signal intent
- Testing a lower-cost alternative to Google search for research-stage queries
- Answering competitor comparisons - prospects reading "X vs Y" threads
- Reaching technical and professional researchers (Quora skews educated and professional - heuristic, validate per audience)

## Workflow

### Step 1: Channel Fit & Intent Logic
- [ ] Map the research questions your ICP asks - Quora is mid-funnel: users are evaluating, comparing, and problem-solving
- [ ] Check question volume exists - search Quora for your core problem questions before budgeting
- [ ] Understand the inventory - Quora's scale is a fraction of Google's; treat it as a surgical intent layer (heuristic)
- [ ] Frame the KPI - lead quality and assisted conversions over raw volume

**Gate:** Question map proving intent exists at volume worth buying.

### Step 2: Question & Topic Research
- [ ] Mine Quora - search core problems, read the top threads, note the language buyers use
- [ ] Harvest related questions - the "related questions" column is a targeting goldmine
- [ ] Group questions into themes - problem awareness, comparison, implementation, alternatives
- [ ] Pull objection data - threads surface the exact objections your landing pages must answer
- [ ] Cross-reference with keyword research for query-level volume context

**Gate:** Themed question list (50+ questions) with intent and objection notes per theme.

### Step 3: Targeting Setup
- **Question targeting** - ad shows on specific questions; highest intent, smallest inventory
- **Topic targeting** - ad shows across a topic's questions; broader reach
- **Interest targeting** - user-profile interests; loosest intent
- **Audience targeting** - website visitors, email lists, lookalikes
- **Broad targeting** - everything; for awareness or retargeting layering
- Layering - combine question targeting with audience exclusions to filter existing customers

**Gate:** Targeting plan per ad group with inventory estimates and exclusion logic.

### Step 4: Creative - Answer First, Pitch Second
- [ ] Write the ad as an answer to the specific question - generic copy fails on question-targeted placements (heuristic)
- [ ] Headline - answer or promise the resolution, not the brand name
- [ ] Body - 1-2 sentences of substance, then a low-pressure CTA
- [ ] Match the question's stage - problem questions get education, comparison questions get differentiation
- [ ] Rotate 2-3 angles per theme; refresh as CTR decays

**Gate:** Ad copy per question theme written in answer-first style with staged CTAs.

### Step 5: B2B Lead Gen Playbook
- [ ] Use question targeting on bottom-funnel themes - comparisons, alternatives, implementation
- [ ] Send traffic to content, not cold landing pages - research-stage buyers want substance; gate only when the content earns it
- [ ] Layer retargeting - Quora visitors into Meta/Google/LinkedIn audiences for the follow-up
- [ ] Measure lead quality, not just volume - Quora leads skew unqualified if the ad over-promises (heuristic - validate with your own qualification data)
- [ ] Integrate with LinkedIn Ads - same ICP, different funnel stage; Quora captures research, LinkedIn captures account targeting

**Gate:** Lead flow mapped to CRM with qualification tracking enabled.

### Step 6: Bidding, Budget & Cost Dynamics
- [ ] Expect lower CPCs than Google for the same research-stage queries (heuristic - varies by vertical; verify with your own tests)
- [ ] Start with CPC bidding and small daily budgets - Quora supports controlled pilots
- [ ] Watch CTR context - Quora CTRs run below search ads; judge on CPL, not CTR (heuristic)
- [ ] Scale winners by adding adjacent questions and topics, then broaden targeting
- [ ] Don't expect Google-scale volume - plan Quora as an incremental layer

**Gate:** Pilot launched with CPL-based verdict criteria.

### Step 7: Measurement & Iteration
- [ ] Weekly - CTR by theme, question-level performance, and a negative question list (where ads waste spend)
- [ ] Monthly - refresh question lists from new threads, prune stale themes, review lead quality by question theme
- [ ] Cross-channel - feed question-level insight (language, objections) into landing page copy and SEO content

**Gate:** Question-level reporting live; insights feeding content and messaging teams.

## Evaluation & QA

### Common Failure Modes
- Running generic brand ads on question targeting - wrong promise, wrong stage
- Sending research-stage traffic to a cold demo-request page
- Judging the channel on CTR instead of CPL and lead quality
- Targeting only topics - paying for intent you haven't verified at question level
- Expecting Google-scale volume from a niche inventory
- Ignoring the objection data sitting in the threads themselves
