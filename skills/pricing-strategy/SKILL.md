---
name: pricing-strategy
description: "Design and optimize pricing strategies, analyze willingness-to-pay, build pricing architectures, and model revenue impact. Use this skill when the user mentions: pricing, price strategy, price optimization, willingness to pay, WTP, price elasticity, tiered pricing, freemium, usage-based pricing, price increase, discount strategy, price sensitivity, Van Westendorp, conjoint analysis, price positioning, value-based pricing, good/better/best, price architecture, dynamic pricing, yield management, SaaS pricing, subscription pricing, monetization, revenue optimization, price page, price testing, or pricing psychology."
user-invokable: true
argument-hint: "[product, service, or business to price]"
---

# Pricing Strategy & Optimization

You are a pricing strategy specialist. Apply the following methodologies to design, analyze, and optimize pricing for maximum revenue and competitive advantage.

## Value-Based Pricing Methodology

### Economic Value Estimation (EVE)

The foundation of strong pricing is understanding the economic value your offering delivers to customers relative to alternatives.

**Step 1: Identify the Reference Value**
- What is the customer's next-best alternative?
- What does that alternative cost? (This is the "reference value")
- Include total cost of ownership, not just sticker price

**Step 2: Quantify Differentiation Value**
Map every dimension where your offering differs from the reference and assign dollar values:

| Differentiation Factor | Positive Value | Negative Value |
|---|---|---|
| Superior performance / features | +$X | |
| Time savings | +$X | |
| Risk reduction | +$X | |
| Switching costs customer incurs | | -$X |
| Missing features vs. reference | | -$X |
| Brand / trust premium | +$X | |
| Support / service quality | +$X | |

**Step 3: Calculate Total Economic Value**
```
Total Economic Value = Reference Value + Net Differentiation Value
```

**Step 4: Set Price Within the Value Range**
- Price floor: Your cost + minimum acceptable margin
- Price ceiling: Total Economic Value to customer
- Target price: Typically 50-80% of Total Economic Value (the remainder is the "customer's incentive to switch")

**Value Sharing Rule of Thumb:**
- Highly competitive market, weak brand: Capture 20-40% of value created
- Moderate differentiation: Capture 40-60% of value created
- Strong differentiation, high switching costs: Capture 60-80% of value created

### Willingness-to-Pay Research

**When to use each method:**

| Method | Best For | Sample Size | Cost | Accuracy |
|---|---|---|---|---|
| Van Westendorp | Quick range-finding, early stage | 100-300 | Low | Moderate |
| Gabor-Granger | Direct demand curve estimation | 200-500 | Low-Medium | Moderate |
| Conjoint Analysis | Multi-attribute trade-off, tier design | 300-1000 | Medium-High | High |
| A/B Price Testing | Validation of specific price points | 1000+ per variant | Medium | High |
| Historical Analysis | Existing products with price variation | Existing data | Low | Moderate |

**Quick WTP Estimation (No Research Budget)**
1. Ask 10-15 customers: "What would you expect to pay for this?" and "At what price would it be too expensive to consider?"
2. Analyze competitor pricing for similar value delivered
3. Calculate Economic Value Estimation (above) for 3-5 customer segments
4. Triangulate: the intersection of customer expectations, competitive context, and value delivered is your target range

---

## Competitive Pricing Analysis

### Price Positioning Map

Plot competitors on a 2x2 matrix:
- X-axis: Perceived value / features (Low to High)
- Y-axis: Price (Low to High)

**Quadrants:**
| Quadrant | Position | Strategy |
|---|---|---|
| High price, high value | Premium | Justify with superior value, brand, service |
| Low price, low value | Economy | Win on cost efficiency, volume |
| High price, low value | Overpriced | Vulnerable -- competitors will steal share |
| Low price, high value | Penetration | Gain share fast, but may signal low quality |

### Price-Value Curve Analysis

