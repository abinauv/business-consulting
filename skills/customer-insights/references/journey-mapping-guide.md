# Customer Journey Mapping Guide

## Journey Mapping Methodology

### 6-Phase Process

1. **Define scope** — Which customer segment? Which journey (end-to-end, or specific episode)? What's the business question?
2. **Gather research** — Customer interviews (8–12), analytics data, support tickets, sales feedback, survey data
3. **Map the journey** — Workshop with cross-functional team (marketing, sales, product, support, operations)
4. **Identify pain points** — Score by severity and frequency; find moments of truth
5. **Design improvements** — Prioritize by impact vs. effort; design future-state journey
6. **Implement and measure** — Build roadmap, assign owners, define success metrics

### Research Inputs for Journey Mapping

| Source | What It Reveals | Effort | Quality |
|--------|---------------|:------:|:-------:|
| Customer interviews (8–12) | Emotions, motivations, frustrations, workarounds | High | Very High |
| Web/app analytics | Actual behavior, drop-off points, paths | Low | High (behavior only) |
| Support tickets | Common issues, failure points, emotional language | Low | High |
| Sales/CS team interviews | What they hear repeatedly, common objections | Medium | Medium-High |
| NPS/CSAT verbatims | Drivers of satisfaction and detraction | Low | Medium |
| Social media/reviews | Unfiltered sentiment, competitive mentions | Low | Medium |
| Session recordings | Actual UX behavior, confusion points | Medium | High |
| Survey data | Quantified satisfaction by touchpoint | Medium | Medium |

## Stage Definitions

### B2B Journey Stages

| Stage | Customer Goal | Key Questions |
|-------|-------------|---------------|
| **Awareness** | "I have a problem/need" | How do they realize they need a solution? Where do they look first? |
| **Consideration** | "What options exist?" | How do they evaluate? Who else is involved? What content do they consume? |
| **Evaluation** | "Is this the right choice?" | What are deal-breakers? How do they compare vendors? Who makes the decision? |
| **Purchase** | "Let's do this" | What is the buying process? How long? How many stakeholders? |
| **Onboarding** | "Help me get started" | What does setup look like? How long until first value? What are common blockers? |
| **Adoption** | "Am I getting value?" | How quickly do they adopt? Which features? What support do they need? |
| **Renewal/Expansion** | "Should I continue/grow?" | What triggers renewal evaluation? What drives expansion? What causes churn risk? |
| **Advocacy** | "I want to recommend this" | What makes them refer? Do they participate in case studies, reviews, references? |

### B2C Journey Stages

| Stage | Customer Goal | Key Questions |
|-------|-------------|---------------|
| **Awareness** | "I want/need something" | What triggers the need? Where do they first encounter the brand? |
| **Consideration** | "Which product is right for me?" | Where do they research? What influences them (reviews, social, friends)? |
| **Purchase** | "Let me buy this" | In-store or online? Cart abandonment reasons? Price sensitivity? |
| **First Use** | "Does this work as expected?" | Unboxing experience? Setup difficulty? First impression? |
| **Ongoing Use** | "Am I happy with this?" | Usage frequency? Pain points? Feature discovery? |
| **Support** | "I need help" | How do they seek help? Resolution speed? Satisfaction after support? |
| **Loyalty/Repeat** | "Should I buy again?" | What drives repeat purchase? Loyalty program? Switching triggers? |
| **Advocacy** | "I love this — let me share" | Social sharing? Reviews? Word of mouth? |

## Touchpoint Identification

### Touchpoint Categories

| Category | Examples | Data Sources |
|----------|---------|-------------|
| **Digital** | Website, app, email, social media, chatbot, online ads | Analytics, session recordings |
| **Human** | Sales calls, support calls, in-store staff, account managers | CRM, call recordings |
| **Physical** | Store visits, product packaging, direct mail, events | Observation, surveys |
| **System** | Billing, shipping notifications, automated emails, self-service portals | System logs, support tickets |

### Touchpoint Catalog Template

| # | Stage | Touchpoint | Channel | Owner | Current Satisfaction | Volume (monthly) |
|---|-------|-----------|---------|-------|:--------------------:|:----------------:|
| 1 | Awareness | Google search | Digital | Marketing | N/A | 50,000 visits |
| 2 | Consideration | Product demo | Human | Sales | 4.2/5 | 200 demos |
| 3 | Purchase | Contract signing | System | Legal | 3.1/5 | 50 contracts |

