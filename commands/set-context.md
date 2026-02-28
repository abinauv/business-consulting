---
description: "Set the client context so all subsequent analyses are automatically tailored — store client name, industry, size, geography, and key facts"
argument-hint: "[client details: name, industry, size, etc.]"
---

# Set Client Context

Store the following client context for use in all subsequent skill invocations and commands.

## Instructions

Parse the information provided in **$ARGUMENTS** and extract:

1. **Client name:** The company or organization name
2. **Industry:** Primary industry / sub-sector
3. **Company size:** Revenue, employee count, or other size indicator
4. **Geography:** Headquarters location and operating regions
5. **Business model:** How the company makes money (SaaS, marketplace, manufacturing, services, etc.)
6. **Key products/services:** Primary offerings
7. **Key facts:** Any additional context (ownership, stage, recent events)

## Context Application

Once set, automatically apply this context in all subsequent analyses:

- **Market research:** Focus on the client's specific industry and geography
- **Competitive analysis:** Compare against competitors in the client's market
- **Financial analysis:** Use industry-appropriate metrics and benchmarks
- **Strategy frameworks:** Tailor framework selection to the client's situation
- **Benchmarking:** Select peers of similar size, industry, and geography
- **Deliverables:** Use client name in headers, tailor language to the client's industry

## Industry Overlay Selection

Based on the industry identified, automatically load the relevant industry overlay from `references/industry-overlays/`:
- Technology / SaaS → `technology-saas.md`
- Healthcare → `healthcare.md`
- Financial Services → `financial-services.md`
- Consumer / Retail → `consumer-retail.md`
- Industrial / Manufacturing → `industrial-manufacturing.md`

If the client's industry doesn't match one of the above, note which overlay is the closest fit and adapt accordingly.

## Output

After parsing, confirm the stored context by displaying:

```
CLIENT CONTEXT SET
━━━━━━━━━━━━━━━━━
Client:        [Name]
Industry:      [Industry / Sub-sector]
Size:          [Revenue / Employees]
Geography:     [HQ + Operating Regions]
Business Model: [Model type]
Key Products:  [Products/Services]
Industry Overlay: [Which overlay applies]
━━━━━━━━━━━━━━━━━
This context will be applied to all subsequent analyses.
Use /set-context again to update.
```

If any critical information is missing, ask for it. At minimum, client name and industry are required.
