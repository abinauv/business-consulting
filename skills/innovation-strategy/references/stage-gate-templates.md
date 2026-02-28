# Stage-Gate Templates

## Stage-Gate Process Overview

```
DISCOVERY → SCOPING → BUSINESS CASE → DEVELOPMENT → TESTING → LAUNCH
    │          │           │              │            │          │
  Gate 1     Gate 2      Gate 3        Gate 4       Gate 5     Gate 6
  (Idea      (Scope      (Go to        (Go to       (Go to     (Post-
  Screen)    Approved)   Develop)      Test)        Launch)    Launch
                                                               Review)
```

## Gate Criteria by Stage

### Gate 1: Idea Screen

**Purpose:** Does this idea warrant investigation?

| Criteria | Must Pass? | Question |
|----------|:---------:|---------|
| Strategic fit | Yes | Does this align with our strategy and target markets? |
| Market opportunity | Yes | Is the market large enough to pursue (>$X)? |
| Technical plausibility | Yes | Is it technically possible (not science fiction)? |
| Not a duplicate | Yes | Are we already pursuing something similar? |
| Differentiation potential | No | Could we create something meaningfully different? |
| Time-to-market feasibility | No | Can we deliver within an acceptable timeframe? |

**Decision options:** Pass → Scoping | Kill | Park (revisit later)
**Time at gate:** 30-minute review
**Decision makers:** Innovation lead + 1 sponsor

### Gate 2: Scope Approved

**Purpose:** Is the opportunity worth a full business case?

| Criteria | Must Pass? | Evidence Required |
|----------|:---------:|------------------|
| Market size confirmed | Yes | TAM/SAM/SOM estimate with sources |
| Customer problem validated | Yes | 5+ customer interviews confirming the pain point |
| Competitive landscape understood | Yes | Competitive scan showing white space or advantage |
| Technical feasibility confirmed | Yes | Engineering assessment (can we build it?) |
| Rough economics positive | No | Back-of-envelope unit economics look viable |
| Team available | No | Can we staff this with the right people? |

**Decision options:** Pass → Business Case | Kill | Pivot (redefine scope)
**Time at gate:** 1-hour review
**Decision makers:** Innovation Board subset (3 people)

### Gate 3: Go to Develop

**Purpose:** Does the business case justify investment?

| Criteria | Must Pass? | Evidence Required |
|----------|:---------:|------------------|
| Customer willingness to pay | Yes | WTP research or LOIs/pre-orders |
| Business case positive | Yes | 3-year financial model with >X% IRR |
| Competitive advantage articulated | Yes | Clear differentiation and defensibility |
| Technical plan credible | Yes | Architecture, timeline, resource plan |
| Risk assessment acceptable | Yes | Key risks identified with mitigation plans |
| Resource plan funded | Yes | Budget and team approved |
| Go-to-market strategy | No | Initial GTM plan with target customers |

**Decision options:** Pass → Development | Kill | Recycle (redo business case with changes)
**Time at gate:** 2-hour review with full Innovation Board
**Decision makers:** Full Innovation Board

### Gate 4: Go to Test

**Purpose:** Is the product ready for customer testing?

| Criteria | Must Pass? | Evidence Required |
|----------|:---------:|------------------|
| MVP functional | Yes | Working product that delivers core value proposition |
| Quality standards met | Yes | No critical bugs, performance acceptable |
| Test plan defined | Yes | Beta customer list, success criteria, feedback process |
| Regulatory/compliance cleared | Yes (if applicable) | All required approvals obtained |
| Support readiness | No | Support team trained, documentation exists |
| Updated financials | No | Business case updated with actual development costs |

**Decision options:** Pass → Testing | Hold (fix critical issues) | Kill
**Time at gate:** 1-hour review

### Gate 5: Go to Launch

**Purpose:** Is the product ready for full market launch?

