# Lean Six Sigma Toolkit

A practical reference for the most commonly used Lean Six Sigma tools. Each entry covers what the tool is, when to use it, how to build it, and how to interpret the results.

---

## Quick Reference: Problem Type to Recommended Tool

| Problem Type | Recommended Tools |
|---|---|
| Need to prioritize which issues to tackle first | Pareto Chart |
| Need to find the root cause of a problem | Fishbone Diagram, 5 Whys, A3 Problem Solving |
| Need to monitor process stability over time | Control Chart |
| Need to understand the distribution of a variable | Histogram |
| Need to explore the relationship between two variables | Scatter Plot |
| Need to collect structured data on a problem | Check Sheet |
| Need to assess whether a process meets specifications | Process Capability Analysis |
| Need to proactively identify and prevent failures | FMEA |
| Need a structured problem-solving framework | A3 Problem Solving |

---

## 1. Pareto Chart

### What It Is
A bar chart that orders categories by frequency or impact (descending), overlaid with a cumulative percentage line. Based on the Pareto principle: roughly 80% of effects come from 20% of causes.

### When to Use
- When you have categorical data on defects, complaints, downtime causes, or cost drivers and need to prioritize
- During the Analyze phase of DMAIC to focus on the vital few causes

### How to Build It
1. List all categories (defect types, complaint categories, cost line items).
2. Count the frequency or total impact (cost, time) for each.
3. Sort from highest to lowest.
4. Calculate cumulative percentage.
5. Plot bars (left axis = count/cost) and the cumulative line (right axis = percentage).
6. Draw a horizontal line at 80% on the cumulative axis. Categories to the left of where this line crosses the bars are your "vital few."

### How to Interpret
- Focus improvement efforts on the first 2-4 bars that account for roughly 80% of the total.
- Re-run the Pareto after improvements to verify the distribution has shifted.
- If the chart is relatively flat (no clear 80/20 pattern), the causes are evenly distributed and you may need a different analytical approach.

---

## 2. Fishbone (Ishikawa) Diagram

### What It Is
A cause-and-effect diagram shaped like a fish skeleton. The "head" is the problem statement. The "bones" are major cause categories, with specific causes branching off each.

### When to Use
- When brainstorming potential root causes with a team
- During the Analyze phase of DMAIC
- When a single root cause is not obvious and you need structured exploration

### How to Build It
1. Write the problem statement clearly in a box on the right side (the fish head).
2. Draw a horizontal spine (arrow) pointing to the problem.
3. Add 4-6 major cause category branches. Standard categories for service processes: People, Process, Technology, Materials/Data, Measurement, Environment. For manufacturing: Man, Machine, Method, Material, Measurement, Mother Nature.
4. For each category, brainstorm specific potential causes. Ask "What within [category] could cause this problem?" Write each on a sub-branch.
5. For the most likely causes, ask "Why does this happen?" and add deeper sub-branches.
6. Circle or highlight the 3-5 most likely root causes based on data or team consensus.

### How to Interpret
- The diagram is a brainstorming tool, not a conclusion. Highlighted causes are hypotheses that must be verified with data.
- If one category has far more sub-branches than others, that area likely deserves the most investigation.
- Use this as input to targeted data collection or the 5 Whys for deeper analysis.

---

## 3. Five Whys

### What It Is
A simple iterative technique: start with a problem and ask "Why?" repeatedly (typically five times) to drill through symptoms to the underlying root cause.

### When to Use
- When a problem has a relatively straightforward cause chain
- As a follow-up to the fishbone diagram to investigate specific hypothesized causes
- For quick root cause analysis when a full statistical study is not warranted

### How to Build It
1. State the problem clearly and specifically (include metrics when possible).
2. Ask "Why does this happen?" and write the answer.
3. Take that answer and ask "Why?" again.
4. Repeat until you reach a cause that is actionable and systemic (not a surface symptom).
5. Five is a guideline, not a rule. Stop when you reach a root cause you can act on. Sometimes it takes 3 iterations, sometimes 7.

### Example
- **Problem:** Order fulfillment errors increased from 2% to 8% this quarter.
- **Why 1:** Warehouse staff are picking the wrong items. **Why 2:** Bin locations in the system do not match physical locations. **Why 3:** The bin location update was not completed after the warehouse reorganization last month. **Why 4:** No one was assigned ownership of updating the WMS after physical moves. **Why 5:** There is no standard procedure for syncing physical moves with the warehouse management system.
- **Root cause:** Missing SOP for WMS updates after physical warehouse changes.

### How to Interpret
- A good root cause is systemic (a process gap, missing procedure, or design flaw), not a person ("John made a mistake").
- If you reach "someone made an error," ask why the system allowed the error. The goal is error-proofing, not blame.
- Validate the cause chain: if you fix the root cause, would each subsequent "why" be prevented?

---

## 4. Control Chart

