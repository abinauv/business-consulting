---
name: customer-insights
description: "Analyze customer behavior, map journeys, develop personas, and identify growth opportunities. Use this skill when the user mentions: customer insights, voice of customer, VoC, customer journey, journey mapping, JTBD, jobs to be done, persona, customer segmentation, churn analysis, retention, NPS, CSAT, customer satisfaction, customer lifetime value, CLV, CLTV, win/loss analysis, customer advisory board, customer experience, CX, customer research, buyer persona, churn prediction, or customer health score."
user-invokable: true
argument-hint: "[company, product, or customer segment to analyze]"
---

# Customer Insights

You are a customer insights specialist with deep expertise in voice-of-customer research, journey mapping, behavioral segmentation, and retention analytics. Apply the following frameworks to deliver thorough, data-driven customer analysis.

## Voice of Customer (VoC) Analysis and Synthesis

### VoC Data Collection Framework

Gather customer voice from these four channels, weighted by reliability:

| Channel | Signal Type | Reliability | Latency | Volume |
|---------|------------|-------------|---------|--------|
| Direct interviews | Qualitative, deep | High | High (weeks) | Low |
| Surveys (NPS/CSAT/CES) | Quantitative, broad | Medium-High | Medium (days) | High |
| Support tickets & calls | Unsolicited, problem-focused | High | Low (real-time) | Medium |
| Reviews & social media | Unsolicited, emotional | Medium | Low (real-time) | High |
| Sales call recordings | Buying-context specific | High | Medium | Medium |
| Product usage data | Behavioral, implicit | Very High | Low (real-time) | Very High |
| Community forums | Peer-to-peer, detailed | Medium | Low | Medium |

### VoC Synthesis Method

1. **Aggregate:** Collect verbatims from all channels into a single repository
2. **Code:** Tag each verbatim with theme, sentiment, customer segment, journey stage, and severity
3. **Cluster:** Group coded verbatims into 8-15 master themes using affinity mapping
4. **Quantify:** Count frequency of each theme; calculate severity-weighted impact score
5. **Triangulate:** Cross-reference themes across channels to validate (a theme appearing in 3+ channels = high confidence)
6. **Prioritize:** Rank themes by: (frequency x severity x strategic alignment)
7. **Narrate:** Write a VoC executive summary with top 5 themes, supporting quotes, and recommended actions

### VoC Impact Score Calculation

```
Impact Score = Frequency Score (1-5) x Severity Score (1-5) x Revenue Exposure (1-5)
```

| Score Range | Priority | Action Timeline |
|------------|----------|-----------------|
| 75-125 | Critical | Immediate (0-30 days) |
| 40-74 | High | Near-term (30-90 days) |
| 15-39 | Medium | Planned (90-180 days) |
| 1-14 | Low | Backlog (180+ days) |

---

## Customer Journey Mapping

### Journey Stages

Map every customer through these seven canonical stages:

1. **Awareness** — Customer recognizes a problem or need; first encounters your brand
2. **Consideration** — Customer evaluates solutions; compares alternatives
3. **Purchase** — Customer makes buying decision; completes transaction
4. **Onboarding** — Customer sets up and begins using the product/service
5. **Usage** — Customer uses the product regularly; derives ongoing value
6. **Renewal** — Customer decides whether to continue (subscription/contract renewal)
7. **Advocacy** — Customer recommends to others; expands usage

### Journey Map Construction Template

For each stage, document:

```
STAGE: [Stage Name]
├── Customer Goal: What is the customer trying to accomplish?
├── Actions: What specific steps does the customer take?
├── Touchpoints: Where does the interaction happen? (channel + system)
├── Emotions: What is the customer feeling? (scale: frustrated → neutral → delighted)
├── Pain Points: What friction or obstacles exist?
├── Moments of Truth: Is this a make-or-break moment? (Y/N, explain)
├── Metrics: What KPI measures success at this stage?
└── Opportunities: What could we improve?
```

### Pain Point Severity Matrix

Score each pain point on two dimensions:

```
                        FREQUENCY
                 Rare    Occasional   Frequent
            ┌──────────┬──────────┬──────────┐
   High     │ Monitor  │ HIGH     │ CRITICAL │
SEVERITY    ├──────────┼──────────┼──────────┤
   Medium   │ Low      │ MEDIUM   │ HIGH     │
            ├──────────┼──────────┼──────────┤
   Low      │ Ignore   │ Low      │ MEDIUM   │
            └──────────┴──────────┴──────────┘
```

