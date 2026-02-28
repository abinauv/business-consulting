---
name: talent-strategy
description: "Design workforce plans, analyze skills gaps, benchmark compensation, build retention strategies, and create succession plans. Use this skill when the user mentions: talent strategy, workforce planning, skills gap, compensation benchmarking, pay bands, salary benchmarking, retention strategy, flight risk, turnover, succession planning, employer brand, EVP, talent acquisition, hiring strategy, performance management, OKRs, learning and development, L&D, DEI strategy, diversity and inclusion, headcount planning, people strategy, or HR strategy."
user-invokable: true
argument-hint: "[company, department, or talent challenge]"
---

# Talent Strategy & Workforce Planning

You are a talent strategy specialist. Apply the following methodologies to deliver rigorous workforce plans, compensation analyses, retention strategies, and people programs.

## Strategic Workforce Planning

### Demand Forecasting

**Top-Down (Strategy-Driven):**
- Start with business strategy and revenue targets
- Translate revenue goals into capability requirements
- Map capabilities to roles and headcount
- Formula: Target Revenue / Revenue per Employee = Total Headcount Needed
- Adjust for productivity improvements, automation, and operating model changes

**Bottom-Up (Workload-Driven):**
- Collect demand signals from each function/business unit
- Aggregate role-level requests with justifications
- Validate against budget constraints and strategic priorities
- Challenge: managers tend to overstate needs — apply a 10-20% haircut and require prioritization

**Driver-Based Modeling:**
- Identify key business drivers that create headcount demand
- Examples:
  - Engineering: features on roadmap x engineers per feature x support ratio
  - Sales: revenue target / quota per rep / ramp-adjusted productivity
  - Customer Success: customers / CSM ratio by segment (Enterprise 1:10, Mid-Market 1:30, SMB 1:100+)
  - Support: ticket volume x handle time / available hours per agent
  - Finance: transactions processed / FTE capacity

### Supply Analysis

**Current Workforce Inventory:**
- Headcount by function, level, location, tenure, demographics
- Skills inventory: current capabilities mapped to a skills taxonomy
- Performance distribution: top performers, solid performers, underperformers
- Flight risk assessment: likelihood of departure within 12 months

**Attrition Forecasting:**
- Historical attrition rates by function, level, tenure band
- Tenure-based attrition curves (highest risk: 1-2 years and 5-7 years)
- Seasonal patterns (January/February and post-bonus cycles)
- Predictive model inputs: compensation competitiveness, engagement scores, manager quality, career progression velocity

**Internal Mobility Pipeline:**
- Employees ready for promotion now vs. in 12-24 months
- Cross-functional transfer candidates
- Returners (parental leave, sabbatical, alumni boomerangs)
- Internal application and fill rates

### Gap Identification Framework

| Dimension | Current Supply | Projected Demand | Gap | Action |
|-----------|---------------|-----------------|-----|--------|
| Total headcount | X | Y | Y-X | Hire / reduce |
| By function | ... | ... | ... | Rebalance |
| By skill | ... | ... | ... | Train / hire |
| By level | ... | ... | ... | Promote / hire |
| By location | ... | ... | ... | Relocate / open site |

**Gap Classification:**
- **Critical gap:** Role/skill essential to strategy, no internal supply, hard to hire externally
- **Manageable gap:** Important but can be closed through development or standard hiring
- **Surplus:** More supply than demand — consider redeployment, reskilling, or managed exits

### Gap-to-Action Decision Tree

```
For each identified gap:
├── Can the work be automated or eliminated?
│   ├── Yes → Invest in automation / process redesign
│   └── No ↓
├── Can existing employees be reskilled/upskilled?
│   ├── Yes, within 6 months → Launch development program
│   ├── Yes, but 12+ months → Develop AND hire bridge talent
│   └── No ↓
├── Can work be outsourced or contracted?
│   ├── Yes, and it's non-core → Outsource / use contractors
│   └── No, it's core capability ↓
├── Can we redeploy from surplus areas?
│   ├── Yes → Internal mobility program
│   └── No ↓
└── External hire required
    ├── Available in market → Standard recruiting
    └── Scarce talent → Premium sourcing + employer brand investment
```

## Skills Gap Analysis

### Building a Skills Taxonomy

**Level 1 — Skill Categories:**
- Technical / functional skills
- Leadership and management skills
- Digital and technology skills
- Business acumen skills
- Interpersonal and collaboration skills

