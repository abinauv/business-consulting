# Risk Quantification Guide

## Expected Loss Calculation

The fundamental formula:

```
Expected Loss = Probability of Occurrence × Financial Impact
```

### Probability Estimation Techniques

| Method | Best For | Accuracy | Effort |
|--------|---------|:--------:|:------:|
| **Historical data** | Recurring risks with track record | High | Low |
| **Industry benchmarks** | Common risks (cyber, fraud, natural disaster) | Medium | Low |
| **Expert elicitation** | Novel risks without data | Medium | Medium |
| **Reference class forecasting** | Project risks, strategic initiatives | Medium-High | Medium |
| **Bayesian updating** | Combining prior knowledge with new data | High | High |
| **Scenario analysis** | Complex, interconnected risks | Medium | Medium |

### Expert Elicitation Best Practices

When using expert judgment to estimate probability:
1. Use multiple experts independently (avoid groupthink)
2. Ask for ranges, not point estimates ("What's the minimum, most likely, and maximum?")
3. Calibrate by asking questions with known answers first
4. Use structured protocols (Delphi method, nominal group technique)
5. Average estimates, weighting by domain expertise
6. Document assumptions and rationale

## Impact Scales

### 5-Level Financial Impact Scale

| Level | Label | Small Company (<$50M rev) | Mid-Market ($50M–$500M) | Enterprise (>$500M) |
|:-----:|-------|:---:|:---:|:---:|
| 1 | Negligible | <$50K | <$250K | <$1M |
| 2 | Minor | $50K–$250K | $250K–$1M | $1M–$5M |
| 3 | Moderate | $250K–$1M | $1M–$5M | $5M–$25M |
| 4 | Major | $1M–$5M | $5M–$25M | $25M–$100M |
| 5 | Critical | >$5M | >$25M | >$100M |

### Multi-Dimensional Impact Scale

| Level | Financial | Operational | Reputational | Regulatory | Safety |
|:-----:|----------|------------|-------------|-----------|--------|
| 1 | <$50K loss | <1 hour disruption | No media coverage | No regulatory interest | No injuries |
| 2 | $50K–$250K | 1–8 hours disruption | Local media, social media buzz | Regulatory inquiry | Minor injury |
| 3 | $250K–$1M | 1–3 days disruption | National media, sustained social media | Formal investigation | Serious injury |
| 4 | $1M–$5M | 1–2 weeks disruption | Major negative coverage, customer impact | Fine, enforcement action | Multiple injuries |
| 5 | >$5M | >2 weeks disruption | Crisis-level, brand damage lasting months+ | License revocation, criminal charges | Fatality |

## 5×5 Risk Heat Map

### Risk Scoring Matrix

| | Impact 1 | Impact 2 | Impact 3 | Impact 4 | Impact 5 |
|:---:|:---:|:---:|:---:|:---:|:---:|
| **Prob 5 (>80%)** | 5 (M) | 10 (H) | 15 (C) | 20 (C) | 25 (C) |
| **Prob 4 (60-80%)** | 4 (M) | 8 (H) | 12 (H) | 16 (C) | 20 (C) |
| **Prob 3 (40-60%)** | 3 (L) | 6 (M) | 9 (H) | 12 (H) | 15 (C) |
| **Prob 2 (20-40%)** | 2 (L) | 4 (M) | 6 (M) | 8 (H) | 10 (H) |
| **Prob 1 (<20%)** | 1 (L) | 2 (L) | 3 (L) | 4 (M) | 5 (M) |

**L** = Low (Green, 1–3) | **M** = Medium (Yellow, 4–6) | **H** = High (Orange, 8–12) | **C** = Critical (Red, 15–25)

### Zone Definitions and Required Response

| Zone | Score Range | Response Required | Review Frequency | Escalation |
|------|:---:|---|---|---|
| **Critical** | 15–25 | Immediate mitigation plan, executive ownership, active management | Weekly | Board/C-suite |
| **High** | 8–12 | Documented mitigation plan, senior management ownership | Monthly | VP/Director |
| **Medium** | 4–6 | Monitored, mitigation plan if trending upward | Quarterly | Manager |
| **Low** | 1–3 | Accepted, monitored periodically | Semi-annually | Risk register |

## Risk Scoring Calibration

### Calibration Exercise

Before a risk assessment workshop, calibrate participants by scoring 3 well-known risks together:

**Example calibration risks:**
1. "Our main data center loses power for 24 hours" — Agree on probability and impact
2. "A key competitor launches a product that undercuts our pricing by 30%" — Score together
3. "Our top sales person leaves for a competitor" — Score together

This ensures all assessors are using the same mental models for the scales.

### Common Calibration Errors

| Error | Description | Fix |
|-------|-----------|-----|
| **Anchoring** | First risk scored anchors all subsequent scores | Randomize risk order, score independently first |
| **Availability bias** | Recent events weighted too heavily | Use historical data, compare to base rates |
| **Clustering** | All risks scored 3×3 (safe middle) | Force distribution — require at least some 1s and 5s |
| **Overconfidence** | Underestimating probability of rare events | Use pre-mortem technique ("assume it happened — why?") |

## Key Risk Indicators (KRIs)

