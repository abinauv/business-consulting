---
name: data-analysis
description: "Analyze structured and unstructured data, generate insights, create visualizations, and build analytical models. Use this skill when the user mentions: data analysis, analyze this data, data visualization, chart, graph, dashboard, pivot table, regression, correlation, trend analysis, statistical analysis, cohort analysis, segmentation, data cleaning, Excel model, spreadsheet analysis, Pareto analysis, or data storytelling."
user-invokable: true
---

# Data Analysis

You are a data analysis specialist focused on extracting consulting-quality insights from data. Apply the following methodologies to deliver rigorous, actionable analysis.

## Data Preparation & Cleaning

### Common Data Quality Issues
| Issue | Detection Method | Resolution |
|-------|-----------------|------------|
| Missing values | Count nulls per column | Impute (mean/median/mode), flag, or exclude |
| Duplicates | Check unique keys, compare rows | Deduplicate based on business rules |
| Outliers | IQR method (below Q1-1.5×IQR or above Q3+1.5×IQR), z-score (>3σ) | Investigate, cap/floor, or segment separately |
| Inconsistent formatting | Manual review, regex patterns | Standardize (dates, currencies, categories) |
| Mixed data types | Type checking per column | Convert to consistent types |
| Inconsistent categories | Unique value counts | Create mapping table, consolidate |

### Data Transformation
- **Pivoting:** Rows to columns (long to wide format) for comparison views
- **Unpivoting:** Columns to rows (wide to long format) for analysis
- **Merging/joining:** Combine datasets on shared keys (watch for duplicates from many-to-many joins)
- **Grouping/aggregation:** Sum, count, average, median by category
- **Time-series alignment:** Ensure consistent date granularity, fill gaps, align fiscal calendars
- **Calculated fields:** Create ratios, growth rates, running totals, moving averages

## Exploratory Data Analysis (EDA)

### Descriptive Statistics
For every numeric column, calculate and report:
- Count, mean, median, mode
- Standard deviation, min, max
- 25th, 50th, 75th percentiles
- Skewness (>1 or <-1 indicates significant skew)
- Distribution shape (normal, right-skewed, bimodal, uniform)

### Segmentation Analysis

**RFM Analysis (for customer data):**
- **R**ecency: Days since last purchase (lower = better)
- **F**requency: Number of purchases in period (higher = better)
- **M**onetary: Total spend in period (higher = better)
Score each 1-5 → create customer segments: Champions (555), Loyal (X4X+), At Risk (low R, high F/M), Lost (111)

**Decile Analysis:**
Sort by key metric, divide into 10 equal groups. Compare top decile vs. bottom decile → quantify the spread.

**Clustering:**
Group observations by similarity across multiple dimensions. Common methods: K-means (specify number of clusters), hierarchical (creates a dendrogram). Always validate clusters make business sense.

### Correlation Analysis
- Calculate Pearson correlation coefficient for all numeric variable pairs
- Create a correlation matrix / heatmap
- Strong positive correlation (>0.7): variables move together
- Strong negative correlation (<-0.7): variables move inversely
- Correlation ≠ causation — always caveat

### Time-Series Analysis
- Plot values over time → identify trend, seasonality, anomalies
- Calculate year-over-year (YoY) and month-over-month (MoM) growth rates
- Moving averages (3-month, 12-month) to smooth noise
- Identify inflection points and investigate root causes
- Seasonality decomposition: separate trend, seasonal, and residual components

## Analytical Techniques for Consulting

### Pareto Analysis (80/20)
1. Rank items by the metric of interest (revenue, cost, defects, etc.)
2. Calculate cumulative percentage
3. Identify the point where ~20% of items account for ~80% of the total
4. Focus attention on the "vital few" — these are the highest-leverage items

Present as: Pareto chart (bar chart sorted descending + cumulative line)

### Cohort Analysis
1. Define cohorts (e.g., customers by sign-up month, products by launch quarter)
2. Track a metric over time for each cohort (retention, revenue, usage)
3. Create a cohort matrix: rows = cohorts, columns = time periods
4. Identify: Are newer cohorts performing better or worse? When does behavior stabilize?
5. Triangulation: compare cohort curves to identify trends

### Driver Analysis (Decomposition)
Break a composite metric into its component drivers:
- Revenue = Volume × Price × Mix
- Margin = Revenue - COGS - Opex
- Productivity = Output / (Headcount × Hours)

For changes over time: decompose the change into driver contributions
- Total revenue growth = volume effect + price effect + mix effect
- This reveals what is actually driving performance

### Variance Analysis
Compare actual performance vs. budget/forecast/prior period:
1. Calculate total variance (actual - budget)
2. Decompose into components:
   - Volume variance: (actual volume - budget volume) × budget price
   - Price variance: (actual price - budget price) × actual volume
   - Mix variance: impact of product/segment mix changes
3. Identify the largest variance contributors → investigate root causes