## Pain Point Scoring

### Severity × Frequency Matrix

```
              HIGH FREQUENCY
                    |
   Annoying but     |  CRITICAL — Fix
   tolerable        |  immediately
   (monitor)        |
                    |
  ──────────────────┼──────────────────
                    |
   Low priority     |  Painful but rare
   (backlog)        |  (quick fix if easy)
                    |
              LOW FREQUENCY
   LOW SEVERITY ────────── HIGH SEVERITY
```

| Priority | Criteria | Action |
|----------|---------|--------|
| **P0 — Critical** | High severity + High frequency | Fix immediately, executive visibility |
| **P1 — High** | High severity + Low frequency, OR Low severity + High frequency | Plan fix within 30 days |
| **P2 — Medium** | Medium severity + Medium frequency | Roadmap for next quarter |
| **P3 — Low** | Low severity + Low frequency | Backlog, fix opportunistically |

### Pain Point Documentation Template

| ID | Stage | Pain Point | Severity (1-5) | Frequency (1-5) | Priority Score | Root Cause | Customer Quote | Improvement Idea |
|----|-------|-----------|:-:|:-:|:-:|---|---|---|

## Moment of Truth Analysis

Moments of truth are make-or-break interactions that disproportionately shape the overall customer experience.

### Common Moments of Truth

| Moment | Stage | Why It Matters | Success Criteria |
|--------|-------|---------------|-----------------|
| **First impression** | Awareness | Sets expectations for entire relationship | Compelling, relevant, easy to understand |
| **First contact with sales** | Consideration | Human connection builds or breaks trust | Responsive (<1 hour), knowledgeable, consultative (not pushy) |
| **Pricing reveal** | Evaluation | Price-value alignment determines conversion | Transparent, justified, competitive |
| **Onboarding experience** | Onboarding | Time-to-first-value predicts retention | Fast setup, clear guidance, early win |
| **First support issue** | Support | Defines "what happens when things go wrong" | Fast resolution, empathetic, competent |
| **Billing/invoice** | Ongoing | Unexpected charges destroy trust | Accurate, clear, matches expectations |
| **Renewal conversation** | Renewal | Retention depends on perceived value | Proactive, demonstrates ROI, offers growth path |

### Moment of Truth Scorecard

For each moment of truth, assess:
- **Current performance** (1-5 based on customer data)
- **Importance to customer** (1-5 based on research)
- **Gap** (Importance minus Performance)
- **Improvement priority** (rank by gap size)

## Emotional Journey Overlay

Map customer emotions at each stage:

| Stage | Emotion | Intensity | Trigger | Opportunity |
|-------|---------|:---------:|---------|-------------|
| Awareness | Curiosity/Frustration | Medium | Problem recognition | Make solution discoverable |
| Consideration | Hope/Anxiety | High | Comparing options | Reduce uncertainty with social proof |
| Purchase | Excitement/Worry | High | Committing budget | Reassure with guarantees, easy cancellation |
| Onboarding | Overwhelm/Anticipation | High | Learning new system | Simplify, celebrate first win |
| Adoption | Satisfaction/Frustration | Medium | Daily usage | Surface unused features, proactive support |
| Renewal | Confidence/Doubt | Medium | Evaluating ROI | Demonstrate value delivered, roadmap ahead |

## Journey Map Template

### Text-Based Journey Map Format

```
STAGE: [Stage Name]
─────────────────────────────────────────────────
Customer Goal:    [What the customer is trying to achieve]
Actions:          [What they actually do — step by step]
Touchpoints:      [Channels and interactions involved]
Emotions:         [How they feel — use ↑↗→↘↓ indicators]
Pain Points:      [Frustrations, barriers, confusion]
Opportunities:    [What we could do better]
Metrics:          [KPIs for this stage]
Owner:            [Team/person responsible]
```

### Journey Map Summary Table

| | Awareness | Consideration | Purchase | Onboarding | Usage | Renewal | Advocacy |
|---|---|---|---|---|---|---|---|
| **Goal** | | | | | | | |
| **Actions** | | | | | | | |
| **Touchpoints** | | | | | | | |
| **Emotion** | ↗ | → | ↑ | ↘ | → | ↗ | ↑ |
| **Pain Points** | | | | | | | |
| **Opportunities** | | | | | | | |
| **KPIs** | | | | | | | |

## Worked Example 1: B2B SaaS Onboarding Journey

