# Persona Development Templates

## Data-Driven Persona Methodology

### The 3-Step Process

1. **Quantitative segmentation** — Cluster customers using behavioral data (purchase patterns, usage data, engagement metrics) to identify distinct groups
2. **Qualitative enrichment** — Conduct 4–6 interviews per segment to understand motivations, goals, frustrations, and decision-making process
3. **Validation** — Test personas against broader data (survey, analytics) to confirm they represent real customer segments

### Common Segmentation Variables

| Variable Type | B2C Examples | B2B Examples |
|-------------|-------------|-------------|
| **Behavioral** | Purchase frequency, basket size, channel preference, feature usage | Product usage, login frequency, feature adoption, support tickets |
| **Needs-based** | Primary problem to solve, desired outcome, urgency | Business challenge, strategic priority, buying criteria |
| **Value-based** | CLV, revenue contribution, referral activity | Contract value, expansion potential, strategic fit |
| **Demographic** | Age, income, location, family status | Company size, industry, role, department budget |

## Data Sources for Persona Building

| Source | What It Reveals | Availability |
|--------|---------------|:------------:|
| **CRM data** | Purchase history, deal size, sales cycle, touchpoints | Usually available |
| **Product analytics** | Feature usage, frequency, activation, retention | Requires instrumentation |
| **Support tickets** | Common issues, frustration points, capability gaps | Usually available |
| **Sales team interviews** | Buyer motivations, objections, decision process | Easy to access |
| **Customer interviews** | Deep motivations, context, emotions, jobs-to-be-done | Requires scheduling |
| **Surveys (NPS/CSAT)** | Satisfaction drivers, verbatim feedback | Often available |
| **Social/review data** | Unfiltered opinions, competitive mentions | Publicly available |
| **Google Analytics** | Content interests, device/channel preferences, paths | Usually available |

## Interview Guide for Persona Research

### 15 Core Questions

**Background & Context**
1. "Tell me about your role. What does a typical day/week look like?"
2. "What are the top 3 challenges you face in your role right now?"
3. "How do you measure success in your work?"

**Problem & Need**
4. "What problem were you trying to solve when you started looking for [product category]?"
5. "What was the trigger that made you start looking? Was there a specific event?"
6. "How were you solving this problem before? What was frustrating about that?"

**Decision Process**
7. "Walk me through how you evaluated options. Where did you look first?"
8. "Who else was involved in the decision? What were their roles and concerns?"
9. "What were your top 3 criteria when choosing a solution?"
10. "What almost stopped you from choosing us? What was your biggest hesitation?"

**Experience & Value**
11. "How would you describe your experience getting started with [product]?"
12. "What value have you gotten from [product]? Can you quantify it?"
13. "What frustrates you most about [product]?"
14. "If you could change one thing, what would it be?"

**Meta**
15. "How do you stay informed about tools and trends in your field? (Sources, communities, events)"

### Probe Questions (for deeper insight)
- "Can you give me a specific example?"
- "Why was that important to you?"
- "What happened next?"
- "How did that make you feel?"
- "What would ideal look like?"

## Persona Card Template

```
╔══════════════════════════════════════════════════════════════╗
║  PERSONA: [Name] — [Title]                                  ║
║  Segment: [Segment name]  |  % of customer base: [X%]       ║
╠══════════════════════════════════════════════════════════════╣
║                                                              ║
║  DEMOGRAPHICS                                                ║
║  • Role/Title: [Title]                                       ║
║  • Company size: [X employees / $X revenue]                  ║
║  • Industry: [Industry]                                      ║
║  • Experience: [Years in role]                               ║
║  • Reports to: [Title]                                       ║
║  • Team size: [X]                                            ║
║                                                              ║
║  GOALS                                          FRUSTRATIONS ║
║  1. [Primary goal]                  1. [Top frustration]     ║
║  2. [Secondary goal]                2. [Second frustration]  ║
║  3. [Tertiary goal]                 3. [Third frustration]   ║
║                                                              ║
║  BEHAVIORS                                                   ║
║  • Uses product [frequency]                                  ║
║  • Primary use case: [what they do most]                     ║
║  • Feature adoption: [which features, which ignored]         ║
║  • Support: [how often, what type]                           ║
║                                                              ║
║  DECISION CRITERIA (ranked)                                  ║
║  1. [Most important factor]                                  ║
║  2. [Second factor]                                          ║
║  3. [Third factor]                                           ║
║                                                              ║
║  PREFERRED CHANNELS                                          ║
║  Information: [email, LinkedIn, industry blogs, conferences] ║
║  Communication: [email, Slack, phone]                        ║
║  Support: [chat, self-service, phone]                        ║
║                                                              ║
║  REPRESENTATIVE QUOTE                                        ║
║  "[Actual quote from interview that captures this persona]"  ║
║                                                              ║
║  DAY IN THE LIFE                                             ║
║  [2-3 sentence narrative of a typical day]                   ║
║                                                              ║
║  WHAT THEY VALUE MOST ABOUT US                               ║
║  [Primary value driver]                                      ║
║                                                              ║
║  BIGGEST RISK OF CHURN                                       ║
║  [What would make them leave]                                ║
╚══════════════════════════════════════════════════════════════╝
```

## B2B Persona Additions

### Buying Committee Mapping

| Role | Persona | Involvement | Concerns | How to Win |
|------|---------|:-----------:|----------|-----------|
| **Decision Maker** | VP/C-level | Final sign-off | ROI, risk, strategic fit | Business case, executive briefing, reference calls |
| **Champion** | Manager/Director | Drives evaluation | Solves their daily pain | Product demo, trial, success metrics |
| **Influencer** | Technical lead | Evaluates fit | Integration, security, scalability | Technical documentation, POC, architecture review |
| **Gatekeeper** | Procurement | Negotiates terms | Price, compliance, vendor risk | Competitive pricing, security questionnaire, references |
| **End User** | Individual contributor | Daily usage | Ease of use, learning curve, time saved | Trial, training, UX quality |