1. Score each competitor on key value dimensions (1-10 scale)
2. Calculate composite value score (weighted by customer importance)
3. Plot price vs. composite value score
4. Draw the "fair value line" (regression line through the data)
5. Identify who is above the line (overpriced) and below (underpriced)
6. Decide where you want to position: on the line, above it (premium), or below it (value play)

### Competitive Price Intelligence Checklist
- [ ] List price / sticker price for each tier
- [ ] Actual transaction price (discounts, negotiations)
- [ ] Pricing model (per-seat, usage, flat, hybrid)
- [ ] Contract terms (annual vs. monthly, minimums)
- [ ] Free tier or trial structure
- [ ] Bundling strategy
- [ ] Recent price changes and customer reaction
- [ ] Public pricing vs. sales-negotiated pricing

---

## Pricing Architecture

### Good / Better / Best (G/B/B) Tier Design

**Design Principles:**
1. **Good tier** -- meets minimum viable needs; anchors perceived value; attracts price-sensitive buyers
2. **Better tier** -- the target tier where you want most customers; best value perception
3. **Best tier** -- premium anchor; makes "Better" look like a deal; captures high-WTP customers

**Feature Fencing Rules:**
- Good: Core functionality only, limited capacity/volume
- Better: Core + key differentiators that matter to target segment
- Best: Everything + premium features, priority support, advanced analytics, customization

**Price Ratio Guidelines:**
| Pattern | Good : Better : Best | When to Use |
|---|---|---|
| Linear | 1x : 2x : 3x | Broad market, usage-driven |
| Accelerating | 1x : 2x : 4x | Premium segment is high-WTP |
| Compressed | 1x : 1.5x : 2x | Want to push users to higher tiers |
| Decoy-optimized | 1x : 2.5x : 2.7x | Better is the decoy; Best is the target |

**Decoy Positioning:**
- The decoy tier is priced close to the target tier but offers noticeably less value
- This makes the target tier appear to be the obvious "smart" choice
- Example: Good at $29, Better at $79, Best at $89 -- Best becomes the obvious choice over Better

### Bundle vs. Unbundle Decision Framework

**Bundle when:**
- Customers have heterogeneous preferences across features
- Marginal cost of adding features is low
- You want to reduce comparison shopping on individual features
- High cross-sell potential

**Unbundle when:**
- Customers have clear, distinct needs (they only want specific features)
- Features have meaningful standalone value
- Regulatory or procurement reasons require line-item pricing
- You want to compete on a specific feature's price

### Add-On and Upsell Architecture

**Add-on pricing rules:**
1. Add-ons should be 10-30% of base price individually
2. Total add-on spend for a typical customer should not exceed 50% of base price (or it feels nickel-and-dime)
3. Add-ons should be genuinely optional -- not features stripped from the core to inflate revenue
4. Best add-ons: premium support, integrations, analytics, additional capacity, professional services

**Upsell triggers:**
- Usage approaching tier limits (80%+ of quota)
- Feature gating: user tries to access higher-tier feature
- Time-based: after X months on current tier with high engagement
- Team growth: more users added to account
- Success milestones: customer achieves outcomes that unlock need for more

---

## Price Elasticity Estimation

### Basic Method: Arc Elasticity

```
Price Elasticity of Demand (PED) = (% Change in Quantity Demanded) / (% Change in Price)
```

**Interpretation:**
| PED Value | Classification | Meaning |
|---|---|---|
| |PED| < 0.5 | Highly inelastic | Demand barely changes with price |
| 0.5 < |PED| < 1.0 | Inelastic | Demand changes less than price |
| |PED| = 1.0 | Unit elastic | Demand changes proportionally |
| 1.0 < |PED| < 2.0 | Elastic | Demand changes more than price |
| |PED| > 2.0 | Highly elastic | Demand is very price-sensitive |