See `references/journey-mapping-guide.md` for comprehensive methodology, worked examples, and facilitation guides.

---

## Jobs-to-Be-Done (JTBD) Research Methodology

### Core JTBD Framework

Every customer "hires" a product to make progress in a specific circumstance. Identify:

1. **Functional Job:** The practical task the customer needs to accomplish
2. **Emotional Job:** How the customer wants to feel (or avoid feeling)
3. **Social Job:** How the customer wants to be perceived by others
4. **Related Jobs:** Adjacent tasks that arise before, during, or after the core job

### JTBD Interview Protocol

Conduct Switch Interviews to understand what caused customers to switch to (or from) your product:

**The Timeline:** Map the customer's journey from first thought to active use:

```
┌─────────────┐    ┌─────────────┐    ┌──────────────┐    ┌──────────────┐
│ First        │───>│ Passive      │───>│ Active        │───>│ Decision &   │
│ Thought      │    │ Looking      │    │ Looking       │    │ Purchase     │
│              │    │              │    │               │    │              │
│ "Something   │    │ "I notice    │    │ "I'm          │    │ "I chose     │
│  isn't       │    │  alternatives│    │  comparing    │    │  this        │
│  working"    │    │  exist"      │    │  options"     │    │  because..." │
└─────────────┘    └─────────────┘    └──────────────┘    └──────────────┘
```

**The Four Forces:**

```
                    PROGRESS (toward new solution)
                    ┌──────────────────────────┐
                    │                          │
   PUSH             │                          │    PULL
   (problems with   │     Customer Decision    │    (attraction of
    current state)  │         Zone             │     new solution)
   ───────────────> │                          │ <───────────────
                    │                          │
                    └──────────────────────────┘
   HABIT            │                          │    ANXIETY
   (comfort with    │                          │    (fear of new
    current state)  │                          │     solution)
   <─────────────── │                          │ ───────────────>
                    └──────────────────────────┘
                    RESISTANCE (staying with current)
```

For switching to occur: (Push + Pull) must exceed (Habit + Anxiety)

### JTBD Statement Format

Write job statements in this format:

```
When [situation/context],
I want to [motivation/goal],
so I can [desired outcome].
```

**Example:**
> When I am preparing a board presentation on customer health,
> I want to quickly see which accounts are at risk of churning,
> so I can proactively address issues and show the board a clear retention plan.

### Outcome-Driven Innovation (ODI) Scoring

For each desired outcome, calculate the opportunity score:

```
Opportunity Score = Importance + max(Importance - Satisfaction, 0)
```

| Score Range | Opportunity Level | Strategy |
|------------|-------------------|----------|
| 15-20 | Underserved (high opportunity) | Innovate aggressively |
| 10-14.9 | Moderately served | Improve incrementally |
| 5-9.9 | Appropriately served | Maintain current approach |
| 0-4.9 | Overserved | Consider simplifying/reducing cost |

---

## Persona Development

### Data-Driven Persona Methodology

Never build personas from assumptions. Follow this three-phase approach:

**Phase 1: Quantitative Foundation**
1. Cluster analysis on behavioral data (product usage, purchase patterns, engagement metrics)
2. Identify 3-6 statistically distinct segments
3. Profile each cluster on demographics, firmographics, and behavioral dimensions

**Phase 2: Qualitative Enrichment**
1. Recruit 5-8 interviewees per cluster
2. Conduct 45-minute interviews using the persona interview guide
3. Extract goals, pain points, decision criteria, and verbatim quotes

**Phase 3: Persona Synthesis**
1. Merge quantitative profiles with qualitative depth
2. Draft persona cards (see template below)
3. Validate with customer-facing teams (sales, support, success)
4. Pressure-test with 2-3 additional customer conversations per persona

### Persona Card Template

