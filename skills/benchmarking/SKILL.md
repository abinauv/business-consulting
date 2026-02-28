---
name: benchmarking
description: "Conduct benchmarking analysis comparing performance against peers, industry standards, and best-in-class organizations. Use this skill when the user mentions: benchmark, best practice, peer comparison, industry standard, maturity assessment, gap analysis, best in class, performance comparison, industry average, peer set, competitive benchmark, or operational benchmark."
user-invokable: true
---

# Benchmarking Analysis

You are a benchmarking specialist. Apply rigorous comparison methodologies to identify performance gaps and improvement opportunities.

## Benchmarking Methodology

### Types of Benchmarking

| Type | Description | When to Use |
|------|------------|-------------|
| **Internal** | Compare across business units, regions, or teams within the same organization | When the organization is large enough to have meaningful internal variation |
| **Competitive** | Compare against direct competitors | When competitive data is available and the goal is to match or beat rivals |
| **Functional** | Compare a specific function against best-in-class from any industry | When seeking step-change improvement in a function (e.g., compare supply chain to Amazon's) |
| **Generic** | Compare against broadly excellent companies | When seeking inspiration for transformational improvement |

### Benchmarking Process
1. **Define scope:** What is being benchmarked? (company, function, process, metric)
2. **Select metrics:** Choose 10-20 metrics that matter for this scope (see metric selection below)
3. **Identify comparators:** Select 5-10 peer companies with rationale for each
4. **Collect data:** Gather benchmarking data from multiple sources, flag confidence levels
5. **Normalize data:** Adjust for size, geography, industry mix, maturity to ensure apples-to-apples
6. **Analyze gaps:** Compare client position vs. peer median and best-in-class
7. **Diagnose root causes:** For significant gaps, hypothesize why the gap exists
8. **Develop action plan:** Recommend specific actions to close priority gaps

### Data Normalization
Adjustments to ensure fair comparison:
- **Size:** Revenue per employee, cost as % of revenue (not absolute dollars)
- **Geography:** Adjust for cost of living, labor rates, regulatory differences
- **Industry mix:** If companies serve different end-markets, adjust for segment profitability
- **Maturity:** Early-stage companies may have different metric profiles than mature ones
- **Accounting differences:** Adjust for different fiscal years, accounting standards (GAAP vs. IFRS), one-time items

## Metric Selection & Data Sourcing

### Financial Benchmarks
| Metric | Definition | Typical Source |
|--------|-----------|---------------|
| Revenue growth (3-year CAGR) | Compound annual growth rate | Public filings, estimates |
| Gross margin | (Revenue - COGS) / Revenue | Public filings |
| EBITDA margin | EBITDA / Revenue | Public filings, estimates |
| SGA as % of revenue | Selling, general & administrative / Revenue | Public filings |
| R&D as % of revenue | Research & development / Revenue | Public filings |
| Capex intensity | Capital expenditure / Revenue | Public filings |
| ROIC | NOPAT / Invested Capital | Calculated from filings |
| Revenue per employee | Revenue / FTEs | Public filings, LinkedIn |
| Free cash flow margin | FCF / Revenue | Calculated from filings |

### Operational Benchmarks
| Metric | Definition | Typical Source |
|--------|-----------|---------------|
| Customer acquisition cost | Total S&M spend / New customers | Industry reports, estimates |
| Net Promoter Score | % Promoters - % Detractors | Surveys, published scores |
| Customer churn rate | Customers lost / Total customers | SaaS reports, industry data |
| On-time delivery | Orders delivered on time / Total orders | Industry reports |
| Defect rate | Defective units / Total units | Industry reports |
| Inventory turns | COGS / Average inventory | Public filings |
| Capacity utilization | Actual output / Maximum output | Industry reports |
| Cycle time | Start to finish of one process cycle | Process benchmarking studies |

### Organizational Benchmarks
| Metric | Definition | Typical Source |
|--------|-----------|---------------|
| Revenue per employee | Revenue / Total FTEs | Public filings |
| Spans of control | Direct reports / Managers | Organizational surveys |
| Management layers | CEO to front line | Organizational analysis |
| HR cost per employee | Total HR cost / Employees | Industry reports |
| Employee engagement | Survey scores | Engagement platforms |
| Voluntary turnover | Voluntary departures / Average headcount | BLS, industry surveys |
| Training spend per employee | Training budget / Employees | Industry reports |

### Data Sources
**Primary:** Public company filings (10-K, annual reports, proxy statements), investor presentations
**Secondary:** Industry reports (IBISWorld, Gartner, Forrester), benchmarking databases (APQC, Hackett Group)
**Tertiary:** Trade association publications, government statistics, analyst estimates
**Proxy data:** LinkedIn headcount, job postings, Glassdoor reviews, web traffic

For every data point, document: source, date, confidence level (High/Medium/Low).

## Gap Analysis

### Quantitative Gap Measurement
For each metric, present:

| Metric | Client | Peer Median | Best-in-Class | Gap vs. Median | Gap vs. Best |
|--------|--------|-------------|---------------|----------------|--------------|
| [Metric] | [Value] | [Value] | [Value] | [Difference] | [Difference] |

Color-code: Green (at or above median), Yellow (within 10% of median), Red (more than 10% below median).

### Qualitative Capability Gap Assessment
Use maturity models (see below) for capabilities that aren't easily quantified:
- Digital maturity
- Data & analytics maturity
- Innovation maturity
- Customer experience maturity

### Prioritizing Gaps
Not all gaps matter equally. Prioritize by:
1. **Strategic impact:** How much does closing this gap affect competitive position?
2. **Financial impact:** What is the estimated value of closing the gap?
3. **Feasibility:** How difficult is it to close this gap? (investment, time, capability)
4. **Urgency:** Is the gap widening? Is there competitive pressure?

Plot on an Impact vs. Feasibility matrix → focus on high-impact, high-feasibility gaps first.

### Root Cause Analysis for Gaps
For the top 3-5 gaps, diagnose root causes:
- **Process issue:** Inefficient or broken processes
- **People issue:** Skills gap, understaffing, organizational structure
- **Technology issue:** Outdated systems, lack of automation, poor data quality
- **Strategy issue:** Misaligned priorities, under-investment, wrong market focus

Use 5 Whys or fishbone diagram to drill to root cause.

## Maturity Assessment Models

### Generic 5-Level Maturity Model
| Level | Name | Description |
|-------|------|-------------|
| 1 | **Ad Hoc** | No standardized process. Outcomes depend on individual heroics. |
| 2 | **Developing** | Basic processes exist but are inconsistently followed. Some documentation. |
| 3 | **Defined** | Standardized processes documented and generally followed. Performance measured. |
| 4 | **Managed** | Processes measured, managed with data. Continuous improvement practices in place. |
| 5 | **Optimized** | Best-in-class. Data-driven optimization. Innovation culture. Industry leadership. |

### Scoring Methodology
For each dimension:
1. Define 3-5 criteria that distinguish each level
2. Gather evidence (interviews, document review, data analysis)
3. Score based on evidence, not aspiration
4. Require consensus from multiple assessors
5. Document evidence for each score

### Radar/Spider Chart Visualization
Plot maturity scores across 6-8 dimensions on a radar chart:
- Current state (solid line)
- Target state (dashed line)
- Peer benchmark (dotted line)
The gap between current and target = improvement roadmap

### Dimension Templates
Adapt dimensions to the function being assessed. Common dimensions:
- **Digital maturity:** Strategy, Culture, Technology, Data, Talent, Operations
- **Operations maturity:** Process standardization, Automation, Quality management, Performance measurement, Continuous improvement, Supply chain management
- **Finance maturity:** Planning & forecasting, Reporting & analytics, Controls, Technology, Talent, Strategic partnership with business
- **HR maturity:** Talent acquisition, Development, Performance management, Compensation, Culture, HR technology

## Output Templates

### Benchmarking Summary Report (5-10 pages)
1. Executive summary (1 page)
2. Peer set and rationale (half page)
3. Metric comparison tables with gap analysis (2-3 pages)
4. Gap visualization (charts showing client vs. peers vs. best-in-class)
5. Root cause analysis for key gaps (1-2 pages)
6. Prioritized action plan (1-2 pages)

### Maturity Assessment Report
1. Overall maturity score and radar chart
2. Dimension-by-dimension narrative (current state, evidence, gap, recommendation)
3. Peer comparison (if available)
4. Improvement roadmap by dimension

### Gap-to-Action Bridge
For each priority gap:
| Gap Identified | Root Cause | Recommended Action | Expected Improvement | Effort Required | Timeline |
|---------------|------------|-------------------|---------------------|----------------|----------|
| [Gap] | [Cause] | [Action] | [Quantified] | [H/M/L] | [Months] |

For detailed data source directories and maturity model templates, consult the reference files in the `references/` directory.
