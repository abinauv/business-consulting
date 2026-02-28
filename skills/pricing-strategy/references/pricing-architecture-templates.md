# Pricing Architecture Templates

Comprehensive templates and frameworks for designing pricing structures, tiers, bundles, and price pages.

---

## Good / Better / Best Tier Design

### Core Principles

**The G/B/B structure works because:**
1. It reduces decision complexity (3 options, not 15)
2. It enables price anchoring (Best makes Better look reasonable)
3. It captures different willingness-to-pay segments with a single product
4. It creates natural upgrade paths (land on Good, expand to Better/Best)

### Feature Fencing Framework

Determine which features go in which tier by scoring each feature on two dimensions:

**Dimension 1: Breadth of Appeal** (1-5)
- 5 = Nearly all customers need this
- 3 = Most customers in target segment need this
- 1 = Only a niche subset needs this

**Dimension 2: Value Intensity** (1-5)
- 5 = This feature delivers massive ROI or solves critical pain
- 3 = Meaningful improvement but not transformative
- 1 = Nice-to-have, marginal impact

**Tier Assignment Matrix:**

| Breadth | Value Intensity | Tier Assignment |
|---|---|---|
| High (4-5) | Low-Medium (1-3) | Good (core feature for all) |
| High (4-5) | High (4-5) | Better (key upgrade driver) |
| Medium (3) | High (4-5) | Better or Best (segment-dependent) |
| Low (1-2) | High (4-5) | Best (premium differentiator) |
| Low (1-2) | Low (1-2) | Add-on or exclude entirely |
| Medium (3) | Medium (3) | Better (fills out the tier value) |

### Price Ratio Patterns

**Pattern 1: Linear (1x / 2x / 3x)**
- Good: $29 / Better: $59 / Best: $89
- Best for: broad market, gradual value increase between tiers
- Target tier distribution: 30% Good, 45% Better, 25% Best

**Pattern 2: Accelerating (1x / 2x / 4x)**
- Good: $29 / Better: $59 / Best: $119
- Best for: enterprise segment has much higher WTP
- Target tier distribution: 35% Good, 45% Better, 20% Best

**Pattern 3: Compressed (1x / 1.5x / 2x)**
- Good: $29 / Better: $45 / Best: $59
- Best for: pushing users up-tier with minimal price friction
- Target tier distribution: 20% Good, 40% Better, 40% Best

**Pattern 4: Decoy-Optimized**
- Good: $29 / Better: $79 / Best: $89
- Better acts as decoy, making Best look like the obvious choice
- Target tier distribution: 25% Good, 10% Better, 65% Best

**Pattern 5: Wide Spread (1x / 3x / 10x)**
- Good: $29 / Better: $99 / Best: $299
- Best for: serving very different segments (startup to enterprise)
- Target tier distribution: 50% Good, 35% Better, 15% Best

### Decoy Positioning Guide

**How to create an effective decoy:**
1. The decoy tier should be priced close to the target tier (within 10-20%)
2. The decoy should offer significantly less value than the target
3. The comparison between decoy and target should be obvious
4. The decoy does not need many subscribers -- its job is to make the target look good

**Example:**

| | Basic | Plus (Decoy) | Pro (Target) |
|---|---|---|---|
| Price | $19/mo | $39/mo | $45/mo |
| Users | 1 | 3 | 10 |
| Storage | 5 GB | 10 GB | 100 GB |
| Support | Email | Email | Priority |
| Custom reports | No | No | Yes |

Why it works: Plus costs $39 for modest improvements over Basic. Pro costs only $6 more but offers massively more value. Rational buyers pick Pro.

### Tier Naming Conventions

| Pattern | Good | Better | Best | Tone |
|---|---|---|---|---|
| Standard | Basic | Professional | Enterprise | Corporate, safe |
| Action | Starter | Growth | Scale | Aspirational |
| Persona | Individual | Team | Organization | User-centric |
| Metaphor | Seed | Grow | Bloom | Friendly, startup |
| Direct | Free | Pro | Business | Clear, SaaS standard |
| Premium | Silver | Gold | Platinum | Prestige, loyalty |

