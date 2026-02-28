---
name: pricing-analysis
description: "Run a comprehensive pricing analysis — assesses current pricing, analyzes competition, estimates willingness-to-pay, designs optimal pricing architecture, quantifies revenue impact, and builds an implementation roadmap"
argument-hint: "[product, service, or company to analyze]"
---

# Comprehensive Pricing Analysis

Conduct a full pricing analysis for **$ARGUMENTS**.

This command chains together multiple pricing strategy methodologies to deliver an end-to-end pricing recommendation with financial projections.

## Phase 1: Current Pricing Assessment

### 1.1 Current Model Audit
- Document the current pricing model (per-seat, usage-based, flat-rate, hybrid, etc.)
- Map all current tiers, plans, add-ons, and their price points
- Identify the current pricing metric (what unit does the customer pay for?)
- Calculate current blended ARPU, ACV, and revenue mix by tier/plan
- Assess current gross margin by plan/tier

### 1.2 Pricing Health Diagnostics
Evaluate each indicator and flag issues:

| Diagnostic | Healthy Signal | Warning Signal |
|---|---|---|
| Tier distribution | 20-30% / 45-55% / 15-25% across tiers | >60% on lowest tier (underpriced or poor fencing) |
| Discount frequency | <30% of deals discounted | >50% of deals discounted (pricing too high or poor discipline) |
| Average discount depth | <15% | >25% (pricing integrity eroding) |
| Win rate vs. price objection | Price is #3+ objection | Price is #1 objection consistently |
| Net revenue retention | >100% | <90% (churn or contraction problem) |
| Expansion revenue | >20% of new ARR | <10% (no natural upgrade path) |
| Monthly-to-annual mix | >50% annual | <30% annual (commitment problem) |
| Time since last price change | <18 months | >24 months (likely underpriced) |

### 1.3 Issue Identification
Based on the audit, identify and rank the top 3-5 pricing issues:
- Underpricing (leaving money on the table)
- Overpricing (losing deals on price)
- Poor tier design (wrong features in wrong tiers)
- Weak price fencing (too easy to stay on low tier)
- Missing expansion path (no natural upsell triggers)
- Discount leakage (too many discounts, too deep)
- Model misalignment (pricing metric does not track value)
- Competitive vulnerability (priced above value-line vs. competitors)

---

## Phase 2: Competitive Price Positioning

### 2.1 Competitive Price Map
Create a structured comparison table:

| Competitor | Pricing Model | Entry Price | Mid-Tier Price | Enterprise Price | Key Differentiator |
|---|---|---|---|---|---|
| [Competitor 1] | | | | | |
| [Competitor 2] | | | | | |
| [Competitor 3] | | | | | |
| [Our Product] | | | | | |

### 2.2 Price-Value Analysis
For each competitor, score on key value dimensions (1-10) and plot price vs. value:
- Calculate composite value score (weighted by customer importance)
- Identify the fair-value line
- Determine who is overpriced and underpriced relative to value
- Position our product on the map

### 2.3 Competitive Insights
- Identify pricing model trends in the market (e.g., shift to usage-based)
- Note any recent competitor price changes and market reaction
- Flag competitive vulnerabilities we can exploit through pricing
- Assess the pricing "white space" (underserved price-value positions)

**Output**: Price positioning map (2x2: price vs. value) and competitive comparison matrix

---

## Phase 3: Price Elasticity & Willingness-to-Pay

### 3.1 Price Elasticity Estimation
Estimate demand elasticity using available data:
- If historical price changes exist: calculate arc elasticity
- If no data: use analogous product benchmarks and expert judgment framework
- Classify as inelastic (<1), unit elastic (=1), or elastic (>1)
- Estimate elasticity by segment if possible (enterprise vs. SMB vs. self-serve)

### 3.2 Willingness-to-Pay Estimation
Using the best available method:
- **If customer data available**: Conduct Economic Value Estimation (EVE)
- **If survey possible**: Recommend Van Westendorp or Gabor-Granger approach with specific questions
- **If neither**: Use competitive triangulation + internal expert calibration

For each segment, determine:
| Segment | Estimated WTP Range | Current Price | Gap |
|---|---|---|---|
| [Segment 1] | $X - $Y | $Z | Over/Under by $N |
| [Segment 2] | $X - $Y | $Z | Over/Under by $N |
| [Segment 3] | $X - $Y | $Z | Over/Under by $N |

### 3.3 Value Driver Analysis
Rank the top 5 value drivers by customer importance and willingness-to-pay:
1. [Feature/benefit]: WTP premium of $X
2. [Feature/benefit]: WTP premium of $X
3. [Feature/benefit]: WTP premium of $X
4. [Feature/benefit]: WTP premium of $X
5. [Feature/benefit]: WTP premium of $X

**Output**: WTP ranges by segment, elasticity estimates, and value driver ranking

---

## Phase 4: Optimal Pricing Architecture