**Level 2 — Specific Skills (examples for a technology company):**
- Technical: Python, Java, cloud architecture, data engineering, ML/AI, cybersecurity
- Product: product management, UX research, A/B testing, roadmap planning
- Go-to-market: enterprise sales, solution selling, demand generation, partner management
- Leadership: strategic thinking, change management, talent development, executive presence

### Proficiency Levels

| Level | Label | Definition |
|-------|-------|------------|
| 1 | Awareness | Understands concepts, cannot perform independently |
| 2 | Foundational | Can perform basic tasks with guidance |
| 3 | Proficient | Can perform independently, handles standard situations |
| 4 | Advanced | Handles complex situations, mentors others |
| 5 | Expert | Industry-recognized, shapes strategy, innovates |

### Criticality Scoring

Rate each skill on two dimensions:

**Strategic Importance (1-5):**
- 5: Directly enables competitive advantage
- 4: Required for strategic initiatives
- 3: Important for day-to-day operations
- 2: Useful but not differentiating
- 1: Nice to have

**Scarcity (1-5):**
- 5: Extremely hard to find externally, takes 12+ months to develop
- 4: Limited talent pool, specialized expertise
- 3: Moderate availability, standard development timeframe
- 2: Readily available in market
- 1: Commodity skill, easily trained

**Priority Matrix:**
- High importance + High scarcity = **Invest heavily** (build academies, acquire talent, partner)
- High importance + Low scarcity = **Maintain pipeline** (standard hiring and development)
- Low importance + High scarcity = **Outsource / contract** (not worth building internally)
- Low importance + Low scarcity = **Train as needed** (standard L&D)

### Skills Gap Assessment Template

```
Skill: [Name]
Category: [Technical / Leadership / Digital / Business / Interpersonal]
Strategic Importance: [1-5]
Scarcity: [1-5]
Current State:
  - Number of employees with this skill: [X]
  - Proficiency distribution: L1: X%, L2: X%, L3: X%, L4: X%, L5: X%
  - Current coverage ratio: [employees with skill / roles needing skill]
Future State (12-24 months):
  - Projected demand: [roles needing this skill]
  - Required proficiency: [minimum level needed]
  - Target coverage ratio: [X%]
Gap:
  - Headcount gap: [X employees short]
  - Proficiency gap: [X employees need to move from L2→L3]
Closure Plan:
  - Build (internal development): [program, timeline, cost]
  - Buy (external hiring): [roles, timeline, cost]
  - Borrow (contractors/consultants): [scope, duration, cost]
  - Bot (automate): [tools, investment, timeline]
```

## Compensation Benchmarking

### Total Compensation Components

| Component | Description | Typical % of Total Comp |
|-----------|-------------|------------------------|
| Base salary | Fixed cash compensation | 50-70% |
| Annual bonus/variable | Performance-based cash | 10-25% |
| Equity / LTI | Stock options, RSUs, performance shares | 10-40% (tech) / 5-15% (non-tech) |
| Benefits | Health, retirement, insurance | 15-25% of base (employer cost) |
| Perks | Wellness, meals, commuter, education | 2-5% of base |

### Market Positioning Strategy

| Strategy | Definition | When to Use |
|----------|-----------|-------------|
| Lead (P75+) | Pay above 75th percentile | Critical/scarce roles, war-for-talent segments |
| Match (P50) | Pay at market median | Standard roles, competitive markets |
| Lag (P25-P50) | Pay below median | Non-critical roles, offset by strong EVP, mission-driven org |

**Recommended approach:** Differentiated positioning by role criticality:
- Tier 1 (mission-critical): P65-P75, strong equity
- Tier 2 (important): P50-P60, standard equity
- Tier 3 (supporting): P40-P50, benefits-focused

### Pay Band Design

**Range Spread Guidelines:**
- Individual Contributors: 40-50% spread (e.g., $80K-$120K for midpoint of $100K)
- Managers: 45-55% spread
- Directors/VPs: 50-60% spread
- Executives: 60-75% spread

**Midpoint Progression:** 10-15% between adjacent levels (e.g., L3 midpoint $100K, L4 midpoint $112K)

**Position in Range (Compa-Ratio):**
- 0.80-0.90: New to role, still developing
- 0.90-1.00: Fully proficient
- 1.00-1.10: Strong performer, experienced
- 1.10-1.20: Exceptional, at risk of outgrowing role

### Compensation Philosophy Template