**Best practices:**
- Avoid names that feel limiting ("Basic" can feel cheap -- "Starter" is better)
- Enterprise tier can be named or just "Contact Sales"
- Align names with your brand personality
- Do not use more than 4 tiers (3 is ideal for most B2B SaaS)

---

## Bundle vs. Unbundle Decision Framework

### When to Bundle

| Signal | Explanation |
|---|---|
| Heterogeneous preferences | Different customers value different features -- bundling captures more surplus |
| Low marginal cost | Adding features costs you little (software, digital content) |
| Reduce comparison shopping | Bundles are harder to price-compare vs. competitors |
| Cross-sell opportunity | Bundling introduces users to features they would not buy standalone |
| Price sensitivity reduction | Bundling makes total price feel lower per feature |

### When to Unbundle

| Signal | Explanation |
|---|---|
| Homogeneous preferences | All customers want the same core; extras feel like a tax |
| High marginal cost | Each feature has meaningful cost to deliver |
| Regulatory / procurement need | Buyer requires line-item pricing for approval |
| Competitive attack | Unbundle to undercut a competitor on specific capability |
| Standalone feature value | A feature has enough value to command its own price |

### Bundle Pricing Math

**Rule of thumb**: A bundle should be priced at 60-80% of the sum of individual component prices.

**Example:**
- Feature A standalone: $30/month
- Feature B standalone: $20/month
- Feature C standalone: $15/month
- Sum: $65/month
- Bundle price: $45-$52/month (30-40% bundle discount)

### Bundle Architecture Patterns

**Pattern 1: Pure Bundle**
- Only available as a bundle; no standalone options
- Example: Microsoft 365 (Word + Excel + PowerPoint sold together)
- Best when: features are tightly integrated and used together

**Pattern 2: Mixed Bundle**
- Bundle available at a discount; components also sold individually
- Example: Adobe Creative Cloud (full suite or individual apps)
- Best when: some customers only need specific features

**Pattern 3: Add-On Bundle**
- Core product sold standalone; bundles add supplementary features
- Example: Salesforce (core CRM + add-on bundles for marketing, analytics)
- Best when: core product is self-sufficient but add-ons enhance value

**Pattern 4: Tiered Bundle**
- Multiple bundle levels with increasing components
- Example: Cable TV packages (basic, standard, premium)
- Best when: customers have varying appetite for breadth

---

## Add-On and Upsell Architecture

### Add-On Design Principles

**Pricing add-ons:**
- Each add-on: 10-30% of base plan price
- Total add-on ceiling: 40-60% of base price for typical customer
- Add-ons should feel optional, not essential (if everyone needs it, put it in the base)

**Best add-on categories:**

| Category | Examples | Typical Pricing |
|---|---|---|
| Capacity / volume | Extra storage, users, API calls | Per-unit incremental |
| Premium support | Priority queue, SLA, dedicated CSM | 15-25% of base price |
| Advanced features | Analytics, reporting, AI capabilities | 20-40% of base price |
| Integrations | Premium connectors, custom API access | $50-$500/month |
| Professional services | Implementation, training, consulting | Project-based or hourly |
| Compliance / security | SSO, SAML, audit logs, SOC2 compliance | 20-50% of base price |

### Upsell Trigger Framework

**Usage-based triggers:**
- User reaches 80% of plan limit (storage, users, API calls)
- Message: "You're approaching your plan limit. Upgrade to [tier] for [X]."

**Feature-based triggers:**
- User attempts to access a higher-tier feature
- Message: "This feature is available on [tier]. Upgrade to unlock [feature + benefit]."

**Time-based triggers:**
- After 30/60/90 days on current plan with high engagement
- Message: "You've gotten great results with [product]. Unlock even more with [tier]."

**Team-based triggers:**
- New team members added, approaching seat limit
- Message: "Your team is growing! [Tier] supports unlimited users."