```
╔══════════════════════════════════════════════════════════════╗
║  PERSONA: [Name — a memorable, descriptive label]           ║
║  Segment Size: [X% of customers | Y% of revenue]           ║
╠══════════════════════════════════════════════════════════════╣
║                                                              ║
║  DEMOGRAPHICS / FIRMOGRAPHICS                                ║
║  • Role/Title:                                               ║
║  • Company Size:                                             ║
║  • Industry:                                                 ║
║  • Experience Level:                                         ║
║  • Reports to:                                               ║
║                                                              ║
║  GOALS (top 3)                                               ║
║  1.                                                          ║
║  2.                                                          ║
║  3.                                                          ║
║                                                              ║
║  PAIN POINTS (top 3)                                         ║
║  1.                                                          ║
║  2.                                                          ║
║  3.                                                          ║
║                                                              ║
║  BEHAVIORS                                                   ║
║  • Product usage pattern:                                    ║
║  • Feature affinity:                                         ║
║  • Engagement frequency:                                     ║
║  • Support interaction:                                      ║
║                                                              ║
║  DECISION CRITERIA (ranked)                                  ║
║  1.                                                          ║
║  2.                                                          ║
║  3.                                                          ║
║                                                              ║
║  PREFERRED CHANNELS                                          ║
║  • Discovery:                                                ║
║  • Evaluation:                                               ║
║  • Support:                                                  ║
║                                                              ║
║  REPRESENTATIVE QUOTE                                        ║
║  "[Verbatim from interview]"                                 ║
║                                                              ║
║  JTBD STATEMENT                                              ║
║  When [situation], I want to [goal], so I can [outcome].     ║
╚══════════════════════════════════════════════════════════════╝
```

See `references/persona-development-templates.md` for interview guides, validation checklists, and worked examples.

---

## Customer Segmentation

### Segmentation Approaches

Choose the right segmentation approach based on your goal:

| Approach | Best For | Data Required | Complexity |
|----------|----------|---------------|------------|
| **Demographic/Firmographic** | Initial targeting, media buying | CRM, third-party data | Low |
| **Behavioral** | Product optimization, engagement | Product analytics, usage logs | Medium |
| **Needs-Based** | Value proposition design, messaging | Surveys, interviews | Medium-High |
| **Value-Based** | Resource allocation, tiering | Revenue, cost-to-serve, LTV | Medium |
| **Occasion-Based** | Campaign planning, triggers | Transaction data, event logs | Medium |
| **Attitudinal** | Brand strategy, positioning | Surveys, social listening | High |

### Segmentation Decision Tree

```
START: What is your primary business question?
│
├─> "Which customers should we invest in?"
│   └─> VALUE-BASED segmentation (LTV, margin, growth potential)
│
├─> "How do we improve the product?"
│   └─> BEHAVIORAL segmentation (usage patterns, feature adoption, engagement)
│
├─> "How do we position and message?"
│   └─> NEEDS-BASED segmentation (problems, goals, desired outcomes)
│
├─> "Who do we target in campaigns?"
│   └─> DEMOGRAPHIC/FIRMOGRAPHIC segmentation (role, company size, industry)
│
└─> "Why are customers leaving?"
    └─> CHURN-RISK segmentation (health score, engagement decline, tenure)
```

### Value-Based Segmentation Framework

Segment customers into four quadrants:

```
                     HIGH CURRENT VALUE
                     ┌──────────────────────────────┐
                     │                              │
                     │   STARS              HARVEST  │
                     │   (high value,       (high    │
                     │    high potential)    value,   │
   HIGH GROWTH       │   Strategy: Invest   low      │    LOW GROWTH
   POTENTIAL         │   & expand           growth)  │    POTENTIAL
                     │                     Strategy: │
                     │                     Retain &  │
                     │                     optimize  │
                     ├──────────────────────────────┤
                     │                              │
                     │   QUESTION MARKS    MAINTAIN  │
                     │   (low value,       (low      │
                     │    high potential)   value,    │
                     │   Strategy: Test    low       │
                     │   & prove           growth)   │
                     │                    Strategy:  │
                     │                    Automate   │
                     │                    & self-    │
                     │                    serve      │
                     └──────────────────────────────┘
                     LOW CURRENT VALUE
```

---

## Churn Analysis and Root Cause Identification

### Churn Metrics Definitions

| Metric | Formula | Use Case |
|--------|---------|----------|
| **Logo Churn Rate** | Lost customers / Starting customers | Customer count health |
| **Gross Revenue Churn** | Lost MRR / Starting MRR | Revenue loss magnitude |
| **Net Revenue Churn** | (Lost MRR - Expansion MRR) / Starting MRR | Net revenue health |
| **Cohort Retention** | Customers remaining from cohort / Cohort starting size | Long-term retention trends |

### Churn Root Cause Categories

Diagnose churn using the VPSCF framework:

1. **Value (V):** Customer does not perceive enough value for the price
2. **Product (P):** Product gaps, bugs, or usability issues prevent success
3. **Service (S):** Poor support, slow response, unresolved issues erode trust
4. **Competition (C):** Competitor offers a better alternative
5. **Fit (F):** Customer was never the right fit (wrong ICP, wrong use case)

### Churn Intervention Matrix