**Product:** Project management SaaS, $50/user/month, mid-market customers

| | Sign Contract | Account Setup | Team Invite | First Project | First Sprint | Handoff to CS |
|---|---|---|---|---|---|---|
| **Goal** | Start using the product | Get configured | Get team on board | Prove value | Build habit | Ongoing success |
| **Actions** | Sign, pay, receive welcome | Set workspace, integrations | Invite team, assign roles | Create first project, import data | Run first sprint/workflow | Meet CSM, set goals |
| **Touchpoints** | DocuSign, payment, welcome email | Setup wizard, docs, chat support | Invite emails, training session | In-app, templates, help center | In-app, Slack integration | CSM call, QBR planning |
| **Emotion** | ↑ Excited | ↘ Overwhelmed by options | → Cautious (will team adopt?) | ↗ Hopeful | ↑ Satisfied (if it works) | → Neutral |
| **Pain Points** | Contract took 3 weeks in legal | Too many config options, no guidance | Team ignores invites, no training | Data import fails, template mismatch | Team reverts to old tool | CSM doesn't know context |
| **Opportunities** | Streamline legal templates | Guided setup wizard, smart defaults | Team onboarding kit, admin training | Industry-specific templates, import assistant | Weekly usage tips, champion program | Warm handoff doc from sales |
| **KPIs** | Contract-to-start time | Setup completion rate | Team activation rate (>50% invite acceptance) | Time to first project | W2 retention, DAU/MAU | CSAT at handoff |

**Key Insight:** The biggest drop-off occurs between Team Invite and First Project. 40% of teams that don't complete their first project within 14 days churn within 90 days.

**Priority Interventions:**
1. Guided setup wizard with smart defaults (reduce config overwhelm)
2. Team onboarding kit with 5-minute training video for invited users
3. Day 7 proactive check-in call from CSM if first project not created
4. Industry-specific templates pre-loaded based on company profile

## Worked Example 2: Retail Purchase Journey

**Brand:** Premium direct-to-consumer skincare, $40–$120 price range

| | Discovery | Research | First Purchase | Unboxing | First Use | Replenishment | Referral |
|---|---|---|---|---|---|---|---|
| **Goal** | Find a solution for skin concern | "Is this right for me?" | Buy with confidence | Experience the brand | See results | Reorder easily | Share with friends |
| **Touchpoints** | Instagram ad, influencer, Google | Website, reviews, quiz | Website, app, Affirm | Package, insert card, email | Product, app (routine tracker) | Email, SMS, subscription | Social, referral program |
| **Emotion** | ↗ Curious | → Skeptical but hopeful | ↑ Excited | ↑ Delighted (premium packaging) | ↗ Optimistic (Day 1) → Impatient (Day 14) | → Routine | ↑ Proud |
| **Pain Points** | Hard to find the right product among hundreds | Confusing ingredient info, no personalization | Shipping cost surprise at checkout | None (well-designed) | No visible results for 2–3 weeks, doubts | Runs out unexpectedly, manual reorder | No easy way to share |
| **Opportunities** | Skin quiz funnel from ads | AI-powered product recommender | Free shipping threshold, trial sizes | Include usage guide, expected timeline | Day 14 "stay the course" email with science | Auto-replenish, usage-based timing | Refer-a-friend: give $15, get $15 |

**Key Insight:** The critical moment of truth is Day 14–21 after first use. Customers expect immediate results, but skincare takes 4–6 weeks. Without education and encouragement, 30% of first-time buyers don't repurchase.

## Prioritizing Journey Improvements

### Impact vs. Effort Matrix

| | Low Effort | High Effort |
|---|---|---|
| **High Impact** | **Quick Wins** — Do immediately | **Strategic Initiatives** — Plan and resource |
| **Low Impact** | **Fill-ins** — Do if time allows | **Deprioritize** — Not worth the investment |

### Prioritization Scorecard

| Improvement | Impact on CX (1-5) | Revenue Impact (1-5) | Effort (1-5, inverted) | Priority Score | Recommendation |
|-------------|:---:|:---:|:---:|:---:|---|
| Guided onboarding wizard | 5 | 4 | 3 | 12 | Do first |
| Day 14 nurture email | 4 | 3 | 5 | 12 | Quick win |
| AI product recommender | 4 | 5 | 1 | 10 | Strategic initiative |
| Referral program | 3 | 4 | 3 | 10 | Plan for Q2 |