**Success-based triggers:**
- Customer achieves key milestone (e.g., 1,000th customer served, $X revenue through platform)
- Message: "Congratulations on [milestone]! Companies at your stage typically upgrade to [tier] for [benefit]."

### Upsell Timing Best Practices
- **Too early**: before the user experiences core value (first 7 days)
- **Just right**: after the user has experienced value and is hitting natural limits (14-60 days)
- **Too late**: after the user has found workarounds for your limitations (90+ days)

---

## Usage-Based Pricing Design

### Selecting the Right Usage Unit

**Criteria for a good pricing unit:**
1. **Customer understands it**: the unit must be intuitive and predictable
2. **Scales with value**: as the customer gets more value, their usage (and bill) increases
3. **Measurable**: you can track it accurately and transparently
4. **Controllable**: the customer can manage their usage if needed
5. **Hard to game**: difficult to artificially reduce usage while maintaining value

**Common pricing units by product type:**

| Product Type | Common Units | Recommended |
|---|---|---|
| API / Infrastructure | API calls, compute hours, data GB | API calls or compute hours |
| Communication | Messages sent, contacts, conversations | Messages or contacts |
| Data / Analytics | Records processed, queries, data rows | Records or queries |
| E-commerce | Transactions, GMV, orders | Transactions or GMV % |
| Storage | GB stored, files, bandwidth | GB stored |
| AI / ML | Predictions, tokens, model runs | Predictions or tokens |
| CRM | Contacts, deals, users | Contacts or users |

### Volume Break Design

**Decreasing marginal rate (most common):**

| Tier | Volume | Per-Unit Price | Tier Price |
|---|---|---|---|
| Tier 1 | 0-1,000 | $0.10 | $0-$100 |
| Tier 2 | 1,001-10,000 | $0.07 | $70-$700 |
| Tier 3 | 10,001-100,000 | $0.04 | $400-$4,000 |
| Tier 4 | 100,001+ | $0.02 | Negotiated |

**Design decisions:**
- **Graduated pricing**: each tier applies only to units within that tier (most transparent, customer-friendly)
- **Volume pricing**: reaching a tier applies the lower rate to ALL units (simpler, but creates "cliff" effects where using one more unit reduces total bill)
- **Committed use discounts**: customer commits to minimum volume for lower rate (predictable for both sides)

### Overage Handling

| Approach | Description | Customer Experience |
|---|---|---|
| Hard cap | Service stops at limit | Frustrating, may lose data/uptime |
| Soft cap with overage rate | Service continues, billed at premium rate | Fair, but surprise bills possible |
| Auto-upgrade | Automatically move to next tier | Smooth, but may feel sneaky |
| Grace period | Allow overage for a period, then require upgrade | Customer-friendly, builds trust |
| Notification + choice | Alert at 80%/100%, let customer decide | Most transparent and preferred |

**Recommended**: Notification at 80% and 100% of limit, with grace period (7-14 days) before requiring action. Overage rate should be 1.5-2x the in-plan rate (not punitive, but incentivizes upgrade).

---

## Freemium Conversion Optimization

### Free Tier Design Principles

**The free tier must:**
1. Deliver enough value for the user to experience the core "aha" moment
2. Create enough limitations that power users naturally outgrow it
3. Be genuinely useful (not a glorified demo or crippled product)
4. Serve as a distribution channel (users recommend it because it is useful)

### What to Limit in Free Tier

| Limit Type | Examples | Effectiveness |
|---|---|---|
| Usage volume | 100 messages/month, 1 GB storage | High -- natural growth trigger |
| Team size | 1-3 users only | High -- expansion drives upgrade |
| Feature depth | Basic analytics, no AI features | Medium -- depends on feature salience |
| History / retention | Last 90 days of data, limited export | Medium -- creates urgency |
| Integrations | No third-party integrations | Medium-High -- critical for power users |
| Support | Community only, no priority support | Low -- most free users do not expect support |
| Branding | "Powered by [product]" watermark | Low impact on conversion, good for awareness |

### Upgrade Trigger Design

