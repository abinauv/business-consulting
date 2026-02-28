# Workforce Planning Toolkit

## Demand Modeling Methodology

### Three Approaches

| Approach | Method | Best For | Accuracy |
|----------|--------|---------|:--------:|
| **Top-down** | Start from business strategy → translate to headcount | Strategic planning, M&A, rapid growth scenarios | Medium |
| **Bottom-up** | Start from workload analysis → calculate FTEs needed | Operational planning, specific function sizing | High |
| **Driver-based** | Use business metrics that drive headcount | Recurring planning, model-driven forecasting | High |

### Top-Down Method

```
Revenue target → Revenue per employee → Required headcount
     $100M      ÷      $250K/emp      =      400 FTEs

Adjust for:
  + New capabilities needed (digital, AI, international)
  + Strategic initiatives (new products, new markets)
  − Productivity improvements (automation, process improvement)
  − Outsourcing decisions
```

### Driver-Based Method

| Function | Primary Driver | Ratio Benchmark | Example |
|----------|---------------|:---:|---|
| Sales | Revenue target | $500K–$2M per rep (B2B) | $50M target ÷ $1M/rep = 50 reps |
| Customer Success | # customers | 1 CSM per 20–50 accounts (mid-market) | 500 accounts ÷ 30 = 17 CSMs |
| Engineering | Product roadmap velocity | 1 PM per 6–10 engineers | 60 engineers → 6–10 PMs |
| Finance | Employee count or transaction volume | 1 finance FTE per 50–100 employees | 500 employees → 5–10 finance FTEs |
| HR | Employee count | 1 HR FTE per 75–150 employees | 500 employees → 3–7 HR FTEs |
| Support | Ticket volume | 1 agent per 400–800 tickets/month | 5,000 tickets → 6–12 agents |
| Recruiting | Open requisitions | 1 recruiter per 15–25 active reqs | 40 reqs → 2–3 recruiters |

## Supply Analysis

### Current Headcount Profile

| Dimension | Data Points to Collect |
|-----------|----------------------|
| **Quantity** | Headcount by function, level, location, full-time vs. contract |
| **Quality** | Skills inventory, performance distribution, tenure |
| **Movement** | Attrition rate (voluntary, involuntary), internal mobility, promotion rate |
| **Pipeline** | Current open requisitions, offer pipeline, time-to-fill |
| **Cost** | Average compensation by level/function, total people cost |

### Attrition Forecasting

| Method | Approach | Data Needed |
|--------|---------|------------|
| **Historical average** | Use trailing 12-month attrition rate | 2+ years of turnover data |
| **Segment-specific** | Different rates by function, level, tenure, performance | Granular turnover data |
| **Regression model** | Predict attrition from engagement, tenure, compensation, manager quality | Employee data + survey data |
| **External benchmarks** | Industry/function benchmarks when internal data insufficient | Industry surveys |

**Simple supply projection:**
```
Future Supply = Current Headcount
              − Projected Attrition (voluntary + involuntary)
              − Planned Separations (retirement, contract end)
              + Planned Hires (already in pipeline)
              + Internal Transfers In
              − Internal Transfers Out
```

## Gap Analysis Framework

### 4 Types of Gaps

| Gap Type | Question | Example |
|----------|---------|---------|
| **Quantity gap** | Do we have enough people? | Need 50 engineers, have 35 → gap of 15 |
| **Quality/skills gap** | Do people have the right skills? | Need cloud architects, have on-prem specialists |
| **Location gap** | Are people in the right places? | Need APAC coverage, team is 100% US |
| **Timing gap** | Will we have them when we need them? | Need 10 data scientists by Q3, can only hire 5 by then |

### Gap Analysis Template

| Role/Skill | Current Supply | Future Demand (12 mo) | Gap | Criticality | Action |
|------------|:---:|:---:|:---:|:---:|---|
| Cloud architects | 2 | 6 | -4 | Critical | Hire 2, upskill 2 from infra team |
| Data scientists | 3 | 8 | -5 | Critical | Hire 3, contract 2 |
| Sales reps (enterprise) | 15 | 20 | -5 | High | Hire 5 (Q1–Q2) |
| Marketing managers | 4 | 3 | +1 | Medium | Redeploy 1 to product marketing |
| Finance analysts | 6 | 4 | +2 | Low | Automate processes, natural attrition |

## Gap-to-Action Bridging

### Decision Framework

```
Is this role/skill critical to strategy?
├── YES: Do we have internal talent that can be developed?
│   ├── YES: How quickly? (less than required timeline?)
│   │   ├── YES → DEVELOP (training, rotations, stretch assignments)
│   │   └── NO → HIRE externally + DEVELOP internal pipeline
│   └── NO: Can we hire in our market?
│       ├── YES → HIRE (direct or agency)
│       └── NO → CONTRACT (consulting, freelance) or ACQUIRE (acqui-hire)
└── NO: Can the work be automated?
    ├── YES → AUTOMATE (RPA, AI, process improvement)
    └── NO → OUTSOURCE (BPO, managed services, nearshore)
```

### Action Comparison

