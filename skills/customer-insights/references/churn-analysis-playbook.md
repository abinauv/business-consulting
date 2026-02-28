# Churn Analysis Playbook

## Churn Definitions

| Metric | Formula | What It Tells You |
|--------|---------|------------------|
| **Logo churn** | Customers lost ÷ Starting customers | % of customers leaving (headcount) |
| **Gross revenue churn** | MRR lost (cancellations + downgrades) ÷ Starting MRR | Revenue loss before expansion |
| **Net revenue churn** | (MRR lost − MRR expansion) ÷ Starting MRR | Revenue loss after upsell/cross-sell offsets |
| **Net revenue retention (NRR)** | (Starting MRR + Expansion − Contraction − Churn) ÷ Starting MRR | Total revenue health of existing customers |

**Benchmark targets:**

| Segment | Logo Churn (monthly) | Gross Revenue Churn | Net Revenue Retention |
|---------|:--------------------:|:-------------------:|:--------------------:|
| Enterprise SaaS | <0.5% | <1% | >120% |
| Mid-market SaaS | <1% | <1.5% | >110% |
| SMB SaaS | <3% | <3% | >100% |
| Consumer subscription | <5% | <5% | >95% |
| E-commerce (repeat purchase) | N/A | N/A | >80% retention rate |

## Churn Measurement Methodology

### Period-Based Churn

```
Monthly Churn Rate = Customers who canceled in month / Customers at start of month
```

**Important:** Exclude new customers acquired during the period from both numerator and denominator.

### Cohort-Based Churn

Track retention by signup cohort — the gold standard:

| Cohort | Month 0 | Month 1 | Month 2 | Month 3 | Month 6 | Month 12 |
|--------|:-------:|:-------:|:-------:|:-------:|:-------:|:--------:|
| Jan 2025 | 100% | 85% | 78% | 74% | 65% | 52% |
| Feb 2025 | 100% | 87% | 80% | 76% | 68% | — |
| Mar 2025 | 100% | 90% | 84% | 80% | — | — |

**Insight:** If later cohorts retain better, your product/onboarding is improving. If they retain worse, you may have a market fit or quality problem.

### Survival Analysis

For deeper analysis, use survival curves (Kaplan-Meier) to model:
- Median customer lifetime (when 50% have churned)
- Hazard rate by tenure (when is churn risk highest?)
- Comparison between segments (which segments survive longer?)

## Churn Segmentation Framework

Segment churn to understand patterns:

### By Reason

