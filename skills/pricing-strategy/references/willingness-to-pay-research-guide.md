# Willingness-to-Pay Research Guide

Comprehensive guide for estimating how much customers will pay, from quick-and-dirty methods to rigorous research techniques.

---

## Van Westendorp Price Sensitivity Meter (PSM)

### Overview
The Van Westendorp PSM uses four price-related questions to identify an acceptable price range and optimal price point. It is the most widely used quick WTP method, requiring no complex analysis software.

### The Four Questions

Ask each respondent (after showing or describing the product):

1. **Too Cheap**: "At what price would you consider this product to be so inexpensive that you would doubt its quality?" (floor)
2. **Cheap / Good Value**: "At what price would you consider this product a bargain -- a great buy for the money?" (value)
3. **Expensive / Getting Expensive**: "At what price would you consider this product starting to get expensive -- not out of the question, but you'd have to think about it?" (consideration)
4. **Too Expensive**: "At what price would this product be so expensive that you would never consider buying it?" (ceiling)

### How to Analyze

**Step 1: Collect responses** (minimum 100 respondents; 200-300 preferred for stable results)

**Step 2: Create cumulative distribution curves**
For each of the four questions, calculate cumulative percentages:
- Too Cheap: cumulative % from HIGH to LOW (i.e., "% who say this price or higher is too cheap")
- Cheap: cumulative % from HIGH to LOW
- Expensive: cumulative % from LOW to HIGH (i.e., "% who say this price or lower is expensive")
- Too Expensive: cumulative % from LOW to HIGH

**Step 3: Plot all four curves on a single chart**
- X-axis: Price points
- Y-axis: Cumulative percentage (0-100%)

**Step 4: Identify key intersection points**

| Intersection | Name | Meaning |
|---|---|---|
| Too Cheap and Expensive | Point of Marginal Cheapness (PMC) | Below this price, more people think it is too cheap than those who think it is expensive. Lower bound of acceptable range. |
| Too Expensive and Cheap | Point of Marginal Expensiveness (PME) | Above this price, more people think it is too expensive than those who think it is cheap. Upper bound of acceptable range. |
| Too Cheap and Too Expensive | Optimal Price Point (OPP) | The price where the fewest people reject on price grounds (either direction). Minimizes resistance. |
| Cheap and Expensive | Indifference Price Point (IDP) | The price where equal numbers find it cheap vs. expensive. Often close to the market's "expected" price. |

**Step 5: Determine the Acceptable Price Range**
- Range: PMC to PME
- Optimal: OPP (where price-based rejection is minimized)
- Market expectation: IDP

### Chart Interpretation Guide

```
100% |  \  Too Cheap                    Too Expensive  /
     |   \                                            /
     |    \           Cheap     Expensive            /
     |     \          /    \   /    \                /
     |      \        /      \ /      \             /
 50% |       \      /    IDP X        \           /
     |        \    /       / \         \         /
     |     PMC X  /       /   \     PME X       /
     |        / \/       /     \       / \     /
     |       /   \      /       \     /   \   /
     |      / OPP X    /         \   /     \ /
  0% |_____/______\___/___________\_/______\/_________
         $10   $20  $30   $40   $50  $60  $70   $80
                     PRICE -->
```

### Limitations and Best Practices
- PSM works best for **new products or categories** where customers have limited reference points
- Less reliable for **highly commoditized** products where prices are well-known
- Always combine with at least one other method for validation
- Segment results by customer type (e.g., enterprise vs. SMB, power users vs. casual users)
- Frame the product description carefully -- the description shown significantly affects responses

---

## Gabor-Granger Method

### Overview
The Gabor-Granger method directly estimates the demand curve by asking respondents about their purchase intent at different price points. It is simpler than conjoint and produces an actionable demand curve.

### Methodology

**Step 1: Define price range**
- Select 5-7 price points spanning your expected range
- Include prices below and above your expected optimal price
- Space prices evenly or concentrate around areas of interest

**Step 2: Sequential questioning**
For each respondent:
1. Show product description
2. Start at a random price point within the range (randomize starting point across respondents to avoid bias)
3. Ask: "Would you buy this product at $X?"
4. If YES: move to the next higher price and ask again
5. If NO: move to the next lower price and ask again
6. Continue until you reach the boundary of the price range or the respondent reverses direction

**Alternative (simpler) approach:**
- Show each respondent ALL price points (randomized order)
- Ask purchase intent on a 5-point scale for each price
- This is less realistic but easier to administer

**Step 3: Construct the demand curve**
- For each price point, calculate the percentage of respondents who said "yes" (or rated 4-5 on intent scale)
- Plot price (X-axis) vs. % who would buy (Y-axis)
- The result is a downward-sloping demand curve

