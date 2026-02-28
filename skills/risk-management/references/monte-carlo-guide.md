# Monte Carlo Simulation Guide

## When to Use Monte Carlo

### Decision Framework

| Situation | Use Monte Carlo? | Alternative |
|-----------|:---:|---|
| Single-point estimate with high uncertainty | Yes | |
| Multiple uncertain inputs that compound | Yes | |
| Need to communicate risk range to stakeholders | Yes | |
| Understanding which inputs drive the most risk | Yes | Tornado chart |
| Quick back-of-envelope estimate needed | No | Scenario analysis (best/base/worst) |
| All inputs are well-known constants | No | Deterministic calculation |
| Very early-stage, no data at all | No | Scenario analysis with expert judgment |

### Monte Carlo vs. Scenario Analysis

| Feature | Monte Carlo | Scenario Analysis |
|---------|:---:|:---:|
| **Number of scenarios** | 10,000+ | 3–5 |
| **Output** | Probability distribution | Point estimates |
| **Input quality needed** | Distribution ranges | Expert estimates |
| **Effort** | Medium (setup code/tool) | Low |
| **Communication** | Percentiles, confidence intervals | Best/base/worst |
| **Best for** | Quantifying uncertainty, portfolio risks | Strategic decisions, board presentations |

## Key Concepts

### Random Sampling
Monte Carlo works by:
1. Defining probability distributions for each uncertain input
2. Randomly sampling from each distribution
3. Calculating the output for each set of samples
4. Repeating 10,000+ times
5. Analyzing the resulting output distribution

### Probability Distributions — When to Use Each

| Distribution | Shape | When to Use | Parameters | Example |
|-------------|:-----:|-----------|-----------|---------|
| **Triangular** | △ | Know min, most likely, max; asymmetric OK | min, mode, max | Project cost: ($800K, $1M, $1.5M) |
| **PERT** | Smooth △ | Like triangular but smoother, less extreme | min, mode, max | Revenue forecast: ($5M, $8M, $12M) |
| **Normal** | 🔔 | Symmetric uncertainty around a mean | mean, std dev | Monthly sales: μ=100, σ=15 |
| **Lognormal** | Right-skewed | Always positive, right-tailed (costs, durations) | ln(mean), ln(std dev) | Insurance claims, project delays |
| **Uniform** | ▬ | Equal probability across a range (maximum ignorance) | min, max | Price between $10 and $20 |
| **Beta** | Flexible | Bounded [0,1] or [a,b], flexible shape | α, β | Probability of success (0 to 1) |
| **Discrete** | Specific values | Known set of possible outcomes | values + probabilities | Market outcome: bull(40%), base(40%), bear(20%) |

**Rule of thumb:** When in doubt, use **triangular** (simple, intuitive) or **PERT** (smoother, more realistic).

## Python Implementation

### Setup

```python
import numpy as np
import matplotlib.pyplot as plt
from scipy import stats

np.random.seed(42)  # For reproducibility
N_SIMULATIONS = 10_000
```

### Example 1: Revenue Forecast Simulation

```python
# --- Inputs (uncertain) ---
# Number of new customers: triangular (50, 80, 120)
new_customers = np.random.triangular(50, 80, 120, N_SIMULATIONS)

# Average contract value: normal ($50K mean, $10K std)
avg_contract = np.random.normal(50_000, 10_000, N_SIMULATIONS)
avg_contract = np.maximum(avg_contract, 20_000)  # Floor at $20K

# Churn rate: beta distribution (centered around 10%)
churn_rate = np.random.beta(2, 18, N_SIMULATIONS)  # ~10% mean

# Existing customer base
existing_customers = 200
existing_arr = 200 * 45_000  # $9M existing ARR

# --- Calculation ---
new_arr = new_customers * avg_contract
retained_arr = existing_arr * (1 - churn_rate)
total_arr = new_arr + retained_arr

# --- Results ---
p10 = np.percentile(total_arr, 10)
p50 = np.percentile(total_arr, 50)
p90 = np.percentile(total_arr, 90)
mean = np.mean(total_arr)

print(f"Revenue Forecast (ARR):")
print(f"  P10 (conservative):  ${p10/1e6:.1f}M")
print(f"  P50 (median):        ${p50/1e6:.1f}M")
print(f"  Mean:                ${mean/1e6:.1f}M")
print(f"  P90 (optimistic):    ${p90/1e6:.1f}M")
print(f"  Range:               ${p10/1e6:.1f}M – ${p90/1e6:.1f}M")
```

### Example 2: Project Timeline Simulation

```python
# Define tasks with (min, most_likely, max) days
tasks = {
    "Requirements":     (10, 15, 25),
    "Design":           (15, 20, 35),
    "Development":      (30, 45, 80),
    "Testing":          (10, 15, 30),
    "Deployment":       (5, 7, 14),
}

# Simulate
total_duration = np.zeros(N_SIMULATIONS)
task_durations = {}

for task, (low, mode, high) in tasks.items():
    durations = np.random.triangular(low, mode, high, N_SIMULATIONS)
    task_durations[task] = durations
    total_duration += durations

# Results
print(f"Project Duration (working days):")
print(f"  P10:  {np.percentile(total_duration, 10):.0f} days")
print(f"  P50:  {np.percentile(total_duration, 50):.0f} days")
print(f"  P90:  {np.percentile(total_duration, 90):.0f} days")
print(f"  Prob of completing in 100 days: {(total_duration <= 100).mean()*100:.0f}%")
```

### Example 3: Sensitivity Analysis (Tornado Chart)

