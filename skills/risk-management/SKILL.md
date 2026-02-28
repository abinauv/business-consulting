---
name: risk-management
description: "Design enterprise risk management frameworks, build risk registers, quantify risks, run Monte Carlo simulations, and develop mitigation strategies. Use this skill when the user mentions: risk management, risk assessment, risk register, risk matrix, risk appetite, risk tolerance, ERM, COSO, ISO 31000, Monte Carlo, risk quantification, risk heat map, business continuity, BCP, crisis management, stress testing, scenario analysis, key risk indicators, KRI, risk mitigation, compliance risk, operational risk, strategic risk, reputational risk, VaR, value at risk, risk scoring, bow-tie analysis, reverse stress test, or risk reporting."
user-invokable: true
argument-hint: "[company, industry, or specific risk domain to assess]"
---

# Enterprise Risk Management

You are a risk management specialist. Apply the following methodologies to design robust risk frameworks, quantify exposures, and build actionable mitigation plans.

## Enterprise Risk Management (ERM) Framework Design

### Framework Selection

**COSO ERM Framework (2017):**
Five interrelated components for integrating risk with strategy and performance:
1. **Governance & Culture** — Board risk oversight, operating structures, commitment to integrity, talent accountability
2. **Strategy & Objective-Setting** — Analyze business context, define risk appetite, evaluate alternative strategies, formulate business objectives
3. **Performance** — Identify risks to objectives, assess severity, prioritize risks, implement responses, develop portfolio view
4. **Review & Revision** — Assess substantial change, review risk and performance, pursue improvement
5. **Information, Communication & Reporting** — Leverage information systems, communicate risk information, report on risk/culture/performance

**ISO 31000:2018 Framework:**
Principles-based approach applicable to any organization:
- **Principles:** Integrated, structured, customized, inclusive, dynamic, best available information, human/cultural factors, continual improvement
- **Framework:** Leadership commitment, integration, design, implementation, evaluation, improvement
- **Process:** Scope/context/criteria, risk assessment (identify, analyze, evaluate), risk treatment, monitoring/review, recording/reporting, communication/consultation

### Framework Selection Decision Tree

```
Is the organization publicly traded or heavily regulated?
├── YES → COSO ERM (aligns with SEC/SOX expectations, board governance)
│   └── Is the organization a financial institution?
│       ├── YES → COSO ERM + Basel III/IV operational risk overlays
│       └── NO → COSO ERM standard implementation
└── NO → ISO 31000 (more flexible, principle-based)
    └── Is the organization operating internationally?
        ├── YES → ISO 31000 (internationally recognized standard)
        └── NO → ISO 31000 or simplified ERM tailored to size
```

### ERM Maturity Assessment

Rate the organization on each dimension (1 = Ad Hoc, 5 = Optimized):

| Dimension | 1 - Ad Hoc | 2 - Initial | 3 - Defined | 4 - Managed | 5 - Optimized |
|---|---|---|---|---|---|
| **Governance** | No formal oversight | Risk discussed informally | Risk committee exists | Board reviews quarterly | Risk integrated into strategy |
| **Risk Identification** | Reactive only | Annual brainstorming | Structured process | Continuous scanning | Predictive analytics |
| **Risk Assessment** | Qualitative only | Basic scoring | Calibrated scales | Quantitative modeling | Monte Carlo / VaR |
| **Risk Response** | Fire-fighting | Basic controls | Defined strategies | Optimized portfolio | Dynamic hedging |
| **Monitoring** | None | Periodic reviews | KRIs defined | Real-time dashboards | Automated alerts |
| **Culture** | Risk-unaware | Risk-averse/siloed | Risk-aware | Risk-informed decisions | Risk-intelligent |
| **Reporting** | None | Ad hoc reports | Standardized reports | Integrated dashboards | Predictive reporting |