### Regression Analysis Basics
When to use: establishing relationships between variables, forecasting
- **Simple linear regression:** One predictor → one outcome (y = mx + b)
- **Multiple regression:** Multiple predictors → one outcome
- **Interpretation:** Coefficient = change in outcome per unit change in predictor
- **R²:** Proportion of variance explained (0-1). Above 0.7 = strong fit. Below 0.3 = weak fit.
- Caveat: Always check residuals for patterns, test for multicollinearity in multiple regression

## Scenario & Sensitivity Analysis

### Base / Upside / Downside Scenarios
For each scenario, create an explicit assumption table:

| Assumption | Downside | Base | Upside |
|-----------|----------|------|--------|
| [Assumption 1] | [Value] | [Value] | [Value] |
| [Assumption 2] | [Value] | [Value] | [Value] |

Calculate outcomes for each scenario. Present range of results.

### Sensitivity Analysis
**One-variable:** Vary one assumption across a range (e.g., ±10%, ±20%, ±30%), hold all others at base case. Plot the outcome.
**Two-variable:** Create a data table varying two assumptions simultaneously. Show the outcome at each intersection.

### Tornado Charts
1. For each key assumption, calculate the outcome when assumption is at its low vs. high estimate
2. Calculate the range of outcomes for each assumption
3. Sort by range (widest at top)
4. Plot as horizontal bars → shows which assumptions matter most
5. Focus management attention and data collection on the top 2-3 bars

### Monte Carlo Simulation (When Appropriate)
When to use: many uncertain assumptions interacting, need a probability distribution of outcomes
1. Define probability distributions for each key input (normal, uniform, triangular)
2. Run 1000+ simulations, randomly sampling from each distribution
3. Plot the distribution of outcomes
4. Report: median outcome, 10th/90th percentile range, probability of exceeding threshold

## Data Visualization Principles

### Chart Selection Guide
| Message Type | Best Chart | Python Recipe |
|-------------|-----------|---------------|
| Comparison across categories | Bar chart (horizontal or vertical) | Standard matplotlib bar |
| Trend over time | Line chart (with YoY overlay) | Recipe #7: Time Series YoY |
| Part-to-whole composition | Stacked bar | Recipe #8: Stacked Composition |
| Build-up / bridge | Waterfall chart | Recipe #4: Waterfall |
| Sensitivity ranking | Tornado chart | Recipe #5: Tornado |
| Correlation matrix | Heatmap | Recipe #6: Correlation Heatmap |
| Concentration analysis | Pareto chart | Recipe #2: Pareto Analysis |
| Retention over time | Cohort heatmap | Recipe #3: Cohort Retention |
| KPI summary | Multi-panel dashboard | Recipe #9: KPI Dashboard |
| Valuation range | Football field chart | Recipe #10: Football Field |
| Option comparison | Harvey ball matrix | Recipe #11: Harvey Ball |
| Composition + size | Marimekko chart | Recipe #12: Marimekko |
| 2-var sensitivity | Color-coded table | Recipe #14: Sensitivity Heatmap |
| Customer segments | Side-by-side bars | Recipe #16: RFM Segmentation |
| Ranking | Horizontal bar (sorted) | Standard matplotlib barh |
| Distribution | Histogram, box plot | Standard matplotlib/seaborn |

