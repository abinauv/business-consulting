# Business Consulting Plugin for Claude Code

A comprehensive management consulting toolkit that transforms Claude into a senior business consultant. Covers the full consulting workflow: market research, competitive analysis, financial modeling, strategy frameworks, operations optimization, benchmarking, data analysis, deliverable creation, change management, pricing strategy, M&A, customer insights, digital transformation, risk management, talent strategy, and innovation strategy.

## Skills (16)

| Skill | Description | Invoke |
|-------|-------------|--------|
| **market-research** | Market sizing (TAM/SAM/SOM), industry analysis, PESTEL, voice-of-market synthesis, emerging market considerations | `/business-consulting:market-research [industry]` |
| **competitive-analysis** | Competitor profiling, VRIO, strategic group mapping, digital intelligence, structured war gaming | `/business-consulting:competitive-analysis [company]` |
| **financial-analysis** | Financial modeling, DCF, LBO, comps, unit economics, SaaS metrics, working capital optimization | `/business-consulting:financial-analysis [scenario]` |
| **strategy-frameworks** | SWOT/TOWS, BCG, Ansoff, Porter's, Blue Ocean, JTBD, Wardley Mapping, framework selection decision tree | `/business-consulting:strategy-frameworks [question]` |
| **operations-analysis** | Process mapping, Lean/Six Sigma, supply chain, automation assessment, shared services design, KPI design | `/business-consulting:operations-analysis [area]` |
| **benchmarking** | Peer comparison, maturity assessment, gap analysis, performance benchmarking | `/business-consulting:benchmarking [subject]` |
| **data-analysis** | Pareto, cohort, correlation, regression, RFM segmentation, survey analysis, Python + Excel recipes | `/business-consulting:data-analysis [data]` |
| **deliverable-creation** | Pyramid Principle, slide storyboarding, report writing, email/memo templates, workshop facilitation guides | `/business-consulting:deliverable-creation [topic]` |
| **change-management** | Stakeholder mapping, ADKAR, Kotter's 8-Step, communication planning, resistance management, cultural assessment | `/business-consulting:change-management [initiative]` |
| **pricing-strategy** | Value-based pricing, pricing architecture, elasticity, SaaS pricing, discount governance, revenue optimization | `/business-consulting:pricing-strategy [product]` |
| **m-and-a-strategy** | M&A strategy, target screening, synergy modeling, integration planning, carve-outs, JVs, post-merger tracking | `/business-consulting:m-and-a-strategy [question]` |
| **customer-insights** | Journey mapping, persona development, churn analysis, NPS/CSAT drivers, CLV modeling, win/loss analysis | `/business-consulting:customer-insights [segment]` |
| **digital-transformation** | Digital maturity assessment, AI/automation, build vs buy vs partner, data strategy, cloud migration, cybersecurity | `/business-consulting:digital-transformation [company]` |
| **risk-management** | ERM frameworks (COSO, ISO 31000), risk quantification, Monte Carlo simulation, BCP, compliance assessment | `/business-consulting:risk-management [area]` |
| **talent-strategy** | Workforce planning, skills gap analysis, compensation benchmarking, retention strategy, succession planning, DEI | `/business-consulting:talent-strategy [function]` |
| **innovation-strategy** | Innovation portfolio (70/20/10), stage-gate, design thinking, lean startup, corporate venture, disruption response | `/business-consulting:innovation-strategy [question]` |

## Commands (24)

### Analysis Commands (12)
| Command | Description |
|---------|-------------|
| `/market-scan [industry]` | Quick market overview: size, growth, players, trends, regulatory environment |
| `/competitor-profile [company]` | Deep competitor profile: financials, products, GTM, strengths/weaknesses, strategic outlook |
| `/swot [company]` | SWOT analysis with TOWS strategic options and prioritized implications |
| `/financial-model [scenario]` | Build a financial model with revenue projections, cost structure, unit economics, sensitivity |
| `/benchmark [subject]` | Benchmark against peers with gap analysis, root cause diagnosis, and action plan |
| `/strategy-deck [topic]` | Create a consulting-style strategy deck storyboard with action titles and slide-by-slide outline |
| `/due-diligence [target]` | Commercial due diligence: market, competitive position, customers, growth, risks |
| `/cost-optimization [area]` | Identify cost reduction opportunities with savings waterfall and phased roadmap |
| `/market-entry [market]` | Market entry strategy: attractiveness, entry modes, GTM plan, financial projections |
| `/org-design [company]` | Organizational assessment: spans & layers, efficiency metrics, design recommendations |
| `/scenario-plan [question]` | Scenario planning: key uncertainties, 2x2 scenarios, robust actions, monitoring dashboard |
| `/analyze-data [data]` | Data analysis with consulting-quality insights, visualizations, and recommendations |
| `/change-plan [initiative]` | Comprehensive change management plan: stakeholder map, ADKAR analysis, communication plan, resistance mitigation, 90-day timeline |
| `/pricing-analysis [product]` | Full pricing analysis: current model assessment, competitive pricing, elasticity, architecture design, revenue impact, implementation roadmap |
| `/ma-strategy [question]` | M&A strategy: strategic rationale, target screening, synergy analysis, integration planning, valuation range |
| `/customer-analysis [segment]` | Customer insights: segmentation, journey mapping, personas, churn analysis, CLV, prioritized recommendations |
| `/digital-assessment [company]` | Digital transformation: maturity assessment (8 dimensions), AI/automation opportunities, technology stack, digital roadmap |
| `/risk-assessment [area]` | Enterprise risk assessment: risk register, heat map, quantification, mitigation strategies, KRI dashboard |
| `/talent-assessment [function]` | Talent strategy: workforce planning, skills gaps, compensation benchmarks, retention risks, succession plan |
| `/innovation-assessment [question]` | Innovation assessment: maturity scorecard, portfolio balance, stage-gate review, culture diagnosis, disruption radar |