**Maturity Scoring:**
- 7-14: **Initial** — Foundational work needed, start with governance and basic identification
- 15-21: **Developing** — Build structured processes and calibrated assessment
- 22-28: **Established** — Advance to quantitative methods and integrated reporting
- 29-35: **Leading** — Optimize with predictive analytics and dynamic risk management

## Risk Identification and Categorization

### Risk Category Taxonomy

**1. Strategic Risks** — Threats to achieving long-term objectives
- Market disruption and technology shifts
- Competitive dynamics (new entrants, substitutes, consolidation)
- M&A execution and integration risk
- Geographic/market expansion risk
- Business model obsolescence
- Strategic misalignment between units

**2. Operational Risks** — Failures in people, processes, systems, or external events
- Supply chain disruption (single-source dependency, logistics failure)
- Quality failures and product defects
- IT system outages and infrastructure failure
- Process breakdowns and human error
- Talent/key person dependency
- Health and safety incidents
- Fraud and internal misconduct

**3. Financial Risks** — Exposure to financial loss
- Credit risk (customer default, counterparty failure)
- Liquidity risk (cash flow timing, access to capital)
- Market risk (interest rates, currency, commodity prices)
- Revenue concentration (customer, product, geography)
- Capital structure and leverage risk
- Financial reporting and accounting errors

**4. Compliance Risks** — Violations of laws, regulations, or internal policies
- Regulatory change and new legislation
- Data privacy (GDPR, CCPA, sector-specific)
- Anti-corruption / anti-bribery (FCPA, UK Bribery Act)
- Environmental regulations and ESG mandates
- Industry-specific compliance (healthcare, finance, energy)
- Contractual and licensing obligations

**5. Reputational Risks** — Damage to brand, stakeholder trust, or social license
- Product safety incidents and recalls
- Data breaches and customer data exposure
- Social media crises and viral negative coverage
- Executive misconduct or ethical failures
- Environmental or social responsibility failures
- Customer experience failures at scale

**6. Technology Risks** — Cyber, digital, and emerging technology threats
- Cybersecurity breaches (ransomware, data exfiltration, DDoS)
- Legacy system failure and technical debt
- AI/ML model risk and algorithmic bias
- Cloud provider outages and vendor lock-in
- Intellectual property theft
- Digital transformation execution failure

**7. External/Macro Risks** — Forces beyond organizational control
- Geopolitical instability and trade restrictions
- Pandemic and public health emergencies
- Natural disasters and climate-related events
- Economic recession and market downturns
- Social unrest and political instability
- Infrastructure failure (power grid, telecom, transportation)

### Risk Identification Methods

Use multiple techniques to ensure comprehensive coverage:

1. **Structured brainstorming workshops** — Cross-functional teams, PESTLE prompts (Political, Economic, Social, Technological, Legal, Environmental)
2. **Process mapping and failure mode analysis** — Walk through key processes and identify failure points
3. **Historical loss analysis** — Review past incidents, near-misses, insurance claims, audit findings
4. **Industry benchmarking** — Study peer company 10-K risk factors, industry loss databases
5. **Scenario analysis** — "What if" exercises for extreme but plausible events
6. **Key stakeholder interviews** — Board members, executives, front-line managers, customers, suppliers
7. **Emerging risk scanning** — Horizon scanning for new/evolving threats (technology, regulation, geopolitics)

## Risk Quantification

### Probability x Impact Scoring

**Probability Scale (calibrated):**

| Level | Label | Probability Range | Calibration Guidance |
|---|---|---|---|
| 1 | Rare | <5% in next 12 months | Has never occurred; would be unprecedented |
| 2 | Unlikely | 5-20% | Has occurred once in past 10 years in industry |
| 3 | Possible | 20-50% | Has occurred multiple times in industry; could happen |
| 4 | Likely | 50-80% | Has occurred at this organization or frequently in industry |
| 5 | Almost Certain | >80% | Expected to occur; has occurred multiple times recently |

**Impact Scale (multi-dimensional):**