### What It Is
A time-series chart of a process metric with three lines: a center line (mean), an upper control limit (UCL), and a lower control limit (LCL). Control limits are typically set at +/- 3 standard deviations from the mean.

### When to Use
- During the Control phase of DMAIC to monitor whether improvements are sustained
- To distinguish between normal variation (common cause) and abnormal variation (special cause)
- When monitoring any ongoing process metric: cycle time, defect rate, throughput

### How to Build It
1. Collect at least 20-25 data points of the metric over time (e.g., daily defect rate for a month).
2. Calculate the mean (center line).
3. Calculate the standard deviation and set UCL = mean + 3 SD and LCL = mean - 3 SD.
4. Plot each data point in chronological order.
5. Draw the center line, UCL, and LCL.

### How to Interpret
- **In control:** All points fall between UCL and LCL with no patterns. Variation is random and expected.
- **Out of control signals:** One or more points beyond UCL/LCL, 7+ consecutive points on one side of the center line (run), 7+ consecutive points trending up or down, or two of three consecutive points near a control limit.
- Out-of-control signals indicate a special cause that should be investigated immediately.
- A stable (in-control) process is predictable. Only then can you calculate meaningful process capability.

---

## 5. Histogram

### What It Is
A bar chart showing the frequency distribution of a continuous variable. Each bar represents a range (bin) of values, and the height shows how many observations fall in that range.

### When to Use
- To understand the shape, center, and spread of process data
- During the Measure phase to characterize baseline performance
- When assessing whether data is normally distributed (important for many statistical tests)

### How to Build It
1. Collect at least 50 data points (more is better for reliable shape).
2. Determine the range (max - min).
3. Choose the number of bins. A common rule: square root of the number of data points, rounded.
4. Calculate bin width = range / number of bins.
5. Count observations in each bin and plot as bars.
6. Optionally overlay specification limits (LSL and USL) to see how much data falls outside spec.

### How to Interpret
- **Bell-shaped (normal):** Process is centered and symmetric. Standard statistical tools apply.
- **Skewed:** Process has a tail in one direction. Investigate why. Common in cycle-time data (most are fast, a few are very slow).
- **Bimodal (two peaks):** Likely two different processes or conditions mixed together. Stratify the data to separate them.
- **Truncated/clipped:** Data is being artificially cut off (e.g., a floor or ceiling). Investigate the constraint.
- Compare the spread of the data to specification limits to get a visual sense of process capability.

---

## 6. Scatter Plot

### What It Is
A two-dimensional chart plotting one variable on the X-axis and another on the Y-axis. Each data point represents one observation. Used to visually explore whether two variables are related.

### When to Use
- When you suspect a relationship between a process input (X) and an output (Y)
- During the Analyze phase to test hypothesized cause-effect relationships
- Before running regression analysis, as a visual sanity check

### How to Build It
1. Identify the suspected input variable (X) and the output variable (Y).
2. Collect paired data (each observation has both an X and a Y value). Aim for 30+ pairs.
3. Plot each pair as a point on the chart.
4. Optionally add a trend line (linear regression line) and the R-squared value.

### How to Interpret
- **Positive correlation:** Points trend upward left to right. As X increases, Y increases.
- **Negative correlation:** Points trend downward left to right. As X increases, Y decreases.
- **No correlation:** Points are scattered randomly with no visible pattern.
- **Nonlinear pattern:** Points follow a curve. A straight trend line will not capture this; consider a transformed model.
- Correlation does not prove causation. A relationship on a scatter plot is a hypothesis to investigate further, not a conclusion.

---

## 7. Check Sheet

### What It Is
A simple, structured form for collecting data in real time. It is designed so that data can be tallied at the point of observation without transcription.

### When to Use
- When you need to collect frequency data on defect types, causes, or locations
- During the Measure phase to establish baselines
- When existing data systems do not capture the detail you need

### How to Build It
1. Define what data you need to collect (e.g., defect type, location, shift, time).
2. Design a simple grid: rows are categories, columns are time periods or observation sessions.
3. Add space for date, observer name, and any relevant conditions.
4. Pilot the form with one or two observers. Revise for clarity.
5. Train all data collectors on definitions and procedures.
6. Collect data for a sufficient period (typically 2-4 weeks minimum).

### How to Interpret
- Tally the totals for each category and feed into a Pareto chart for prioritization.
- Look for patterns across time (e.g., more defects on night shift) or location (e.g., more errors in one region).
- Data quality depends entirely on consistent, disciplined collection. Inconsistent recording invalidates the analysis.

---

## 8. Process Capability Overview

### What It Is
A measure of how well a process meets specifications. Expressed as Cp (potential capability, assuming the process is centered) and Cpk (actual capability, accounting for how centered the process is).

### When to Use
- After establishing a stable (in-control) process using control charts
- To quantify whether a process can consistently meet customer or specification requirements
- When comparing processes or evaluating the impact of improvements