**Most effective triggers (in order):**
1. Team growth (invite blocked at limit) -- 35-45% of upgrades
2. Usage limits reached (storage, messages, etc.) -- 25-35% of upgrades
3. Feature gating (tried to use a paid feature) -- 15-25% of upgrades
4. Time-based trial expiry (reverse trial ending) -- 10-20% of upgrades

### Conversion Rate Benchmarks

| Free Tier Design | Typical Conversion | Examples |
|---|---|---|
| Feature-limited free | 2-4% | Most SaaS tools |
| Usage-limited free | 4-7% | Storage, communication tools |
| Time-limited trial (no free tier) | 15-25% | Enterprise SaaS, complex tools |
| Reverse trial (full access, then downgrade) | 8-15% | Notion, Airtable approach |
| Open-source with managed offering | 1-3% | Developer tools, infrastructure |

### Reverse Trial Model

**How it works:**
1. New user gets full product access (Best tier) for 14 days
2. After 14 days, account downgrades to Free tier
3. User has experienced full value and feels the loss of features
4. Upgrade prompt highlights what they are losing

**Why it works:**
- Loss aversion: losing features feels worse than never having them
- User has already invested in the full product (data, workflows, integrations)
- Informed decision: user knows exactly what they are paying for

---

## Enterprise Pricing

### Negotiation Guardrails

**What sales can negotiate:**
- Discount off list price (within approval matrix)
- Payment terms (monthly vs. quarterly vs. annual)
- Contract length (1-year vs. multi-year)
- Implementation / onboarding fees
- Volume of users or usage included
- Support level / SLA terms

**What sales cannot negotiate (without executive approval):**
- Pricing model (e.g., switching from per-seat to flat-rate)
- Feature inclusion that bypasses tier structure
- Custom SLAs with financial penalties
- Unlimited usage at a fixed price
- Most Favored Nation (MFN) clauses
- Perpetual license terms for SaaS

### Discount Approval Matrix

| Discount from List | Approver | Required Documentation |
|---|---|---|
| 0-10% | Account Executive | Standard: competitive bid or volume |
| 11-15% | Sales Manager | Competitive analysis + strategic justification |
| 16-20% | VP Sales / CRO | Written business case with expansion plan |
| 21-25% | CRO + CFO | Board-level strategic account, 3-year plan |
| 26-30% | CEO | Exceptional circumstances, full business case |
| 30%+ | Decline or restructure | Rarely approved; redesign deal structure instead |

### Discount Exchange Table

Every discount should require something in return:

| Discount | Customer Must Provide |
|---|---|
| 5-10% | Annual (not monthly) commitment |
| 10-15% | 2-year commitment + case study rights |
| 15-20% | 3-year commitment + reference customer + logo rights |
| 20-25% | All above + co-marketing + advisory board participation |
| Volume discount | Committed minimum volume (use-it-or-lose-it) |
| Early payment discount | Payment within 10 days (2% discount is standard: "2/10 net 30") |

### Enterprise Price Calculation Template

```
Base price:           [List price per user x users]
Volume adjustment:    [-X% for volume above threshold]
Term adjustment:      [-X% for multi-year commitment]
Payment adjustment:   [-X% for annual upfront payment]
Strategic adjustment: [-X% for strategic value (case study, reference, co-marketing)]
                      ─────────────────────────
Net price:            [Final negotiated price]
Effective discount:   [Total discount % from list]
Floor check:          [Is net price above minimum floor? Y/N]
Approval required:    [Based on discount level: AE / Manager / VP / CRO / CEO]
```

---

## Price Page Design Principles

### Layout Best Practices

**1. Show 3-4 tiers maximum**
- Fewer than 3: no anchoring effect, limited self-selection
- More than 4: decision fatigue, comparison paralysis
- Sweet spot: 3 tiers for most B2B SaaS, 4 if you include Free

**2. Highlight the recommended tier**
- Use visual emphasis: "Most Popular" badge, different color, larger card
- Position in the center (left-to-right reading: the center gets most attention)
- Show why it is the best value