| Level | Financial Impact | Operational Impact | Reputational Impact | Safety Impact |
|---|---|---|---|---|
| 1 - Insignificant | <$100K or <0.1% revenue | Minor process disruption, <4 hours | Internal awareness only | First aid only |
| 2 - Minor | $100K-$1M or 0.1-1% revenue | Operational disruption, <1 day | Local media coverage | Medical treatment |
| 3 - Moderate | $1M-$10M or 1-5% revenue | Significant disruption, 1-7 days | National media, social media attention | Serious injury |
| 4 - Major | $10M-$50M or 5-15% revenue | Major disruption, 1-4 weeks | Sustained negative coverage, customer loss | Life-changing injury |
| 5 - Catastrophic | >$50M or >15% revenue | Extended shutdown, >1 month | Existential brand damage, regulatory action | Fatality |

*Note: Calibrate financial thresholds to the organization's revenue and margin profile. The ranges above suit a mid-market company ($100M-$1B revenue).*

### Expected Loss Modeling

```
Expected Loss = Probability × Financial Impact (midpoint)

Example:
- Risk: Key supplier failure
- Probability: 30% (Level 3)
- Financial Impact: $5M (Level 3 midpoint)
- Expected Loss: 0.30 × $5,000,000 = $1,500,000

Annualized Loss Expectancy (ALE):
ALE = Annual Rate of Occurrence (ARO) × Single Loss Expectancy (SLE)
- ARO: 0.3 events/year
- SLE: $5,000,000
- ALE: $1,500,000
```

### Value at Risk (VaR) Concepts — Simplified

VaR answers: "What is the maximum loss we would expect over a given time period at a specified confidence level?"

- **95% VaR of $10M over 1 year** means: "We are 95% confident our losses will not exceed $10M in the next year."
- In other words, there is a 5% chance losses could be worse than $10M.
- **Limitations:** VaR does not tell you how bad things could get beyond the threshold (use Conditional VaR / Expected Shortfall for that).

For non-financial contexts, express VaR conceptually:
- "In 19 out of 20 years, our total risk losses should be below $X."
- "In the worst 1-in-20 year, we could lose more than $X."

## Risk Appetite and Tolerance

### Definitions

- **Risk Appetite:** The broad level of risk an organization is willing to accept in pursuit of its strategic objectives. Set by the Board. Expressed qualitatively and quantitatively.
- **Risk Tolerance:** The specific, measurable boundaries around individual risk categories or metrics. Operational limits within the appetite.
- **Risk Capacity:** The maximum level of risk the organization can absorb before viability is threatened.

### Risk Appetite Statement Template

```
[Organization Name] Risk Appetite Statement

Overall Appetite: [Organization] accepts [moderate/conservative/aggressive] levels of
risk in pursuit of [strategic objectives]. We will not accept risks that could
[threaten solvency / cause regulatory sanctions / endanger safety / damage brand
beyond recovery].

By Category:
- Strategic Risk: [Appetite level] — We [will/will not] pursue [types of strategic bets]
- Operational Risk: [Appetite level] — We accept up to [X days] of disruption
  with financial impact not exceeding [$Y]
- Financial Risk: [Appetite level] — Maximum acceptable earnings volatility of
  [X%]; minimum liquidity ratio of [Y]
- Compliance Risk: ZERO TOLERANCE for willful regulatory violations
- Reputational Risk: [Appetite level] — We will not accept risks that could
  result in [specific reputational thresholds]
- Technology/Cyber Risk: [Appetite level] — Maximum acceptable downtime of
  [X hours]; zero tolerance for customer data breaches

Approved by: [Board of Directors]
Date: [Date]
Review Frequency: [Annual / Semi-annual]
```

### Tolerance Threshold Examples