| Action | Speed | Cost | Risk | Control | Best For |
|--------|:-----:|:----:|:----:|:-------:|---------|
| **Hire** | 2–6 months | High (salary + recruiting) | Medium (mis-hire) | Full | Core roles, long-term needs |
| **Develop** | 6–18 months | Medium (training + productivity dip) | Low | Full | Adjacent skills, succession |
| **Contract** | 1–4 weeks | Very High (day rate) | Low (short-term) | Medium | Temporary surge, specialized expertise |
| **Redeploy** | 1–3 months | Low (training only) | Medium (fit) | Full | Surplus in one area, gap in another |
| **Outsource** | 1–3 months | Medium-High | Medium (quality) | Low | Non-core, well-defined processes |
| **Automate** | 3–12 months | Medium (build) then Low | Medium (execution) | Full | Repetitive, rule-based work |

## Workforce Planning Data Requirements

| Data Category | Specific Data | Source | Frequency |
|--------------|-------------|--------|:---------:|
| **Headcount** | FTE count by org, function, level, location | HRIS | Monthly |
| **Attrition** | Voluntary/involuntary, by segment, tenure | HRIS | Monthly |
| **Compensation** | Base, bonus, equity, benefits, total comp | HRIS/Payroll | Annual |
| **Performance** | Ratings distribution, high performer identification | Performance system | Annual |
| **Skills** | Skills inventory, certifications, proficiency levels | Skills database or surveys | Annual |
| **Engagement** | Engagement scores, eNPS, satisfaction | Survey platform | Semi-annual |
| **Hiring** | Open reqs, pipeline, time-to-fill, offer acceptance | ATS | Weekly |
| **Business** | Revenue, customers, transactions (driver metrics) | Finance/Operations | Monthly |
| **Market** | Industry salary data, talent availability, competitor hiring | Surveys, LinkedIn | Annual |

## Worked Example: Technology Company Workforce Plan

**Context:** SaaS company scaling from 500 to 800 employees over 18 months to support $50M→$100M ARR growth.

### Current State (500 employees)

| Function | Current | % of Total | Cost ($M) |
|----------|:-------:|:----------:|:---------:|
| Engineering | 180 | 36% | $27M |
| Sales | 80 | 16% | $12M |
| Customer Success | 40 | 8% | $4M |
| Marketing | 30 | 6% | $4.5M |
| G&A (Finance, HR, Legal, IT) | 60 | 12% | $6M |
| Product | 25 | 5% | $4M |
| Operations | 85 | 17% | $8.5M |
| **Total** | **500** | **100%** | **$66M** |

### Demand Forecast (800 employees at $100M ARR)

| Function | Current | Demand | Gap | Driver | Key Hires |
|----------|:-------:|:------:|:---:|--------|-----------|
| Engineering | 180 | 280 | +100 | Product roadmap: AI features, platform scale | 40 backend, 25 ML/AI, 20 frontend, 15 SRE |
| Sales | 80 | 140 | +60 | $100M ARR ÷ $700K/rep quota | 35 AEs, 15 SDRs, 10 SEs |
| Customer Success | 40 | 70 | +30 | 1 CSM per 25 accounts → 1,750 accounts | 20 CSMs, 5 onboarding, 5 support |
| Marketing | 30 | 50 | +20 | Brand awareness + demand gen for upmarket | 8 demand gen, 5 content, 4 product marketing, 3 brand |
| G&A | 60 | 85 | +25 | 1 G&A per 9 employees | 8 finance, 6 HR, 5 IT, 4 legal, 2 facilities |
| Product | 25 | 40 | +15 | 1 PM per 7 engineers | 10 PMs, 3 designers, 2 researchers |
| Operations | 85 | 135 | +50 | Order volume + international expansion | 25 ops, 15 implementation, 10 data ops |
| **Total** | **500** | **800** | **+300** | | |

### Supply-Side Adjustments

| Factor | Impact | Net Gap |
|--------|:------:|:-------:|
| Starting gap | | +300 |
| Projected attrition (18 mo at 15% annual) | -110 replacements needed | +410 |
| Current pipeline (accepted offers) | -20 joining in 30 days | +390 |
| Internal promotions/transfers | -15 fill higher roles | +375 (but still need backfill) |
| Contractor conversion | -10 converting to FTE | +365 |
| **Total hiring need over 18 months** | | **~390 hires** |

### Hiring Plan

| Quarter | Target Hires | Focus Areas | Recruiting Investment |
|---------|:-----------:|------------|:--------------------:|
| Q1 | 50 | Engineering (AI/ML), Sales (AEs) | 5 recruiters, 2 agencies |
| Q2 | 70 | Engineering, CS, Product | 7 recruiters, 2 agencies |
| Q3 | 80 | Engineering, Sales, Operations | 8 recruiters, 3 agencies |
| Q4 | 70 | G&A, Marketing, Operations | 7 recruiters, 2 agencies |
| Q5 | 60 | Engineering, Sales (international) | 6 recruiters, 2 agencies |
| Q6 | 60 | All functions (backfill + growth) | 6 recruiters, 1 agency |
| **Total** | **390** | | **$4.5M recruiting cost** |

### Key Risks and Mitigations

| Risk | Probability | Impact | Mitigation |
|------|:-----------:|:------:|-----------|
| Can't hire AI/ML engineers fast enough | High | High | University partnerships, acqui-hire options, contract-to-perm |
| Attrition increases with hypergrowth | Medium | High | Retention program, equity refresh, culture investment |
| Quality of hire drops when hiring fast | Medium | High | Structured interviews, hiring bar keeper role, 90-day reviews |
| Over-hiring if revenue growth slows | Low | High | Quarterly plan review, contractor buffer (20%), ramp plan gates |