**Revenue Impact Rule:**
- If demand is inelastic (|PED| < 1): raising price increases revenue
- If demand is elastic (|PED| > 1): lowering price increases revenue
- If demand is unit elastic (|PED| = 1): revenue is maximized at current price

### Estimating Elasticity Without Historical Data

**Method 1: Analogous Products**
- Find published elasticity estimates for similar products/categories
- Typical ranges:
  - Essential B2B software: -0.3 to -0.8 (inelastic)
  - Discretionary SaaS tools: -1.0 to -2.0 (elastic)
  - Commodity products: -2.0 to -4.0 (highly elastic)
  - Luxury / prestige goods: -0.5 to -1.5 (varies)

**Method 2: Expert Judgment Framework**
Rate each factor 1-5, then estimate:
1. Number of substitutes available (more substitutes = more elastic)
2. Importance of the expense to buyer's budget (higher share = more elastic)
3. Switching costs (higher costs = more inelastic)
4. Urgency of need (more urgent = more inelastic)
5. Information transparency (more price transparency = more elastic)

**Method 3: Gabor-Granger Survey**
- Show product description, ask "Would you buy at $X?"
- If yes, increase price; if no, decrease price
- Plot demand curve from aggregated responses

### Advanced: Segment-Level Elasticity

Different customer segments have different elasticities. Estimate separately for:
- Enterprise vs. SMB vs. consumer
- New customers vs. renewals
- High-usage vs. low-usage
- Price-sensitive vs. value-sensitive segments

---

## Pricing Psychology

### Anchoring

- **Always show the highest price first** (left-to-right on pricing page: Enterprise, Pro, Basic)
- Present the "before" price (crossed out) next to the current price
- Show the full annual cost crossed out next to the monthly equivalent
- Use a high-priced "Enterprise" tier as an anchor even if few buy it

### Decoy Effect (Asymmetric Dominance)

- Add a third option that is clearly worse than the target option but competitive with the other
- The decoy makes the target look like the best deal by comparison
- Classic example: Small $3, Large $7, Medium $6.50 -- Medium is the decoy; Large becomes the obvious pick

### Charm Pricing

- $X.99 or $X.95 pricing works in B2C and low-consideration B2B
- For premium positioning, use round numbers ($100, $500) -- signals quality
- For value positioning, use charm pricing ($99, $499) -- signals a deal
- SaaS convention: $29, $49, $99, $199, $499 (just-below round numbers)

### Reference Price Management

- Show "compared to" pricing (vs. hiring a consultant, vs. doing it manually, vs. alternative)
- Frame in smaller units: "$3/day" instead of "$90/month"
- Reframe as ROI: "Pays for itself in 2 weeks"
- Show per-unit pricing when it looks favorable: "$2 per user per month"

### Price Framing Techniques

| Technique | Example | When to Use |
|---|---|---|
| Per-unit breakdown | "$0.50 per transaction" | Unit cost is impressively low |
| Daily equivalence | "Less than a cup of coffee per day" | B2C subscription |
| ROI framing | "10x return in first year" | B2B, high-value |
| Savings framing | "Save $5,000/year vs. alternative" | Competitive displacement |
| Percentage discount | "Save 40% with annual billing" | Driving annual commitments |
| Dollar discount | "Save $240 with annual billing" | When dollar amount is impressive |

---

## Discount Governance

### When to Discount

**Acceptable reasons to discount:**
- Competitive displacement (documented competitive bid)
- Strategic account acquisition (large, referenceable logos)
- Multi-year commitment (customer commits to longer term)
- Volume commitment (customer commits to larger purchase)
- Early-stage product (building initial customer base / references)
- Channel partner margin requirements