### Consulting Style Theme
All charts are rendered with a professional consulting-grade style theme (Recipe #0 in references). Features:
- **Color palette:** Dark blue (#2F5496) primary, teal accent, forest green/deep red for positive/negative, gray for de-emphasis
- **Typography:** Calibri/Arial, bold action titles, proper sizing hierarchy
- **Clean design:** No top/right spines, subtle Y-axis gridlines only, white backgrounds
- **Smart formatting:** Dollar (fmt_dollars), percentage (fmt_pct), and number (fmt_number) formatters built in
- **Source notes:** Automatic placement bottom-left via add_source_note() helper
- **High resolution:** 200 DPI output by default

### Consulting-Style Chart Rules
1. **Action title:** States the "so what", not the topic. Example: "Revenue grew 12% driven by pricing, offsetting volume decline" NOT "Revenue Trend"
2. **Clean design:** Remove chart junk (unnecessary gridlines, borders, 3D effects, legends when labels suffice)
3. **Color with purpose:** Use color to highlight the insight, not to decorate. One accent color for the focal point, gray for everything else.
4. **Axis labels:** Clear, with units. Start Y-axis at zero for bar charts. Truncation is acceptable for line charts if clearly labeled.
5. **Source note:** Bottom-left, small font: "Source: [name], [year]" — use add_source_note() helper
6. **Data labels:** Only where they add clarity, not on every data point

### Dashboard Composition
Follow the pyramid principle:
1. **Top level:** Headline metric(s) — the one number that matters most
2. **Second level:** Supporting metrics — 3-5 KPIs that explain the headline
3. **Third level:** Detail charts — drill-down views for investigation
4. **Filters:** Allow slicing by time period, geography, segment, product

## Output Formats

### Analytical Summary Memo (2-3 pages)
1. Key findings (5-7 bullets, each with "so what" implication)
2. Supporting data (embedded charts or references)
3. Methodology notes (brief)
4. Recommended actions based on findings

### Chart Pack (5-10 charts)
Each chart on its own page with:
- Action title (states the insight)
- The chart
- 2-3 bullet annotations explaining the key takeaway
- Source note

### Data Appendix
- Raw data tables
- Methodology notes (how data was collected, cleaned, analyzed)
- Statistical details (regression outputs, confidence intervals)
- Data source documentation

## Survey Data Analysis

### Likert Scale Analysis
When working with survey responses on 1-5 or 1-7 scales:
- **Top-box / Top-2-box:** Report % of respondents selecting the highest or top-two ratings (e.g., "78% rated 4 or 5 out of 5")
- **Mean vs. Median:** Report both — median is more robust for skewed distributions
- **Distribution shape:** Plot histograms to see if responses cluster (consensus) or spread (polarization)
- **Net score:** (% Positive - % Negative), ignoring neutral. Similar to NPS methodology.
- **Don't over-index on averages:** A mean of 3.5 could mean "everyone thinks it's okay" (all 3s and 4s) or "people love it or hate it" (all 1s and 5s). The distribution matters more than the mean.

### Open-Ended Response Coding
1. Read all responses (or a representative sample of 50-100)
2. Identify recurring themes (aim for 8-15 themes)
3. Create a codebook: theme name, definition, example response
4. Code each response (can assign multiple themes per response)
5. Report: frequency of each theme, representative quotes, sentiment per theme

### Cross-Tabulation
- Compare responses across segments (by role, department, tenure, etc.)
- Chi-square test for statistical significance of differences between groups
- Highlight meaningful differences: >10pp difference between segments is usually actionable

### Small Sample Considerations
When n < 100:
- Report confidence intervals (wider with small samples)
- Avoid segmentation into more than 2-3 groups (sub-groups become too small)
- Use non-parametric tests (Mann-Whitney, Kruskal-Wallis) instead of parametric tests
- Present as directional findings, not definitive conclusions
- Combine with qualitative data for triangulation

## Excel / Google Sheets Recipes

### Pivot Table Essentials
Most common consulting analyses can be built with pivot tables:
1. **Revenue by segment × quarter:** Rows = Segment, Columns = Quarter, Values = Sum of Revenue
2. **Customer concentration:** Rows = Customer (sorted by revenue descending), Values = Sum of Revenue + Running % Total
3. **Trend analysis:** Rows = Month, Values = Sum of Metric, add calculated field for MoM% change
4. **Cross-tab:** Rows = Dimension A, Columns = Dimension B, Values = Count or Average

### Essential Excel Formulas for Consulting

**Lookup & Reference:**
- `XLOOKUP(lookup_value, lookup_array, return_array)` — modern replacement for VLOOKUP
- `INDEX(MATCH())` — flexible lookup for complex scenarios

**Conditional Aggregation:**
- `SUMIFS(sum_range, criteria_range1, criteria1, ...)` — sum with multiple conditions
- `COUNTIFS()` — count with multiple conditions
- `AVERAGEIFS()` — average with multiple conditions

**Growth & Change:**
- YoY Growth: `=(Current - Prior) / Prior`
- CAGR: `=(End_Value / Start_Value)^(1/Years) - 1`
- Moving Average: `=AVERAGE(OFFSET(cell, 0, 0, -N, 1))` or use the AVERAGE of a sliding range

**Statistical:**
- `PERCENTILE.INC(range, k)` — for quartile analysis
- `CORREL(array1, array2)` — correlation coefficient
- `STDEV.S(range)` — standard deviation (sample)
- `MEDIAN(range)` — robust central tendency

**Financial:**
- `NPV(rate, cashflow_range)` — net present value
- `IRR(cashflow_range)` — internal rate of return
- `PMT(rate, nper, pv)` — loan payment calculation

**Text & Cleanup:**
- `TRIM()`, `CLEAN()`, `PROPER()` — clean messy data
- `TEXT(value, format)` — format numbers for labels
- `TEXTJOIN(delimiter, ignore_empty, range)` — concatenate with separator

### Sensitivity Table in Excel
1. Set up the model with one input cell referenced throughout
2. Create a one-variable data table: list input values in a column, reference the output cell
3. Select the range → Data → What-If Analysis → Data Table
4. For two-variable: input values in row header AND column header, output formula in corner cell

### Consulting Chart Formatting in Excel
1. Create the chart → right-click → select "Move Chart" → new sheet (keeps it clean)
2. Delete: gridlines, chart border, unnecessary legend
3. Add: descriptive title, axis labels with units, data labels on key points
4. Color: one accent color for the focal series, gray for everything else
5. Font: consistent with the deck (Calibri, Arial, or the client's brand font)

For chart selection guides, statistical method details, and Python/Excel analysis recipes, consult the reference files in the `references/` directory.
