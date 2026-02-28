# Market Sizing Templates & Worked Examples

This reference provides practical, step-by-step market sizing examples across three common business models, along with sensitivity analysis guidance and presentation templates.

---

## 1. B2B SaaS Market Sizing — Worked Example

**Scenario:** A startup is building an AI-powered contract management platform for mid-market companies (100-1,000 employees) in the United States.

### Top-Down Approach

| Step | Description | Value | Source |
|------|-------------|-------|--------|
| 1 | Global contract lifecycle management (CLM) market | $2.9B (2024) | Grand View Research |
| 2 | North America share of global CLM market | 42% | Grand View Research |
| 3 | North America CLM market | $2.9B x 0.42 = **$1.218B** | Calculated |
| 4 | U.S. share of North America | ~88% | Estimated from GDP ratio |
| 5 | U.S. CLM market | $1.218B x 0.88 = **$1.072B** | Calculated |
| 6 | Mid-market segment share (vs. enterprise + SMB) | 30% | Estimated from Gartner segmentation |
| 7 | **SAM (U.S. mid-market CLM)** | $1.072B x 0.30 = **$322M** | Calculated |

**TAM:** $2.9B (global CLM market)
**SAM:** $322M (U.S. mid-market segment)

### Bottom-Up Approach

| Step | Description | Value | Source |
|------|-------------|-------|--------|
| 1 | Total U.S. companies with 100-1,000 employees | ~120,000 | Census Bureau, County Business Patterns |
| 2 | % that manage 500+ contracts annually | ~35% | Industry survey proxy |
| 3 | Target customer count | 120,000 x 0.35 = **42,000** | Calculated |
| 4 | Average annual contract value (ACV) for mid-market CLM | $18,000/year | Pricing benchmark from competitor analysis |
| 5 | **SAM (bottom-up)** | 42,000 x $18,000 = **$756M** | Calculated |
| 6 | Realistic penetration in 5 years (new entrant) | 2-4% | Benchmark for B2B SaaS |
| 7 | **SOM** | $756M x 0.03 = **$22.7M** | Calculated (using 3% midpoint) |

### Triangulation

- Top-down SAM: $322M
- Bottom-up SAM: $756M
- Delta: 135% — this is significant and requires investigation

**Diagnosis:** The bottom-up approach counts all companies that could use CLM, while the top-down measures current spending. The gap suggests that many mid-market companies still manage contracts manually (Excel, shared drives). This is actually a positive signal — it means there is unmet demand. Adjust the bottom-up by applying a "willingness to pay for software" filter of ~45%, yielding $756M x 0.45 = $340M. The adjusted delta is now under 6%, giving high confidence.

**Final Estimates:** TAM: $2.9B | SAM: $330M (average of adjusted estimates) | SOM: $22-23M (5-year target)

---

## 2. B2C Consumer Market Sizing — Worked Example

**Scenario:** A D2C brand selling premium plant-based protein bars targeting health-conscious millennials and Gen Z in the U.S.

### Top-Down Approach

| Step | Value | Source |
|------|-------|--------|
| U.S. protein bar market | $6.2B (2024) | Statista |
| Plant-based segment share | 14% | Mordor Intelligence |
| Plant-based protein bar market | $6.2B x 0.14 = **$868M** | Calculated |
| Premium tier (price point > $3.50/bar) | 25% of segment | Estimated from retail shelf analysis |
| **SAM** | $868M x 0.25 = **$217M** | Calculated |

### Bottom-Up Approach

| Step | Value | Source |
|------|-------|--------|
| U.S. millennials + Gen Z (ages 18-42) | ~140M | Census Bureau |
| % identifying as health-conscious | 38% | Mintel consumer survey |
| % who buy protein bars monthly | 22% | Nielsen panel data |
| % who prefer plant-based options | 18% | Food Industry Association |
| Target consumers | 140M x 0.38 x 0.22 x 0.18 = **2.1M** | Calculated |
| Average annual spend on protein bars per buyer | $156/year ($13/month) | Nielsen |
| Premium price uplift | 1.3x | Estimated |
| **SAM (bottom-up)** | 2.1M x $156 x 1.3 = **$426M** | Calculated |
| Realistic capture rate (Year 3) | 0.5-1.5% | D2C benchmark |
| **SOM** | $426M x 0.01 = **$4.3M** | Calculated (using 1% midpoint) |

### Triangulation

- Top-down SAM: $217M
- Bottom-up SAM: $426M
- Delta: 96%

**Diagnosis:** The bottom-up estimate is higher because it captures total potential spend from the target demographic, including those currently buying non-plant-based premium bars who could switch. The top-down reflects current market structure. Use the top-down for conservative planning and bottom-up for upside scenario.

---

## 3. Platform / Marketplace Market Sizing — Worked Example

**Scenario:** A freelancer marketplace connecting independent graphic designers with small businesses needing design work, operating in the U.S.

### Key Distinction for Marketplaces

Marketplaces have two sides. Size the transaction volume (GMV) first, then apply the platform take rate to get revenue.

