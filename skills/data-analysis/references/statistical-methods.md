# Statistical Methods for Consulting

A consulting-friendly reference for the statistical techniques most commonly used in business analysis. Each method is explained in plain English with guidance on when to use it, how to interpret results, and what pitfalls to avoid.

---

## Regression Analysis

### Simple Linear Regression

**What it is:** A method for modeling the relationship between one input variable (predictor) and one output variable (outcome). The result is a straight line of best fit: y = a + bx, where "a" is the intercept (the value of y when x is zero) and "b" is the slope (how much y changes for each one-unit increase in x).

**When to use in consulting:** Estimating the relationship between advertising spend and sales revenue. Forecasting costs based on production volume. Modeling the impact of price changes on demand.

**Interpretation:** The slope coefficient "b" is the key output. If b = 2.5, it means that for each additional unit of x, y increases by 2.5 units, holding all else equal. The sign of b tells you the direction: positive means x and y move together, negative means they move inversely.

**Worked example:** A retailer wants to understand how floor space (in square meters) relates to store revenue (in thousands of dollars). After running a regression on 50 stores, the result is: Revenue = 120 + 3.8 × Floor Space. This means: a store with zero floor space would theoretically generate $120K (the baseline from other factors), and each additional square meter of floor space is associated with $3.8K in additional revenue. An R-squared of 0.72 means floor space explains 72% of the variation in revenue across stores.

### Multiple Linear Regression

**What it is:** An extension that includes two or more predictor variables. The model becomes: y = a + b1×x1 + b2×x2 + ... + bn×xn. This allows you to isolate the effect of each variable while controlling for the others.

**When to use:** When the outcome depends on multiple factors. For example, store revenue depends on floor space, foot traffic, local income levels, and marketing spend. Multiple regression separates each contribution.

**Interpretation:** Each coefficient represents the change in y for a one-unit change in that predictor, holding all other predictors constant. This "all else equal" interpretation is the power of multiple regression: it lets you isolate individual effects.

### Key Metrics

**R-squared (R²):** The proportion of variance in the outcome explained by the model. Ranges from 0 to 1. Above 0.7 is generally a strong fit for business data. Between 0.4 and 0.7 is moderate. Below 0.3 suggests the model is missing important factors.

**p-value for each coefficient:** Tests whether the relationship is statistically significant. A p-value below 0.05 means there is less than a 5% probability that the observed relationship is due to random chance. In consulting, focus on practical significance (is the effect large enough to matter?) alongside statistical significance.

**Common pitfalls:** Multicollinearity occurs when predictor variables are highly correlated with each other (for example, floor space and rent cost). This inflates uncertainty in the coefficients and makes individual effects unreliable. Check the Variance Inflation Factor (VIF); values above 5 indicate a problem. Omitted variable bias occurs when an important predictor is left out, causing other coefficients to absorb its effect and become misleading.

---

## Correlation Analysis

### Pearson Correlation

**What it is:** A measure of the linear relationship between two continuous variables. The correlation coefficient "r" ranges from -1 to +1. A value of +1 means perfect positive linear relationship, -1 means perfect negative linear relationship, and 0 means no linear relationship.

**Interpretation thresholds for business data:**
- |r| > 0.7: Strong relationship. Worth investigating further.
- 0.4 < |r| < 0.7: Moderate relationship. May be useful with caveats.
- |r| < 0.4: Weak relationship. Unlikely to be a reliable predictor on its own.

**When to use in consulting:** As an initial scan to identify which variables might be related before building a regression model. Creating a correlation matrix across all numeric variables in a dataset quickly highlights the strongest relationships and potential redundancies.

### Spearman Correlation

**What it is:** A variant that measures the strength of a monotonic (consistently increasing or decreasing) relationship, even if it is not linear. It works by ranking the data and computing the correlation on the ranks.

**When to use instead of Pearson:** When the relationship between variables is nonlinear but consistently directional (e.g., exponential growth curves). When the data contains significant outliers that would distort Pearson correlation. When working with ordinal data (survey ratings, satisfaction scores).

### Correlation Does Not Equal Causation

This is the single most important caveat in data analysis. Two variables may be correlated because: (a) one causes the other, (b) the other causes the first, (c) a third variable causes both, or (d) the correlation is coincidental. In consulting, always investigate the mechanism behind a correlation before making causal claims. Use language like "is associated with" rather than "causes" unless you have experimental or quasi-experimental evidence.

---

## Hypothesis Testing

### What It Is

A formal framework for deciding whether an observed pattern in data is likely real or likely due to random chance. You start with a null hypothesis (there is no effect or no difference) and test whether the data provides sufficient evidence to reject it.

### p-Values Explained Simply

The p-value answers the question: "If there were truly no effect, how likely would we be to see data this extreme or more extreme?" A p-value of 0.03 means there is a 3% chance of observing the result if the null hypothesis were true. By convention, a p-value below 0.05 is considered statistically significant, meaning we reject the null hypothesis.

**Important nuance for consultants:** Statistical significance is not the same as practical significance. A very large dataset can make a tiny, meaningless effect statistically significant. Always ask: "Is the effect large enough to matter for business decisions?"

### t-Test

**What it is:** Tests whether the means of two groups are significantly different from each other.

**When to use:** Comparing average sales between two store formats. Testing whether a marketing campaign changed average order value. Evaluating whether customers in region A spend differently from customers in region B.

