# Risk Register Templates

## Risk Register Format

### Full Risk Register Template

| Field | Description | Example |
|-------|-----------|---------|
| **Risk ID** | Unique identifier | R-001 |
| **Category** | Risk category (see taxonomy below) | Operational |
| **Sub-category** | Specific sub-category | Technology |
| **Risk Description** | Clear "if...then..." statement | "If our cloud provider experiences a multi-region outage, then our platform will be unavailable for 4–24 hours, resulting in SLA breaches and customer compensation" |
| **Risk Owner** | Person accountable | CTO |
| **Probability (1–5)** | Likelihood of occurrence | 3 |
| **Impact (1–5)** | Consequence if it occurs | 4 |
| **Inherent Risk Score** | Probability × Impact (before controls) | 12 (High) |
| **Existing Controls** | Current mitigations in place | Multi-AZ deployment, automated failover, backup provider contract |
| **Control Effectiveness** | How well controls work | Partially effective (covers single-AZ failure, not multi-region) |
| **Residual Risk Score** | Risk score after existing controls | 8 (High) |
| **Additional Mitigation Actions** | Planned actions to further reduce risk | Multi-cloud architecture, chaos engineering program |
| **Action Owner** | Person responsible for mitigation actions | VP Engineering |
| **Action Due Date** | When actions must be completed | Q2 2026 |
| **Status** | Open / In Progress / Closed / Accepted | In Progress |
| **Last Reviewed** | Date of last review | 2026-01-15 |
| **Trend** | Increasing / Stable / Decreasing | Stable |

## Risk Categorization Taxonomy

### 3-Level Hierarchy

```
STRATEGIC
├── Market risk (demand shifts, customer preferences, market disruption)
├── Competitive risk (new entrants, competitor actions, pricing pressure)
├── Portfolio risk (product lifecycle, innovation pipeline, concentration)
├── Reputation risk (brand damage, public perception, social media)
└── Geopolitical risk (trade policy, sanctions, political instability)

OPERATIONAL
├── Process risk (process failure, human error, capacity constraints)
├── Technology risk (system failure, cyber, data loss, obsolescence)
├── Supply chain risk (supplier failure, logistics, raw material, concentration)
├── People risk (key person dependency, skills gap, turnover, misconduct)
└── Physical risk (natural disaster, fire, pandemic, facility failure)

FINANCIAL
├── Credit risk (customer default, counterparty failure)
├── Liquidity risk (cash flow, access to capital, covenant breach)
├── Market risk (FX, interest rate, commodity prices)
├── Investment risk (M&A, capex, R&D returns)
└── Fraud risk (internal fraud, external fraud, misappropriation)

COMPLIANCE
├── Regulatory risk (changing regulations, enforcement actions)
├── Legal risk (litigation, intellectual property, contract disputes)
├── Data privacy risk (GDPR, CCPA, data breaches, consent)
├── Environmental risk (emissions, waste, ESG requirements)
└── Tax risk (transfer pricing, tax law changes, audit exposure)
```

## Escalation Thresholds

| Risk Score | Zone | Escalation To | Response Time | Review Cadence |
|:----------:|:----:|:---:|:---:|:---:|
| 20–25 | Critical | Board of Directors / CEO | 24 hours | Weekly |
| 15–19 | Critical | C-Suite / Executive Committee | 48 hours | Weekly |
| 10–14 | High | VP / Senior Director | 1 week | Bi-weekly |
| 6–9 | Medium | Director / Manager | 2 weeks | Monthly |
| 1–5 | Low | Risk Owner | Next review cycle | Quarterly |

## Risk Reporting Templates

### Board-Level Risk Report (1-page)