**Step 4: Calculate revenue-maximizing price**
- Revenue at each price = Price x % who would buy (as a proxy for demand)
- The price that maximizes this product is the revenue-maximizing price point

### Example Demand Curve and Revenue Calculation

| Price | % Would Buy | Revenue Index (Price x %) |
|---|---|---|
| $19 | 85% | 16.15 |
| $29 | 72% | 20.88 |
| $39 | 58% | 22.62 |
| $49 | 41% | 20.09 |
| $59 | 28% | 16.52 |
| $69 | 15% | 10.35 |
| $79 | 7% | 5.53 |

**Optimal price: $39** (highest revenue index)

### Best Practices
- **Sample size**: 200-500 respondents per segment
- **Randomize starting price** to avoid anchoring bias
- **Include a "definitely would buy" and "probably would buy" scale** rather than binary yes/no for more nuance
- **Apply a "purchase intent discount"**: multiply stated intent by 0.3-0.5 to get realistic demand (people overstate purchase intent in surveys)
- **Segment results**: run separately for different customer types

---

## Conjoint Analysis Basics

### Overview
Conjoint analysis is the gold standard for WTP research. It measures how customers make trade-offs between product attributes (including price) to determine the relative importance and value of each feature.

### Key Concepts

**Attributes**: The dimensions of the product that vary (e.g., price, features, brand, support level)
**Levels**: The specific options within each attribute (e.g., price: $29, $49, $79; support: email, chat, phone)
**Profiles**: Specific product configurations combining one level from each attribute
**Choice tasks**: Respondents choose their preferred profile from a set of 2-4 options (plus "none")

### Design Steps

**Step 1: Select attributes and levels**
- Include 4-7 attributes (more creates respondent fatigue)
- Include 2-5 levels per attribute
- Price MUST be one of the attributes
- Levels should be realistic and span the range you are considering

**Example for a SaaS project management tool:**

| Attribute | Levels |
|---|---|
| Price (per user/month) | $9, $19, $29, $49 |
| Storage | 10 GB, 50 GB, Unlimited |
| Integrations | 5 apps, 20 apps, Unlimited |
| Support | Email only, Email + Chat, Dedicated CSM |
| AI features | None, Basic automation, Advanced AI |

**Step 2: Generate experimental design**
- Use fractional factorial design (you cannot show all possible combinations)
- Software tools: Sawtooth Software, Qualtrics, R (conjoint package), Python (pyDOE)
- Typically requires 8-15 choice tasks per respondent

**Step 3: Field the survey**
- Show respondents a series of choice tasks
- Each task presents 2-4 product profiles and a "none of these" option
- Respondents pick their preferred option

**Example choice task:**

| | Option A | Option B | Option C |
|---|---|---|---|
| Price | $19/user/mo | $29/user/mo | $49/user/mo |
| Storage | 10 GB | 50 GB | Unlimited |
| Integrations | 5 apps | 20 apps | Unlimited |
| Support | Email only | Email + Chat | Dedicated CSM |
| AI features | Basic | None | Advanced AI |
| **Your choice** | [ ] | [ ] | [ ] |
| | | **None of these** [ ] | |

**Step 4: Analyze results**
- Run hierarchical Bayes (HB) estimation or multinomial logit model
- Output: part-worth utilities for each level of each attribute
- These utilities quantify the relative value of each feature at each level

**Step 5: Interpret and apply**

From part-worth utilities, you can derive:
1. **Relative importance** of each attribute (price vs. features vs. support)
2. **Willingness-to-pay for specific features** (e.g., "customers will pay $8 more per month for advanced AI")
3. **Optimal product configurations** for different segments
4. **Demand simulation**: model market share at different price/feature combinations
5. **Price sensitivity**: how demand changes as you vary price while holding features constant

### Conjoint Analysis Checklist
- [ ] 4-7 attributes, each with 2-5 realistic levels
- [ ] Price included as an attribute (use realistic market prices)
- [ ] "None" option included in each choice task
- [ ] 8-15 choice tasks per respondent (avoid fatigue)
- [ ] Sample size: 300-1,000 respondents (minimum 200 per segment)
- [ ] Respondents are screened for purchase relevance
- [ ] Experimental design is balanced (orthogonal or near-orthogonal)
- [ ] Pilot test with 20-30 respondents before full launch

---

## Method Comparison

