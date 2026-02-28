# Business Consulting Plugin for Claude

A comprehensive management consulting toolkit that transforms Claude into a senior strategy consultant. Just install the plugin and start asking — no technical knowledge required.

**16 consulting skills** | **24 ready-to-use commands** | **5 industry overlays** | **48 reference guides with templates**

---

## What This Plugin Does

Once installed, Claude gains deep expertise in management consulting — from market sizing and competitive analysis to M&A strategy and digital transformation. You get structured, consultant-grade deliverables instead of generic answers.

**Before this plugin:** "Can you help me analyze my market?"
→ Generic bullet points

**After this plugin:** `/market-scan HR software for mid-market companies`
→ TAM/SAM/SOM sizing, growth drivers, competitive landscape, regulatory trends, key players, and strategic implications — structured like a McKinsey engagement

---

## Quick Start

### Step 1: Install

In Claude Cowork or Claude Code, run:

```
/plugin marketplace add abinauv/business-consulting
/plugin install business-consulting@abinauv-business-consulting
```

### Step 2: Set Your Context (Optional but Recommended)

Tell Claude about your company so every analysis is automatically tailored:

```
/set-context Acme Corp, B2B SaaS, $50M ARR, 600 employees, US-based, selling HR software to mid-market companies
```

### Step 3: Start Using Commands

Just type a command and describe what you need. That's it.

---

## Commands at a Glance

| What You Need | Command | Just Type... |
|---------------|---------|-------------|
| Market overview | `/market-scan` | `/market-scan electric vehicle charging` |
| Competitor deep-dive | `/competitor-profile` | `/competitor-profile Salesforce` |
| SWOT analysis | `/swot` | `/swot our company vs top 3 competitors` |
| Financial model | `/financial-model` | `/financial-model SaaS company, $5M ARR, 30% growth` |
| Benchmark vs peers | `/benchmark` | `/benchmark our sales efficiency vs industry` |
| Strategy deck | `/strategy-deck` | `/strategy-deck market expansion into Europe` |
| Due diligence | `/due-diligence` | `/due-diligence TargetCo acquisition` |
| Cost reduction | `/cost-optimization` | `/cost-optimization our G&A spending` |
| Market entry plan | `/market-entry` | `/market-entry Southeast Asia` |
| Org design review | `/org-design` | `/org-design spans & layers assessment` |
| Scenario planning | `/scenario-plan` | `/scenario-plan impact of AI on our industry` |
| Data analysis | `/analyze-data` | `/analyze-data` then upload a CSV or paste data |
| Change management | `/change-plan` | `/change-plan ERP migration affecting 500 employees` |
| Pricing strategy | `/pricing-analysis` | `/pricing-analysis our SaaS pricing tiers` |
| M&A strategy | `/ma-strategy` | `/ma-strategy should we acquire DataCo for $80M` |
| Customer insights | `/customer-analysis` | `/customer-analysis why are enterprise customers churning` |
| Digital transformation | `/digital-assessment` | `/digital-assessment our company's digital maturity` |
| Risk assessment | `/risk-assessment` | `/risk-assessment supply chain and operational risks` |
| Talent strategy | `/talent-assessment` | `/talent-assessment engineering team retention` |
| Innovation strategy | `/innovation-assessment` | `/innovation-assessment our R&D portfolio balance` |

### Multi-Step Playbooks

These combine multiple skills into end-to-end analyses:

| Playbook | What It Produces |
|----------|-----------------|
| `/growth-strategy [company]` | Market landscape → competitive position → strategic options → financial case → presentation-ready deliverable |
| `/turnaround-playbook [company]` | Financial diagnosis → 90-day stabilization → 12-month restructuring → transformation roadmap |
| `/ma-assessment [target]` | Strategic rationale → commercial DD → valuation → synergies → risk analysis → go/no-go recommendation |

---

## Usage Examples with Sample Responses

### Example 1: Market Scan

**You type:**
```
/market-scan HR technology for mid-market companies
```

**Claude responds with:**