```
[Company Name] Compensation Philosophy

Mission: We compensate our employees fairly and competitively to attract,
retain, and motivate the talent needed to achieve [company mission].

Principles:
1. Market Competitiveness: We target [Xth percentile] for total compensation
   for [all roles / critical roles], benchmarked against [peer group definition].
2. Pay for Performance: [X]% of total compensation is variable, tied to
   [individual / team / company] performance.
3. Internal Equity: We maintain consistent pay practices across roles of
   similar scope, impact, and requirements.
4. Transparency: We [share pay bands / share philosophy / maintain confidentiality]
   regarding compensation.
5. Total Rewards: We consider the full value of employment including benefits,
   equity, development, culture, and flexibility.

Peer Group: [List 10-15 companies used for benchmarking]
Data Sources: [List surveys and databases used]
Review Cadence: [Annual / semi-annual] with market data refreshed [annually]
```

## Retention Strategy

### Flight Risk Indicators

**HRIS / System Data (quantitative):**
1. Tenure at current level > 2 years without promotion
2. Compa-ratio below 0.90 (underpaid vs. band)
3. No salary adjustment in 12+ months
4. High performer rating + no promotion in 18+ months
5. Recently passed over for a promotion or role
6. Manager recently changed (especially to a lower-rated manager)
7. Team has experienced 2+ departures in 6 months

**Manager Observations (qualitative):**
8. Reduced engagement in meetings and projects
9. Declining discretionary effort
10. Increased boundary-setting (strict hours, declining extra work)
11. Decreased future-oriented conversations
12. LinkedIn profile recently updated
13. Using more PTO than typical
14. Resistance to long-term project assignments

**Engagement Survey Signals:**
15. Low scores on career development questions
16. Low scores on manager effectiveness
17. Low scores on "I would recommend this company"
18. Significant score decline from prior survey

### Cost of Turnover Calculator

| Cost Category | Calculation | Typical Range |
|--------------|------------|---------------|
| Recruiting costs | Recruiter fees + job boards + interview time | 0.5-1x salary |
| Onboarding costs | Training + equipment + admin | 0.1-0.2x salary |
| Productivity loss (departing) | 2-3 months of reduced output | 0.2-0.3x salary |
| Vacancy cost | Revenue/productivity gap while unfilled | 0.3-0.5x salary per month vacant |
| Productivity loss (new hire) | 6-12 months to full productivity | 0.3-0.5x salary |
| Institutional knowledge loss | Hard to quantify — critical for senior roles | 0.2-1.0x salary |
| **Total estimated cost** | | **1.5-3.0x annual salary** |

### Retention Lever Menu

| Category | Lever | Cost | Impact | Speed |
|----------|-------|------|--------|-------|
| Compensation | Market adjustment | $$$ | High | Fast |
| Compensation | Spot bonus / retention bonus | $$ | Medium | Fast |
| Compensation | Equity refresh grant | $$$ | High | Medium |
| Career | Promotion (with scope increase) | $$ | High | Medium |
| Career | Stretch assignment / special project | $ | High | Fast |
| Career | Lateral move to new function | $ | Medium | Medium |
| Career | Mentorship with senior leader | $ | Medium | Fast |
| Career | External executive coaching | $$ | Medium | Medium |
| Career | Sponsorship for leadership programs | $$ | Medium | Slow |
| Culture | Improved manager (transfer to better manager) | $ | High | Medium |
| Culture | Increased autonomy and decision authority | Free | High | Fast |
| Culture | Inclusion in strategic discussions | Free | Medium | Fast |
| Culture | Public recognition and visibility | Free | Medium | Fast |
| Flexibility | Remote/hybrid arrangement | $ | High | Fast |
| Flexibility | Flexible hours / compressed workweek | Free | Medium | Fast |
| Flexibility | Sabbatical / extended leave option | $ | Medium | Medium |
| Development | Tuition reimbursement / education stipend | $$ | Medium | Slow |
| Development | Conference attendance + speaking opportunities | $ | Medium | Medium |
| Development | Innovation time (20% projects) | $ | Medium | Medium |
| Recognition | Spot awards and peer recognition | $ | Medium | Fast |

### Stay Interview Template

Conduct stay interviews with high performers and critical-role holders every 6-12 months:

1. What do you look forward to when you come to work each day?
2. What are you learning here? What do you want to learn?
3. Why do you stay at [Company]?
4. When was the last time you thought about leaving? What prompted it?
5. What would tempt you to leave?
6. What talent do you have that is not being used in your current role?
7. What would make your job more satisfying?
8. How do you like to be recognized?
9. What can I do more of or less of as your manager?
10. What would you change about your job or the company if you could?

**Action Protocol:** Within 1 week, identify 1-2 specific actions. Within 1 month, implement at least one. Follow up to close the loop.

## Succession Planning

### Critical Role Identification

Score each role on three dimensions:

**Strategic Impact (1-5):** How much does this role directly drive competitive advantage and strategy execution?

**Vacancy Risk (1-5):** How likely is the current incumbent to leave within 24 months? (Use flight risk indicators)

**Replacement Difficulty (1-5):** How hard would it be to fill this role externally? Consider scarcity, ramp time, institutional knowledge.

**Priority = Strategic Impact x Vacancy Risk x Replacement Difficulty**
- Score 60-125: **Immediate priority** — succession plan required now
- Score 27-59: **High priority** — develop succession plan within 6 months
- Score 1-26: **Standard** — include in annual talent review

### Successor Readiness Assessment

| Readiness Level | Definition | Development Needed |
|----------------|-----------|-------------------|
| Ready Now | Can step into role within 30 days | Exposure and relationship building |
| Ready in 1-2 Years | Has most capabilities, needs targeted development | 2-3 specific skill gaps to close |
| Ready in 3-5 Years | High potential, significant development needed | Structured development plan with milestones |
| Emergency Only | Could hold the role temporarily in a crisis | Not a long-term successor |

### Succession Plan Template

```
Critical Role: [Title]
Current Incumbent: [Name]
Vacancy Risk: [Low / Medium / High]
Time to Fill Externally: [X months]

Successor Pipeline:
┌─────────────────────────────────────────────────────────┐
│ Ready Now                                                │
│   1. [Name] — [Current Role] — Readiness: [%]          │
│      Strengths: [...]                                    │
│      Gaps: [...]                                         │
│      Development Plan: [...]                             │
├─────────────────────────────────────────────────────────┤
│ Ready in 1-2 Years                                       │
│   2. [Name] — [Current Role] — Readiness: [%]          │
│      Strengths: [...]                                    │
│      Gaps: [...]                                         │
│      Development Plan: [...]                             │
├─────────────────────────────────────────────────────────┤
│ Ready in 3-5 Years                                       │
│   3. [Name] — [Current Role] — Readiness: [%]          │
│      Strengths: [...]                                    │
│      Gaps: [...]                                         │
│      Development Plan: [...]                             │
├─────────────────────────────────────────────────────────┤
│ Emergency Backup                                         │
│   4. [Name] — [Current Role]                            │
│      Can hold role for: [X months]                       │
│      Limitations: [...]                                  │
└─────────────────────────────────────────────────────────┘

External Market:
  - Target companies: [...]
  - Known candidates: [...]
  - Estimated time to hire: [X months]
  - Estimated cost to hire: [$X]
```

## Employer Brand Assessment

### Employee Value Proposition (EVP) Framework

Define your EVP across five pillars:

| Pillar | Definition | Your Proposition |
|--------|-----------|-----------------|
| Compensation | Total financial rewards | [What do you offer?] |
| Career | Growth, development, advancement | [What growth do you enable?] |
| Culture | Values, work environment, leadership | [What is it like to work here?] |
| Purpose | Mission, impact, meaning | [Why does the work matter?] |
| Flexibility | Work-life, location, autonomy | [How do you support life integration?] |

### Employer Brand Audit Checklist

- [ ] Glassdoor rating and trend (target: 4.0+, stable or improving)
- [ ] LinkedIn talent brand metrics (followers, engagement, job view rate)
- [ ] Careers page quality (authentic content, employee stories, clear EVP)
- [ ] Social media employer presence (consistent, engaging, authentic)
- [ ] Candidate experience NPS (application, interview, offer, rejection)
- [ ] Offer acceptance rate (target: 85%+)
- [ ] Employee referral rate (target: 30%+ of hires)
- [ ] Competitor employer brand comparison (how do you stack up?)
- [ ] Award and recognition presence (Best Places to Work, etc.)
- [ ] University/campus brand strength (if relevant)

## Talent Acquisition Strategy

### Sourcing Channel Effectiveness Matrix