| Dimension | Van Westendorp | Gabor-Granger | Conjoint Analysis |
|---|---|---|---|
| **What it measures** | Acceptable price range | Demand at each price point | Trade-offs between price and features |
| **Output** | Price range, optimal price | Demand curve, revenue-maximizing price | WTP for features, optimal bundles, demand simulation |
| **Complexity** | Low | Low-Medium | High |
| **Survey length** | 4 questions | 5-7 questions | 10-20 minutes |
| **Sample size needed** | 100-300 | 200-500 | 300-1,000 |
| **Cost** | $2,000-$10,000 | $5,000-$20,000 | $20,000-$100,000 |
| **Analysis tools** | Excel/spreadsheet | Excel/spreadsheet | Specialized software |
| **Best for** | Early-stage range finding | Price point optimization | Tier design, feature valuation |
| **Limitation** | No demand curve | Ignores feature trade-offs | Expensive, complex, requires expertise |
| **Accuracy** | Moderate | Moderate-Good | High |
| **Time to execute** | 1-2 weeks | 2-3 weeks | 4-8 weeks |

### Decision Guide: Which Method to Use

```
START: What do you need to learn?
|
|-- "What price range is acceptable?"
|   --> Van Westendorp PSM
|
|-- "What specific price maximizes revenue?"
|   --> Gabor-Granger
|
|-- "How should I structure tiers and features?"
|   --> Conjoint Analysis
|
|-- "I need quick directional input, not precision"
|   --> Van Westendorp or Quick WTP Estimation (below)
|
|-- "I need to justify pricing to the board with rigor"
|   --> Conjoint Analysis (or Gabor-Granger + competitive analysis)
```

---

## Survey Design Best Practices

### Sample Size Guidelines

| Method | Minimum | Recommended | Ideal |
|---|---|---|---|
| Van Westendorp | 100 | 200-300 | 500+ |
| Gabor-Granger | 200 | 300-500 | 500+ |
| Conjoint | 200 | 300-500 per segment | 1,000+ |
| A/B Price Test | 500 per variant | 1,000 per variant | 5,000+ per variant |

### Question Wording Dos and Don'ts

**Do:**
- Describe the product clearly and consistently before asking price questions
- Use realistic price points that customers might actually encounter
- Randomize price order to avoid anchoring
- Include the full product context (brand, competitive alternatives, purchase situation)
- Specify the unit of measurement clearly ("per user per month," "per year," "one-time")

**Don't:**
- Lead with price ("This product costs $49 -- would you buy it?" anchors the response)
- Use unrealistic extreme prices (they waste statistical power)
- Ask about WTP without providing product context
- Combine WTP questions with satisfaction or NPS surveys (different mindset)
- Use only round numbers (include $37, $43, etc. for realism)

### Avoiding Common Biases

| Bias | Description | Mitigation |
|---|---|---|
| Anchoring | First price shown influences all subsequent responses | Randomize starting price; use multiple starting points |
| Hypothetical bias | Stated WTP is higher than actual WTP | Apply 30-50% discount to stated WTP; use incentive-compatible methods |
| Social desirability | Respondents give "acceptable" answers | Use indirect methods (conjoint); ensure anonymity |
| Range bias | Respondents anchor to the range of prices shown | Ensure price range is wide enough; include "too cheap" and "too expensive" endpoints |
| Order effects | Earlier questions influence later responses | Randomize question order; counterbalance designs |
| Framing effects | How the product is described changes WTP | Standardize description; test multiple frames |

### Respondent Screening

Always screen respondents to ensure they are:
1. **In the target market** (industry, company size, role)
2. **Decision makers or influencers** for this purchase category
3. **Familiar with the product category** (or shown sufficient context)
4. **Not price-immune** (e.g., not purchasing with unlimited corporate budget where price is irrelevant)
5. **Attentive** (include attention check questions, discard speeders)

---

## Quick WTP Estimation Techniques

### When You Cannot Run Formal Research

Sometimes you need a WTP estimate in days, not weeks, and without a research budget. Here are pragmatic alternatives:

### Technique 1: Customer Interview Method (3-5 Days)

**Process:**
1. Interview 10-15 customers or prospects (mix of segments)
2. Ask these questions in this order:
   a. "What are you currently using to solve this problem? What does it cost you?" (establishes reference price)
   b. "What is the biggest pain point with your current solution?" (identifies value drivers)
   c. "If this product solved [pain point], what would that be worth to you annually?" (value-based WTP)
   d. "At what price would you definitely buy this?" (floor)
   e. "At what price would you have to really think about it?" (ceiling)
   f. "What would make you choose this over [competitor] at the same price?" (differentiation value)

**Analysis:**
- Map responses into a simple range: [Floor -- Median -- Ceiling]
- Segment by customer type if responses cluster differently
- Discount stated WTP by 30-40% for realistic estimate

### Technique 2: Competitive Triangulation (1-2 Days)