| Category | Sub-reasons | Typical % | Data Source |
|----------|-----------|:---------:|-----------|
| **Product** | Missing features, bugs, performance, UX issues | 20–30% | Exit surveys, support tickets |
| **Value** | Doesn't justify cost, ROI unclear | 15–25% | Exit surveys, usage data |
| **Service** | Poor support, implementation failures | 10–15% | Support data, NPS |
| **Competition** | Switched to competitor | 10–20% | Exit surveys, sales intel |
| **Fit** | Wrong customer (shouldn't have sold to them) | 5–15% | Account analysis |
| **Budget** | Budget cuts, downsizing | 5–10% | Exit surveys, news |
| **Involuntary** | Payment failure, bankruptcy | 5–10% | Billing data |
| **Internal** | Champion left, reorg, strategic shift | 5–15% | CRM, exit surveys |

### By Customer Segment

| Segment Variable | Analysis Question |
|-----------------|------------------|
| **By size** | Do larger or smaller customers churn more? |
| **By industry** | Are certain industries a poor fit? |
| **By acquisition channel** | Do some channels attract lower-quality customers? |
| **By tenure** | When is churn risk highest (month 3? month 12?) |
| **By plan/price** | Do certain plans have higher churn? |
| **By usage level** | Does low usage predict churn? What's the threshold? |
| **By onboarding** | Did customers who completed onboarding retain better? |

## Predictive Churn Indicators

### 15 Leading Indicators

| # | Indicator | Data Source | Warning Threshold | Lead Time |
|---|----------|-----------|------------------|-----------|
| 1 | **Login frequency decline** | Product analytics | >30% decrease vs. prior period | 30–60 days |
| 2 | **Feature usage drop** | Product analytics | Stopped using core features | 30–60 days |
| 3 | **Support ticket volume spike** | Support system | 3x increase in tickets | 14–30 days |
| 4 | **Support sentiment** | NLP on tickets | Negative sentiment increase | 14–30 days |
| 5 | **NPS score drop** | Survey | Score dropped below 6 (Detractor) | 60–90 days |
| 6 | **Contract downsized** | Billing | Reduced seats/tier | 30 days |
| 7 | **Champion departure** | CRM/LinkedIn | Primary contact left the company | 60–90 days |
| 8 | **Billing issues** | Billing system | Failed payment, late payment | 14 days |
| 9 | **No engagement with CS** | CRM | No response to CSM outreach for 30+ days | 30–60 days |
| 10 | **Competitor evaluation** | Sales intel | Seen in competitor demo/trial | 30–60 days |
| 11 | **Onboarding incomplete** | Product | Didn't complete setup within 30 days | 30 days |
| 12 | **Low adoption breadth** | Product analytics | Only 1 user active in multi-seat account | 30–60 days |
| 13 | **Seasonal pattern** | Historical data | Approaching contract renewal date | 60–90 days |
| 14 | **Company news** | News feeds | Layoffs, M&A, budget cuts, leadership change | 30–90 days |
| 15 | **QBR declined** | CRM | Customer declined quarterly business review | 30 days |

### Health Score Model

Combine leading indicators into a composite health score:

| Component | Weight | Scoring |
|-----------|:------:|---------|
| Product usage (frequency, depth, breadth) | 30% | 0–100 based on usage vs. benchmark |
| Support health (ticket volume, sentiment, CSAT) | 20% | 0–100 based on sentiment and resolution |
| Engagement (CSM meetings, QBRs, email opens) | 15% | 0–100 based on responsiveness |
| Relationship (champion tenure, stakeholder access) | 15% | 0–100 based on relationship depth |
| Financial (payment history, expansion, contract terms) | 10% | 0–100 based on payment and growth |
| Growth signals (feature requests, expansion interest) | 10% | 0–100 based on forward-looking signals |

**Health zones:**
- **Green (80–100):** Healthy, likely to renew and expand
- **Yellow (50–79):** At risk, needs proactive intervention
- **Red (0–49):** High churn risk, immediate action required

## Intervention Strategies by Churn Risk

| Risk Level | Timing | Interventions | Owner |
|:----------:|--------|-------------|-------|
| **Red (imminent)** | Immediate | Executive sponsor call, custom save offer, on-site visit (if warranted), address root cause directly | CS Manager + Exec |
| **Yellow (elevated)** | Within 1 week | CSM outreach, health check call, additional training, success plan refresh, demonstrate ROI | CSM |
| **Green (healthy)** | Proactive | Quarterly business review, expansion opportunities, feature beta access, advisory board invite | CSM |

### Save Plays by Churn Reason

| Churn Reason | Save Play | Offer | Success Rate |
|-------------|----------|-------|:------------:|
| **Missing feature** | Roadmap preview, beta access, custom build consideration | Early access to upcoming feature | Medium |
| **Poor ROI** | ROI analysis, optimization session, usage training | Professional services hours, usage audit | Medium-High |
| **Price** | Value demonstration, right-sizing, term discount | Annual commitment discount (10–20%), plan adjustment | Medium |
| **Poor support** | Escalated support tier, dedicated resource | Premium support trial, assigned engineer | High |
| **Champion left** | New champion onboarding, exec alignment | Re-onboarding package, executive sponsor match | Medium |
| **Competitor threat** | Competitive comparison, custom demo, exec engagement | Feature match commitment, loyalty discount | Low-Medium |

## Retention Program Design

### Onboarding (Days 0–30) — Prevent Early Churn

- [ ] Welcome email with clear next steps (Day 0)
- [ ] Setup wizard or guided onboarding (Day 0–3)
- [ ] First value milestone achieved (Day 7)
- [ ] Check-in call or email (Day 14)
- [ ] Training session completed (Day 21)
- [ ] Onboarding success confirmation (Day 30)

### Adoption (Days 30–90) — Build Habit

- [ ] Weekly usage tips based on their use case
- [ ] Feature discovery prompts (introduce unused features)
- [ ] Best practices webinar invitation
- [ ] First QBR / success review (Day 60–90)
- [ ] Integration recommendations

### Maturity (Days 90+) — Deepen Value

- [ ] Quarterly business reviews with ROI reporting
- [ ] Expansion opportunity identification
- [ ] Customer advisory board invitation
- [ ] Case study / reference opportunity
- [ ] Product roadmap input sessions

## Win-Back Strategies

### Timing

| Time Since Churn | Win-Back Approach | Success Rate |
|:----------------:|------------------|:------------:|
| 1–3 months | "We miss you" + address original churn reason | 15–25% |
| 3–6 months | Product update highlighting new features | 10–15% |
| 6–12 months | Re-engagement campaign with special offer | 5–10% |
| 12+ months | Cold reactivation (treat as new prospect) | <5% |

### Win-Back Campaign Design

1. **Acknowledge** — "We understand why you left" (don't pretend it didn't happen)
2. **Show change** — "Here's what's different now" (new features, improved support, fixed bugs)
3. **Offer incentive** — Welcome-back pricing, free month, enhanced onboarding
4. **Remove friction** — Data migration, preserved settings, fast setup
5. **Set expectations** — Success plan for re-onboarding, assigned CSM

## Churn Economics

### Cost of Churn Calculator

| Component | Calculation | Example |
|-----------|-----------|---------|
| **Lost revenue** | Churned customer ACV × remaining lifetime | $50K ACV × 3 years = $150K |
| **Customer acquisition cost** | CAC to replace the customer | $25K |
| **Onboarding cost** | Time and resources to onboard replacement | $5K |
| **Revenue ramp** | Time to reach full revenue from replacement | 6 months × $50K/12 = $25K opportunity cost |
| **Referral loss** | Lost referral revenue | Est. $10K |
| **Total cost of one churned customer** | Sum of above | **$215K** |

### Retention Investment ROI

```
ROI = (Revenue saved from retained customers − Cost of retention program) / Cost of retention program

Example:
- Retention program cost: $200K/year (2 CSMs + tools)
- Customers saved: 20 accounts × $50K ACV = $1M
- ROI = ($1M − $200K) / $200K = 400%
```

**Rule of thumb:** It costs 5–7x more to acquire a new customer than to retain an existing one. Even modest retention improvements have outsized impact on revenue.

### Impact of Churn Reduction on Revenue

| Annual Revenue | Current Churn | Improved Churn | Revenue Impact (Year 1) | Revenue Impact (5-Year Cumulative) |
|:-:|:-:|:-:|:-:|:-:|
| $10M | 15% | 12% | +$300K | +$2.3M |
| $10M | 15% | 10% | +$500K | +$4.1M |
| $50M | 10% | 8% | +$1M | +$8.4M |
| $50M | 10% | 5% | +$2.5M | +$22.6M |

## Industry Churn Benchmarks

| Industry | Annual Churn (Logo) | Annual Churn (Revenue) | Net Revenue Retention |
|----------|:-------------------:|:---------------------:|:--------------------:|
| Enterprise SaaS | 5–7% | 5–8% | 115–130% |
| Mid-market SaaS | 10–15% | 8–12% | 105–115% |
| SMB SaaS | 30–40% | 20–30% | 90–100% |
| Consumer subscription (streaming) | 40–60% | 35–50% | 80–90% |
| Consumer subscription (fitness) | 50–70% | 45–60% | 70–85% |
| E-commerce (repeat purchase rate) | — | — | 25–40% repeat rate |
| Financial services | 10–15% | 8–12% | 95–105% |
| Telecom | 15–25% | 12–20% | 90–100% |
| Insurance | 10–20% | 8–15% | 95–105% |
