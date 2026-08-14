---
name: shopify-marketing-audit
category: ecommerce
description: Audit a Shopify store's marketing setup for conversion, retention, and growth opportunities.
triggers:
  - "Shopify audit"
  - "ecommerce audit"
  - "store marketing review"
  - "Shopify growth"
  - "DTC marketing"
inputs:
  - store_url
  - current_revenue
  - traffic_sources
  - email_list_size
outputs:
  - audit_report
  - opportunity_matrix
  - priority_fixes
  - 90_day_plan
related_skills:
  - abandoned-cart-flow
  - marketing-optimize/cro-audit
  - marketing-channels/lifecycle-sequences
  - marketing-paid/meta-ads
required_context:
  - .context/product-marketing.md
allowed_tools:
  - mcp:web-search
  - mcp:shopify
version: 1.0.0
---

## When to Use

Invoke when:
- Shopify store launched but not growing
- Conversion rate below 2% (industry avg for DTC)
- High traffic, low sales
- Looking for quick wins to increase revenue
- Planning Q-over-Q growth strategy

## Workflow

### Step 1: Storefront & Conversion Audit
Review the customer-facing experience:

**Homepage:**
- [ ] Clear value prop above the fold
- [ ] Best-selling products featured
- [ ] Social proof visible (reviews, press, UGC)
- [ ] Clear navigation and CTAs
- [ ] Mobile-optimized (check on phone)

**Product Pages (PDP):**
- [ ] High-quality images (multiple angles, lifestyle, scale)
- [ ] Compelling product descriptions (benefits > features)
- [ ] Reviews/ratings displayed prominently
- [ ] Clear pricing and shipping info
- [ ] Urgency/scarcity elements (if genuine)
- [ ] Cross-sell/upsell widgets
- [ ] Add-to-cart always visible (sticky on mobile)

**Checkout:**
- [ ] Guest checkout available
- [ ] Minimal form fields
- [ ] Trust badges and security signals
- [ ] Multiple payment options (Apple Pay, Shop Pay, etc.)
- [ ] Clear shipping costs upfront (no surprise at checkout)
- [ ] Order bump or upsell in checkout

**Gate:** All customer-facing issues documented with priority.

### Step 2: Retention & Email/SMS Audit
Review post-purchase marketing:

- [ ] Welcome flow exists (3-5 emails)
- [ ] Abandoned cart flow (3 emails + optional SMS)
- [ ] Post-purchase flow (thank you, review request, cross-sell)
- [ ] Winback flow (30/60/90 day inactive)
- [ ] Browse abandonment flow
- [ ] VIP/loyalty program
- [ ] SMS capture and flows
- [ ] Newsletter/regular campaigns

| Flow | Exists? | Revenue/mo | Improvement Opportunity |
|------|---------|-----------|------------------------|
| Welcome | Y/N | $ | |
| Abandoned Cart | Y/N | $ | |
| Post-Purchase | Y/N | $ | |
| Winback | Y/N | $ | |

**Gate:** All lifecycle flows audited with revenue attribution and gaps.

### Step 3: Traffic & Acquisition Audit
Where is traffic coming from and how efficient is it?

| Source | % of Traffic | Conv Rate | CAC | Revenue | ROAS |
|--------|-------------|-----------|-----|---------|------|
| Organic | | | | | |
| Meta Ads | | | | | |
| Google Ads | | | | | |
| Email | | | | | |
| Direct | | | | | |
| Social | | | | | |
| Influencer | | | | | |

Key questions:
- Is there channel concentration risk (>50% from one source)?
- Which channels have best CAC and ROAS?
- Are there untapped channels for this product type?

**Gate:** Traffic mix analyzed with efficiency metrics and diversification needs.

### Step 4: Quick Wins & Roadmap
Prioritize by revenue impact:

**Quick wins (this week, no dev needed):**
- Add reviews to PDP if missing
- Fix abandoned cart emails
- Add urgency to low-stock items
- Enable Shop Pay for faster checkout
- Add cross-sells to cart page

**30-day projects:**
- Build or fix email flows (welcome, abandoned cart, post-purchase)
- Optimize top 5 PDPs (copy, images, social proof)
- Set up Meta retargeting
- Launch subscription or bundle offer

**90-day strategy:**
- Scale winning paid channel
- Launch influencer/UGC program
- Build referral or loyalty program
- Content/SEO for organic growth

**Gate:** Prioritized roadmap with estimated revenue impact per initiative.

## Evaluation & QA

### Common Failure Modes
- Focusing on traffic without fixing conversion first (fix the bucket before filling it)
- No email flows (leaving 20-30% of revenue on the table)
- Ignoring mobile experience (70%+ of DTC traffic is mobile)
- No post-purchase strategy (one-time buyers vs repeat customers)
- Competing on price instead of brand/experience