> ## HR Technology — Mid-Market Segment: Market Overview
>
> ### Market Sizing
> | Metric | Value |
> |--------|-------|
> | **TAM** (Global HR Tech) | $62B (2025), growing at 11.2% CAGR |
> | **SAM** (Mid-Market HR Tech, North America) | $14.8B |
> | **SOM** (Realistic addressable) | $1.2–1.8B based on positioning |
>
> ### Growth Drivers
> 1. **Remote/hybrid workforce complexity** — driving demand for integrated platforms
> 2. **Compliance burden** — multi-state and multi-country regulations increasing
> 3. **AI-powered automation** — talent acquisition, performance management
> 4. **Employee experience** — retention pressure shifting budget to engagement tools
>
> ### Competitive Landscape
> | Tier | Players | Positioning |
> |------|---------|-------------|
> | Leaders | Workday, ADP, UKG | Full suite, enterprise-leaning |
> | Challengers | BambooHR, Paylocity, Rippling | Mid-market native, modern UX |
> | Disruptors | Deel, Gusto, Oyster | Global payroll, contractor-first |
>
> ### Key Trends
> - Platform consolidation (point solutions → unified suites)
> - AI copilots for HR business partners
> - Skills-based talent management replacing role-based
>
> ### Strategic Implications
> - **Opportunity:** Mid-market remains underserved by enterprise vendors
> - **Threat:** Horizontal platforms (Rippling) expanding feature coverage rapidly
> - **Action required:** Differentiate on industry-specific workflows or vertical integration

---

### Example 2: SWOT Analysis

**You type:**
```
/swot Our company — $50M ARR SaaS selling HR software, 600 employees, strong in mid-market but losing enterprise deals
```

**Claude responds with:**

> ## SWOT Analysis: Acme Corp
>
> ### SWOT Matrix
>
> | | **Helpful** | **Harmful** |
> |---|---|---|
> | **Internal** | **Strengths:** Strong mid-market NRR (112%), deep HR domain expertise, 4.5 G2 rating, fast implementation (avg 38 days), loyal customer base | **Weaknesses:** Limited enterprise feature set, single-product dependency, brand recognition below top 5, engineering team stretched thin, gross margin (73%) below best-in-class |
> | **External** | **Opportunities:** AI-powered features as differentiator, international expansion (UK/ANZ), vertical-specific modules (healthcare, manufacturing), partner ecosystem | **Threats:** Enterprise vendors moving downmarket, economic slowdown affecting mid-market budgets, rising CAC across channels, consolidation pressure from PE-backed competitors |
>
> ### TOWS Strategic Options
>
> | Strategy | Action | Priority |
> |----------|--------|----------|
> | **SO** (Strength + Opportunity) | Leverage domain expertise to build AI-powered vertical modules | **HIGH** |
> | **WO** (Weakness + Opportunity) | Partner with system integrators to compensate for limited enterprise capabilities | MEDIUM |
> | **ST** (Strength + Threat) | Double down on mid-market loyalty programs to defend against enterprise downmarket push | **HIGH** |
> | **WT** (Weakness + Threat) | Invest in brand building and analyst relations before window closes | MEDIUM |
>
> ### Recommended Next Steps
> 1. Commission a build-vs-buy analysis for enterprise features (Q1)
> 2. Launch 3 vertical-specific modules starting with healthcare (Q2)
> 3. Establish strategic partnerships with 2 SI firms (Q2)

---

### Example 3: Financial Model

**You type:**
```
/financial-model SaaS company, $50M ARR, 35% growth, 73% gross margin, targeting Rule of 40
```

**Claude responds with:**

> ## 3-Year Financial Projection
>
> | Metric | Year 1 | Year 2 | Year 3 |
> |--------|--------|--------|--------|
> | **ARR** | $67.5M | $87.8M | $110.0M |
> | Growth Rate | 35% | 30% | 25% |
> | **MRR** | $5.63M | $7.32M | $9.17M |
> | New ARR | $20.0M | $23.5M | $25.5M |
> | Churned ARR | ($3.5M) | ($4.2M) | ($4.8M) |
> | Net New ARR | $17.5M | $20.3M | $22.2M |
> | **Gross Margin** | 74% | 76% | 78% |
> | **EBITDA Margin** | 5% | 12% | 18% |
> | **Rule of 40 Score** | 40 | 42 | 43 |
> | **FCF** | $1.7M | $7.0M | $14.3M |
>
> ### Unit Economics
> | Metric | Current | Target |
> |--------|---------|--------|
> | CAC | $38,000 | $32,000 |
> | ACV | $83,000 | $95,000 |
> | LTV | $332,000 | $427,500 |
> | LTV/CAC | 8.7x | 13.4x |
> | CAC Payback | 14 months | 11 months |
>
> ### Sensitivity Analysis
> | Scenario | ARR Y3 | EBITDA Y3 | Rule of 40 |
> |----------|--------|-----------|------------|
> | Bull (40%/35%/30%) | $130.7M | 20% | 50 |
> | **Base (35%/30%/25%)** | **$110.0M** | **18%** | **43** |
> | Bear (30%/25%/20%) | $93.6M | 14% | 34 |
>
> ### Key Assumptions & Risks
> - NRR assumed at 112%, declining to 110% as base grows
> - S&M spend dropping from 45% to 38% of revenue (efficiency gains)
> - **Risk:** If NRR drops below 105%, Rule of 40 target at risk in bear case