| Criteria | Must Pass? | Evidence Required |
|----------|:---------:|------------------|
| Beta results positive | Yes | Customer satisfaction >X, key metrics met |
| Product-market fit signal | Yes | Retention, engagement, or conversion data supports fit |
| Go-to-market plan complete | Yes | Pricing, positioning, channels, launch timeline |
| Operations ready | Yes | Support, billing, fulfillment, SLAs defined |
| Sales enablement complete | Yes | Sales training, demo, battlecard, pricing guide |
| Updated financial forecast | Yes | Revised forecast based on test results |
| Launch budget approved | Yes | Marketing spend, headcount, launch costs |

**Decision options:** Pass → Launch | Hold (conditional — fix specific items) | Kill (doesn't meet threshold)
**Time at gate:** 2-hour review with full Innovation Board

### Gate 6: Post-Launch Review

**Purpose:** Is the product performing? What did we learn?

| Criteria | Evaluate | Timing |
|----------|---------|:------:|
| Revenue vs. forecast | Compare actuals to business case projections | 90 days post-launch |
| Customer adoption | Usage metrics, activation rate, retention | 90 days |
| Customer satisfaction | NPS, CSAT, support ticket volume | 90 days |
| Operational health | Uptime, error rates, support capacity | 30, 60, 90 days |
| Competitive response | How did competitors react? | 90 days |
| Lessons learned | What went well? What would we do differently? | 90 days |
| Scale decision | Invest more, maintain, or sunset? | 90–180 days |

## Gate Review Template

### Review Presentation Format (30 minutes)

| Section | Time | Content |
|---------|:----:|---------|
| Context | 3 min | Initiative name, stage, key milestones since last gate |
| Customer evidence | 5 min | What did we learn from customers? (data, quotes, metrics) |
| Progress vs. plan | 5 min | What was delivered? What was delayed? Why? |
| Key risks and mitigations | 5 min | Top 3 risks, status of mitigations |
| Financial update | 5 min | Updated business case, actual vs. planned spend |
| Recommendation | 2 min | Go / Kill / Pivot / Recycle — with rationale |
| Discussion | 5 min | Questions, debate, decision |

### Gate Review Decision Template

```
Initiative: [Name]
Stage: [Current stage → Proposed next stage]
Date: [Date]
Reviewers: [Names]

DECISION: [ ] GO  [ ] KILL  [ ] HOLD  [ ] PIVOT  [ ] RECYCLE

Conditions (if Hold/Pivot):
1. [Condition that must be met]
2. [Condition that must be met]
Review date for conditions: [Date]

Rationale:
[2-3 sentences explaining the decision]

Next milestone: [What must be achieved by the next gate]
Budget approved for next stage: $[Amount]
```

## Kill Criteria

### When to Stop Investing

| Signal | Threshold | Action |
|--------|----------|--------|
| Customer problem not validated | 10+ interviews, no clear pain point | Kill |
| No willingness to pay | WTP research shows <50% would pay minimum viable price | Kill or major pivot |
| Technical barrier insurmountable | 2+ failed technical approaches within budget | Kill |
| Market too small | TAM <$[minimum threshold] after refined analysis | Kill |
| Can't differentiate | No defensible advantage identified after competitive analysis | Kill or pivot to niche |
| Unit economics don't work | CAC > 3× LTV after optimization attempts | Kill or fundamental pivot |
| Team can't be staffed | Can't attract/allocate required talent within 90 days | Hold or kill |
| Strategic misalignment | Company strategy changed; initiative no longer fits | Kill or divest |
| Overtaken by competitor | Competitor launched equivalent product with significant head start | Kill or acquire |

### Sunk Cost Discipline

Questions to prevent sunk cost fallacy:
1. "If we were starting fresh today with no investment, would we start this project?"
2. "What would a new CEO do with this initiative?"
3. "If we gave the team and budget to something else, what could we achieve?"

## Pivot Frameworks

### Types of Pivots

| Pivot Type | Description | Example |
|-----------|-----------|---------|
| **Customer segment** | Same product, different customer | B2C → B2B (or vice versa) |
| **Problem** | Same customer, different problem | Build CRM → build analytics |
| **Solution** | Same problem, different approach | Software → services (or vice versa) |
| **Channel** | Same product, different distribution | Direct sales → self-serve / marketplace |
| **Revenue model** | Same product, different pricing | Subscription → usage-based |
| **Technology** | Same value, different technology | On-prem → cloud, manual → AI |
| **Platform** | Product → platform | Single app → developer platform |
| **Feature zoom** | One feature becomes the product | Comprehensive suite → focused tool |

### Pivot Decision Framework

```
Have we run 3+ experiments testing our core hypothesis?
├── NO → Run more experiments before deciding
└── YES → Did any experiment show positive signal?
    ├── YES → Double down on what's working (iterate, don't pivot)
    └── NO → Is the customer problem real?
        ├── NO → Customer segment pivot (find a new customer)
        └── YES → Solution pivot (find a new approach to the real problem)
```

## Innovation Metrics by Stage

| Stage | Primary Metrics | Secondary Metrics |
|-------|----------------|------------------|
| **Discovery** | # ideas generated, # customer interviews conducted | Idea quality score, diversity of sources |
| **Scoping** | # ideas that pass Gate 1, time-to-scope | Market size estimates, competitive landscape clarity |
| **Business Case** | Business case quality score, # passing Gate 3 | Projected IRR/NPV, payback period |
| **Development** | Sprint velocity, milestone completion rate | Technical debt, bug rate, cost vs. budget |
| **Testing** | Beta customer satisfaction, product-market fit score | Activation rate, Day 7/30 retention, NPS |
| **Launch** | Revenue vs. forecast, customer acquisition rate | CAC, LTV, market share, competitive win rate |
| **Post-Launch** | ROI vs. business case, NRR, growth rate | Market share trend, customer expansion rate |

### Portfolio-Level Metrics

| Metric | Definition | Benchmark |
|--------|-----------|:---------:|
| **Idea-to-launch ratio** | % of ideas that reach market | 5–15% |
| **Time-to-market** | Average time from idea to launch | Industry-specific |
| **Innovation revenue %** | % of revenue from products <3 years old | 20–30% |
| **R&D productivity** | Revenue from new products / R&D spend | >3x over 5 years |
| **Portfolio balance** | Actual 70/20/10 vs. target allocation | Within 10% of target |
| **Kill rate** | % of initiatives killed per year | 30–50% (healthy discipline) |
| **Pivot rate** | % of initiatives that pivoted | 20–30% |
| **Innovation ROI** | NPV of launched innovations / Total innovation investment | >2x over 3 years |

## Fast-Track Process for Small Bets

For experiments under $50K and 30 days:

| Element | Standard Stage-Gate | Fast-Track |
|---------|:---:|:---:|
| **Approval** | Innovation Board | Single sponsor (VP+) |
| **Business case** | Full financial model | 1-page experiment brief |
| **Gates** | 6 formal gates | 2 checkpoints (start + review) |
| **Timeline** | 6–18 months | 2–4 weeks |
| **Success criteria** | Revenue, market share | Hypothesis validated/invalidated |
| **Kill decision** | Board decision | Team + sponsor can kill anytime |
| **Documentation** | Full stage-gate documentation | Experiment card (hypothesis, test, result, learning) |

### Experiment Card Template

```
EXPERIMENT #[number]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Hypothesis: "We believe [target customers] will [take action]
             because [reason], which we'll measure by [metric]."

Test:        [What we'll do to test this — specific, time-bound]
Duration:    [X weeks]
Budget:      [$X]
Success:     [Specific metric threshold that validates hypothesis]
Failure:     [Specific metric threshold that invalidates hypothesis]

RESULT: [ ] VALIDATED  [ ] INVALIDATED  [ ] INCONCLUSIVE

Data:        [Actual results vs. success criteria]
Learning:    [What did we learn? What was surprising?]
Next step:   [ ] Scale  [ ] Iterate  [ ] Pivot  [ ] Kill
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```
