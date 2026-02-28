# Chart Selection Guide for Consulting

## Decision Tree: What Chart Should I Use?

Start with the question: **"What is the message I need to communicate?"**

```
What is your message?
├── Comparison → How do items rank or differ?
│   ├── Few categories (≤7) → Vertical bar chart
│   ├── Many categories (>7) → Horizontal bar chart (sorted)
│   ├── Two variables per category → Grouped bar chart
│   └── Across time + categories → Small multiples or grouped bar
├── Trend → How has something changed over time?
│   ├── One series → Line chart
│   ├── Multiple series (≤4) → Multi-line chart
│   ├── Emphasize volume → Area chart (use sparingly)
│   └── Discrete periods → Vertical bar chart with time axis
├── Composition → What makes up the whole?
│   ├── At one point in time → Stacked bar, treemap, or pie (≤5 slices)
│   ├── Over time → Stacked bar or stacked area
│   ├── Two dimensions → Marimekko / mosaic chart
│   └── Hierarchical → Treemap
├── Distribution → How is data spread?
│   ├── One variable → Histogram or box plot
│   ├── Compare distributions → Side-by-side box plots
│   └── Density shape → Violin plot or kernel density
├── Relationship → How do two variables relate?
│   ├── Two variables → Scatter plot
│   ├── Three variables → Bubble chart (size = third variable)
│   └── Many variables → Correlation heatmap
└── Flow → How do things move between stages?
    ├── Sequential stages → Funnel chart
    ├── Multi-path flows → Sankey diagram
    └── Process with gains/losses → Waterfall chart
```

---

## Detailed Guidance by Chart Type

### Bar Charts (Vertical and Horizontal)

**When to use vertical bars:** Comparing values across a small number of categories (up to 7), or showing values at discrete time intervals (monthly revenue by quarter). The horizontal axis carries the categories; the vertical axis carries the values.

**When to use horizontal bars:** When you have many categories (more than 7), when category labels are long (product names, region names), or when you want to show a ranking. Horizontal bars make long labels readable and naturally suggest a ranked list when sorted from top to bottom.

**When NOT to use bars:** Do not use bar charts to show continuous trends over dozens of time periods. A line chart is far more effective for that purpose. Avoid 3D bar charts entirely; they distort perception and add no information.

**Formatting rules:** Always start the value axis at zero. Truncating the axis exaggerates differences and misleads readers. Use consistent bar widths. Space between bars should be roughly half the bar width.

### Line Charts

**Primary use:** Showing trends over continuous time. Line charts excel when you need to show the shape of change: acceleration, deceleration, inflection points, cycles.

**Multiple series:** Limit to four lines on a single chart. Beyond that, the chart becomes unreadable. Use small multiples instead: the same chart repeated for each series, sharing a common axis for easy comparison.

**When NOT to use lines:** Do not use line charts for categorical data that has no natural order. A line implies continuity between points, which is misleading when the x-axis categories are unordered (e.g., product names, regions).

**Area charts:** Use area charts only when the filled area conveys meaning, such as showing cumulative volume or emphasizing the magnitude of change. Stacked area charts can show composition over time but become hard to read with more than three or four series because only the bottom series sits on a flat baseline.

### Scatter Plots and Bubble Charts

**Scatter plots:** Show the relationship between two continuous variables. Each point is one observation. The pattern of points reveals whether the relationship is positive, negative, linear, nonlinear, or nonexistent.

**When to add a bubble dimension:** When a third variable (such as revenue size or market share) adds important context. The bubble area should be proportional to the value, not the radius, because humans perceive area more accurately. Always include a legend showing what bubble sizes represent.

**When NOT to use scatter:** Avoid scatter plots when one axis is categorical. Use a strip plot or box plot instead. Avoid them when you have very few data points (under 10) as the pattern will not be meaningful.

### Pie Charts (Use Sparingly)

**The rule:** Use pie charts only when you have five or fewer slices, and only when the message is about the dominant share of one or two segments. Pie charts are effective for a single message: "Segment A accounts for over half of the total."

**When NOT to use pie:** Do not use pie charts to compare multiple similarly sized segments. Humans are poor at comparing angles and areas, so differences of a few percentage points are invisible in a pie chart. Use a horizontal bar chart instead, which maps values to length, a dimension humans perceive accurately.

**Never use:** Exploded pie charts, 3D pie charts, or pie charts with more than five slices. Donut charts share the same limitations as pie charts but are acceptable when a headline number occupies the center.

### Treemaps

**When to use:** Showing part-to-whole relationships in hierarchical data with many categories. A treemap can handle dozens of categories effectively by using nested rectangles where the area encodes the value. They are excellent for showing "where does the money go" across many cost categories or "which products generate revenue" across a large portfolio.

**When NOT to use:** When exact comparison matters. It is difficult to compare two similarly sized rectangles, so treemaps work best when there are clear size differences.