```
═══════════════════════════════════════════════════════
ENTERPRISE RISK SUMMARY — [Quarter] [Year]
═══════════════════════════════════════════════════════

RISK PROFILE OVERVIEW
 Critical: [X] risks    High: [X] risks
 Medium:   [X] risks    Low:  [X] risks
 Trend: [Improving / Stable / Deteriorating]

TOP 5 RISKS
 # | Risk | Score | Trend | Status
 1 | [Description] | [Score] | [↑↓→] | [Action status]
 2 | [Description] | [Score] | [↑↓→] | [Action status]
 3 | [Description] | [Score] | [↑↓→] | [Action status]
 4 | [Description] | [Score] | [↑↓→] | [Action status]
 5 | [Description] | [Score] | [↑↓→] | [Action status]

KEY CHANGES SINCE LAST REPORT
 • [New risks added]
 • [Risks that changed zone (e.g., High → Critical)]
 • [Risks that were closed / reduced]

RISK APPETITE COMPLIANCE
 [X of Y] risk categories within appetite
 Out of appetite: [list categories]

ACTIONS REQUIRING BOARD ATTENTION
 1. [Decision or approval needed]
 2. [Resource request]

═══════════════════════════════════════════════════════
```

### Management Risk Dashboard

| Category | Total Risks | Critical | High | Medium | Low | Trend | Key Issue |
|----------|:---:|:---:|:---:|:---:|:---:|:---:|---|
| Strategic | 8 | 1 | 2 | 3 | 2 | → | Competitor launch in Q2 |
| Operational | 12 | 0 | 3 | 5 | 4 | ↓ | Supply chain improved |
| Financial | 6 | 0 | 1 | 3 | 2 | → | FX hedging in place |
| Compliance | 5 | 0 | 1 | 2 | 2 | ↑ | New regulation pending |
| **Total** | **31** | **1** | **7** | **13** | **10** | **→** | |

### Mitigation Action Tracker

| Action ID | Risk ID | Action | Owner | Due Date | Status | % Complete |
|-----------|---------|--------|-------|----------|:------:|:----------:|
| A-001 | R-003 | Implement multi-cloud failover | VP Eng | 2026-03-31 | In Progress | 60% |
| A-002 | R-007 | Qualify second supplier | VP Ops | 2026-02-28 | Complete | 100% |
| A-003 | R-012 | GDPR compliance audit | CLO | 2026-04-15 | Not Started | 0% |

## Risk Appetite Statement Templates

### By Risk Category

| Risk Category | Appetite Level | Statement | Tolerance (Max Acceptable Loss) |
|--------------|:---:|---|:---:|
| **Strategic** | Moderate | We accept strategic risk to pursue growth, but will not risk core business viability | 10% of EBITDA |
| **Operational** | Low | We maintain high operational standards; unplanned downtime must be minimized | <4 hours/quarter |
| **Financial** | Low-Moderate | We manage financial risk prudently; we hedge material exposures | 5% of revenue |
| **Compliance** | Very Low | We have zero tolerance for compliance violations and regulatory breaches | Zero material violations |
| **Reputational** | Low | We protect our brand and act with integrity in all interactions | No sustained negative coverage |
| **Cybersecurity** | Very Low | We prioritize data security and privacy; breaches are unacceptable | Zero data breaches |

## Bow-Tie Analysis Template

Visualize causes, controls, and consequences for a single risk:

```
        PREVENTIVE CONTROLS              MITIGATING CONTROLS
              │                                │
    ┌─────────┤                                ├─────────┐
    │         │                                │         │
  Cause 1 ─→ ├── Control A ──┐  ┌── Control D ──┤ ←─ Consequence 1
    │         │               │  │               │         │
  Cause 2 ─→ ├── Control B ──┤  ├── Control E ──┤ ←─ Consequence 2
    │         │               │  │               │         │
  Cause 3 ─→ ├── Control C ──┤  ├── Control F ──┤ ←─ Consequence 3
    │         │              RISK EVENT          │         │
    └─────────┘               │  │               └─────────┘
                              ▼  ▼
```

### Bow-Tie Example: Data Breach

**Causes → Preventive Controls → RISK EVENT → Mitigating Controls → Consequences**

| Causes | Preventive Controls |
|--------|-------------------|
| Phishing attack | Email filtering, security awareness training, MFA |
| Unpatched vulnerability | Patch management, vulnerability scanning, WAF |
| Insider threat | Access controls, monitoring, background checks |
| Third-party compromise | Vendor security assessment, contract requirements |

