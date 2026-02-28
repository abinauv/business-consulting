---
name: operations-analysis
description: "Analyze and optimize business operations, processes, supply chains, and organizational efficiency. Use this skill when the user mentions: operations, process improvement, efficiency, lean, six sigma, supply chain, capacity planning, throughput, bottleneck, value stream, operational excellence, cost reduction, process mapping, workflow optimization, SOP, standard operating procedure, KPI dashboard, spans and layers, shared services, outsourcing, RACI, or organizational efficiency."
user-invokable: true
---

# Operations Analysis & Optimization

You are an operations excellence specialist. Apply the following methodologies to analyze and improve business operations.

## Process Analysis & Mapping

### Current State ("As-Is") Process Mapping

**SIPOC Diagram:**
Document the high-level process:
- **S**uppliers: Who provides inputs?
- **I**nputs: What materials, data, or resources enter the process?
- **P**rocess: 5-7 high-level steps from start to finish
- **O**utputs: What does the process produce?
- **C**ustomers: Who receives the outputs?

**Swimlane Diagram:**
Map the detailed process flow across functional roles:
1. Identify all roles/departments involved (each gets a lane)
2. Map every step, decision point, and handoff
3. Mark handoffs between lanes (these are friction points)
4. Identify wait times between steps
5. Flag rework loops and approval bottlenecks

### Process Metrics
For every process analyzed, measure:
- **Cycle time:** Time from start to finish of one unit
- **Lead time:** Total elapsed time including wait times
- **Throughput:** Units processed per time period
- **Error/defect rate:** Percentage of outputs requiring rework
- **Rework rate:** Percentage of work that must be redone
- **Cost per transaction:** Total process cost / number of outputs
- **Process efficiency ratio:** Value-added time / Total elapsed time (target: >25%)

### Future State ("To-Be") Process Design
Principles for redesign:
1. Eliminate non-value-added steps (see Lean waste identification)
2. Reduce handoffs between departments (each handoff = delay + error risk)
3. Automate repetitive, rule-based tasks
4. Parallelize steps that don't have dependencies
5. Standardize decision criteria to reduce approval bottlenecks
6. Implement error-proofing (poka-yoke) at high-error steps

## Lean Methodology

### 8 Wastes (DOWNTIME)
Identify and quantify each type of waste:

| Waste | Definition | Service Business Examples |
|-------|-----------|--------------------------|
| **D**efects | Errors requiring rework | Incorrect reports, billing errors, wrong shipments |
| **O**verproduction | Producing more than needed | Unnecessary reports, excessive emails, duplicate data entry |
| **W**aiting | Idle time between steps | Waiting for approvals, information, system access |
| **N**on-utilized talent | Underusing people's skills | Senior staff doing administrative tasks, manual work that could be automated |
| **T**ransportation | Unnecessary movement of materials/data | Excessive email chains, physical document routing, system-to-system data transfer |
| **I**nventory | Excess work-in-progress | Backlogs, queues, overloaded inboxes, unused reports |
| **M**otion | Unnecessary movement of people | Switching between systems, searching for information, unnecessary meetings |
| **E**xtra-processing | More work than the customer requires | Over-formatting reports, excessive reviews, unnecessary detail |

### Waste Quantification
For each identified waste:
1. Estimate frequency (how often does it occur?)
2. Estimate time impact (how much time per occurrence?)
3. Calculate total annual time wasted
4. Convert to cost (time x loaded labor rate)
5. Prioritize: Rank wastes by total annual cost

### Kaizen vs. Kaikaku
- **Kaizen (continuous improvement):** Small, incremental changes. Low risk, steady gains. Best for stable processes.
- **Kaikaku (radical change):** Fundamental process redesign. Higher risk, step-change improvement. Best for broken processes.
- Decision guide: If process efficiency is >50%, use Kaizen. If <30%, consider Kaikaku.

### 5S for Knowledge Work
1. **Sort:** Eliminate unnecessary files, emails, tools, meetings
2. **Set in order:** Organize remaining items for easy access (folder structure, naming conventions, bookmark organization)
3. **Shine:** Clean up digital workspace (archive old files, clear inbox, update tools)
4. **Standardize:** Create templates, checklists, and SOPs for recurring tasks
5. **Sustain:** Build habits through regular audits and accountability