### B2B Persona: Context Section

Add to standard persona card:
- **Strategic priorities** — What is their company trying to achieve this year?
- **Budget cycle** — When do they plan/approve budgets?
- **Technology stack** — What other tools do they use? What must integrate?
- **Regulatory environment** — Any compliance requirements affecting the purchase?
- **Political dynamics** — Who do they need buy-in from? Who might block them?

## Anti-Persona Concept

Define who is NOT your customer to prevent wasted effort:

| Anti-Persona | Why They're Not a Fit | Warning Signs | What to Do |
|-------------|----------------------|--------------|-----------|
| "Tire kicker" | No real intent to buy, just researching | Excessive demo requests, no timeline, won't commit to next steps | Qualify early, provide self-serve resources, don't invest sales time |
| "Wrong segment" | Product doesn't fit their needs | Feature requests outside roadmap, constant complaints, high support cost | Honest conversation, suggest alternatives, decline gracefully |
| "Price shopper" | Only cares about lowest price, no loyalty | Compares on price alone, no interest in value discussion, churns at first discount elsewhere | Don't compete on price, maintain value positioning, let them go |

## Persona Validation Checklist

Before finalizing personas, verify:

- [ ] Each persona represents at least 15% of your customer base (or a strategically important segment)
- [ ] Personas are based on real data (not assumptions or stereotypes)
- [ ] At least 4 customer interviews inform each persona
- [ ] Sales and CS teams recognize the personas ("Yes, I talk to this person every day")
- [ ] Personas have distinct enough needs to justify different approaches
- [ ] Decision criteria are ranked (not just listed)
- [ ] The persona includes actionable information (not just demographics)
- [ ] Each persona maps to specific product/marketing implications

## Worked Example: B2B SaaS Buyer Personas

### Persona 1: "Strategic Sarah" — VP of Operations

**Segment:** Enterprise (500+ employees), 35% of revenue
- **Demographics:** VP-level, 12+ years experience, reports to COO, manages 50+ people
- **Goals:** Standardize operations across regions, reduce manual processes by 40%, get real-time visibility into KPIs
- **Frustrations:** Data scattered across 15 spreadsheets, teams use different processes in each office, can't get a single source of truth
- **Decision criteria:** (1) Enterprise-grade security, (2) Customization, (3) Integration with SAP, (4) Vendor stability
- **Buying behavior:** 6-month sales cycle, involves IT and procurement, needs board-level business case
- **Quote:** "I don't need another tool — I need THE tool that replaces the 10 we're using today."
- **Best channels:** LinkedIn, Gartner reports, peer recommendations, executive events
- **How to win:** Executive briefing, custom ROI analysis, reference calls with similar companies

### Persona 2: "Tactical Tom" — Operations Manager

**Segment:** Mid-market (50–500 employees), 45% of revenue
- **Demographics:** Manager-level, 5–8 years experience, reports to VP Ops, manages 8–15 people
- **Goals:** Save 10 hours/week on reporting, eliminate errors in the monthly close, look good to his boss
- **Frustrations:** Spends 60% of time on manual data collection, gets blamed when reports are wrong, can't get IT to prioritize his requests
- **Decision criteria:** (1) Ease of use, (2) Quick implementation, (3) Price, (4) Good support
- **Buying behavior:** 2-month sales cycle, can sign up to $30K/year without VP approval, wants trial first
- **Quote:** "I just need something that works, doesn't require a PhD to set up, and my team will actually use."
- **Best channels:** Google search, G2/Capterra reviews, webinars, free trial
- **How to win:** Free trial, self-service onboarding, ROI calculator, case studies from similar companies

### Persona 3: "Data-Driven Dana" — Business Analyst

**Segment:** All sizes, End User (influences 60% of deals)
- **Demographics:** IC/Senior IC, 2–5 years experience, reports to Ops Manager, data-savvy
- **Goals:** Automate reporting, build dashboards, find insights in the data, advance her career
- **Frustrations:** Current tools can't handle complex queries, has to export to Excel for everything, wants API access
- **Decision criteria:** (1) Data flexibility (custom queries, API), (2) Visualization quality, (3) Speed, (4) Learning resources
- **Buying behavior:** Recommends tools to manager, creates POC, becomes internal champion
- **Quote:** "If I can't write a custom query, it's useless to me. But if I can, I'll sell it to everyone on the team."
- **Best channels:** YouTube tutorials, dev docs, community forums, Product Hunt
- **How to win:** Excellent documentation, powerful query builder, community, freemium/developer tier

## How to Use Personas in Strategy

| Application | How Personas Help | Example |
|------------|------------------|---------|
| **Product roadmap** | Prioritize features by persona value | "Strategic Sarah needs SSO; this unlocks enterprise deals" |
| **Marketing messaging** | Tailor value props per persona | Tom cares about ease; Sarah cares about enterprise-grade |
| **Content strategy** | Create content for each persona's preferred channels/topics | Dana → technical blog posts; Sarah → Gartner-style reports |
| **Sales playbook** | Customize pitch by buyer type | Champion enablement kit for Dana, ROI deck for Sarah |
| **Customer success** | Tailor onboarding and health metrics | Tom needs quick-start guide; Sarah needs implementation plan |
| **Pricing** | Design tiers for different personas | Self-serve for Tom, enterprise for Sarah, developer tier for Dana |
