# Valuation Methods Deep Dive

This reference provides step-by-step walkthroughs of the two most commonly used valuation methodologies — Discounted Cash Flow (DCF) and Comparable Company Analysis (Comps) — with worked examples, common pitfalls, and guidance on when to use each approach.

---

## DCF Valuation: Step-by-Step Walkthrough

### Overview

A DCF values a company by projecting its future free cash flows and discounting them back to present value. It is the most theoretically rigorous valuation method because it derives value from the company's own fundamentals rather than from market sentiment or peer pricing.

### Worked Example: CloudMetrics Inc. (Hypothetical SaaS Company)

**Company Profile:**
- Current ARR: $50M
- Revenue growth rate: 25% (decelerating over time)
- Gross margin: 65%
- Operating expenses: 50% of revenue currently, improving with scale
- Capital expenditures: 3% of revenue
- Tax rate: 25%
- Net debt: $0 (cash-rich, no debt)

**Step 1: Project Revenue (5-Year Forecast)**

Start with current ARR and apply growth rates that decelerate as the company scales. High-growth SaaS companies rarely sustain 25%+ growth for more than a few years as they reach market saturation and face competitive pressure.

| Year | Growth Rate | Revenue ($M) |
|------|-----------|-------------|
| Year 0 (Current) | — | 50.0 |
| Year 1 | 25% | 62.5 |
| Year 2 | 22% | 76.3 |
| Year 3 | 18% | 90.0 |
| Year 4 | 15% | 103.5 |
| Year 5 | 12% | 115.9 |

**Step 2: Project Free Cash Flow**

For each year, calculate: Revenue minus COGS minus Operating Expenses minus Taxes minus CapEx plus Depreciation and Amortization. In a simplified model:

- Gross margin improves from 65% to 70% over 5 years as the company achieves scale in hosting costs
- Operating expenses decline from 50% of revenue to 38% as sales efficiency improves and G&A scales
- CapEx remains at 3% of revenue

| Year | Revenue | Gross Profit (Margin) | OpEx | EBIT | Taxes (25%) | CapEx | FCF |
|------|---------|-----------------------|------|------|-------------|-------|-----|
| Y1 | 62.5 | 40.6 (65%) | 31.3 | 9.4 | 2.3 | 1.9 | 5.2 |
| Y2 | 76.3 | 50.3 (66%) | 35.3 | 15.0 | 3.7 | 2.3 | 9.0 |
| Y3 | 90.0 | 60.8 (67.5%) | 38.7 | 22.1 | 5.5 | 2.7 | 13.9 |
| Y4 | 103.5 | 71.4 (69%) | 41.4 | 30.0 | 7.5 | 3.1 | 19.4 |
| Y5 | 115.9 | 81.1 (70%) | 44.0 | 37.1 | 9.3 | 3.5 | 24.3 |

**Step 3: Calculate WACC**

Assume CloudMetrics is all-equity financed (common for growth SaaS):
- Risk-free rate: 4.0% (10-year Treasury yield)
- Equity risk premium: 5.5%
- Beta: 1.3 (typical for high-growth software)
- Cost of equity = 4.0% + 1.3 × 5.5% = 11.15%
- WACC = 11.15% (no debt, so WACC equals cost of equity)

**Step 4: Calculate Terminal Value**

Using the Gordon Growth Model with a 3% perpetual growth rate:
- Terminal Value = FCF in Year 5 × (1 + g) / (WACC - g)
- Terminal Value = 24.3 × 1.03 / (0.1115 - 0.03)
- Terminal Value = 25.0 / 0.0815
- Terminal Value = $307.0M

**Step 5: Discount to Present Value**

| Component | Future Value | Discount Factor (at 11.15%) | Present Value |
|-----------|--------------|-----------------------------|---------------|
| Y1 FCF | 5.2 | 0.900 | 4.7 |
| Y2 FCF | 9.0 | 0.809 | 7.3 |
| Y3 FCF | 13.9 | 0.728 | 10.1 |
| Y4 FCF | 19.4 | 0.655 | 12.7 |
| Y5 FCF | 24.3 | 0.589 | 14.3 |
| Terminal Value | 307.0 | 0.589 | 180.8 |
| **Enterprise Value** | | | **$229.9M** |

**Step 6: Derive Equity Value**

- Enterprise Value: $229.9M
- Plus cash: assume $10M on balance sheet
- Minus debt: $0
- **Equity Value: $239.9M**
- Implied EV/ARR multiple: approximately 4.6x current ARR

**Step 7: Sensitivity Analysis**

Build a two-variable data table varying WACC (9% to 13%) and terminal growth rate (2% to 4%):

| WACC \ Terminal Growth | 2.0% | 2.5% | 3.0% | 3.5% | 4.0% |
|------------------------|-------|-------|-------|-------|-------|
| 9.0% | 285 | 310 | 342 | 382 | 435 |
| 10.0% | 242 | 260 | 282 | 309 | 343 |
| 11.15% | 206 | 218 | 230 | 248 | 270 |
| 12.0% | 185 | 195 | 207 | 221 | 238 |
| 13.0% | 165 | 173 | 182 | 193 | 207 |

Values are Enterprise Value in $M. This table shows the range of plausible outcomes and highlights how sensitive the valuation is to assumptions about the discount rate and long-term growth.