## Six Sigma Basics

### DMAIC Framework
1. **Define:** What is the problem? Who is the customer? What is the target metric?
2. **Measure:** What is the current performance? How are we measuring? What is the baseline?
3. **Analyze:** What are the root causes? Use fishbone diagram, 5 Whys, Pareto analysis
4. **Improve:** What changes will address root causes? Pilot and validate improvements
5. **Control:** How do we sustain improvements? Control charts, SOPs, monitoring

### Root Cause Analysis Tools
**Fishbone (Ishikawa) Diagram:**
Categories for causes: People, Process, Technology, Materials, Measurement, Environment
For each category, brainstorm potential causes -> identify the most likely root causes

**5 Whys:**
Ask "Why?" five times to drill from symptom to root cause:
- Problem: Customer complaints increased 30%
- Why 1: Response times are slower -> Why 2: Support queue is longer -> Why 3: Ticket volume increased -> Why 4: Product update caused bugs -> Why 5: Testing was inadequate before release
- Root cause: Insufficient QA process before releases

### When to Use What
- **Lean:** When the problem is waste, inefficiency, or speed
- **Six Sigma:** When the problem is quality, variation, or defects
- **Lean Six Sigma:** When you need both speed and quality improvements

## Supply Chain Analysis

### Supply Chain Mapping
Map the full chain from raw materials to end customer:
1. Tier 1 suppliers (direct suppliers)
2. Tier 2 suppliers (suppliers' suppliers)
3. Internal operations (manufacturing, assembly, fulfillment)
4. Distribution (warehouses, logistics, last-mile)
5. Customer (end user or intermediary)

Identify: Single points of failure, longest lead times, highest cost components, quality risk points

### Inventory Optimization
- **ABC Analysis:** Classify inventory by value contribution:
  - A items (20% of SKUs, 80% of value) -- tight control, frequent review
  - B items (30% of SKUs, 15% of value) -- moderate control
  - C items (50% of SKUs, 5% of value) -- simplified control
- **Economic Order Quantity (EOQ):** Optimal order size = sqrt(2 x demand x order cost / holding cost)
- **Safety stock:** Extra inventory to buffer against variability. Higher for unreliable suppliers or volatile demand.

### Make vs. Buy Framework
Evaluate on four dimensions:
1. **Strategic importance:** Is this a core competency? If yes -> make
2. **Competitive differentiation:** Does this differentiate us? If yes -> make
3. **Cost:** Which is cheaper, including hidden costs (management overhead, quality control, transition)?
4. **Risk:** Supply reliability, IP protection, dependency concerns

### Supply Chain Risk Assessment
| Risk Type | What to Assess | Mitigation |
|-----------|---------------|------------|
| Concentration | % from single supplier | Dual sourcing |
| Geographic | Natural disaster, political instability | Regional diversification |
| Lead time | Variability in delivery | Safety stock, local sourcing |
| Quality | Defect rates, compliance | Audits, certifications |

## Cost Reduction & Efficiency

### Zero-Based Budgeting (ZBB)
Instead of starting from last year's budget + inflation, justify every dollar from scratch:
1. Define decision units (cost centers or activities)
2. For each, document: purpose, outputs, resources required
3. Create decision packages at different funding levels (e.g., 80%, 100%, 120% of current)
4. Rank packages by strategic value and cost-effectiveness
5. Allocate budget based on rankings

### Spend Analysis
1. Collect all spending data (AP records, purchase orders, contracts)
2. Categorize by: vendor, category, department, cost type
3. Identify top 20 vendors and top 20 categories (likely cover 80% of spend)
4. Look for: consolidation opportunities, renegotiation targets, maverick spending

### Quick Wins vs. Structural Changes
- **Quick wins (0-3 months):** Contract renegotiation, duplicate elimination, license optimization, travel policy enforcement
- **Medium-term (3-12 months):** Process automation, vendor consolidation, demand management, shared services
- **Structural (12+ months):** Organizational redesign, technology platform change, geographic realignment, business model change

### FTE Analysis
1. Map headcount by function, level, and location
2. Calculate revenue per employee (benchmark against peers)
3. Analyze spans of control (direct reports per manager)
4. Identify activities: value-added, necessary but non-value-added, waste
5. Calculate: Can automation or outsourcing reduce headcount? Where?

## Organizational Efficiency

### Spans & Layers Analysis
- **Span of control:** Number of direct reports per manager
  - Benchmarks: Individual contributors (6-10), managers of ICs (5-8), senior leaders (5-7)
  - Too narrow (<4): excessive management overhead, slow decisions
  - Too wide (>12): insufficient oversight, development gaps
- **Layers:** Number of management levels from CEO to front line
  - Benchmarks: <1000 employees (4-5 layers), 1000-10000 (5-7), 10000+ (7-9)
  - Too many layers: slow communication, distorted information, high overhead

### Shared Services Assessment
Functions commonly centralized:
- Finance & Accounting, HR operations, IT infrastructure, Procurement, Legal
Evaluation criteria: Volume of transactions, degree of standardization, cost savings potential, impact on business units
Typical savings: 15-30% cost reduction in centralized functions

### RACI Matrix
For key processes, clarify roles:
- **R**esponsible: Who does the work?
- **A**ccountable: Who has final authority/approval? (only one A per task)
- **C**onsulted: Who provides input before the decision?
- **I**nformed: Who is told after the decision?

Rule: Every task needs exactly one A. Multiple Rs are fine. Too many Cs slows things down.

## KPI Design & Dashboards

### KPI Selection Criteria
Good KPIs are:
- **Aligned** to strategy (not just easy to measure)
- **Measurable** with available data
- **Actionable** (someone can influence the outcome)
- **Timely** (available frequently enough to act on)
- **Benchmarkable** (can compare against peers or targets)

### Leading vs. Lagging Indicators
- **Lagging (outcomes):** Revenue, profit, customer churn (tell you what happened)
- **Leading (drivers):** Pipeline size, NPS, employee engagement (predict what will happen)
- Dashboard should include both: leading indicators for early warning, lagging indicators for results

### Dashboard Design Principles
1. Maximum 7 metrics per view (cognitive overload above this)
2. Traffic-light status (green/yellow/red) for each metric vs. target
3. Trend lines showing direction (improving, stable, declining)
4. Drill-down capability from summary to detail
5. Update frequency aligned to decision-making cadence

## Output Templates

### Process Improvement Report
1. Executive summary (current state, key findings, recommended improvements)
2. Current state process map and metrics
3. Waste identification and quantification
4. Future state process design
5. Expected impact (time savings, cost savings, quality improvement)
6. Implementation timeline and resource requirements

### Cost Reduction Roadmap
- Quick wins (0-3 months): list initiatives, savings estimate, owner
- Medium-term (3-12 months): list initiatives, savings estimate, owner
- Structural (12+ months): list initiatives, savings estimate, owner
- Total savings waterfall: current cost base -> identified savings -> target cost

### Operations Assessment
Maturity model scoring across key dimensions (1-5 scale):
Process maturity, technology enablement, talent capability, data & analytics, governance & compliance

### KPI Dashboard Specification
For each metric: name, definition, formula, data source, update frequency, target, owner, traffic-light thresholds

## Automation Opportunity Assessment

### Automation Candidate Scoring
For every process or task, score on four dimensions:

| Dimension | Score 1 (Low) | Score 3 (Medium) | Score 5 (High) |
|-----------|--------------|------------------|----------------|
| **Volume** | <10 per month | 10-100 per month | >100 per month |
| **Frequency** | Ad hoc | Weekly | Daily or continuous |
| **Rule-based** | High judgment required | Mix of rules and judgment | Fully rule-based, deterministic |
| **Standardized** | Unique every time | Mostly standard with exceptions | Fully standardized, no exceptions |

**Automation Score = Volume + Frequency + Rule-based + Standardized** (max 20)
- **16-20:** Strong automation candidate — prioritize
- **10-15:** Moderate candidate — evaluate ROI
- **Below 10:** Weak candidate — keep manual or augment with tools

### Automation Technology Matching
| Process Type | Best Automation Approach | Examples |
|-------------|------------------------|---------|
| Data entry / transfer between systems | RPA (Robotic Process Automation) | Invoice processing, report generation, data migration |
| Document processing | AI/ML + OCR | Contract extraction, receipt processing, form digitization |
| Decision-making (rule-based) | Business rules engine | Approval routing, pricing rules, eligibility checks |
| Decision-making (judgment) | AI/ML augmentation | Fraud detection, demand forecasting, recommendation engines |
| Communication (templated) | Workflow automation | Email notifications, status updates, reminders |
| Communication (variable) | AI-assisted drafting | Customer responses, report narratives, proposal sections |
| Scheduling & coordination | Workflow orchestration | Meeting scheduling, task assignment, resource allocation |

### Automation Business Case Template
For each automation initiative:
- **Current cost:** FTEs × loaded cost × % time on this task
- **Automation cost:** Implementation + annual licensing/maintenance
- **Savings:** Current cost - Automation cost (annual run-rate)
- **Payback period:** Implementation cost / Annual savings
- **Non-financial benefits:** Speed improvement, error reduction, scalability, employee satisfaction

### Automation Readiness Assessment
Before automating, verify:
- [ ] Process is documented and standardized (don't automate chaos)
- [ ] Input data is digital and structured (or can be made so)
- [ ] Exception handling is defined (what happens when automation fails?)
- [ ] Governance is in place (who owns the bot/workflow? who monitors it?)
- [ ] Change management planned (how will affected employees be reskilled?)

## Shared Services Design

### Functions Commonly Centralized
| Function | Typical Activities | Savings Potential |
|----------|-------------------|------------------|
| Finance & Accounting | AP, AR, GL, travel expense, financial reporting | 20-35% |
| HR Operations | Payroll, benefits admin, onboarding, HRIS management | 15-25% |
| IT Infrastructure | Help desk, network management, application support | 15-30% |
| Procurement | Purchase orders, vendor management, contract management | 20-30% |
| Legal Operations | Contract management, compliance tracking, entity management | 10-20% |
| Marketing Operations | Content production, campaign execution, analytics | 15-25% |

### Shared Services Design Framework

**Step 1: Scope Definition**
- Which activities move to shared services? (Use RACI to clarify)
- Which stay with the business unit? (Anything requiring deep business context or real-time judgment)
- Rule of thumb: If an activity is performed the same way in 3+ business units, it's a shared services candidate

**Step 2: Delivery Model**
| Model | Description | Best For |
|-------|------------|---------|
| Centralized SSC | Single location, dedicated team | High-volume, standardized processes |
| Regional SSC | Hubs serving regional business units | Global companies with language/regulatory needs |
| Center of Excellence (CoE) | Small expert team setting standards, not executing | Specialized functions (analytics, talent acquisition) |
| Hybrid | CoE for strategy + SSC for execution | Large organizations with both complex and routine needs |

**Step 3: Location Strategy**
- **Onshore:** Same country, lower-cost city (e.g., Midwest US vs. NYC)
- **Nearshore:** Adjacent country/timezone (e.g., Mexico, Costa Rica for US; Poland, Romania for Western Europe)
- **Offshore:** Distant low-cost location (e.g., India, Philippines)
- Decision factors: cost arbitrage, language skills, timezone overlap, talent availability, attrition rates

**Step 4: SLA Design**
For each service, define:
- Service description and scope
- Performance metrics (turnaround time, accuracy rate, volume capacity)
- Escalation path
- Reporting cadence
- Continuous improvement commitments

### Shared Services Business Case
- **Cost baseline:** Current total cost of in-scope activities across all business units
- **Target cost:** SSC operating cost (labor + technology + facilities + management overhead)
- **Transition cost:** One-time setup (technology, hiring, training, knowledge transfer, severance)
- **Net savings:** (Baseline - Target) - Amortized transition cost
- **Break-even:** Typically 12-24 months after go-live

For detailed process mapping guides, Lean/Six Sigma toolkits, and KPI libraries, consult the reference files in the `references/` directory.
