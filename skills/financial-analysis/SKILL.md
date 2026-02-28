---
name: financial-analysis
description: "Build financial models, perform valuations, analyze cost structures, and develop business cases. Use this skill when the user mentions: financial analysis, financial model, DCF, valuation, P&L, revenue model, cost structure, unit economics, break-even, ROI, NPV, IRR, sensitivity analysis, pro forma, three-statement model, LBO, comparable analysis, comps, business case, investment analysis, or financial projections."
user-invokable: true
---

# Financial Analysis & Modeling

You are a financial analysis specialist. Apply the following methodologies to deliver rigorous financial models, valuations, and business cases.

## Revenue Modeling

### Revenue Driver Decomposition by Business Model

**SaaS / Subscription:**
- Revenue = Number of Customers × ARPU × Retention Rate
- Growth drivers: New customer acquisition, expansion revenue (upsell/cross-sell), churn reduction
- Key metrics: MRR, ARR, net revenue retention, logo retention, expansion MRR
- Cohort analysis: track revenue retention by customer cohort over time

**E-Commerce / Retail:**
- Revenue = Website Traffic × Conversion Rate × Average Order Value × Purchase Frequency
- Growth drivers: traffic growth (organic, paid, referral), conversion optimization, AOV increase, repeat purchase rate
- Key metrics: CAC, ROAS, cart abandonment rate, repeat purchase rate

**Marketplace / Platform:**
- Revenue = Gross Merchandise Value (GMV) × Take Rate
- Two-sided metrics: supply-side (sellers, listings, inventory) and demand-side (buyers, orders, GMV)
- Growth drivers: liquidity (matching efficiency), geographic expansion, category expansion
- Key metrics: GMV, take rate, buyer/seller ratio, repeat rate

**Professional Services:**
- Revenue = Headcount × Utilization Rate × Average Bill Rate
- Growth drivers: headcount growth, utilization improvement, rate increases, service mix shift
- Key metrics: utilization rate, realization rate, revenue per consultant, project margin

**Manufacturing / Product:**
- Revenue = Units Sold × Average Selling Price (ASP)
- Growth drivers: volume growth, pricing power, product mix, geographic expansion
- Key metrics: capacity utilization, yield rate, ASP trends, volume growth

### Growth Rate Assumptions
- **Historical extrapolation:** Use 3-5 year CAGR, adjust for one-time events
- **S-curve modeling:** For new markets — slow start, rapid growth, plateau
- **Market-share-based:** Target market size × expected share gain per year
- Always create three scenarios: Base (most likely), Upside (things go right), Downside (things go wrong)

## Cost Structure Analysis

### Fixed vs. Variable Decomposition
- **Fixed costs:** Rent, salaries (non-production), insurance, depreciation, software licenses
- **Variable costs:** COGS, sales commissions, shipping, transaction processing, cloud hosting (usage-based)
- **Semi-variable:** Customer support, marketing (has a fixed base + variable component)

### Operating Leverage Analysis
- How does margin change with revenue growth?
- High fixed cost businesses have high operating leverage — margins improve rapidly with scale
- Calculate: contribution margin, break-even revenue, margin at 2× current revenue

### Cost Benchmarking
Compare cost ratios against industry peers:
- COGS as % of revenue
- S&M as % of revenue
- R&D as % of revenue
- G&A as % of revenue
- Total operating expenses as % of revenue
- Flag any category that is >20% above peer median as an optimization opportunity

## Unit Economics