| Step | Value | Source |
|------|-------|--------|
| U.S. freelance graphic design spending | $15.8B (2024) | IBISWorld + Upwork data |
| % conducted through online platforms | 35% | Staffing Industry Analysts |
| Online freelance design market | $15.8B x 0.35 = **$5.53B** | Calculated |
| Small business segment (< 50 employees) | 60% of online volume | Estimated |
| **Addressable GMV** | $5.53B x 0.60 = **$3.32B** | Calculated |
| Platform take rate | 15% | Benchmark (Upwork 10-20%, Fiverr 20%) |
| **SAM (platform revenue)** | $3.32B x 0.15 = **$498M** | Calculated |
| Realistic GMV capture (Year 3) | 0.3% | Marketplace benchmark |
| **SOM (GMV)** | $3.32B x 0.003 = **$9.96M GMV** | Calculated |
| **SOM (Revenue)** | $9.96M x 0.15 = **$1.49M** | Calculated |

Always present marketplace sizing with both GMV and revenue clearly labeled. Investors and executives often confuse the two.

---

## 4. Sensitivity Analysis Template

Sensitivity analysis shows how your market size estimate changes when key assumptions vary. Always present low, base, and high scenarios.

### Structure

Identify the 3-4 assumptions with the highest uncertainty and vary each by a reasonable range.

**Example (using the B2B SaaS case above):**

| Assumption | Low | Base | High | Basis for Range |
|-----------|-----|------|------|-----------------|
| Target companies (count) | 35,000 | 42,000 | 50,000 | Census data +/- methodology variance |
| % managing 500+ contracts | 25% | 35% | 45% | Survey confidence interval |
| ACV | $14,000 | $18,000 | $24,000 | Competitor pricing range |
| Penetration rate (5-yr) | 2% | 3% | 5% | B2B SaaS benchmarks |

**Scenario Outputs:**

| Scenario | SAM | SOM |
|----------|-----|-----|
| **Low** | 35,000 x 0.25 x $14,000 = $122.5M | $122.5M x 0.02 = $2.5M |
| **Base** | 42,000 x 0.35 x $18,000 = $264.6M | $264.6M x 0.03 = $7.9M |
| **High** | 50,000 x 0.45 x $24,000 = $540.0M | $540.0M x 0.05 = $27.0M |

**Interpretation:** The SOM ranges from $2.5M to $27.0M, with a base case of $7.9M. The widest driver of variance is the penetration rate assumption. The recommendation is to invest in validating penetration rate through pilot data before committing to a full launch.

### Tornado Chart Guidance

To build a tornado chart, vary one assumption at a time (holding others at base) and plot the impact on the output metric. This identifies which single assumption moves the needle the most, guiding where to invest research effort.

---

## 5. Common Market Sizing Mistakes

| Mistake | Why It Happens | How to Avoid It |
|---------|---------------|-----------------|
| **Confusing TAM with SAM** | Desire to impress with big numbers | Always filter TAM by geography, segment, and channel to get SAM |
| **Double-counting** | Including overlapping customer segments or revenue streams | Map customer segments mutually exclusively; track what each dollar represents |
| **Stale data** | Using market reports that are 3+ years old | Always note the year of every data point; adjust for growth if needed |
| **Ignoring substitutes** | Only counting direct competitors | Include alternative solutions (manual processes, adjacent tools, DIY) |
| **Assuming 100% conversion** | Not applying realistic penetration rates | Use industry benchmarks: B2B SaaS typically captures 1-5% of SAM in first 3-5 years |
| **Mixing GMV and revenue** | Common in marketplace models | Always label clearly; investors will catch this |
| **Precision bias** | Presenting $347.2M when the range is $200-500M | Round appropriately; show ranges; communicate confidence level |
| **No triangulation** | Using only top-down or only bottom-up | Always run both approaches and reconcile; if you only have one, flag the risk |

---

## 6. Client Presentation Template — Market Sizing One-Pager

### Recommended Layout

**Header:** Market title, date, and confidence rating (High / Medium / Low)

**Section 1 — The Numbers (top third of page)**
- Three concentric circles or nested bars showing TAM / SAM / SOM
- Each labeled with dollar value and brief descriptor
- Growth rate (CAGR) noted next to each

**Section 2 — Key Assumptions (middle third)**
- Table with 4-6 critical assumptions
- Each row: Assumption name | Value used | Source | Confidence (H/M/L)
- Highlight the 1-2 assumptions with lowest confidence in a different color

**Section 3 — Sensitivity & Implications (bottom third)**
- Low / Base / High range for SOM (the number the client cares about most)
- One-sentence implication: "At the base case, this market supports a $X ARR business within Y years"
- One-sentence risk: "The biggest uncertainty is [assumption]; we recommend [validation step]"

### Formatting Rules
- No more than 30 words per bullet point
- Every number must have a source citation (even if it is "estimated" or "calculated")
- Use consistent units ($M or $B, not mixed)
- Include a date stamp — market sizes are perishable