**Variants:** An independent samples t-test compares two separate groups. A paired t-test compares the same group before and after an intervention.

### Chi-Square Test

**What it is:** Tests whether two categorical variables are independent or associated. It compares observed frequencies in a contingency table to the frequencies you would expect if the variables were unrelated.

**When to use:** Testing whether customer segment (premium vs. standard) is related to churn (yes/no). Evaluating whether product defect rates differ across manufacturing plants. Checking whether survey response patterns differ by demographic group.

**Interpretation:** A significant chi-square result (p < 0.05) means the variables are associated, but it does not tell you how strongly. Use Cramer's V as a follow-up to measure the strength of association.

---

## Forecasting Basics

### Moving Averages

**What it is:** The average of the most recent "n" data points. As each new data point arrives, the oldest point drops off. A 3-month moving average smooths short-term noise; a 12-month moving average removes seasonality.

**When to use:** When you need a simple, robust estimate that smooths out fluctuations. Effective for stable, non-trending data or as a baseline to compare against more sophisticated methods.

**Limitation:** Moving averages lag behind the actual data. They respond slowly to sudden shifts and do not capture trends or seasonality explicitly.

### Exponential Smoothing

**What it is:** A weighted average of all past observations, where more recent observations receive higher weights. The smoothing parameter alpha (between 0 and 1) controls how quickly old data is discounted. A high alpha (e.g., 0.8) makes the forecast very responsive to recent changes. A low alpha (e.g., 0.2) makes it smoother and more stable.

**When to use:** When recent observations should matter more than older ones. Particularly useful for short-term forecasting (next month or next quarter). Holt's method extends exponential smoothing to capture trends. Holt-Winters extends it further to capture both trends and seasonality.

### Linear Trend Extrapolation

**What it is:** Fitting a straight line to historical data and extending it into the future. The simplest form of trend-based forecasting.

**When to use:** When the historical data shows a clear, consistent trend and you believe that trend will continue. Appropriate for medium-term forecasts (one to three years) in stable markets.

**Pitfall:** Linear extrapolation assumes the future will look like the past. It fails when markets hit saturation points, when disruptions occur, or when growth is inherently nonlinear (exponential or logistic). Always sanity-check the extrapolated values: does the forecast imply a market share above 100%? A negative cost? If so, the model is wrong.

### When to Use Which Method

| Situation | Recommended Method |
|-----------|-------------------|
| Stable data, no clear trend | Simple moving average |
| Recent data more important | Exponential smoothing |
| Clear upward or downward trend | Linear trend extrapolation or Holt's method |
| Seasonal patterns | Holt-Winters or seasonal decomposition |
| Multiple drivers, complex relationships | Regression-based forecasting |
| High uncertainty, need ranges | Scenario analysis (not point forecasting) |

---

## Confidence Intervals

### What They Mean

A confidence interval provides a range of plausible values for an estimate, along with a stated confidence level. A 95% confidence interval means: if we repeated this analysis many times on different samples from the same population, 95% of the intervals we calculate would contain the true value. It is not the probability that the true value falls within this specific interval, though it is often communicated that way informally.

### How to Calculate

For a sample mean: CI = sample mean plus or minus (critical value multiplied by standard error). The critical value for a 95% confidence interval is approximately 1.96. The standard error equals the standard deviation divided by the square root of the sample size. Larger samples produce narrower intervals (more precision).

### How to Communicate to Clients

**Do say:** "Based on our analysis of 500 customer transactions, the average order value is $85, with a 95% confidence interval of $78 to $92. We are confident the true average falls within this range."

**Do say:** "Our revenue forecast for next year is $12M, with a range of $10.5M to $13.5M reflecting the uncertainty in our key assumptions."

**Do not say:** "There is a 95% probability that the true value is between $78 and $92." This is a common misstatement. The true value either is or is not in the interval; the 95% refers to the long-run reliability of the method.

**Practical tip for consulting:** Clients respond better to ranges than to point estimates followed by error bars. Frame the interval as a "range of likely outcomes" or "our best estimate is X, with a plausible range of Y to Z." Tie the width of the interval to actionable implications: "If the true value is at the low end of the range, we would still break even on this investment."

### Common Pitfalls

**Confusing confidence with precision:** A 99% confidence interval is wider than a 95% interval. Higher confidence means a wider range, not a more precise estimate. Choose the confidence level based on the consequences of being wrong: use 99% when the stakes are very high.

**Ignoring sample size:** Small samples produce wide, unhelpful intervals. If a client asks for analysis with 15 data points, set expectations that the results will have considerable uncertainty. Recommend collecting more data if precision matters.

**Assuming normality:** Confidence intervals for means assume the data is approximately normally distributed or the sample is large enough for the Central Limit Theorem to apply (generally n > 30). For small samples of skewed data, use bootstrap confidence intervals instead.

---

## Quick Reference: Choosing the Right Method

| Question | Method |
|----------|--------|
| Is there a relationship between X and Y? | Correlation (Pearson or Spearman) |
| How much does Y change when X changes? | Regression (simple or multiple) |
| Are two group means different? | t-test |
| Are two categorical variables related? | Chi-square test |
| What will happen next month? | Moving average, exponential smoothing, or trend extrapolation |
| How certain is our estimate? | Confidence interval |
| Which variables matter most? | Multiple regression, then check coefficient size and significance |
| Is this pattern real or random? | Hypothesis test (check p-value and effect size) |