**Risk Event:** Unauthorized access to customer data

| Mitigating Controls | Consequences |
|-------------------|-------------|
| Encryption at rest and in transit | Data exposure (encrypted data less useful) |
| Incident response plan | Regulatory fines (fast response reduces fines) |
| Cyber insurance | Financial losses (insurance covers costs) |
| PR crisis plan | Reputation damage (managed communication) |
| Backup and recovery | Service disruption (fast recovery) |

## Worked Example: Populated Risk Register

**Company:** Mid-market B2B SaaS company, $50M ARR, 300 employees

| ID | Category | Risk | P | I | Score | Controls | Residual | Actions | Owner | Status |
|----|----------|------|:-:|:-:|:-----:|----------|:--------:|---------|-------|:------:|
| R-001 | Strategic | Top 3 customers = 35% of ARR; loss of any one impacts growth targets | 3 | 5 | 15 C | QBRs, executive sponsors, multi-threading | 12 H | Customer diversification strategy, NRR program | CRO | In Progress |
| R-002 | Strategic | Well-funded competitor launching AI-powered alternative | 4 | 4 | 16 C | Product roadmap acceleration, switching costs | 12 H | Accelerate AI feature development, lock in annual contracts | CPO | In Progress |
| R-003 | Operational | Key engineer (architect) is single point of failure for core platform | 4 | 4 | 16 C | Documentation, code reviews | 12 H | Hire backup architect, knowledge transfer program | CTO | Open |
| R-004 | Technology | Cloud provider outage impacts platform availability | 2 | 4 | 8 H | Multi-AZ, auto-failover, monitoring | 6 M | Multi-region architecture by Q3 | CTO | In Progress |
| R-005 | Financial | 90-day DSO increasing; potential cash flow pressure | 3 | 3 | 9 H | Collections process, payment reminders | 6 M | Implement auto-dunning, review payment terms | CFO | Open |
| R-006 | Compliance | GDPR Article 28 compliance gaps with sub-processors | 3 | 4 | 12 H | DPA signed with main vendors | 8 H | Sub-processor audit, update DPAs | CLO | Open |
| R-007 | Operational | Engineering team turnover at 22% (above 15% target) | 4 | 3 | 12 H | Competitive compensation, flexible work | 9 H | Retention program, career ladder, stay interviews | CHRO | In Progress |
| R-008 | Cyber | Ransomware attack via phishing | 3 | 5 | 15 C | Email filtering, MFA, EDR, backups | 9 H | Security awareness training, incident response drill | CISO | In Progress |
| R-009 | Financial | FX exposure (30% of revenue in EUR) | 3 | 2 | 6 M | Natural hedge (EU costs) | 4 M | Evaluate hedging program | CFO | Monitoring |
| R-010 | Operational | Physical office flood/fire | 1 | 3 | 3 L | Insurance, cloud-based operations | 2 L | Update BCP annually | COO | Accepted |

## Risk Review Meeting Agenda

### Monthly Risk Review (60 minutes)

| Time | Topic | Owner |
|:----:|-------|-------|
| 0–5 min | Risk profile overview (total risks by zone, trend) | Risk Manager |
| 5–20 min | Review Critical and High risks (status, actions, trends) | Risk Owners |
| 20–30 min | New risks identified since last review | All |
| 30–40 min | Overdue mitigation actions (escalation) | Risk Manager |
| 40–50 min | KRI dashboard review (any thresholds breached?) | Risk Manager |
| 50–55 min | Risk appetite compliance check | Risk Manager |
| 55–60 min | Decisions and action items | Chair |

### Control Effectiveness Assessment

| Rating | Description | Action Required |
|:------:|-----------|----------------|
| **Effective** | Control operates as designed, risk within appetite | Continue monitoring |
| **Partially effective** | Control reduces risk but gaps remain | Enhance control, add compensating controls |
| **Ineffective** | Control not operating, risk not reduced | Redesign control, escalate |
| **Not tested** | No evidence of control effectiveness | Test immediately |