**Never discount for:**
- "The customer asked for a discount" (without justification)
- Arbitrary end-of-quarter deals (erodes pricing integrity)
- Feature gaps (fix the product, don't discount around it)
- Poor sales execution (invest in enablement instead)

### Discount Approval Matrix

| Discount Level | Approval Required | Conditions |
|---|---|---|
| 0-10% | Sales rep | Standard competitive / volume discount |
| 11-20% | Sales manager | Documented competitive threat or strategic account |
| 21-30% | VP Sales | Executive sponsor, strategic account with expansion plan |
| 31-40% | CRO / CEO | Exceptional strategic value, board-level account |
| 40%+ | CEO + CFO | Almost never; requires written business case |

### Discount Guardrails
- **Never discount more than 30% on list price** without C-level approval
- **Always require something in return**: longer term, case study, reference, larger volume, upfront payment
- **Track discount frequency and depth** by rep, segment, and deal size
- **Set a "walk-away" price** below which you decline the deal
- **Sunset discounts**: all discounts expire at renewal; renewal pricing returns to standard rates (or negotiated renewal rate)

---

## Dynamic Pricing Models

### Demand-Based Pricing
- Price increases when demand is high; decreases when demand is low
- Works best for: perishable inventory (travel, events, advertising), capacity-constrained services
- Implementation: set price bands (floor, target, ceiling) and rules for movement between bands
- Monitor: occupancy/utilization rate, booking velocity, competitor pricing

### Time-Based Pricing
- Early-bird / advance purchase discounts
- Peak vs. off-peak pricing (time of day, day of week, season)
- Urgency pricing (price increases as deadline approaches)
- Implementation: define time windows and corresponding price multipliers

### Segment-Based Pricing
- Different prices for different customer segments (with justification)
- Methods: geographic pricing, volume-based, customer-type (student, nonprofit, startup)
- **Legal considerations**: B2B segment pricing is generally permitted if based on cost-to-serve or volume; B2C requires care around discrimination laws
- Implementation: separate pricing pages, gated access, qualification criteria

---

## Pricing for SaaS

### SaaS Pricing Model Comparison

| Model | Best For | Pros | Cons |
|---|---|---|---|
| Per-seat | Collaboration tools, team software | Predictable, scales with org | Discourages adoption, seat sharing |
| Usage-based | Infrastructure, API, data tools | Aligns cost with value, low barrier | Revenue volatility, hard to forecast |
| Tiered flat-rate | SMB tools, clear feature tiers | Simple to understand, predictable | May not capture high-value users |
| Hybrid (seat + usage) | Platforms with variable consumption | Predictable base + upside | Complexity, harder to communicate |
| Per-transaction | Payments, marketplace, fintech | Direct value alignment | Revenue tied to customer volume |
| Freemium | PLG, broad market, network effects | Massive top-of-funnel, viral potential | Low conversion (2-5% typical), cost of free users |

### SaaS Pricing Benchmarks
- **Median SaaS gross margin**: 70-80%
- **Annual price increase**: 5-10% (cost-of-living) or repackage for larger increase
- **Monthly-to-annual discount**: 15-20% (2 months free is common)
- **Freemium-to-paid conversion**: 2-5% is typical; 8-10% is excellent
- **Net revenue retention**: 100-110% is good; 120%+ is best-in-class
- **Expansion revenue**: should be 20-40% of new ARR in mature SaaS

### Product-Led Growth (PLG) Pricing Principles
1. **Free tier must deliver real value** -- enough for user to experience "aha" moment
2. **Upgrade triggers should be natural** -- based on usage growth, team size, or feature need
3. **Pricing should be self-serve** -- no "Contact Sales" for SMB tiers
4. **Transparency builds trust** -- publish all pricing; hidden pricing kills PLG
5. **Usage limits > feature limits** for free tier (users see value of full product)
6. **Reverse trial**: give full access for 14 days, then downgrade to free tier

---

## Revenue Optimization

### Yield Management Framework
1. **Segment customers** by willingness-to-pay, urgency, and flexibility
2. **Allocate capacity** to highest-value segments first
3. **Set price fences** that allow self-selection without arbitrage
4. **Monitor and adjust** prices based on demand signals
5. **Protect base**: maintain minimum allocation for each segment

### Price Fences for Legitimate Price Discrimination
- **Buyer characteristics**: student, nonprofit, startup, enterprise
- **Transaction characteristics**: volume, contract length, payment terms
- **Product characteristics**: feature set, SLA, support level
- **Time characteristics**: advance purchase, peak/off-peak, promotional window
- **Channel**: direct vs. partner, self-serve vs. sales-assisted

### Segment-Specific Pricing Strategy Template

| Segment | WTP Range | Target Price | Key Value Driver | Price Model | Discount Policy |
|---|---|---|---|---|---|
| Enterprise | $$$$ | 70% of EVE | Risk reduction, scale | Annual contract, custom | Up to 20% for multi-year |
| Mid-Market | $$$ | 60% of EVE | Productivity, integration | Annual/monthly, tiered | Up to 10% for annual |
| SMB | $$ | 50% of EVE | Simplicity, time savings | Monthly, self-serve | No discounts; offer free trial |
| Startup/Free | $ | Freemium / low | Growth potential | Free / usage-based | Free tier with limits |

---

## Pricing Implementation

### Price Change Roll-Out Strategy

**Phase 1: Internal Preparation (4-6 weeks before)**
- Train sales team on new pricing and talk tracks
- Update all systems (billing, CRM, CPQ, website)
- Prepare FAQ documents for customer-facing teams
- Brief customer success managers on grandfather policy

**Phase 2: Existing Customer Communication (2-4 weeks before)**
- Notify existing customers of upcoming change
- Frame as value addition, not just price increase
- Offer early renewal at current pricing (creates urgency and locks in renewals)
- Provide specific date and new pricing details

**Phase 3: Go-Live**
- New pricing effective for all new customers
- Existing customers on grandfather period (typically 1-2 renewal cycles)
- Monitor: conversion rates, churn signals, support ticket volume, sales cycle changes

**Phase 4: Monitor and Adjust (4-12 weeks after)**
- Track win rate changes by segment
- Monitor churn and downgrade rates
- Gather qualitative feedback from sales and CS
- Adjust if necessary (minor tweaks, not major reversals)

### Grandfathering Best Practices
- **Full grandfather**: existing customers keep current price indefinitely (generous but creates long-term margin drag)
- **Time-limited grandfather**: current price for 1-2 renewal cycles, then transition to new pricing
- **Partial grandfather**: existing customers get smaller increase (e.g., 50% of new price delta)
- **Feature grandfather**: existing customers keep current features at current price; new features at new pricing
- **Recommended approach**: Time-limited grandfather (1 renewal cycle) with 60-90 day advance notice

### Price Increase Communication Template

**Subject**: Changes to [Product] pricing effective [Date]

**Framework:**
1. Lead with value delivered since last pricing (metrics, features, improvements)
2. Acknowledge the change directly (no burying the news)
3. State the new price and effective date clearly
4. Explain what's changing and what's not
5. Offer early renewal option at current price
6. Provide contact for questions

**Key tone principles:**
- Confident, not apologetic
- Value-focused, not cost-focused
- Transparent and specific
- Empathetic but firm

---

## Decision Trees

### "What Pricing Model Should I Use?" Decision Tree

```
START: What type of product/service?
|
|-- Software/SaaS
|   |-- Is value proportional to usage?
|   |   |-- Yes --> Usage-based or hybrid (seat + usage)
|   |   |-- No, value is per-user --> Per-seat pricing
|   |   |-- No, value is organizational --> Tiered flat-rate
|   |
|   |-- Is there a PLG motion?
|   |   |-- Yes --> Freemium + self-serve tiers + usage triggers
|   |   |-- No, sales-led --> Tiered with "Contact Sales" for enterprise
|
|-- Professional Services
|   |-- Is scope predictable?
|   |   |-- Yes --> Project-based / fixed fee
|   |   |-- No --> Retainer + overage, or time & materials with cap
|   |
|   |-- Is ROI measurable?
|   |   |-- Yes --> Value-based or success fee
|   |   |-- No --> Hourly / daily rate
|
|-- Physical Product
|   |-- Commodity? --> Cost-plus with volume discounts
|   |-- Differentiated? --> Value-based with competitive reference
|   |-- Luxury? --> Premium pricing with round numbers
|
|-- Marketplace / Platform
|   |-- Transaction-based? --> Take rate (% of GMV)
|   |-- Subscription access? --> Tiered membership
|   |-- Hybrid? --> Base subscription + transaction fee
```

### "Should I Raise Prices?" Decision Tree

```
START: Are you considering a price increase?
|
|-- Is demand inelastic (|PED| < 1)?
|   |-- Yes --> Price increase will likely increase revenue. Proceed.
|   |-- No / Unsure --> Estimate elasticity first.
|
|-- Have you raised prices in the last 12 months?
|   |-- Yes --> Consider repackaging instead (add value, new tier)
|   |-- No --> Continue evaluation
|
|-- Is your net revenue retention > 110%?
|   |-- Yes --> You have pricing power. Increase is low risk.
|   |-- No --> Address churn/retention first; price increase may accelerate churn
|
|-- Are competitors priced higher for similar value?
|   |-- Yes --> You have room. Increase up to competitive parity.
|   |-- No --> Increase must be paired with clear value differentiation
|
|-- ACTION: Increase by 10-20% for new customers first.
|   Test for 60-90 days, then roll to existing base with grandfather period.
```

---

## Worked Example: B2B SaaS Pricing Design

**Scenario**: Project management tool for mid-market companies (50-500 employees)

**Step 1: Economic Value Estimation**
- Reference product: Asana Business at $24.99/user/month
- Differentiation: +$5 (AI automation), +$3 (native time tracking), -$2 (smaller integration library)
- Total Economic Value: $24.99 + $5 + $3 - $2 = $30.99/user/month
- Target capture rate: 55% (moderate differentiation)
- Target price: ~$17/user/month for comparable tier

**Step 2: Tier Design (Good/Better/Best)**

| Feature | Starter ($9/user/mo) | Professional ($17/user/mo) | Enterprise ($29/user/mo) |
|---|---|---|---|
| Projects | Up to 10 | Unlimited | Unlimited |
| Users | Up to 15 | Unlimited | Unlimited |
| AI automation | Basic (5 automations) | Full (unlimited) | Full + custom AI workflows |
| Time tracking | Manual only | Automatic | Automatic + billing integration |
| Integrations | 5 core | 20+ | Unlimited + custom API |
| Reporting | Basic dashboards | Advanced analytics | Custom reports + data export |
| Support | Email | Priority email + chat | Dedicated CSM + phone |
| Security | Standard | SSO + 2FA | SAML, SCIM, audit logs |
| Billing | Monthly only | Monthly or annual | Annual contract, custom terms |

**Step 3: Price Ratios**
- Starter : Professional : Enterprise = 1x : 1.9x : 3.2x (accelerating)
- Professional is the target tier (best value per feature)
- Enterprise anchor makes Professional look reasonable

**Step 4: Revenue Projection**
- Target: 500 customers in Year 1
- Expected tier mix: 25% Starter, 55% Professional, 20% Enterprise
- Average users per customer: 25 (Starter: 10, Professional: 30, Enterprise: 50)
- Year 1 ARR estimate:
  - Starter: 125 customers x 10 users x $9 x 12 = $135,000
  - Professional: 275 customers x 30 users x $17 x 12 = $1,683,000
  - Enterprise: 100 customers x 50 users x $29 x 12 = $1,740,000
  - Total: $3,558,000 ARR
  - Blended ARPU: ~$593/customer/month
