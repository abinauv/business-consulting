# Compensation Benchmarking Guide

## Data Sources Directory

| Source | Coverage | Strengths | Limitations | Cost |
|--------|---------|-----------|------------|:----:|
| **Radford (Aon)** | Tech, life sciences | Gold standard for tech; detailed by level, function, geo | Expensive, annual cycle | $$$$ |
| **Mercer** | All industries, global | Broadest coverage, global data, robust methodology | Can be slow to update | $$$$ |
| **Willis Towers Watson** | All industries | Strong executive comp, global data | Complex methodology | $$$$ |
| **Levels.fyi** | Tech companies | Real-time, detailed equity data, user-verified | Tech-only, self-reported, US-heavy | $ |
| **Glassdoor** | All industries | Large sample, company-specific data | Self-reported, verification varies | Free–$ |
| **Payscale** | All industries | Good for SMBs, real-time, easy to use | Smaller sample for niche roles | $–$$ |
| **LinkedIn Salary** | All industries | Large professional network data | Limited detail, US-focused | Free |
| **Pave** | Tech, startups | Real-time comp data from integrated payroll, equity details | Primarily tech/startups | $$$ |
| **Carta** | Startups, private companies | Excellent equity data for private companies | Equity-focused, limited base salary | $$–$$$ |
| **BLS (Bureau of Labor Statistics)** | All industries (US) | Free, government data, good for broad benchmarks | Broad categories, lagging | Free |
| **Industry-specific surveys** | Varies | Most relevant for niche roles, associations often publish | Narrow, may have small samples | $–$$ |

## Benchmarking Methodology

### Job Matching Process

1. **Identify benchmark roles** — Focus on roles that represent 80%+ of headcount or are critical/hard-to-fill
2. **Match to survey jobs** — Match internal roles to survey job descriptions based on:
   - Scope and responsibility (not just title)
   - Reporting level and span of control
   - Required skills and experience
   - Revenue/budget responsibility
3. **Validate match quality** — Ensure at least 70% of job content matches survey description
4. **Collect data** — Gather P25, P50 (median), P75 for each compensation element

### Market Positioning Strategy

| Position | % of Market Median | When to Use | Trade-offs |
|----------|:---:|---|---|
| **Lead (P75+)** | 110–120% | Critical talent in competitive markets, key revenue-generating roles | Higher cost, but better attraction and retention |
| **Match (P50)** | 95–105% | Most roles, standard market positioning | Balanced cost and competitiveness |
| **Lag (P25)** | 85–95% | Non-critical roles, strong employer brand, compelling mission/culture | Lower cost, but harder to attract top talent |
| **Hybrid** | Varies by role | Different positioning for different role segments based on criticality | Optimizes cost while being competitive where it matters |

### Data Aging

Survey data is collected at a point in time and ages:
```
Aged Value = Survey Value × (1 + Annual Movement Rate) ^ (Months Since Survey / 12)

Example: Survey median $120K collected 9 months ago, 4% annual movement
Aged Value = $120K × (1.04)^(9/12) = $120K × 1.03 = $123,600
```

Typical annual movement rates:
- Technology: 4–5%
- Professional services: 3–4%
- Manufacturing: 2–3%
- Healthcare: 3–4%

### Geographic Adjustments

| Market | Cost of Living Index (relative to US national average) |
|--------|:---:|
| San Francisco Bay Area | 140–160% |
| New York City | 130–145% |
| Seattle | 120–130% |
| Boston | 120–130% |
| Los Angeles | 115–125% |
| Austin / Denver / Nashville | 105–115% |
| US National Average | 100% |
| Remote (US) | 90–100% (company policy varies) |
| London | 110–120% |
| Western Europe | 85–100% |
| India (tier 1 cities) | 25–40% |

## Total Compensation Framework

### Compensation Components

| Component | Description | Benchmark Separately? |
|-----------|-----------|:---:|
| **Base salary** | Fixed annual cash compensation | Yes |
| **Annual bonus/variable** | Performance-based cash (target % and actual payout) | Yes |
| **Equity/LTI** | Stock options, RSUs, performance shares (annualized value) | Yes |
| **Signing bonus** | One-time cash at hire | Reference only |
| **Benefits** | Health, dental, vision, 401k match, PTO, perks | Benchmark as package |
| **Total cash** | Base + target bonus | Yes |
| **Total compensation** | Total cash + annualized equity | Yes |

### Compensation Mix by Level

