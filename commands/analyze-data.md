---
description: "Analyze a dataset and extract consulting-quality insights"
argument-hint: "[path to data file or description of data]"
---

# Data Analysis

Analyze the data described in **$ARGUMENTS** and extract actionable insights.

## Instructions

### Step 1: Data Understanding
- Load and examine the data
- Report: row count, column count, data types, date range
- Identify missing values, outliers, and data quality issues
- Document any cleaning or transformation steps taken

### Step 2: Descriptive Statistics
- Summary statistics for all numeric columns (mean, median, std, min, max, quartiles)
- Distribution analysis for key variables
- Identify skewness, outliers, and anomalies

### Step 3: Key Analysis (choose what's relevant)

**If time-series data:**
- Trend analysis (YoY, MoM growth rates)
- Seasonality patterns
- Anomaly detection
- Moving averages

**If customer/transaction data:**
- Pareto analysis (which 20% drives 80%?)
- Segmentation (RFM or other relevant cuts)
- Cohort analysis (if longitudinal)

**If comparative data:**
- Benchmarking and gap analysis
- Correlation analysis
- Driver decomposition

### Step 4: Visualization
Create 3-5 charts that tell the story. Each chart must have:
- An action title (states the insight, not the topic)
- Clean formatting following consulting standards
- Source note

### Step 5: Key Findings
Present 5-7 findings, each as:
- **[Bolded insight]:** Supporting evidence with specific numbers and "so what" implication for the business.

### Step 6: Recommendations
Based on the data, provide 3-5 actionable recommendations ranked by expected impact.

Use Python (pandas, matplotlib/seaborn) for analysis when a data file is provided. Save all charts as PNG files.
