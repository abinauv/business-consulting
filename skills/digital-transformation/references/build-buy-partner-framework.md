# Build vs. Buy vs. Partner Decision Framework

## Decision Criteria Matrix

| Criteria | Weight | Build | Buy | Partner |
|----------|:------:|:-----:|:---:|:-------:|
| **Strategic importance** | 25% | If core to competitive advantage | If commodity/non-differentiating | If adjacent, shared value |
| **Time to market** | 20% | If time allows (12–36 months) | If urgent (<6 months) | If moderate (6–12 months) |
| **Internal capability** | 15% | If talent available and experienced | If no internal expertise | If partial capability, need complement |
| **Total cost (5-year)** | 15% | Often lower long-term, higher upfront | Higher long-term (licenses), lower upfront | Moderate, shared investment |
| **Competitive differentiation** | 10% | If unique capability needed | If market-standard solution adequate | If co-created differentiation possible |
| **Control needed** | 10% | Full control required | Vendor roadmap acceptable | Shared control acceptable |
| **Risk tolerance** | 5% | Execution risk | Vendor lock-in risk | Partnership alignment risk |

### Quick Decision Tree

```
Is this capability core to your competitive advantage?
├── YES: Do you have the talent and time to build it?
│   ├── YES → BUILD
│   └── NO: Can you acquire a company that has it?
│       ├── YES → ACQUIRE (M&A)
│       └── NO → PARTNER (with strong governance)
└── NO: Does a proven solution exist in the market?
    ├── YES: Is vendor lock-in acceptable?
    │   ├── YES → BUY
    │   └── NO → BUILD or BUY (with open standards)
    └── NO → BUILD or PARTNER
```

## Build Evaluation

### When to Build

- The capability IS your competitive advantage
- No market solution fits your specific requirements
- You have strong engineering talent available
- Long-term cost of ownership is lower than buying
- You need full control over roadmap and IP

### Build Assessment Template

| Factor | Assessment | Score (1-5) |
|--------|-----------|:-----------:|
| **Technical complexity** | [Low/Medium/High — technology stack, integrations, scale requirements] | |
| **Team readiness** | [Can current team build it? Skills gaps? Hiring needed?] | |
| **Timeline** | [Estimated time to MVP? To full production?] | |
| **Ongoing maintenance** | [Team size needed to maintain? Bug fixes, updates, security patches?] | |
| **Opportunity cost** | [What else could the team build instead?] | |
| **Risk** | [What if it's late? Over budget? Doesn't meet requirements?] | |

### Build Cost Model

| Cost Category | Year 0 | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | Total |
|-------------|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| Development team (FTEs × salary) | | | | | | | |
| Infrastructure (cloud, tools) | | | | | | | |
| External contractors/consulting | | | | | | | |
| QA and testing | | | | | | | |
| Project management | | | | | | | |
| Ongoing maintenance (post-launch) | — | | | | | | |
| Enhancement/feature development | — | | | | | | |
| **Total** | | | | | | | |

## Buy Evaluation

### When to Buy

- The capability is commodity/table-stakes (not differentiating)
- Speed to market is critical
- Proven, mature solutions exist
- Internal team should focus on core capabilities
- Vendor ecosystem provides ongoing innovation

### Vendor Evaluation Criteria (20+ Categories)

**Functionality (30%)**
- [ ] Meets >80% of must-have requirements out of the box
- [ ] Configuration flexibility without custom development
- [ ] API availability and quality
- [ ] Mobile support
- [ ] Reporting and analytics capabilities
- [ ] Workflow and automation features

**Technology (20%)**
- [ ] Architecture (cloud-native, multi-tenant, microservices)
- [ ] Security (SOC 2, encryption, SSO, MFA)
- [ ] Scalability (can handle 10x growth)
- [ ] Performance (SLA commitments, uptime history)
- [ ] Integration capabilities (pre-built connectors, API, webhooks)
- [ ] Data portability (can you get your data out?)

**Commercial (20%)**
- [ ] Pricing model (per-user, usage-based, flat fee)
- [ ] Total cost of ownership (license + implementation + customization + training)
- [ ] Contract terms (length, flexibility, exit clauses)
- [ ] Pricing trajectory (historical price increases, competitive pressure)

**Vendor Viability (15%)**
- [ ] Company financials (revenue, growth, profitability, funding)
- [ ] Customer base (size, retention, similar to you)
- [ ] Market position (leader, challenger, niche)
- [ ] Product roadmap (aligns with your needs)
- [ ] Leadership team (experience, stability)

**Support & Services (15%)**
- [ ] Implementation methodology and timeline
- [ ] Support model (SLA, channels, hours, dedicated vs. shared)
- [ ] Training and documentation quality
- [ ] User community and ecosystem
- [ ] Partner/SI network for implementation

### Vendor Comparison Matrix

| Criteria | Weight | Vendor A | Vendor B | Vendor C |
|----------|:------:|:--------:|:--------:|:--------:|
| Functionality | 30% | 4 (1.2) | 5 (1.5) | 3 (0.9) |
| Technology | 20% | 4 (0.8) | 4 (0.8) | 5 (1.0) |
| Commercial | 20% | 3 (0.6) | 4 (0.8) | 5 (1.0) |
| Vendor viability | 15% | 5 (0.75) | 3 (0.45) | 4 (0.6) |
| Support | 15% | 4 (0.6) | 3 (0.45) | 4 (0.6) |
| **Total** | 100% | **3.95** | **4.00** | **4.10** |