### 4.1 Pricing Model Recommendation
Based on the analysis:
- Recommend the optimal pricing model (or confirm current model)
- Define the pricing metric and justify why it aligns with value
- Specify any model changes needed (e.g., shift from flat-rate to usage-based)

### 4.2 Tier Design
Design the recommended tier structure:

| | Tier 1 (Name) | Tier 2 (Name) | Tier 3 (Name) |
|---|---|---|---|
| **Target segment** | | | |
| **Price** | | | |
| **Key features** | | | |
| **Usage limits** | | | |
| **Support level** | | | |
| **Target % of customers** | | | |

### 4.3 Feature Fencing
For each major feature, specify which tier includes it and why:
- Core features: which tier and rationale
- Differentiating features: which tier and upgrade-driver role
- Premium features: which tier and WTP justification

### 4.4 Add-Ons and Expansion
- Recommend add-on products/features and their prices
- Design upsell triggers and upgrade paths
- Specify volume discounts or usage-based components

### 4.5 Discount Governance
- Set discount approval matrix (who can approve what level)
- Define acceptable discount reasons and required quid pro quo
- Establish floor prices (minimum acceptable price per tier)

**Output**: Complete pricing architecture with tiers, features, prices, and governance rules

---

## Phase 5: Revenue Impact Quantification

### 5.1 Revenue Model: Current State
Calculate baseline revenue:

| Metric | Current Value |
|---|---|
| Total customers | |
| Customer mix by tier | |
| Blended ARPU | |
| Monthly recurring revenue | |
| Annual recurring revenue | |
| Net revenue retention | |
| Expansion revenue rate | |

### 5.2 Revenue Model: Proposed State
Project revenue under new pricing:

| Metric | Current | Year 1 | Year 2 | Year 3 |
|---|---|---|---|---|
| New customer ARPU | | | | |
| Existing customer ARPU | | | | |
| Blended ARPU | | | | |
| Total customers | | | | |
| MRR | | | | |
| ARR | | | | |
| Net revenue retention | | | | |

### 5.3 Scenario Analysis
Model three scenarios:

| Scenario | Assumptions | ARR Impact |
|---|---|---|
| Conservative | Lower conversion, some churn from price increase | +$X (+Y%) |
| Base case | Expected conversion and retention | +$X (+Y%) |
| Optimistic | Higher uptake of premium tiers, lower churn | +$X (+Y%) |

### 5.4 Risk Assessment
- Churn risk: estimated customer loss from price changes
- Competitive risk: likelihood of competitive response
- Execution risk: implementation complexity
- Timeline risk: delays in rollout

**Output**: Financial projections table, scenario analysis, and risk assessment

---

## Phase 6: Implementation Roadmap

### 6.1 Pre-Launch (Weeks 1-6)
- [ ] Finalize pricing architecture and get executive approval
- [ ] Update billing and CRM systems
- [ ] Train sales team on new pricing, talk tracks, and objection handling
- [ ] Prepare customer communication materials
- [ ] Brief customer success team on grandfathering policy
- [ ] Update website, pricing page, and marketing collateral
- [ ] Set up tracking for key metrics (conversion, churn, ARPU, win rate)

### 6.2 Soft Launch (Weeks 7-8)
- [ ] New pricing for new customers only
- [ ] Monitor conversion rate vs. baseline daily
- [ ] Collect feedback from sales team and early customers
- [ ] Adjust messaging or positioning if needed (not price)

### 6.3 Existing Customer Communication (Weeks 9-12)
- [ ] Send advance notice to existing customers (60-90 days before change)
- [ ] Offer early renewal at current pricing (creates urgency)
- [ ] Provide clear timeline: current price until [date], new price after
- [ ] Make grandfathering policy explicit and generous

### 6.4 Full Rollout (Weeks 13+)
- [ ] New pricing applies to all new customers and non-renewed existing
- [ ] Grandfather period begins for existing customers (1-2 renewal cycles)
- [ ] Weekly monitoring of key metrics
- [ ] Monthly pricing review for first 3 months

### 6.5 Ongoing Optimization
- [ ] Quarterly pricing review cadence
- [ ] A/B test pricing page elements (layout, anchoring, CTAs)
- [ ] Annual competitive pricing audit
- [ ] Customer WTP research refresh every 12-18 months

**Output**: Gantt-style implementation timeline with owners, milestones, and success metrics

---

## Deliverable Format

Present the complete analysis as a structured report with:

1. **Executive Summary** (1 page): key findings, recommended price, and projected revenue impact
2. **Current State Assessment**: audit findings and identified issues
3. **Competitive Positioning**: price map and comparison matrix
4. **WTP Analysis**: customer value and price sensitivity findings
5. **Recommended Architecture**: tier design, prices, features, governance
6. **Financial Projections**: revenue model with scenarios
7. **Implementation Plan**: phased roadmap with timeline
8. **Appendix**: detailed data tables, methodology notes, assumptions

Use tables, matrices, and structured formats throughout. Provide specific numbers and actionable recommendations, not generic advice.