```python
# Calculate correlation of each input with total output
# to determine which inputs drive the most variance

from scipy.stats import spearmanr

inputs = {
    "New Customers": new_customers,
    "Avg Contract Value": avg_contract,
    "Churn Rate": churn_rate,
}

correlations = {}
for name, values in inputs.items():
    corr, _ = spearmanr(values, total_arr)
    correlations[name] = corr

# Sort by absolute correlation
sorted_corr = sorted(correlations.items(), key=lambda x: abs(x[1]), reverse=True)

print("Sensitivity Analysis (Spearman correlation with output):")
for name, corr in sorted_corr:
    bar = "█" * int(abs(corr) * 50)
    print(f"  {name:25s} {corr:+.3f} {bar}")
```

## Interpreting Output Distributions

### Key Statistics

| Statistic | What It Tells You | Use Case |
|-----------|------------------|---------|
| **Mean** | Average outcome across all simulations | Expected value for decision-making |
| **Median (P50)** | "Most likely" outcome (50% chance above, 50% below) | Central planning estimate |
| **P10** | Conservative estimate (90% chance of being better) | Downside planning, worst-case budgeting |
| **P90** | Optimistic estimate (only 10% chance of being better) | Upside scenario, stretch targets |
| **Standard deviation** | Spread of outcomes | Measure of total uncertainty |
| **Skewness** | Whether outcomes are asymmetric | Identifies if risk is concentrated on upside or downside |

### Confidence Intervals

| Confidence Level | Percentile Range | Interpretation |
|:----------------:|:---:|---|
| 80% | P10 to P90 | "We're 80% confident the outcome will be between X and Y" |
| 90% | P5 to P95 | "We're 90% confident..." |
| 95% | P2.5 to P97.5 | "We're 95% confident..." |

## Common Pitfalls

| Pitfall | Why It's a Problem | How to Avoid |
|---------|------------------|-------------|
| **Too few simulations** | Results don't converge, unreliable | Run at least 10,000; check convergence |
| **Wrong distribution choice** | Garbage in, garbage out | Use triangular/PERT when uncertain; validate with data |
| **Ignoring correlations** | Understates risk if inputs move together | Model correlations between inputs (e.g., revenue and costs) |
| **Over-precision** | Reporting $12,345,678 from uncertain inputs | Round to appropriate precision ($12.3M) |
| **Ignoring tail risks** | P99 events happen | Report P1/P99 or VaR, not just P10/P90 |
| **Not validating** | Model may have errors | Backtest against historical data; sanity-check extremes |

## Communicating Results to Executives

### Do
- Lead with the **decision** the simulation informs, not the methodology
- Use **three numbers**: conservative (P10), expected (P50), optimistic (P90)
- Show a **histogram** — one picture is worth 1,000 words
- Frame as **confidence**: "We're 80% confident revenue will be between $X and $Y"
- Highlight **what drives uncertainty** (tornado chart — top 2–3 drivers)

### Don't
- Lead with methodology ("We ran 10,000 Monte Carlo simulations...")
- Report false precision ($12,345,678.23)
- Show complex statistical output (PDFs, CDFs, skewness, kurtosis)
- Assume executives understand percentiles without explanation

### Executive Summary Template

> **Revenue Forecast for FY2027**
>
> Based on our analysis of key uncertainties (customer acquisition, contract size, and retention), we project FY2027 ARR of **$12.5M** (expected case).
>
> We are **80% confident** revenue will fall between **$10.8M** (conservative) and **$14.2M** (optimistic).
>
> The biggest driver of uncertainty is **new customer acquisition** — a 10% change in close rates swings revenue by ±$1.2M.
>
> **Recommendation:** Budget to the P25 ($11.5M) to maintain 75% confidence of meeting plan, while targeting the P50 ($12.5M) for stretch goals.

## Worked Example: New Product Launch Financial Simulation

**Context:** Consumer goods company launching a new product. Three major uncertainties: market size, market share, and pricing.

### Input Distributions

| Variable | Distribution | Parameters | Rationale |
|----------|:---:|---|---|
| Market size (units/year) | Triangular | (500K, 800K, 1.2M) | Based on category data; new category so wide range |
| Market share (Year 1) | PERT | (2%, 5%, 10%) | Comparable launches achieved 3–8% |
| Average selling price | Normal | ($24.99, $2.00) | Price testing suggests $22–$28 range |
| COGS per unit | Triangular | ($8, $10, $14) | Supplier quotes; volume-dependent |
| Marketing spend | Fixed | $2M | Budgeted |
| Launch fixed costs | Triangular | ($500K, $750K, $1.2M) | Packaging, displays, slotting fees |

### Results

```
Year 1 Profit/Loss Distribution:
  P10:  -$1.2M  (loss — low share, high costs)
  P25:  -$0.3M  (near breakeven)
  P50:   $0.8M  (modest profit)
  P75:   $2.1M  (solid profit)
  P90:   $3.5M  (strong success)
  Mean:  $0.9M

Probability of breakeven: 62%
Probability of >$1M profit: 43%
Probability of >$1M loss: 15%

Top drivers of uncertainty:
  1. Market share (r = 0.72) — BY FAR the biggest driver
  2. Market size (r = 0.45)
  3. COGS (r = -0.31)
  4. ASP (r = 0.28)
```

**Decision recommendation:** The launch has a 62% probability of breaking even in Year 1. The expected profit of $0.9M justifies the investment given the upside potential ($3.5M at P90). However, the 15% chance of losing >$1M should be mitigated with a staged launch (test market first to validate market share assumptions before national rollout).