---

### Example 4: Customer Analysis

**You type:**
```
/customer-analysis Why are our enterprise customers churning at 2x the rate of mid-market?
```

**Claude responds with:**

> ## Enterprise Churn Analysis
>
> ### Churn Comparison
> | Segment | Logo Churn | Revenue Churn | NRR |
> |---------|-----------|---------------|-----|
> | Enterprise (500+ emp) | 14% annual | 11% | 94% |
> | Mid-Market (50-500) | 7% annual | 4% | 112% |
> | **Gap** | **2x worse** | **2.75x worse** | **18 pts below** |
>
> ### Root Cause Analysis (Pareto)
> | Cause | % of Enterprise Churn | Cumulative |
> |-------|-----------------------|------------|
> | Missing enterprise features (SSO, SCIM, audit logs) | 32% | 32% |
> | Poor executive relationship management | 24% | 56% |
> | Implementation took >90 days (expectation: 45) | 18% | 74% |
> | Competitor displacement (Workday, UKG) | 15% | 89% |
> | Budget cuts / M&A | 11% | 100% |
>
> ### Customer Health Score — Enterprise vs Mid-Market
> | Health Indicator | Enterprise Avg | Mid-Market Avg |
> |-----------------|---------------|----------------|
> | Product usage (DAU/MAU) | 28% | 52% |
> | Feature adoption (modules used) | 2.1 / 6 | 4.3 / 6 |
> | Support tickets / month | 12.4 | 3.2 |
> | Exec sponsor engagement | Low (1 QBR/yr) | Medium (2/yr) |
> | NPS | +8 | +42 |
>
> ### Recommended Actions
> | Priority | Initiative | Expected Impact | Timeline |
> |----------|-----------|----------------|----------|
> | **P0** | Build SSO/SCIM/audit log (table stakes) | -8% enterprise churn | Q1-Q2 |
> | **P0** | Assign dedicated CSMs to all enterprise accounts | -5% churn, +6 NPS | Immediate |
> | **P1** | Redesign enterprise onboarding (90→45 day target) | -4% churn | Q2 |
> | **P1** | Quarterly exec business reviews (not just QBRs) | Improved retention signal | Q1 |
> | **P2** | Win-back campaign for recent churns (<6 months) | 15-20% recovery rate | Q2 |

---

### Example 5: Change Management Plan

**You type:**
```
/change-plan We're migrating from 3 separate HR tools to one unified platform, affecting 400 employees across 5 offices
```

**Claude responds with:**

> ## Change Management Plan: HR Platform Consolidation
>
> ### Stakeholder Map
> | Stakeholder | Influence | Impact | Current Stance | Strategy |
> |------------|-----------|--------|---------------|----------|
> | CHRO (sponsor) | Very High | High | Champion | Leverage as visible advocate |
> | IT Director | High | Very High | Supportive | Co-own technical decisions |
> | Regional HR Managers (5) | High | Very High | Mixed | Convert through early wins |
> | Payroll Team (12) | Medium | Very High | Resistant | Address fears, show benefits |
> | All Employees (400) | Low | Medium | Unaware | Phased communication campaign |
>
> ### ADKAR Assessment
> | Phase | Status | Gap | Action |
> |-------|--------|-----|--------|
> | **A**wareness | Low | Employees don't know why change is happening | Town halls in Week 1-2 |
> | **D**esire | Medium | HR team sees value; payroll team fears job loss | 1:1 sessions with payroll |
> | **K**nowledge | Not started | No training plan yet | Build role-based training tracks |
> | **A**bility | Not started | Depends on system go-live | Sandbox environment + practice |
> | **R**einforcement | Not started | No success metrics defined | Define KPIs and celebrate wins |
>
> ### 90-Day Communication Plan
> | Week | Audience | Channel | Message |
> |------|----------|---------|---------|
> | 1-2 | All staff | Town hall + email | Why we're changing (vision + burning platform) |
> | 3-4 | HR + Payroll | Workshop | What's changing for YOUR role specifically |
> | 5-6 | Managers | Toolkit | Manager talking points + FAQ for their teams |
> | 7-8 | All staff | Video + intranet | Demo of new system — see it in action |
> | 9-10 | Power users | Training | Hands-on sandbox training (train-the-trainer) |
> | 11-12 | All staff | Go-live comms | Launch day guide + support resources |
>
> ### Risk & Resistance Mitigation
> | Risk | Likelihood | Impact | Mitigation |
> |------|-----------|--------|------------|
> | Payroll team resistance | High | High | Guarantee no job losses; show how role evolves |
> | Data migration errors | Medium | Very High | Parallel run for 2 pay cycles |
> | Training fatigue | Medium | Medium | Bite-sized modules (15 min), not full-day sessions |
> | Regional adoption gaps | Medium | High | Local change champions in each office |