### Reference Check Guide

Ask 3–5 existing customers:
1. How long have you been using [product]? What was the implementation like?
2. What problems does it solve well? Where does it fall short?
3. How responsive is their support when issues arise?
4. Have they kept their product roadmap promises?
5. What would you do differently if you started over?
6. Would you choose them again? Why or why not?
7. What's the biggest surprise (positive or negative) since implementation?

## Partner Evaluation

### Partnership Models

| Model | Control | Investment | Risk | Best For |
|-------|:-------:|:----------:|:----:|---------|
| **Strategic alliance** | Shared | Low-Medium | Medium | Market access, co-marketing, referrals |
| **Technology partnership** | Shared | Medium | Medium | Integration, co-development, platform extension |
| **Joint venture** | 50/50 | High | High | New market entry, combined capabilities |
| **Licensing** | Low (licensee) | Low | Low | Using proven IP/technology, non-core |
| **White-label** | Medium | Low | Low-Medium | Offering partner's product under your brand |
| **Co-development** | Shared | High | High | Creating new product/technology together |

### Partnership Assessment Criteria

| Factor | Questions to Evaluate |
|--------|----------------------|
| **Strategic alignment** | Do both parties benefit? Are goals compatible long-term? |
| **Cultural compatibility** | Similar decision speed, risk appetite, communication styles? |
| **Capability complementarity** | Does each partner bring something the other lacks? |
| **Financial commitment** | Can both parties fund their obligations? What if one can't? |
| **Governance** | How are decisions made? How are disputes resolved? |
| **IP/Data** | Who owns what? How is shared IP handled? |
| **Exit terms** | How does the partnership end? What happens to shared assets? |

## Total Cost of Ownership (TCO) Model

### 5-Year Comparison Framework

| Cost Component | Build | Buy (Vendor A) | Partner |
|---------------|:-----:|:---:|:---:|
| **Year 0: Setup** | | | |
| License/subscription fees | — | $100K | $50K |
| Development costs | $500K | — | $200K |
| Implementation/consulting | $50K | $150K | $100K |
| Infrastructure | $30K | — (SaaS) | $15K |
| Training | $20K | $30K | $25K |
| Data migration | $40K | $40K | $40K |
| **Year 0 Total** | **$640K** | **$320K** | **$430K** |
| | | | |
| **Annual (Years 1–5)** | | | |
| License/subscription | — | $100K | $50K |
| Maintenance team (FTEs) | $200K (1.5 FTE) | — | $100K (0.75 FTE) |
| Infrastructure | $30K | — | $15K |
| Enhancements/customization | $100K | $30K | $50K |
| Support fees | — | $25K | $15K |
| **Annual Total** | **$330K** | **$155K** | **$230K** |
| | | | |
| **5-Year TCO** | **$2.29M** | **$1.10M** | **$1.58M** |

### Hidden Costs to Include

| Often Missed | Build | Buy | Partner |
|-------------|-------|-----|---------|
| Opportunity cost of dev team | High | — | Medium |
| Integration with existing systems | Medium | Medium-High | Medium |
| Change management and adoption | Medium | Medium | Medium |
| Vendor management overhead | — | Low | Medium |
| Contract negotiation and legal | — | Low | Medium |
| Switching costs if it doesn't work | Very High | Medium | Medium |
| Security and compliance maintenance | High | Low (vendor handles) | Shared |

## Risk Comparison

| Risk | Build | Buy | Partner |
|------|:-----:|:---:|:-------:|
| **Schedule overrun** | HIGH (30–50% of projects) | LOW (proven product) | MEDIUM |
| **Budget overrun** | HIGH | LOW-MEDIUM | MEDIUM |
| **Doesn't meet requirements** | MEDIUM (you control scope) | MEDIUM (vendor limitations) | MEDIUM |
| **Vendor/partner failure** | N/A | MEDIUM (vendor viability) | MEDIUM (partner commitment) |
| **Lock-in** | LOW (you own the code) | HIGH (switching costs) | MEDIUM |
| **Security** | HIGH (your responsibility) | LOW-MEDIUM (vendor handles) | MEDIUM (shared) |
| **Talent dependency** | HIGH (key person risk) | LOW | MEDIUM |
| **Technology obsolescence** | MEDIUM (must maintain) | LOW (vendor innovates) | LOW-MEDIUM |

## Worked Example: CRM Platform Decision

**Context:** $100M B2B company needs CRM. Currently using spreadsheets. 50 sales reps, 5,000 accounts.

| Option | Pros | Cons | 5-Year TCO | Recommendation |
|--------|------|------|:----------:|:-:|
| **Build custom CRM** | Exactly fits workflow, no per-user fees | 12–18 months to build, 2 FTE to maintain, no ecosystem | $1.8M | No |
| **Buy Salesforce** | Market leader, massive ecosystem, proven at scale | Expensive per-user, complex, over-engineered for needs | $1.2M | Maybe |
| **Buy HubSpot** | Right-sized, strong UX, marketing integration | Less enterprise customization, growing pains | $600K | Yes |
| **Partner (integrate with existing ERP)** | Familiar interface, single vendor | CRM is not ERP vendor's strength, limited innovation | $900K | No |

**Decision: Buy HubSpot.** CRM is not a competitive differentiator — it's table-stakes. HubSpot offers best value for mid-market B2B with strong UX (driving adoption), marketing integration (driving lead quality), and 60% lower TCO than Salesforce.