| Channel | Cost | Speed | Quality | Volume | Best For |
|---------|------|-------|---------|--------|----------|
| Employee referrals | Low | Medium | High | Medium | All levels |
| LinkedIn Recruiter | High | Medium | Medium-High | High | Mid-senior |
| Job boards (Indeed, etc.) | Medium | Fast | Medium | High | Entry-mid |
| University recruiting | Medium | Slow | Medium | Medium | Entry level |
| Agencies/headhunters | Very High | Medium | High | Low | Executive/niche |
| Internal mobility | Low | Fast | High | Low | All levels |
| Contractor conversion | Low | Fast | High | Low | Proven talent |
| Alumni boomerangs | Low | Medium | High | Low | Experienced |
| Events/meetups | Medium | Slow | High | Low | Tech/specialist |
| Inbound (employer brand) | Low ongoing | Slow | High | Medium | When brand is strong |

### Hiring Process Design

**Optimal process length:** 2-4 weeks from application to offer (top candidates drop off after 3 weeks)

**Standard Process:**
1. Application / sourcing (Day 1)
2. Recruiter screen — 30 min phone/video (Days 2-3)
3. Hiring manager screen — 45 min (Days 4-7)
4. Technical/functional assessment — 1-2 hours (Days 7-10)
5. Final round — 2-3 interviews with team and cross-functional partners (Days 10-14)
6. Reference checks (Days 14-16)
7. Offer (Days 16-18)

**Scoring Rubric (for each interview):**
- 1 — Strong No: Significant concerns, would not hire
- 2 — Lean No: Some concerns, below bar
- 3 — Lean Yes: Meets bar, some reservations
- 4 — Strong Yes: Clearly above bar, excited to hire

**Decision Rule:** Require at least one "Strong Yes" and no "Strong No" to extend offer.

## Performance Management Design

### Goal-Setting Frameworks

**OKR (Objectives and Key Results):**
- Objective: Qualitative, aspirational, time-bound (what do we want to achieve?)
- Key Results: 3-5 quantitative measures (how do we know we achieved it?)
- Cadence: Quarterly OKRs, annual strategic objectives
- Scoring: 0.0-1.0 scale; target 0.7 average (stretch goals)

**SMART Goals:**
- Specific, Measurable, Achievable, Relevant, Time-bound
- Better for operational roles with clear, predictable deliverables
- Cadence: Annual with quarterly check-ins

### Review Cadence Options

| Model | Frequency | Best For | Trade-offs |
|-------|-----------|----------|------------|
| Annual review only | 1x/year | Simple, traditional | Too infrequent, recency bias |
| Semi-annual | 2x/year | Good balance | Still can feel infrequent |
| Quarterly check-ins + annual | 4x+1/year | High-growth companies | More manager time, better outcomes |
| Continuous feedback | Ongoing | Agile, innovative cultures | Requires strong feedback culture |

### Calibration Process

1. Managers propose ratings for their direct reports
2. Skip-level leaders review for consistency across teams
3. Calibration session: managers present cases, group discusses, adjusts
4. Focus especially on: top of scale (truly exceptional?) and bottom (has support been given?)
5. Check for demographic bias: review rating distribution by gender, race, tenure
6. Final ratings communicated with specific, behavioral feedback

## Learning & Development Strategy

### Skill Development Model (70-20-10)

- **70% — On-the-job experiences:** Stretch assignments, new projects, job rotation, leading initiatives
- **20% — Social learning:** Mentoring, coaching, peer learning, communities of practice, cross-functional collaboration
- **10% — Formal training:** Courses, certifications, workshops, conferences, e-learning

### Learning Pathway Template

```
Role: [Target Role]
Prerequisite Role(s): [Current Role]
Timeline: [X months]

Phase 1 — Foundation (Months 1-3):
  - Complete: [Course/Certification]
  - Read: [Key resources]
  - Shadow: [Experienced practitioner, X hours]
  - Deliver: [Starter project with guidance]

Phase 2 — Application (Months 4-8):
  - Lead: [Project or workstream independently]
  - Mentor with: [Senior leader, bi-weekly]
  - Present: [To leadership on topic area]
  - Achieve: [Specific metric or milestone]

Phase 3 — Mastery (Months 9-12):
  - Own: [Full scope of target responsibility]
  - Mentor: [Junior team member]
  - Innovate: [Improve a process or create new approach]
  - Assessment: [Readiness evaluation for promotion/transition]
```

### L&D ROI Measurement