| Risk Category | Green (Within Appetite) | Amber (Approaching Limit) | Red (Exceeds Tolerance) |
|---|---|---|---|
| Financial Loss (single event) | <$1M | $1M-$5M | >$5M |
| Revenue Concentration | Top customer <15% | Top customer 15-25% | Top customer >25% |
| System Downtime | <4 hours/quarter | 4-24 hours/quarter | >24 hours/quarter |
| Safety Incidents | 0 lost-time injuries | 1-2 lost-time injuries/year | >2 or any fatality |
| Compliance Violations | 0 material findings | 1-2 minor findings | Any material finding |
| Employee Turnover | <15% annual | 15-25% annual | >25% annual |

## Risk Register Construction

### Required Fields

Every risk register entry should contain:

| Field | Description |
|---|---|
| Risk ID | Unique identifier (e.g., STR-001, OPS-015) |
| Category | Strategic / Operational / Financial / Compliance / Reputational / Technology / External |
| Risk Description | Clear, specific statement: "Risk that [event] occurs, causing [consequence]" |
| Risk Owner | Named individual accountable for managing the risk |
| Inherent Probability | Score before controls (1-5) |
| Inherent Impact | Score before controls (1-5) |
| Inherent Risk Score | Probability x Impact (1-25) |
| Existing Controls | Current mitigation measures in place |
| Control Effectiveness | Effective / Partially Effective / Ineffective |
| Residual Probability | Score after controls (1-5) |
| Residual Impact | Score after controls (1-5) |
| Residual Risk Score | Probability x Impact (1-25) |
| Risk Response | Accept / Avoid / Transfer / Mitigate |
| Action Plan | Specific actions to further reduce risk |
| Target Risk Score | Desired residual risk level |
| Status | Open / In Progress / Monitoring / Closed |
| Last Review Date | Date of most recent review |
| Next Review Date | Scheduled review date |

### Risk Heat Map (5x5 Matrix)

```
Impact →        1-Insignif.  2-Minor    3-Moderate   4-Major    5-Catastrophic
Probability ↓
5-Almost Certain   [5-MED]    [10-HIGH]  [15-CRIT]   [20-CRIT]   [25-CRIT]
4-Likely           [4-MED]    [8-HIGH]   [12-HIGH]   [16-CRIT]   [20-CRIT]
3-Possible         [3-LOW]    [6-MED]    [9-HIGH]    [12-HIGH]   [15-CRIT]
2-Unlikely         [2-LOW]    [4-MED]    [6-MED]     [8-HIGH]    [10-HIGH]
1-Rare             [1-LOW]    [2-LOW]    [3-LOW]     [4-MED]     [5-MED]

Zone Definitions:
- CRITICAL (15-25): Immediate executive attention, mandatory mitigation plan within 30 days
- HIGH (8-14): Senior management attention, mitigation plan within 60 days
- MEDIUM (4-7): Management monitoring, review quarterly
- LOW (1-3): Accept and monitor, review annually
```

## Risk Mitigation Strategy — Decision Framework

### The 4T Framework

```
Is the risk within our risk appetite?
├── YES → ACCEPT (Tolerate)
│   └── Document acceptance rationale
│   └── Monitor for changes in probability/impact
│   └── Set trigger points for reassessment
│
└── NO → Can we eliminate the risk source entirely?
    ├── YES → AVOID (Terminate)
    │   └── Exit the activity, market, or product line
    │   └── Cost-benefit: Is avoidance worth the opportunity cost?
    │
    └── NO → Can a third party bear the risk more efficiently?
        ├── YES → TRANSFER
        │   └── Insurance (property, liability, cyber, D&O)
        │   └── Contractual transfer (indemnification, limitation of liability)
        │   └── Outsourcing (but retain oversight and residual risk)
        │   └── Hedging (financial instruments for market risk)
        │
        └── NO → MITIGATE (Treat)
            └── Preventive controls (reduce probability)
            │   └── Training, process redesign, automation, redundancy
            └── Detective controls (identify occurrence quickly)
            │   └── Monitoring, alerts, audits, inspections
            └── Corrective controls (reduce impact when it occurs)
                └── Incident response plans, backup systems, crisis comms
```

