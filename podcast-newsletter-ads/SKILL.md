---
name: podcast-newsletter-ads
category: paid
description: Buy podcast and newsletter sponsorships with host-read vs programmatic trade-offs, package negotiation, and promo-code measurement.
triggers:
  - "podcast sponsorship"
  - "newsletter sponsorship"
  - "host-read ads"
  - "sponsor a podcast"
  - "newsletter advertising"
  - "podcast ads"
  - "creator sponsorship deals"
inputs:
  - product_context
  - icp
  - budget
  - offer_and_promo_code
  - landing_page_url
  - target_show_shortlist
outputs:
  - channel_fit_assessment
  - sponsorship_shortlist
  - pricing_negotiation_plan
  - ad_read_script
  - measurement_plan
related_skills:
  - paid-strategy
  - media-planning
  - performance-reporting
  - spotify-ads
  - native-ads
  - marketing-channels/podcast-appearances
  - marketing-optimize/attribution-model-selection
  - marketing-optimize/utm-governance
required_context:
  - .context/product-marketing.md
allowed_tools:
  - none
version: 1.0.0
---

## When to Use

Invoke when:
- Evaluating podcast or newsletter sponsorships as a channel
- Deciding between host-read and programmatic audio ads
- Negotiating rates with shows or creator networks
- Writing sponsorship copy or ad-read scripts
- Setting up attribution for sponsorship spend

## Workflow

### Step 1: Channel Fit & Audience Match
- [ ] Sponsorships are brand-and-consideration media with strong trust transfer - rarely a direct-response channel alone (heuristic - some DTC brands do see direct response)
- [ ] Audience match check - download or readership demographics vs ICP; ask shows for audience data or use public chart data
- [ ] Fit check - niche shows convert better than big ones; several small shows often beat one celebrity show (heuristic - validate with your own tests)
- [ ] Test small before scaling - single-episode buys on 3-5 shows before multi-episode packages
- [ ] Check content adjacency - the show's topic and tone must be brand-safe by your standards

**Gate:** Audience-match evidence gathered for each shortlisted show before any money moves.

### Step 2: Inventory Types & Pricing Models
- **Podcast placements** - pre-roll (first 15-60s), mid-roll (most attention, highest price), post-roll (cheapest, lowest recall)
- **Host-read vs programmatic** - host-read is the host delivering your message in their voice; programmatic is pre-produced audio dynamically inserted
- **Baked-in vs dynamic insertion** - baked-in lives in the episode forever; dynamic can be swapped, rotated, and geo-targeted
- **Newsletter inventory** - dedicated send (entire email is you), main sponsor slot (top block), secondary slots, classified-style footer ads
- Pricing is CPM-based (heuristic - podcast CPMs typically run higher than newsletter CPMs; negotiate from published rate cards, which are usually discountable)
- [ ] Compute effective CPM for every offer - demand impressions or downloads per placement, not just a flat rate

**Gate:** Every offer converted to an effective CPM with placement type labeled.

### Step 3: Host-Read vs Programmatic
- [ ] Choose host-read when - trust and endorsement matter, the host's audience is a tight ICP match, budget allows the premium
- [ ] Choose programmatic when - you need scale across many shows, tight message control, or test-and-learn volume
- Middle option - host-read intro with a pre-produced core message
- [ ] Give hosts talking points, not scripts - forced scripts kill the authenticity that makes host-read work
- [ ] Programmatic still needs real copy - pre-produced reads win or lose on the first line like any ad

**Gate:** Decision written per campaign with rationale tied to objectives.

### Step 4: Sponsor Copy & Ad Read Scripting
- [ ] Build a read that covers - hook, problem, product, offer, promo code, where to go
- [ ] Unique promo code per show - the entire measurement system hangs on it
- [ ] Keep the URL short and speakable - vanity URL or simple domain path
- [ ] Newsletter creative - native-style copy matching the publication's tone; clear CTA; one message per placement
- [ ] Match tone to host or publication - read their past sponsor placements and style guide
- [ ] Include tracking links in newsletter ads; codes carry the podcast side

**Gate:** One read script plus one newsletter ad variant per placement with unique codes.

### Step 5: Measurement & Attribution
- [ ] Promo code redemptions per show - primary signal
- [ ] UTM-tagged vanity URLs per show - traffic signal
- [ ] Post-purchase surveys ("where did you hear about us") - catch non-code buyers
- [ ] Branded search lift during and after flights
- [ ] Attribute conservatively - sponsorships run concurrently with other channels; use holdout or geo tests when scale justifies (heuristic - small budgets rely on codes and surveys)
- [ ] Track cost per redemption and per acquisition per show, then renew or cut by show

**Gate:** Attribution stack live before the first episode airs - retrofitting is impossible.

### Step 6: Negotiation & Buying
- [ ] Rate cards are anchors, not prices - multi-episode packages, annual commitments, and off-peak seasons all discount (heuristic - commonly meaningful discounts off card; negotiate from your own data)
- [ ] Ask for added value - extra placements, newsletter mention, social posts, first-position choice
- [ ] Network deals - buy across a network's shows for better rates and portfolio reach
- [ ] Contract terms - flight dates, episode placement type, makegoods for missed reads, cancellation windows
- [ ] Get everything in writing - a missed host read is common; agree makegood terms up front
- [ ] Renewal decisions by data - renew winners at negotiated rates, drop losers without guilt

**Gate:** Signed terms include makegoods and exact placement inventory.

## Evaluation & QA

### Common Failure Modes
- Buying one big show instead of testing several small ones
- No promo code, or one shared code across shows - cannot tell which show worked
- Scripting host reads word-for-word - kills authenticity, the entire value of the format
- Paying rate card for single episodes - no package or added-value negotiation
- Judging a sponsorship on last-click attribution alone
- Ignoring makegoods when reads are missed or mis-delivered
- Newsletter ads written in ad-speak instead of the publication's native tone