### 20+ Example KRIs by Category

**Strategic Risks**
| KRI | Threshold (Green/Yellow/Red) | Frequency |
|-----|------|:---------:|
| Market share change | >0% / -1 to 0% / <-1% | Quarterly |
| Customer concentration (top 10%) | <30% / 30-50% / >50% | Quarterly |
| New product revenue as % of total | >15% / 10-15% / <10% | Quarterly |
| Employee engagement score | >4.0 / 3.5-4.0 / <3.5 | Semi-annually |

**Operational Risks**
| KRI | Threshold | Frequency |
|-----|-----------|:---------:|
| System uptime | >99.9% / 99.5-99.9% / <99.5% | Daily |
| Order fulfillment error rate | <0.5% / 0.5-2% / >2% | Weekly |
| Supplier on-time delivery | >95% / 90-95% / <90% | Monthly |
| Safety incident rate | <1 / 1-3 / >3 per 100K hours | Monthly |

**Financial Risks**
| KRI | Threshold | Frequency |
|-----|-----------|:---------:|
| Days Sales Outstanding (DSO) | <45 / 45-60 / >60 days | Monthly |
| Bad debt ratio | <1% / 1-3% / >3% | Monthly |
| Budget variance | <5% / 5-10% / >10% | Monthly |
| Cash runway (months) | >12 / 6-12 / <6 months | Monthly |

**Compliance Risks**
| KRI | Threshold | Frequency |
|-----|-----------|:---------:|
| Open audit findings | 0 / 1-3 / >3 | Monthly |
| Regulatory complaints | 0 / 1-2 / >2 | Monthly |
| Policy violations | 0 / 1-5 / >5 | Monthly |
| Training completion rate | >95% / 85-95% / <85% | Quarterly |

**Cybersecurity Risks**
| KRI | Threshold | Frequency |
|-----|-----------|:---------:|
| Unpatched critical vulnerabilities | 0 / 1-5 / >5 | Weekly |
| Phishing test failure rate | <5% / 5-15% / >15% | Monthly |
| Mean time to detect (MTTD) | <1hr / 1-24hr / >24hr | Monthly |
| Mean time to respond (MTTR) | <4hr / 4-24hr / >24hr | Monthly |

## Value at Risk (VaR) — Simplified

### Concept for Non-Financial Contexts

VaR answers: "What is the maximum loss we could expect with X% confidence over a given time period?"

**Example:** "We are 95% confident that our maximum loss from cyber incidents in any given year will not exceed $5M."

### Simple VaR Estimation

1. **Gather historical loss data** (or expert estimates if no history)
2. **Fit a distribution** (often lognormal for operational losses)
3. **Calculate the percentile** (95th or 99th percentile = VaR)

For a quick estimate without statistical modeling:
- **Expected loss** = Most likely scenario
- **VaR (95%)** ≈ 2–3× expected loss (for moderate-tailed risks)
- **VaR (99%)** ≈ 4–6× expected loss (for fat-tailed risks)

## Worked Example: Supply Chain Disruption Risk

**Context:** Manufacturing company assessing the risk of a major supplier disruption.

### Risk Identification

| Risk Event | Cause | Consequence |
|-----------|-------|------------|
| Key supplier factory shutdown (>30 days) | Fire, natural disaster, financial failure, labor dispute | Production halt, customer backlog, expediting costs, potential customer loss |

### Quantification

**Probability estimation:**
- Historical: 2 events in past 10 years across 15 key suppliers → 1.3% per supplier per year
- For the most critical supplier: Adjusted to 3% (older facility, single site, weaker financials)
- **Probability: 3% per year (Score: 2)**

**Impact estimation:**
- Revenue at risk: $20M/quarter if production halts (this supplier = 40% of critical component)
- Expediting cost if alternative supplier found: $2M (premium pricing, air freight)
- Customer penalties: $1M (SLA violations)
- Best case (alternative supplier in 30 days): $3M total impact
- Expected case (60 days): $8M total impact
- Worst case (90+ days, customer defections): $25M total impact
- **Expected impact: $8M (Score: 4)**

**Risk score: 2 × 4 = 8 (High)**

### Mitigation Plan

| Mitigation Action | Type | Cost | Risk Reduction | Priority |
|-------------------|------|:----:|:--------------:|:--------:|
| Qualify second source for critical component | Mitigate | $200K setup | Impact: 5→3 | 1 |
| Hold 60-day safety stock | Mitigate | $500K inventory cost | Impact: 4→2 | 2 |
| Business interruption insurance | Transfer | $100K/year premium | Financial impact: partial | 3 |
| Supplier financial monitoring (KRI) | Monitor | $10K/year | Early warning | 1 |
| Annual supplier site audit | Monitor | $15K/year | Early warning | 2 |

**Post-mitigation risk score:** Probability 2 × Impact 2 = **4 (Medium)**

**Decision:** Invest $825K to reduce risk from 8 (High) to 4 (Medium). The $8M expected loss × 3% probability = $240K expected annual loss. With mitigation, expected annual loss drops to ~$40K. The mitigation is justified if the safety stock and dual-source are valuable beyond risk reduction (they usually are for operational resilience).