---

## Comparable Company Analysis (Comps): Step-by-Step Walkthrough

### Overview

Comps values a company by comparing it to publicly traded peers using standardized valuation multiples. It reflects what the market is currently willing to pay for similar businesses and serves as a reality check against intrinsic valuation methods like DCF.

### Worked Example: Valuing CloudMetrics via Comps

**Step 1: Select Peer Companies**

Choose 5 public SaaS companies with similar characteristics: cloud-based, B2B, $30M-$150M revenue range, subscription model.

| Company | Revenue ($M) | Growth Rate | Gross Margin | EBITDA Margin |
|---------|-------------|-------------|-------------|---------------|
| PeerCo Alpha | 80 | 30% | 72% | 15% |
| PeerCo Beta | 45 | 20% | 68% | 8% |
| PeerCo Gamma | 120 | 18% | 70% | 22% |
| PeerCo Delta | 55 | 35% | 66% | -5% |
| PeerCo Epsilon | 95 | 22% | 71% | 12% |

**Step 2: Calculate Multiples for Each Peer**

Using current enterprise values from market data:

| Company | EV ($M) | EV/Revenue | EV/Gross Profit | Growth-Adj. EV/Rev |
|---------|---------|-----------|-----------------|---------------------|
| PeerCo Alpha | 640 | 8.0x | 11.1x | 0.27x |
| PeerCo Beta | 270 | 6.0x | 8.8x | 0.30x |
| PeerCo Gamma | 720 | 6.0x | 8.6x | 0.33x |
| PeerCo Delta | 495 | 9.0x | 13.6x | 0.26x |
| PeerCo Epsilon | 570 | 6.0x | 8.5x | 0.27x |
| **Median** | | **6.0x** | **8.8x** | **0.27x** |
| **Mean** | | **7.0x** | **10.1x** | **0.29x** |

Growth-adjusted EV/Revenue divides the EV/Revenue multiple by the growth rate, providing a way to compare companies growing at different speeds.

**Step 3: Apply to CloudMetrics**

CloudMetrics: $50M revenue, 25% growth, 65% gross margin.

| Method | Multiple | Applied To | Implied EV ($M) |
|--------|----------|-----------|-----------------|
| Median EV/Revenue | 6.0x | $50M | 300 |
| Mean EV/Revenue | 7.0x | $50M | 350 |
| Median EV/Gross Profit | 8.8x | $32.5M | 286 |
| Growth-adj. (median × growth) | 0.27x × 25% = 6.8x | $50M | 338 |

**Implied valuation range: $286M - $350M**, with a midpoint around $318M.

**Step 4: Adjustments**

- CloudMetrics has a lower gross margin (65%) versus the peer median (70%). Apply a slight discount of 5-10%.
- CloudMetrics growth rate of 25% is in line with the peer median of 22%, supporting a slight premium.
- Net adjustment: roughly neutral, so the range stands.

**Final comps-implied EV: $285M - $340M**

---

## Common DCF Mistakes

1. **Inconsistent growth and margin assumptions.** Revenue growth deceleration should be paired with margin expansion. If you project slowing growth but also flat margins, you are likely being too conservative. Conversely, projecting high growth with already-peak margins is too aggressive.

2. **Unrealistic terminal value.** If the terminal value represents more than 75% of total enterprise value, your explicit forecast period is too short or your terminal assumptions are too aggressive. Extend the projection period or reduce the terminal growth rate.

3. **Wrong WACC inputs.** Using the company's own cost of debt when it is distressed, or using a beta calculated from a short time period with high volatility, will distort the discount rate. Use industry-average beta and normalize the capital structure.

4. **Not stress-testing the model.** A single-point DCF estimate is nearly useless. Always run sensitivity analysis on at least two variables (typically WACC and terminal growth rate) and present a range rather than a single number.

5. **Ignoring working capital.** Changes in accounts receivable, inventory, and accounts payable consume or release cash. Omitting working capital changes from FCF projections will overstate cash flow, particularly for companies with growing revenues.

6. **Double-counting growth.** Including high growth in the explicit forecast period and then also using a high terminal growth rate effectively counts the same growth opportunity twice. The terminal growth rate should reflect mature, steady-state growth — typically GDP growth or slightly above.

---

## When to Use Which Method

**Use DCF when:**
- The company has predictable, recurring revenue (SaaS, subscription, contracts)
- You have confidence in long-term projections (3+ years of history, clear market dynamics)
- The company is in a unique position with no close public peers
- You need to understand how specific operational changes affect value

**Use Comps when:**
- You need a quick market-based sanity check
- There is a robust set of publicly traded peers
- You want to understand how the market is pricing similar businesses right now
- The company is preparing for a fundraise or IPO and needs to set expectations

**Use Precedent Transactions when:**
- The company is being acquired or considering a sale
- You need to understand what buyers have historically paid for similar assets
- You want to capture the control premium (typically 20-40% above trading multiples)
- You are advising on deal negotiations and need leverage on pricing

**Best practice:** Use at least two methods and triangulate. Present a football field chart showing the valuation range from each methodology. Where the ranges overlap is the most defensible valuation zone. If methods diverge significantly, investigate why — it usually reveals a key assumption that needs further diligence.