**Process:**
1. List all direct competitors and their pricing
2. List indirect competitors / alternatives and their cost
3. Map your relative value vs. each competitor (better, same, worse on key dimensions)
4. Calculate a "fair price" based on relative value positioning
5. Adjust for market positioning strategy (premium, parity, or value)

**Formula:**
```
Your Fair Price = Competitor Price x (Your Value Score / Competitor Value Score)
```

### Technique 3: Internal Expert Calibration (1 Day)

**Process:**
1. Gather 5-8 people close to customers (sales reps, CSMs, product managers)
2. Independently, each person estimates:
   - The price at which 80% of prospects would buy (low end)
   - The price at which 20% of prospects would buy (high end)
   - The price at which 50% would buy (midpoint)
3. Average the estimates, weighting by experience
4. Discuss outliers and reasons for disagreement
5. Converge on a consensus range

### Technique 4: Price Ladder Test (1-2 Weeks)

**Process:**
1. Present your product at three different price points to different prospect groups
2. Measure conversion rate, engagement, and objection frequency at each price
3. Plot a simple demand curve from the three data points
4. Select the revenue-maximizing price

This is essentially a lightweight A/B test that does not require large sample sizes (50-100 prospects per price point can give directional signal).

---

## Worked Example: SaaS Product WTP Analysis

### Scenario
**Product**: AI-powered customer support automation platform
**Target market**: Mid-market SaaS companies (100-1,000 employees)
**Current pricing**: $2,000/month flat rate
**Goal**: Determine if pricing should change and by how much

### Step 1: Quick Competitive Triangulation

| Competitor | Pricing | Key Differentiator |
|---|---|---|
| Zendesk AI | $89/agent/month (avg 15 agents = $1,335/mo) | Established brand, broad feature set |
| Intercom Fin | $0.99/resolved conversation (avg 3,000/mo = $2,970/mo) | Usage-aligned, strong product |
| Ada | Custom pricing (~$3,000-$8,000/mo estimated) | Enterprise focus, high automation rate |
| Freshdesk Freddy | $29-$69/agent/month (avg = ~$735/mo) | Budget option, basic AI |

**Our value positioning**: Between Intercom and Ada (strong AI, mid-market focus)
**Competitive price range**: $1,500-$5,000/month for comparable value

### Step 2: Van Westendorp PSM (n=187 mid-market CS leaders)

| Metric | Result |
|---|---|
| Point of Marginal Cheapness (PMC) | $1,200/month |
| Indifference Price Point (IDP) | $2,800/month |
| Optimal Price Point (OPP) | $2,400/month |
| Point of Marginal Expensiveness (PME) | $4,200/month |
| **Acceptable range** | **$1,200 - $4,200/month** |

### Step 3: Economic Value Estimation

**Reference**: Zendesk AI ($1,335/month for 15-agent team)

| Differentiation Factor | Value |
|---|---|
| Higher AI resolution rate (70% vs 40%) | +$2,000/mo (saves 4.5 agent FTEs) |
| Faster implementation (2 weeks vs 8 weeks) | +$200/mo (amortized) |
| Proactive AI (not just reactive) | +$500/mo (reduces ticket volume) |
| Less brand recognition | -$300/mo |
| Smaller integration library | -$200/mo |
| **Total Economic Value** | **$3,535/month** |

**Target price at 60% value capture**: $3,535 x 0.6 = $2,121/month

### Step 4: Synthesis and Recommendation

| Data Source | Price Indication |
|---|---|
| Competitive triangulation | $1,500-$5,000 range |
| Van Westendorp OPP | $2,400/month |
| Van Westendorp acceptable range | $1,200-$4,200/month |
| Economic Value Estimation (60% capture) | $2,121/month |
| Current price | $2,000/month |

**Recommendation**: Increase price to **$2,500/month** for the core plan.

**Rationale:**
- Current $2,000/month is below the Van Westendorp OPP ($2,400) and the indifference price ($2,800)
- $2,500 is within the acceptable range and captures approximately 70% of economic value
- The increase is 25% over current pricing, which is significant but justified by value data
- Introduce a usage-based component (per-resolved-conversation above a base quota) for expansion revenue

**Tier structure recommendation:**

| Tier | Price | Included Resolutions | Overage |
|---|---|---|---|
| Growth | $1,500/mo | 2,000 | $0.60/resolution |
| Professional | $2,500/mo | 5,000 | $0.45/resolution |
| Enterprise | $5,000/mo | 15,000 | $0.30/resolution |

**Projected revenue impact:**
- Current: $2,000/mo x 200 customers = $400K MRR
- Projected (with new tiers and price increase): blended $2,800/mo x 220 customers = $616K MRR
- Uplift: +54% MRR ($216K/month, $2.6M annualized)