---

## Working With Your Own Data

You can upload files and Claude will analyze them using consulting frameworks:

- **Upload a CSV** of monthly metrics → `/analyze-data Review this for trends, anomalies, and strategic insights`
- **Paste a P&L** → `/financial-model Build a 3-year projection based on this data`
- **Share customer data** → `/customer-analysis Segment these customers and identify churn risks`
- **Upload org chart** → `/org-design Assess spans of control and recommend restructuring`

Claude will ask clarifying questions if it needs more information — just answer naturally.

---

## All 16 Skills

| Skill | What It Does | Try It |
|-------|-------------|--------|
| **Market Research** | Market sizing, industry analysis, growth drivers, regulatory landscape | `/market-scan fintech payments` |
| **Competitive Analysis** | Competitor profiles, strategic group mapping, war gaming | `/competitor-profile HubSpot` |
| **Financial Analysis** | Financial models, DCF, unit economics, SaaS metrics | `/financial-model our Q4 budget scenario` |
| **Strategy Frameworks** | SWOT, Porter's Five Forces, BCG Matrix, Blue Ocean | `/swot our product line` |
| **Operations** | Process optimization, Lean/Six Sigma, supply chain | `/cost-optimization customer support operations` |
| **Benchmarking** | Peer comparison, gap analysis, maturity assessment | `/benchmark our engineering team vs industry` |
| **Data Analysis** | Cohort analysis, regression, segmentation, trend analysis | `/analyze-data` + upload file |
| **Deliverables** | Slide decks, memos, board presentations | `/strategy-deck Q1 board update` |
| **Change Management** | Stakeholder mapping, communication plans, training | `/change-plan office relocation` |
| **Pricing** | Value-based pricing, tier design, elasticity | `/pricing-analysis our subscription plans` |
| **M&A** | Target screening, synergy modeling, integration planning | `/ma-strategy evaluate 3 acquisition targets` |
| **Customer Insights** | Journey mapping, personas, churn drivers, CLV | `/customer-analysis NPS deep-dive` |
| **Digital Transformation** | Digital maturity, AI opportunities, tech stack | `/digital-assessment our operations` |
| **Risk Management** | Risk registers, Monte Carlo simulation, mitigation | `/risk-assessment regulatory compliance risks` |
| **Talent Strategy** | Workforce planning, retention, compensation benchmarks | `/talent-assessment sales team attrition` |
| **Innovation** | Innovation portfolio, stage-gate, design thinking | `/innovation-assessment our R&D pipeline` |

---

## Industry-Specific Analysis

The plugin includes pre-built industry overlays. Use `/set-context` and Claude automatically applies the right metrics, benchmarks, and terminology:

| Industry | Example Metrics Applied |
|----------|----------------------|
| **Technology / SaaS** | ARR, NRR, Rule of 40, burn multiple, LTV/CAC |
| **Healthcare** | Readmission rates, reimbursement, FDA pathways, clinical outcomes |
| **Financial Services** | NIM, efficiency ratio, combined ratio, AUM, TPV |
| **Consumer / Retail** | Comp sales, sales per sq ft, basket size, e-commerce conversion |
| **Industrial / Manufacturing** | OEE, capacity utilization, book-to-bill, aftermarket mix |

---

## Installation

### In Claude Cowork or Claude Code

```
/plugin marketplace add abinauv/business-consulting
/plugin install business-consulting@abinauv-business-consulting
```

### For Local Testing

```bash
git clone https://github.com/abinauv/business-consulting.git
claude --plugin-dir ./business-consulting
```

---

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on adding new skills, commands, or industry overlays.

## License

MIT — see [LICENSE](LICENSE) for details.