---

## Consulting-Specific Chart Types

### Waterfall / Bridge Charts

**Purpose:** Show how a value builds up or breaks down from a starting point to an ending point, with intermediate positive and negative contributions. The classic consulting use case is a year-over-year revenue bridge: starting with last year's revenue, adding growth drivers (volume, price, new products), subtracting headwinds (churn, discounts), and arriving at this year's revenue.

**Key formatting:** Positive contributions in one color (blue or green), negative contributions in another (red or orange), and total bars in a darker or neutral color (dark blue or gray). Each bar floats from the running total, creating the waterfall effect. Label each bar with its value.

**Common use cases:** Revenue bridges, cost walks, EBITDA reconciliations, headcount changes, market size build-ups.

### Marimekko / Mosaic Charts

**Purpose:** Show composition across two dimensions simultaneously. The width of each column represents one variable (e.g., segment size), and the height of sections within each column represents another variable (e.g., market share by competitor within each segment). The total area of each cell is proportional to its share of the overall total.

**When to use:** Market landscape analysis (segments on x-axis, competitors on y-axis), portfolio analysis (geographies on x-axis, product lines on y-axis). Highly effective for showing where to compete: large cells are large opportunities.

**Caveat:** Marimekko charts are information-dense and require careful labeling. Do not use them in presentations to audiences unfamiliar with the format.

### Harvey Ball Matrices

**Purpose:** Qualitative comparison across multiple criteria. A matrix where rows are options (e.g., strategic initiatives, vendors, market segments) and columns are evaluation criteria. Each cell contains a Harvey ball: empty circle (low), quarter-filled, half-filled, three-quarter-filled, or full circle (high).

**When to use:** Comparing strategic options against criteria where precise quantification is not possible or necessary. Prioritization matrices, capability assessments, vendor evaluations.

**Best practice:** Limit to five to seven criteria (columns) and five to seven options (rows) to keep the matrix scannable. Always weight the criteria if they differ in importance.

### Football Field Charts (Valuation Ranges)

**Purpose:** Show the range of estimated values from multiple valuation methodologies on a single chart. Each methodology appears as a horizontal bar spanning from its low to high estimate, with a marker for the midpoint. The bars are stacked vertically so the reader can compare the ranges across methods at a glance.

**When to use:** M&A valuations, scenario comparisons, any analysis where multiple methods produce ranges of estimates.

**Formatting:** Use consistent colors for each methodology. Add a vertical reference line for the current price or proposed value. Label the low, mid, and high values for each bar.

### Tornado Charts

**Purpose:** Show sensitivity of an outcome to changes in individual assumptions. Each assumption is shown as a horizontal bar extending left (downside) and right (upside) from the base case. Bars are sorted by total range, widest at the top, creating the tornado shape.

**When to use:** After building a financial model or forecast, to communicate which assumptions matter most. This directs the audience's attention to the variables that have the greatest impact on the outcome.

**Formatting:** Use two colors (one for upside, one for downside). Label the assumption values at each end. Include the base case value as a vertical center line.

---

## Common Chart Mistakes in Consulting

### Too Many Colors
Using a different color for every data series creates visual noise and makes it impossible to direct the reader's attention. Instead, use one accent color to highlight the focal point of your message and gray for all supporting data. If you must distinguish multiple series, use a maximum of three to four distinct colors drawn from a colorblind-safe palette.

### 3D Effects
Three-dimensional charts distort the data. A 3D bar chart makes bars in the back appear smaller than they are, and 3D pie charts exaggerate slices at the front. There is no analytical reason to use 3D effects. They exist only as decoration and they actively mislead. Remove them always.

### Misleading Axes
Truncating the y-axis of a bar chart (not starting at zero) exaggerates small differences and can mislead readers into thinking a 2% change is dramatic. For bar charts, always start at zero. For line charts, truncation is acceptable if clearly labeled, because the message is about the trend shape rather than absolute magnitude. Dual y-axes are almost always confusing. If you must use them, ensure the two series are clearly distinguished and the reader understands which axis applies to which series.

### Overloaded Charts
Trying to tell five stories on one chart tells none of them well. Each chart should communicate one message. If you have five insights, create five charts. The temptation to combine arises from a desire to be efficient with slide space, but clarity always beats density. If the audience needs time to decode the chart, you have lost them.

### Chartjunk and Decoration
Gridlines, borders, background colors, gradient fills, drop shadows, and decorative icons all compete with the data for the reader's attention. Remove everything that does not directly support comprehension of the data. Edward Tufte's principle applies: maximize the data-to-ink ratio.

### Legend Placement
Placing the legend in a separate box forces the reader to look back and forth between the chart and the legend. Instead, label the data directly on the chart whenever possible. Place the series label at the end of each line or next to each bar. If a legend is unavoidable, place it close to the data it describes, not in a distant corner.