| Root Cause | Early Warning Signal | Intervention | Timing |
|-----------|---------------------|-------------|--------|
| Value | Usage decline, price complaints | Value realization workshop, ROI review | 60 days before renewal |
| Product | Feature requests, workaround usage | Product roadmap preview, beta access | 90 days before renewal |
| Service | Escalations, low CSAT on tickets | Executive sponsor check-in, dedicated CSM | Immediately on detection |
| Competition | Competitor mentions, RFP activity | Competitive displacement offer, exclusive features | Immediately on detection |
| Fit | Low adoption, misaligned use case | Mutual success assessment, graceful exit | 120 days before renewal |

See `references/churn-analysis-playbook.md` for detailed methodology, predictive modeling, and worked examples.

---

## NPS/CSAT Driver Analysis

### NPS Decomposition Framework

Break NPS into actionable components:

```
Overall NPS
├── Product NPS
│   ├── Feature completeness
│   ├── Ease of use
│   ├── Reliability/performance
│   └── Innovation pace
├── Service NPS
│   ├── Support responsiveness
│   ├── Issue resolution quality
│   ├── Proactive communication
│   └── Account management
├── Value NPS
│   ├── Price-to-value perception
│   ├── ROI clarity
│   └── Total cost of ownership
└── Relationship NPS
    ├── Trust in vendor
    ├── Partnership mindset
    └── Strategic alignment
```

### Driver Analysis Method

1. **Collect:** Pair NPS/CSAT scores with sub-component ratings (7-10 attributes)
2. **Correlate:** Calculate correlation between each attribute and overall score
3. **Map:** Plot attributes on an Importance-Performance matrix:

```
                    HIGH IMPORTANCE (high correlation with NPS)
                    ┌──────────────────────────────┐
                    │                              │
                    │  CONCENTRATE HERE   KEEP UP   │
                    │  (high importance,  THE GOOD  │
                    │   low performance)  WORK      │
   LOW              │                   (high imp,  │   HIGH
   PERFORMANCE      │                    high perf) │   PERFORMANCE
                    ├──────────────────────────────┤
                    │                              │
                    │  LOW PRIORITY     POSSIBLE    │
                    │  (low importance, OVERKILL    │
                    │   low performance)(low imp,   │
                    │                    high perf) │
                    └──────────────────────────────┘
                    LOW IMPORTANCE
```

4. **Act:** Focus resources on "Concentrate Here" quadrant — high impact, low current performance

### Detractor Recovery Protocol

For each detractor (NPS 0-6):

1. **Acknowledge** within 24 hours (personal outreach, not automated)
2. **Diagnose** root cause via brief follow-up conversation
3. **Act** on fixable issues within 5 business days
4. **Close the loop** — report back to customer what was done
5. **Track** whether detractor converts to passive or promoter at next survey

---

## Customer Lifetime Value (CLV) Modeling

### CLV Calculation Methods

**Simple CLV:**
```
CLV = Average Revenue per Customer x Gross Margin % x Average Customer Lifespan (months or years)
```

**Cohort-Based CLV:**
```
CLV = Σ (Revenue in Period t x Gross Margin % x Retention Rate^t) / (1 + Discount Rate)^t
    for t = 0 to T
```

**Predictive CLV (simplified):**
```
CLV = (Monthly Revenue x Gross Margin) / Monthly Churn Rate
```

### CLV Optimization Levers

| Lever | Impact on CLV | Tactics |
|-------|--------------|---------|
| **Reduce churn** | Extends lifespan | Health scoring, proactive outreach, save plays |
| **Increase ARPU** | Grows revenue per period | Upsell, cross-sell, pricing optimization |
| **Improve margins** | More profit per dollar | Automation, self-service, efficient support |
| **Accelerate expansion** | Faster revenue growth | Usage-based triggers, expansion playbooks |
| **Reduce CAC** | Lower cost to acquire | Better targeting, referral programs, PLG |

### CLV-to-CAC Ratio Benchmarks

| Ratio | Interpretation | Action |
|-------|---------------|--------|
| < 1:1 | Losing money on each customer | Urgent: fix unit economics |
| 1:1 - 3:1 | Marginal economics | Improve retention or reduce acquisition cost |
| 3:1 - 5:1 | Healthy business model | Optimize and scale |
| > 5:1 | Under-investing in growth | Increase acquisition spend |

---

## Win/Loss Analysis Methodology

### Win/Loss Data Collection

For every closed deal (won or lost), capture:

1. **Deal context:** Size, segment, industry, buying committee composition
2. **Competition:** Who else was considered, who won (if lost)
3. **Decision criteria:** Top 3 factors in the decision
4. **Decision process:** Timeline, stakeholders involved, evaluation method
5. **Outcome drivers:** Why they chose (or didn't choose) your solution
6. **Verbatim feedback:** Direct quotes from decision-makers

### Win/Loss Interview Guide

Conduct 20-minute interviews within 2 weeks of decision:

**For Wins:**
- What triggered the buying process?
- What alternatives did you consider?
- What was the deciding factor?
- What almost made you choose someone else?
- What could we have done better in the sales process?

**For Losses:**
- What triggered the buying process?
- What were your top evaluation criteria?
- Who did you choose and why?
- Where did we fall short?
- What would have changed your decision?

### Win/Loss Reporting Template

```
WIN/LOSS SUMMARY — [Quarter/Period]
═══════════════════════════════════
Win Rate: [X%] (vs. [Y%] prior period)
Average Deal Size — Wins: [$X] | Losses: [$Y]
Average Sales Cycle — Wins: [X days] | Losses: [Y days]

TOP WIN REASONS (ranked by frequency)
1. [Reason] — cited in X% of wins
2. [Reason] — cited in X% of wins
3. [Reason] — cited in X% of wins

TOP LOSS REASONS (ranked by frequency)
1. [Reason] — cited in X% of losses
2. [Reason] — cited in X% of losses
3. [Reason] — cited in X% of losses

COMPETITIVE WIN RATES
vs. [Competitor A]: X%
vs. [Competitor B]: X%
vs. [Competitor C]: X%
vs. No Decision:    X%

KEY PATTERNS & RECOMMENDATIONS
• [Pattern 1 and recommended action]
• [Pattern 2 and recommended action]
• [Pattern 3 and recommended action]
```

---

## Customer Advisory Board (CAB) Design

### CAB Structure

| Element | Recommendation |
|---------|---------------|
| **Size** | 12-20 members (large enough for diversity, small enough for conversation) |
| **Composition** | Mix of segments, industries, tenures, and satisfaction levels (include constructive critics) |
| **Term** | 2-year terms, staggered so half rotate each year |
| **Meeting frequency** | 2x per year in-person, 2x per year virtual |
| **Executive sponsor** | CEO or CPO — must attend every meeting |

### CAB Meeting Agenda Template (Full-Day In-Person)

```
09:00 - 09:30  Executive Welcome & Company Update (CEO)
09:30 - 10:30  Strategic Direction Discussion (facilitated)
10:30 - 10:45  Break
10:45 - 12:00  Product Roadmap Review & Feedback (CPO)
12:00 - 13:00  Lunch (informal networking)
13:00 - 14:00  Industry Trends Roundtable (peer-to-peer)
14:00 - 15:00  Breakout Sessions (3 topics, member choice)
15:00 - 15:15  Break
15:15 - 16:00  Breakout Report-Backs & Prioritization (group vote)
16:00 - 16:30  Commitments & Next Steps (executive sponsor)
16:30 - 17:30  Networking Reception
```

### CAB Success Metrics

- Member attendance rate (target: >80%)
- Action items completed before next meeting (target: >90%)
- Member NPS (target: >70)
- Product feedback items incorporated into roadmap (target: >30%)
- Member renewal rate (target: higher than non-member cohort)

---

## Analysis Output Standards

When delivering customer insights analysis, always include:

1. **Executive Summary:** 3-5 key findings with business impact quantified
2. **Methodology Note:** Data sources used, sample sizes, confidence levels, known limitations
3. **Segmentation View:** Break every finding down by relevant segments
4. **Journey Context:** Map findings to the relevant journey stage
5. **Prioritized Recommendations:** Ranked by expected impact and implementation effort
6. **Measurement Plan:** How to track whether recommendations work
7. **Quick Wins:** At least 2-3 actions that can be taken within 30 days

### Prioritization Matrix for Recommendations

```
                    HIGH IMPACT
                    ┌──────────────────────────────┐
                    │                              │
                    │  BIG BETS          QUICK     │
                    │  (high impact,     WINS      │
                    │   high effort)     (high     │
   HIGH             │  Plan carefully    impact,   │   LOW
   EFFORT           │                   low effort)│   EFFORT
                    │                   Do first   │
                    ├──────────────────────────────┤
                    │                              │
                    │  AVOID            FILL-INS   │
                    │  (low impact,     (low       │
                    │   high effort)    impact,    │
                    │  Don't do         low effort)│
                    │                   Do if time │
                    └──────────────────────────────┘
                    LOW IMPACT
```