### Key Formulas
- **Cp** = (USL - LSL) / (6 x standard deviation). Measures the spread relative to the tolerance. Cp >= 1.33 is generally considered capable.
- **Cpk** = minimum of [(USL - mean) / (3 x SD), (mean - LSL) / (3 x SD)]. Accounts for centering. Cpk >= 1.33 means the process is both capable and centered.

### How to Interpret
- Cp = 1.0: The process spread exactly equals the tolerance width. About 0.27% defects (2,700 per million).
- Cp = 1.33: Good capability. About 63 defects per million.
- Cp = 2.0: Excellent capability (Six Sigma level). About 3.4 defects per billion.
- If Cp is high but Cpk is low, the process is capable but not centered. Shifting the mean is usually easier than reducing variation.

---

## 9. FMEA (Failure Mode and Effects Analysis)

### What It Is
A proactive risk assessment tool that systematically identifies potential failure modes in a process or product, assesses their severity, likelihood, and detectability, and prioritizes them for preventive action.

### When to Use
- When designing a new process or product (preventive)
- When modifying an existing process and want to anticipate what could go wrong
- During the Improve phase to evaluate risks of proposed changes
- Whenever high-consequence failures are possible

### How to Build It
1. List every process step or component.
2. For each, brainstorm potential failure modes (what could go wrong).
3. For each failure mode, identify the effect (impact on customer or downstream process).
4. Score three dimensions (each on a 1-10 scale):
   - **Severity (S):** How bad is the effect if the failure occurs? (1 = negligible, 10 = catastrophic)
   - **Occurrence (O):** How likely is the failure to occur? (1 = very unlikely, 10 = almost certain)
   - **Detection (D):** How likely is it that the failure will be detected before reaching the customer? (1 = always detected, 10 = undetectable)
5. Calculate the Risk Priority Number: RPN = S x O x D. Range is 1 to 1000.
6. Rank failure modes by RPN. Address the highest-priority items first.
7. For top items, assign corrective actions, responsible owners, and target dates.
8. After implementing actions, rescore to verify RPN has decreased.

### How to Interpret
- There is no universal RPN threshold. A common approach: address all items with RPN above 100-200 or the top 20% of items.
- Pay special attention to any failure mode with Severity of 9 or 10, regardless of RPN, because catastrophic failures warrant action even if unlikely.
- FMEA is a living document. Update it whenever the process changes or new failure modes are discovered.

---

## 10. A3 Problem Solving

### What It Is
A structured problem-solving approach documented on a single A3-sized sheet of paper (11x17 inches). Originated at Toyota. Forces concise, logical thinking and clear communication by constraining the analysis to one page.

### When to Use
- For any problem that requires structured analysis and cross-functional collaboration
- When you need to communicate the problem, analysis, and proposed solution to leadership concisely
- As the standard format for improvement proposals in Lean organizations

### How to Build It

The A3 has seven sections, read left-to-right, top-to-bottom:

**Left side (problem understanding):**
1. **Background:** Why is this problem important? Context, business impact, strategic relevance. Two to three sentences.
2. **Current Condition:** What is happening now? Use data, charts, and process maps. Be factual and specific.
3. **Goal/Target:** What specific, measurable outcome do we want? By when?
4. **Root Cause Analysis:** What is causing the problem? Use fishbone, 5 Whys, Pareto, or other tools. Show the analysis, not just the conclusion.

**Right side (solution and execution):**
5. **Countermeasures:** What specific actions will address each root cause? For each action: what, who, when.
6. **Implementation Plan:** Timeline, milestones, resource requirements. Often shown as a Gantt-style chart.
7. **Follow-up:** How will we verify the countermeasures worked? What metrics will we track? When will we review?

### How to Interpret
- A good A3 tells a logical story: the background leads to the current condition, which reveals a gap to the target, which is explained by root causes, which are addressed by specific countermeasures.
- If any section is vague, the analysis is incomplete. Each section should have data, not just opinions.
- The A3 is also a coaching tool. Leaders should ask questions about the thinking process, not just approve or reject the conclusion.

---

## Selecting the Right Tool

When beginning an analysis, start with these questions:

1. **Do we understand the problem?** If not, start with Check Sheets and Histograms to characterize the situation.
2. **Do we know the top contributors?** If not, use Pareto Charts to prioritize.
3. **Do we know the root cause?** If not, use Fishbone Diagrams and 5 Whys to investigate.
4. **Is the process stable?** If unknown, use Control Charts to assess stability.
5. **Can the process meet requirements?** If unknown, use Process Capability Analysis to quantify.
6. **Are we designing something new or changing something existing?** Use FMEA to anticipate failures.
7. **Do we need to communicate the full analysis on one page?** Use the A3 format.

Combine tools as needed. A typical DMAIC project will use most of these tools across different phases. The key is matching the right tool to the right question at the right time.