### Mitigation Cost-Benefit Analysis

```
Should we invest in this mitigation?

Mitigation Value = (Expected Loss Before - Expected Loss After) - Cost of Mitigation

Example:
- Current Expected Loss: $1,500,000/year (30% × $5M)
- After Mitigation: $300,000/year (10% × $3M)
- Annual Risk Reduction: $1,200,000
- Cost of Mitigation: $400,000/year
- Net Value: $800,000/year → INVEST

Rule of thumb: Invest if mitigation cost < 50% of expected loss reduction
(accounts for uncertainty in estimates)
```

## Scenario-Based Risk Assessment

### Stress Testing Process

1. **Select scenarios** — Choose 3-5 extreme but plausible scenarios relevant to the organization
2. **Define parameters** — Specify severity, duration, and scope for each scenario
3. **Model impact** — Quantify financial, operational, and strategic impact
4. **Test resilience** — Assess whether the organization can survive (capital, liquidity, operations)
5. **Identify gaps** — Document where current controls and resources are insufficient
6. **Develop responses** — Create contingency plans for each scenario

**Standard Stress Scenarios:**
- Major customer loss (top 3 customers leave within 6 months)
- Key supplier failure (primary supplier ceases operations)
- Cybersecurity breach (customer data exfiltrated, 30-day remediation)
- Economic recession (revenue drops 20-30%, credit tightens)
- Regulatory change (major new compliance requirement, 12-month implementation)
- Key person departure (CEO or critical technical leader leaves suddenly)
- Natural disaster (primary facility destroyed, 90-day recovery)
- Pandemic (50% workforce unavailable for 3 months)

### Reverse Stress Testing

Work backward from failure: "What combination of events would cause the organization to fail?"

Steps:
1. Define "failure" (insolvency, regulatory shutdown, permanent brand destruction)
2. Brainstorm event combinations that could cause failure
3. Assess plausibility of each combination
4. Identify the most plausible paths to failure
5. Build early warning indicators for those paths
6. Design preventive actions to block the most plausible failure paths

## Regulatory Compliance Assessment

### Compliance Risk Assessment Process

1. **Regulatory inventory** — List all applicable laws, regulations, standards, and contractual obligations
2. **Obligation mapping** — Map each regulation to specific organizational processes and functions
3. **Gap analysis** — Assess current compliance status against each obligation
4. **Risk scoring** — Rate likelihood and impact of non-compliance for each obligation
5. **Remediation planning** — Prioritize and plan actions to close gaps
6. **Monitoring design** — Establish ongoing compliance monitoring and testing

### Common Regulatory Domains

| Domain | Key Regulations | Risk if Non-Compliant |
|---|---|---|
| Data Privacy | GDPR, CCPA, HIPAA | Fines up to 4% global revenue, lawsuits, reputation |
| Financial | SOX, Basel III, Dodd-Frank | Fines, restatements, license revocation |
| Anti-Corruption | FCPA, UK Bribery Act | Criminal liability, massive fines, debarment |
| Environmental | EPA, EU Green Deal, ESG | Fines, remediation costs, operating restrictions |
| Employment | FLSA, EEOC, OSHA | Lawsuits, fines, operational disruption |
| Industry-Specific | FDA, FCC, FINRA, PCI-DSS | License revocation, product recalls, fines |

## Business Continuity Planning (BCP)

### BCP Development Process

**Phase 1: Business Impact Analysis (BIA)**
- Identify critical business functions and processes
- Determine Maximum Tolerable Downtime (MTD) for each function
- Establish Recovery Time Objectives (RTO) and Recovery Point Objectives (RPO)
- Quantify financial and operational impact of disruption over time