**3. Anchor high, then offer value**
- Order tiers from highest to lowest price (left to right): Enterprise | Pro | Starter
- Alternatively, use the "highlight the middle" approach: Starter | Pro (highlighted) | Enterprise
- Both work; test which converts better for your audience

**4. Show annual pricing by default**
- Display annual price with monthly equivalent
- Show savings: "Save 20% with annual billing" or "$X/month (billed annually)"
- Include monthly option but make annual the default/prominent choice

**5. Feature comparison table below tiers**
- Expandable or below-the-fold detailed comparison
- Use checkmarks, X marks, and specific values (not just "Limited" -- say "Up to 10")
- Group features by category (Core, Advanced, Support, Security)

**6. Social proof near pricing**
- Customer logos at or near the pricing section
- "Trusted by X,000 companies" or "Used by teams at [logos]"
- Segment-specific proof: "Built for mid-market teams" with relevant logos

**7. Clear CTAs**
- Free tier or trial: "Start Free" or "Start Trial"
- Paid tiers: "Start Trial" or "Get Started" (not "Buy Now" -- too committal)
- Enterprise: "Contact Sales" or "Talk to Sales"

### Price Page Anti-Patterns

| Anti-Pattern | Why It Hurts | Fix |
|---|---|---|
| Too many tiers (5+) | Decision fatigue | Consolidate to 3-4 |
| Hidden pricing ("Contact Sales" for all tiers) | Kills self-serve conversion, frustrates buyers | Publish pricing for at least 2-3 tiers |
| Feature overload in comparison table | Overwhelming, hard to compare | Show top 8-10 features; expandable for full list |
| No recommended tier highlighted | No guidance, slower decision | Add "Most Popular" or "Best Value" badge |
| Per-seat pricing without calculator | Buyer cannot estimate cost | Add interactive price calculator |
| Monthly pricing only | Appears expensive; no commitment incentive | Show annual with savings |
| Vague feature descriptions | "Advanced analytics" means nothing | Be specific: "Custom dashboards, 50+ report templates, data export" |

---

## Worked Example: B2B SaaS 3-Tier Structure

### Scenario
**Product**: Employee onboarding and training platform
**Target**: Mid-market companies (50-2,000 employees)
**Current**: Single plan at $8/employee/month

### Step 1: Feature Inventory and Tier Assignment

| Feature | Breadth | Value | Tier |
|---|---|---|---|
| Digital onboarding checklists | 5 | 3 | Good |
| Document management / e-signatures | 5 | 3 | Good |
| Basic reporting (completion rates) | 5 | 2 | Good |
| Custom workflows | 4 | 4 | Better |
| Integrations (HRIS, Slack, etc.) | 4 | 4 | Better |
| Advanced analytics + dashboards | 3 | 4 | Better |
| Automated reminders / nudges | 4 | 3 | Better |
| AI-powered content creation | 2 | 5 | Best |
| Custom branding / white-label | 2 | 3 | Best |
| API access | 2 | 4 | Best |
| SSO / SAML / SCIM | 3 | 5 | Best |
| Dedicated CSM | 1 | 4 | Best |
| SLA guarantee | 1 | 4 | Best |
| Compliance tracking (SOC2, GDPR) | 2 | 5 | Best |

### Step 2: Tier Definition

| | Essentials | Professional | Enterprise |
|---|---|---|---|
| **Price** | $5/employee/mo | $10/employee/mo | $16/employee/mo |
| **Minimum** | 50 employees | 50 employees | 200 employees |
| **Billing** | Monthly or annual | Annual (monthly +20%) | Annual only |
| **Onboarding checklists** | Yes | Yes | Yes |
| **Document management** | Yes | Yes | Yes |
| **E-signatures** | Yes | Yes | Yes |
| **Reporting** | Basic | Advanced + dashboards | Custom + export |
| **Workflows** | 3 templates | Unlimited custom | Unlimited + API |
| **Integrations** | 3 core (email, calendar, Slack) | 15+ (HRIS, ATS, LMS) | Unlimited + custom |
| **Reminders** | Manual | Automated | Automated + AI-triggered |
| **AI content** | No | No | Yes |
| **Branding** | Standard | Custom colors/logo | Full white-label |
| **Security** | 2FA | 2FA + SSO | SSO + SAML + SCIM + audit |
| **Compliance** | No | Basic | Full (SOC2, GDPR, HIPAA) |
| **Support** | Email (48hr) | Priority email + chat (4hr) | Dedicated CSM + phone (1hr) |
| **SLA** | 99.5% uptime | 99.9% uptime | 99.95% + financial SLA |
| **Onboarding** | Self-serve docs | Guided setup (2 sessions) | Full implementation (dedicated PM) |