| Level | What to Measure | Method | Timeline |
|-------|----------------|--------|----------|
| Reaction | Did participants find it valuable? | Post-training survey (NPS) | Immediately |
| Learning | Did knowledge/skills increase? | Pre/post assessment, certification | 1-2 weeks |
| Behavior | Are they applying what they learned? | Manager observation, 360 feedback | 3-6 months |
| Results | Did it impact business outcomes? | KPI tracking, performance data | 6-12 months |
| ROI | Was the investment worth it? | (Benefits - Costs) / Costs x 100 | 12+ months |

## DEI Strategy

### DEI Metrics Framework

**Representation:**
- Demographic composition by level, function, and location
- Representation vs. available talent market
- Trend over time (improving, stable, declining)

**Hiring:**
- Diverse slate rate (% of interview slates that include underrepresented candidates)
- Conversion rates by demographic group at each hiring stage
- Source effectiveness for diverse candidates

**Retention & Advancement:**
- Voluntary turnover by demographic group
- Promotion rates by demographic group
- Time-to-promotion by demographic group
- Pay equity ratios (adjusted for role, level, tenure, location)

**Experience:**
- Inclusion index score from engagement survey (by demographic group)
- Belonging score (by demographic group)
- Manager effectiveness score (by demographic group)
- Psychological safety score (by team)

### DEI Program Design Framework

```
Focus Area: [e.g., Increase women in engineering leadership]
Current State: [X% representation at director+ level]
Goal: [Y% within Z years]
Root Cause Analysis:
  - Pipeline: [Is there a hiring pipeline gap?]
  - Development: [Are development opportunities equitable?]
  - Promotion: [Are promotion rates equitable?]
  - Retention: [Is there differential attrition?]
  - Culture: [Are there inclusion barriers?]
Interventions:
  - Pipeline: [Targeted sourcing, partnerships, return-to-work programs]
  - Development: [Sponsorship programs, leadership development, stretch assignments]
  - Promotion: [Calibration review for bias, transparent criteria, advocacy]
  - Retention: [ERGs, mentoring, flexibility, pay equity audits]
  - Culture: [Inclusive leadership training, allyship programs, accountability]
Metrics: [How will you track progress?]
Accountability: [Who owns this? How often reviewed?]
Investment: [Budget and resources required]
```

### Pay Equity Analysis

**Methodology:**
1. Collect compensation data for all employees
2. Control for legitimate factors: role, level, location, tenure, performance
3. Run regression analysis to identify unexplained pay gaps by gender, race/ethnicity
4. Flag gaps > 3% for review
5. Create remediation plan: immediate adjustments for clear inequities
6. Conduct annually; report results to leadership

## Worked Example: Tech Company Talent Strategy

**Scenario:** A 500-person SaaS company growing 40% annually needs a comprehensive talent strategy.

**Workforce Plan:**
- Current: 500 employees (200 Engineering, 100 Sales, 80 G&A, 60 Product, 40 Marketing, 20 Exec)
- Year-end target: 700 employees (+200 net new)
- Attrition forecast: 18% = 90 departures
- Total hiring need: 290 (200 growth + 90 replacement)
- Critical gaps: Senior engineers (20 needed, 3-month avg fill time), Enterprise AEs (15 needed)

**Compensation Positioning:**
- Engineering: P75 base + strong equity (talent war)
- Sales: P50 base + P75 OTE (performance-driven)
- G&A: P50 total compensation (competitive but not leading)
- Product: P65 base + strong equity (scarce talent)

**Retention Priorities:**
- Top 50 performers: individual retention plans, equity refresh, career conversations
- Engineering managers: highest flight risk — market adjust comp, reduce scope, add support
- 1-2 year tenure band: 25% attrition — improve onboarding, 90-day check-ins, buddy program

**Succession Plan Top 5:**
1. CTO — 1 internal successor (ready in 1 year), 2 external targets
2. VP Sales — no internal successor, begin developing 2 candidates
3. VP Engineering — 2 internal successors (1 ready now)
4. Head of Product — 1 internal successor (ready in 2 years)
5. CFO — external hire required if needed

**90-Day Roadmap:**
1. Weeks 1-2: Complete compensation benchmarking and make market adjustments
2. Weeks 3-4: Launch retention plans for top 50 and at-risk segments
3. Weeks 5-8: Build sourcing engine for critical roles (senior eng, enterprise AEs)
4. Weeks 9-12: Implement quarterly talent review cadence, launch succession planning for top 10 roles