**Phase 2: Strategy Development**
- Identify recovery strategies for each critical function
- Resource requirements (people, technology, facilities, data, suppliers)
- Alternative operating procedures (manual workarounds, alternate sites)
- Third-party dependencies and backup arrangements

**Phase 3: Plan Documentation**
- Emergency response procedures (first 0-4 hours)
- Crisis management protocols (4-72 hours)
- Business recovery procedures (72 hours to full recovery)
- Communication plans (internal, external, regulatory, media)
- Roles and responsibilities (incident commander, crisis team, functional leads)

**Phase 4: Testing and Maintenance**
- Tabletop exercises (quarterly)
- Functional tests of specific recovery procedures (semi-annually)
- Full-scale simulation (annually)
- Plan updates after every test and after significant organizational changes

### Crisis Management Communication Template

```
INITIAL CRISIS COMMUNICATION (within 2 hours of incident)

To: [Stakeholder group]
From: [Authorized spokesperson]
Date/Time: [Timestamp]

What happened: [Brief factual description — confirmed facts only]
What we are doing: [Immediate actions taken]
What we know: [Confirmed information]
What we don't know yet: [Acknowledge gaps honestly]
Next update: [Specific time for next communication]
Contact: [Point of contact for questions]

Key principles:
- Be first (own the narrative)
- Be factual (no speculation)
- Be empathetic (acknowledge impact on affected parties)
- Be actionable (tell people what to do)
```

## Worked Example: Mid-Market Manufacturing Company Risk Assessment

**Company Profile:** $250M revenue manufacturer, 800 employees, 3 facilities, sells to automotive and industrial customers.

### Top 5 Risks Identified

| Risk ID | Risk | Prob | Impact | Score | Response |
|---|---|---|---|---|---|
| STR-001 | EV transition reduces demand for legacy auto components | 4 | 5 | 20-CRIT | Mitigate: Invest in EV component R&D, diversify customer base |
| OPS-003 | Single-source supplier for critical raw material fails | 3 | 4 | 12-HIGH | Mitigate: Qualify second supplier, build 90-day safety stock |
| FIN-002 | Top 3 customers represent 55% of revenue | 4 | 4 | 16-CRIT | Mitigate: Accelerate new customer acquisition, cap single customer at 20% |
| TEC-001 | Ransomware attack on OT systems shuts production | 3 | 5 | 15-CRIT | Mitigate: OT/IT segmentation, offline backups, incident response plan |
| COM-004 | New EPA emissions standards require $15M facility upgrade | 4 | 3 | 12-HIGH | Mitigate: Phase investment over 3 years, apply for green financing |

### Risk Response Plan for STR-001 (EV Transition)

```
Risk: EV transition reduces demand for legacy automotive components
Current State: 40% of revenue from internal combustion engine (ICE) components
Risk Score: 20 (Critical)
Risk Owner: Chief Strategy Officer

Mitigation Actions:
1. Invest $10M over 3 years in EV component R&D (battery housings, power electronics)
2. Hire EV engineering team (5 engineers by Q2)
3. Target 3 EV OEM qualification programs by year-end
4. Reduce ICE revenue dependency to <25% within 5 years
5. Monitor ICE-to-EV transition pace quarterly (leading indicators: EV sales %, OEM announcements)

Key Risk Indicators:
- ICE component order backlog (trigger: <6 months vs. target >12 months)
- EV revenue as % of total (target: >15% by Year 3)
- OEM customer EV transition announcements (track quarterly)

Residual Risk Score (after mitigation): 3 × 4 = 12 (High, but managed)
Target Risk Score (Year 3): 2 × 3 = 6 (Medium)
```

## Reference Materials

For detailed guidance, refer to:
- `references/risk-quantification-guide.md` — Probability estimation, impact scales, VaR, KRI design
- `references/risk-register-templates.md` — Complete register templates, taxonomy, reporting formats, worked examples
- `references/monte-carlo-guide.md` — Simulation setup, Python code, interpretation, executive communication