### Customer Acquisition Cost (CAC)
- **Blended CAC:** Total S&M spend / New customers acquired
- **Channel CAC:** S&M spend per channel / New customers from that channel
- Include: marketing spend, sales salaries, sales tools, onboarding costs
- Exclude: customer success (that's retention spend, not acquisition)

### Lifetime Value (LTV)
- **Simple:** ARPU × Gross Margin % × Average Customer Lifespan
- **DCF-based:** Sum of discounted future gross profit from a customer
- **Predictive:** Use retention curves and expansion revenue patterns

### LTV:CAC Ratio
- Below 1:1 = Losing money on every customer (unsustainable)
- 1:1 to 3:1 = Marginal, need improvement
- 3:1 to 5:1 = Healthy, efficient growth
- Above 5:1 = Could be under-investing in growth

### Payback Period
- Months to recover CAC from gross profit
- Payback = CAC / (Monthly ARPU × Gross Margin %)
- Target: <12 months for SMB, <18 months for mid-market, <24 months for enterprise

### Contribution Margin Waterfall
Revenue → minus COGS → Gross Profit → minus variable S&M → minus variable CS → Contribution Margin

## Valuation Methodologies

### DCF (Discounted Cash Flow)
1. Project free cash flow for 5-10 years
2. Calculate terminal value (Gordon Growth: FCF × (1+g) / (WACC-g), or Exit Multiple: EBITDA × multiple)
3. Discount all cash flows to present value using WACC
4. Enterprise Value = Sum of discounted FCFs + discounted terminal value
5. Equity Value = Enterprise Value - Net Debt + Cash

**WACC Calculation:**
- Cost of equity: Risk-free rate + Beta × Equity Risk Premium
- Cost of debt: Interest rate × (1 - Tax rate)
- WACC = (E/V × Cost of Equity) + (D/V × Cost of Debt)

**Sensitivity tables:** Always create 2-variable sensitivity on discount rate (WACC) and terminal growth rate.

### Comparable Company Analysis (Comps)
1. Select peer set (5-10 companies): same industry, similar size, similar growth profile
2. Calculate multiples: EV/Revenue, EV/EBITDA, P/E, EV/FCF
3. Use median or mean of peer multiples
4. Apply to target's metrics → implied valuation range
5. Adjust for: growth rate differences, margin differences, size premium/discount

### Precedent Transactions
1. Source relevant M&A transactions (same industry, last 3-5 years)
2. Calculate implied multiples: EV/Revenue, EV/EBITDA
3. Adjust for: market conditions at time of deal, strategic vs. financial buyer, control premium
4. Apply to target → implied valuation range

### Sum-of-the-Parts
Use when a company has distinct business segments with different characteristics:
1. Value each segment independently using the most appropriate method
2. Sum segment values → total enterprise value
3. Apply holding company discount if appropriate (10-25%)

### Rule-of-Thumb Valuations
- **SaaS:** 5-15× ARR (depending on growth rate, retention, margins)
- **Rule of 40:** Revenue growth % + EBITDA margin % should exceed 40% for premium valuation
- **E-commerce:** 1-3× revenue, 10-20× EBITDA
- **Services:** 1-2× revenue, 8-12× EBITDA

## Business Case Construction

### NPV / IRR / Payback
- **NPV:** Sum of discounted net cash flows. Positive NPV = value-creating investment.
- **IRR:** Discount rate at which NPV = 0. Should exceed cost of capital.
- **Payback period:** Time to recover initial investment from cash flows.

### Risk-Adjusted Returns
- Create 3-5 scenarios with explicit probability weights
- Expected NPV = Sum of (Probability × NPV) for each scenario
- Present as a probability-weighted outcome distribution

### Sensitivity & Tornado Charts
- Identify the 5-7 most impactful assumptions
- Vary each ±20% while holding others constant
- Rank by impact on NPV → tornado chart
- Focus management attention on the top 2-3 assumptions

## Output Templates

### Business Case One-Pager
Investment ask → Expected return (NPV, IRR) → Key risks (top 3) → Recommendation (invest/don't invest)

### Financial Summary Dashboard
Key metrics table → Trend charts (revenue, margin, cash flow) → Peer comparison → Scenario summary

### Valuation Summary
Methodology used → Key assumptions → Range of values → Football field chart (DCF range, comps range, precedents range)

### Unit Economics Snapshot
CAC → LTV → LTV:CAC ratio → Payback period → Contribution margin — all in a single visual

## LBO Model (Leveraged Buyout)

### When to Use
PE-style acquisition analysis. Used when evaluating a take-private, sponsor-backed acquisition, or management buyout.

### LBO Model Structure
1. **Entry:** Purchase price (as multiple of EBITDA), equity contribution, debt financing (senior + mezzanine + subordinated), transaction fees
2. **Operating Period (5-year hold):**
   - Revenue and EBITDA projections
   - Mandatory debt repayment schedule (amortization)
   - Cash sweep: excess free cash flow used to pay down debt
   - Capex, working capital changes
3. **Exit:** Exit price (apply exit multiple to Year 5 EBITDA), net debt payoff, equity proceeds
4. **Returns:** IRR to equity investors, cash-on-cash multiple (MOIC), payback period

### Key LBO Metrics
- **Entry multiple:** Purchase EV / EBITDA (typically 6-12× depending on industry)
- **Leverage ratio:** Total Debt / EBITDA at entry (typically 4-6×)
- **Equity contribution:** 30-50% of total purchase price
- **IRR target:** 20-25%+ for PE sponsors
- **MOIC target:** 2.5-3.5× over 5-year hold
- **Value creation sources:** EBITDA growth, margin improvement, multiple expansion, debt paydown

### Sensitivity Table for LBO
Two-variable sensitivity on Entry Multiple vs. Exit Multiple → resulting IRR:
- Entry multiple range: 7× to 11×
- Exit multiple range: 7× to 11×
- Highlight the diagonal (entry = exit) to isolate operational value creation from multiple arbitrage

## Working Capital Optimization

### Cash Conversion Cycle (CCC)
CCC = DSO + DIO - DPO (measured in days)
- **DSO (Days Sales Outstanding):** How quickly customers pay. Lower = better.
- **DIO (Days Inventory Outstanding):** How long inventory sits. Lower = better.
- **DPO (Days Payable Outstanding):** How long to pay suppliers. Higher = better (but maintain relationships).

### Working Capital Improvement Levers

| Metric | Current | Target | Improvement Lever |
|--------|---------|--------|------------------|
| DSO | [days] | [days] | Invoice promptly, tighten payment terms, offer early payment discounts, automate collections |
| DIO | [days] | [days] | Demand forecasting, JIT inventory, reduce SKU count, ABC inventory management |
| DPO | [days] | [days] | Negotiate longer payment terms, use supply chain financing, optimize payment timing |

### Working Capital Impact Quantification
- Cash freed = (DSO improvement in days × Daily Revenue) + (DIO improvement × Daily COGS) - (DPO improvement × Daily COGS)
- Example: Reducing DSO by 10 days on $100M revenue = $100M/365 × 10 = $2.7M cash freed

## SaaS Financial Metrics

### SaaS-Specific KPIs
- **ARR / MRR:** Annual/Monthly Recurring Revenue — the heartbeat metric
- **Net Revenue Retention (NRR):** (Beginning ARR + Expansion - Contraction - Churn) / Beginning ARR. World-class: >120%
- **Gross Revenue Retention (GRR):** (Beginning ARR - Contraction - Churn) / Beginning ARR. Healthy: >90%
- **Magic Number:** Net New ARR / Prior Quarter S&M Spend. Above 1.0 = efficient growth. Below 0.5 = fix GTM.
- **Burn Multiple:** Net Burn / Net New ARR. Below 1.5× = efficient. Above 2× = concerning.
- **Rule of 40:** Revenue Growth % + FCF Margin % should exceed 40% for premium valuation.
- **CAC Payback:** Months to recover CAC from gross profit. SMB: <12 months. Enterprise: <18 months.
- **NDR-Adjusted Growth:** Growth rate adjusted for net dollar retention provides a more nuanced view than raw growth.

### SaaS Revenue Projection Template
Build the ARR waterfall:

| Component | Q1 | Q2 | Q3 | Q4 | Annual |
|-----------|----|----|----|----|--------|
| Beginning ARR | | | | | |
| + New Business ARR | | | | | |
| + Expansion ARR | | | | | |
| - Contraction ARR | | | | | |
| - Churned ARR | | | | | |
| = Ending ARR | | | | | |
| Net New ARR | | | | | |
| NRR (annualized) | | | | | |

### SaaS Valuation Benchmarks
| Growth Rate | NRR > 120% | NRR 100-120% | NRR < 100% |
|------------|-----------|-------------|-----------|
| >40% growth | 15-25× ARR | 10-18× ARR | 6-12× ARR |
| 20-40% growth | 8-15× ARR | 6-10× ARR | 4-8× ARR |
| <20% growth | 5-8× ARR | 3-6× ARR | 2-4× ARR |

For detailed walkthroughs, industry multiples, and model best practices, consult the reference files in the `references/` directory.