### Cross-Skill Playbooks (3)
| Command | Description |
|---------|-------------|
| `/growth-strategy [company]` | End-to-end growth strategy: market landscape → competitive position → strategic options → financial case → deliverable |
| `/turnaround-playbook [company]` | Full turnaround plan: financial diagnosis → stabilization (90-day) → restructuring (12-month) → transformation |
| `/ma-assessment [target]` | Complete M&A assessment: strategic rationale → commercial DD → financial valuation → synergies → risk → recommendation |

### Utility Commands (1)
| Command | Description |
|---------|-------------|
| `/set-context [client details]` | Store client name, industry, size, geography so all subsequent analyses are automatically tailored |

## Hooks

- **SessionStart:** Automatically configures Claude as a strategy consultant with structured thinking principles, Pyramid Principle, and awareness of all available skills and commands.

## Industry Overlays

Pre-built industry-specific reference files that customize metrics, benchmarks, frameworks, and terminology for five key verticals:

| Overlay | Covers |
|---------|--------|
| **Technology / SaaS** | ARR/MRR, NRR, Rule of 40, burn multiple, SaaS valuation, PLG metrics |
| **Healthcare** | Provider, payer, pharma, medtech metrics, FDA process, reimbursement, regulatory landscape |
| **Financial Services** | Banking (NIM, efficiency ratio), insurance (combined ratio), asset management (AUM, flows), payments (TPV, take rate) |
| **Consumer / Retail** | Comp sales, sales per sq ft, CPG metrics, D2C unit economics, e-commerce conversion |
| **Industrial / Manufacturing** | OEE, capacity utilization, book-to-bill, cycle indicators, aftermarket mix |

Use `/set-context` to automatically load the relevant industry overlay.

## Reference Libraries

Each skill includes curated reference files with:
- Detailed methodology guides and worked examples
- Ready-to-use templates and frameworks
- Industry-specific data source directories
- Python and Excel code recipes for analytical tasks
- KPI libraries with 200+ metrics and benchmarks
- Maturity model templates for 5 functions
- Consulting writing style guides and slide templates

## Installation

### Local development (testing)
```bash
claude --plugin-dir ./business-consulting
```

### From marketplace
```bash
claude plugin install business-consulting
```

## Usage Examples

```
# Set client context first (optional but recommended)
/set-context Acme Corp, B2B SaaS, $50M ARR, 200 employees, US-based, selling HR software

# Quick market overview
/market-scan electric vehicle charging

# Deep competitor analysis
/competitor-profile Stripe

# Full SWOT with strategic options
/swot Shopify

# Build a financial model
/financial-model B2B SaaS company with $5M ARR, 30% growth, targeting enterprise

# End-to-end growth strategy (cross-skill playbook)
/growth-strategy Acme Corp

# Full turnaround plan
/turnaround-playbook RetailCo struggling with margin compression

# M&A assessment
/ma-assessment Acme Corp acquiring DataCo for $100M

# Scenario planning
/scenario-plan Impact of AI on our consulting business over the next 5 years
```

## Architecture

```
business-consulting/
├── .claude-plugin/
│   └── plugin.json
├── skills/
│   ├── market-research/          (SKILL.md + 3 reference files)
│   ├── competitive-analysis/     (SKILL.md + 2 reference files)
│   ├── financial-analysis/       (SKILL.md + 3 reference files)
│   ├── strategy-frameworks/      (SKILL.md + 3 reference files)
│   ├── operations-analysis/      (SKILL.md + 3 reference files)
│   ├── benchmarking/             (SKILL.md + 2 reference files)
│   ├── data-analysis/            (SKILL.md + 3 reference files)
│   ├── deliverable-creation/     (SKILL.md + 3 reference files)
│   ├── change-management/        (SKILL.md + 3 reference files)
│   ├── pricing-strategy/         (SKILL.md + 3 reference files)
│   ├── m-and-a-strategy/         (SKILL.md + 3 reference files)
│   ├── customer-insights/        (SKILL.md + 3 reference files)
│   ├── digital-transformation/   (SKILL.md + 3 reference files)
│   ├── risk-management/          (SKILL.md + 3 reference files)
│   ├── talent-strategy/          (SKILL.md + 3 reference files)
│   └── innovation-strategy/      (SKILL.md + 3 reference files)
├── commands/                     (24 command files)
├── references/
│   └── industry-overlays/        (5 industry vertical files)
├── hooks/
│   └── hooks.json
└── README.md
```