### Step 3: Price Ratios and Psychology

- Essentials : Professional : Enterprise = 1x : 2x : 3.2x (slightly accelerating)
- Professional is the target tier (highlighted as "Most Popular")
- Enterprise anchor makes Professional feel affordable
- Essentials prevents low-end churn (gives budget-constrained buyers an option)

### Step 4: Projected Distribution and Revenue

| Tier | % of Customers | Avg Employees | Monthly Revenue / Customer | ARR / Customer |
|---|---|---|---|---|
| Essentials | 25% | 75 | $375 | $4,500 |
| Professional | 55% | 150 | $1,500 | $18,000 |
| Enterprise | 20% | 500 | $8,000 | $96,000 |

**Blended metrics** (for 200 customers):
- Essentials: 50 customers x $4,500 = $225,000 ARR
- Professional: 110 customers x $18,000 = $1,980,000 ARR
- Enterprise: 40 customers x $96,000 = $3,840,000 ARR
- **Total: $6,045,000 ARR**
- **Blended ARPU: $30,225/year ($2,519/month)**

---

## Worked Example: Consumer Subscription Bundles

### Scenario
**Product**: Personal finance app with budgeting, investing, and credit monitoring
**Target**: US consumers, 25-45 years old
**Current**: Single plan at $9.99/month

### Bundle Architecture

| | Free | Plus ($7.99/mo) | Premium ($14.99/mo) | Family ($19.99/mo) |
|---|---|---|---|---|
| **Budgeting** | Basic (3 accounts) | Unlimited accounts | Unlimited | Unlimited, 5 members |
| **Bill tracking** | Manual | Automatic | Automatic | Automatic, shared |
| **Investing** | View only | Basic portfolio tracking | Advanced + recommendations | Advanced, 5 portfolios |
| **Credit monitoring** | Score only (monthly) | Score + report (weekly) | Real-time + alerts | Real-time, all members |
| **Goals** | 1 goal | 5 goals | Unlimited | Unlimited, shared |
| **Reports** | Monthly summary | Weekly + monthly | Custom + tax reports | Custom, per member |
| **Ads** | Yes | No | No | No |
| **Support** | Community | Email | Priority + chat | Priority + chat |

### Pricing Psychology Applied

1. **Anchoring**: Family plan at $19.99 makes Premium at $14.99 feel reasonable
2. **Charm pricing**: $7.99, $14.99, $19.99 (just below round numbers)
3. **Loss aversion**: Free tier shows investing insights as "locked" -- user sees what they are missing
4. **Annual incentive**: Annual pricing at $59.99/year for Plus (save $35.89 = 37% discount), $119.99 for Premium (save $59.89)
5. **Framing**: "Less than $0.50/day" for Premium; "Less than $0.14/day per family member" for Family

### Conversion Funnel Targets

| Stage | Target Rate | Trigger |
|---|---|---|
| Sign-up to Free | 40% of visitors | Low-friction onboarding |
| Free to Plus | 6% within 90 days | Ad removal + credit report access |
| Free to Premium | 3% within 90 days | Investment recommendations trigger |
| Plus to Premium | 15% within 12 months | Investment feature engagement |
| Premium to Family | 10% within 12 months | Life event (marriage, kids, shared finances) |
| Monthly to Annual | 40% at first renewal | Prominent annual savings at renewal prompt |