| Level | Base | Bonus (% of base) | Equity (% of total comp) | Total Comp |
|-------|:----:|:---:|:---:|:---:|
| Individual Contributor | 85–95% of total cash | 5–10% | 0–15% | $60K–$150K |
| Senior IC / Lead | 80–90% | 10–20% | 10–25% | $120K–$250K |
| Manager | 75–85% | 15–25% | 10–20% | $150K–$300K |
| Director | 70–80% | 20–30% | 15–25% | $200K–$400K |
| VP | 60–70% | 25–40% | 20–35% | $300K–$600K |
| C-Suite | 40–60% | 30–50% | 30–50% | $500K–$2M+ |

## Pay Equity Analysis

### Compa-Ratio Analysis

```
Compa-Ratio = Actual Salary / Range Midpoint × 100

Interpretation:
  <80%:  Significantly below range — retention risk
  80-90%: Below midpoint — may indicate new hire or development
  90-110%: Within target zone — appropriately compensated
  110-120%: Above midpoint — tenured high performer
  >120%: Significantly above range — review needed
```

### Regression-Based Pay Equity

Run regression to identify unexplained pay gaps:
```
Salary = f(Level, Function, Experience, Performance, Location, Tenure)

If gender/ethnicity coefficient is statistically significant after
controlling for legitimate factors → potential pay equity issue
```

## Compensation Structure Design

### Pay Band Construction

| Element | Definition | Typical Value |
|---------|-----------|:---:|
| **Range midpoint** | Market-competitive target rate (typically P50) | 100% |
| **Range minimum** | Entry-level for the grade (% below midpoint) | 80–85% |
| **Range maximum** | Ceiling for the grade (% above midpoint) | 115–120% |
| **Range spread** | (Max − Min) / Min × 100 | 40–50% (individual contributors), 50–60% (management) |
| **Midpoint progression** | % increase from one grade's midpoint to the next | 10–15% |
| **Overlap** | How much adjacent grades overlap | 30–50% |

### Example Pay Band Structure

| Grade | Level | Minimum | Midpoint | Maximum | Spread |
|:-----:|-------|:-------:|:--------:|:-------:|:------:|
| G1 | Junior IC | $55K | $65K | $78K | 42% |
| G2 | IC | $65K | $78K | $94K | 45% |
| G3 | Senior IC | $80K | $96K | $115K | 44% |
| G4 | Lead / Staff | $100K | $120K | $144K | 44% |
| G5 | Manager | $115K | $140K | $170K | 48% |
| G6 | Senior Manager | $135K | $165K | $200K | 48% |
| G7 | Director | $160K | $200K | $248K | 55% |
| G8 | VP | $200K | $260K | $335K | 68% |

## Equity Compensation Benchmarks

### By Company Stage

| Stage | Option Pool (% of fully diluted) | Typical IC Grant (% of company) | Vesting | Exercise Window |
|-------|:---:|:---:|---|---|
| **Seed** | 10–15% | 0.5–2.0% | 4-year, 1-year cliff | 90 days (options) |
| **Series A** | 10–12% | 0.1–0.5% | 4-year, 1-year cliff | 90 days post-term |
| **Series B** | 10–12% | 0.05–0.2% | 4-year, 1-year cliff | 90 days post-term |
| **Series C+** | 8–10% | 0.01–0.1% | 4-year, 1-year cliff | 90 days post-term |
| **Pre-IPO** | 5–8% | RSUs, value-based | 4-year, often no cliff | N/A (RSUs) |
| **Public** | Ongoing dilution 1–3%/year | RSUs, value-based | 4-year, quarterly | N/A |

## Compensation Philosophy Statement Template

> **[Company Name] Compensation Philosophy**
>
> We believe compensation should attract, motivate, and retain the talent needed to achieve our mission. Our philosophy is guided by these principles:
>
> 1. **Market competitiveness:** We target the [P50/P60/P75] of our compensation peer group for [total cash/total compensation].
> 2. **Internal equity:** We maintain fair and consistent pay for equivalent work, regardless of personal characteristics.
> 3. **Pay for performance:** We differentiate compensation based on individual and company performance.
> 4. **Transparency:** We share our compensation structure, bands, and philosophy with all employees.
> 5. **Total rewards:** We consider the full employee value proposition (compensation, benefits, growth, mission, culture).
>
> **Compensation peer group:** [List 10–15 companies of similar size, industry, and talent market]
>
> **Review cadence:** Annual compensation review in [month], with mid-year adjustments for market corrections or promotions.
