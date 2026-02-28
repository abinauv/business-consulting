# Process Mapping Guide

This reference provides step-by-step instructions for creating process maps used in operations analysis engagements. Each section includes a worked example, practical tips, and common pitfalls to avoid.

---

## 1. SIPOC Diagrams

### What It Is
A SIPOC diagram is a high-level process overview that captures the Suppliers, Inputs, Process steps, Outputs, and Customers. It is the starting point for any process analysis because it frames the scope before diving into detail.

### When to Use
- At the beginning of any process improvement initiative to align stakeholders on scope
- When defining the boundaries of a DMAIC project
- When communicating a process overview to executive sponsors who do not need step-level detail

### How to Build It

**Step 1: Name the process.** Choose a clear verb-noun format (e.g., "Order-to-Cash," "Hire-to-Onboard," "Procure-to-Pay").

**Step 2: Identify the 5-7 high-level process steps.** Start with the trigger event and end with the final delivery to the customer. Avoid going below the major-phase level.

**Step 3: Identify Outputs.** What does the process produce? Include both the primary deliverable and any secondary outputs (reports, notifications, records).

**Step 4: Identify Customers.** Who receives each output? This can be an internal department, an external client, or a regulatory body.

**Step 5: Identify Inputs.** What materials, data, or resources are required to start and sustain the process?

**Step 6: Identify Suppliers.** Who provides each input?

### Worked Example: Order-to-Cash Process

| Suppliers | Inputs | Process | Outputs | Customers |
|-----------|--------|---------|---------|-----------|
| Customer | Purchase order | 1. Receive order | Confirmed order | Sales team |
| Sales team | Product catalog, pricing | 2. Validate and enter order | Order in ERP system | Warehouse |
| Warehouse | Inventory, packaging | 3. Pick, pack, and ship | Shipped package, tracking number | Customer, Logistics |
| Logistics provider | Shipping network | 4. Deliver to customer | Delivered goods, proof of delivery | Customer |
| Finance | Invoice template, payment terms | 5. Invoice customer | Invoice sent | Customer |
| Customer | Payment (check, wire, card) | 6. Receive and apply payment | Payment recorded, receipt | Finance, Customer |
| Finance | Aging report | 7. Close order and reconcile | Closed order record | Finance, Audit |

### Tips
- Complete the Process column first, then work outward to Outputs/Customers and Inputs/Suppliers.
- Keep process steps at 5-7. If you have more than 7, you are going too granular for SIPOC.
- Validate the SIPOC with the process owner before proceeding to detailed mapping.

---

## 2. Swimlane Diagrams

### What It Is
A swimlane (cross-functional) diagram maps detailed process steps organized into horizontal or vertical lanes, one per role or department. It makes handoffs between teams visually obvious, which is critical because handoffs are the most common source of delays and errors.

### When to Use
- When you need to understand who does what and where work crosses organizational boundaries
- When diagnosing handoff delays, approval bottlenecks, or accountability gaps
- As the primary "as-is" process documentation in any improvement project

### How to Build It

**Step 1: Identify the lanes.** List every role or department that touches the process. Common examples: Customer, Sales, Operations, Finance, IT, Management. Each gets its own horizontal lane.

**Step 2: Define the start and end events.** Use rounded rectangles or circles for the trigger (e.g., "Customer submits order") and the endpoint (e.g., "Order closed and reconciled").

**Step 3: Map each step as a rectangle.** Place each activity in the lane of the person/team who performs it. Use verb-noun format: "Review application," "Approve request," "Generate invoice."

**Step 4: Add decision points as diamonds.** Label each branch clearly (Yes/No, Approved/Rejected, Complete/Incomplete). Always show what happens on both paths.

**Step 5: Draw arrows for flow and handoffs.** Arrows within a lane show sequential steps. Arrows crossing lanes represent handoffs -- mark these prominently as they are friction points.

**Step 6: Annotate with data.** Add cycle time for each step, wait time between steps, error rates at key steps, and volume (transactions per day/week/month).

### Worked Example: Employee Expense Reimbursement

**Lanes:** Employee | Manager | Finance | Accounts Payable

**Flow:**
1. [Employee] Submit expense report with receipts (5 min)
2. [Wait] Average 2 days in manager queue
3. [Manager] Review expense report -- Decision: Approve or Reject?
   - If Reject: return to Employee with comments (rework loop)
   - If Approve: forward to Finance
4. [Wait] Average 1 day in Finance queue
5. [Finance] Validate against policy and budget -- Decision: Compliant?
   - If Non-compliant: return to Employee for correction (rework loop)
   - If Compliant: forward to Accounts Payable
6. [Accounts Payable] Process payment (10 min)
7. [Accounts Payable] Issue reimbursement to employee bank account
8. [Employee] Receive payment confirmation

**Key findings from the map:**
- Total lead time: 5-8 business days. Value-added time: approximately 25 minutes.
- Two rework loops create repeated delays for roughly 20% of submissions.
- Wait time in queues accounts for over 95% of total elapsed time.

### Tips
- Interview actual process participants, not just managers. The documented process and the actual process are often different.
- Always map the real process (what actually happens), not the ideal process (what should happen). The gap between them is where improvement lives.
- Use sticky notes on a whiteboard during workshops so steps can be easily rearranged.

---

## 3. Value Stream Maps

### What It Is
A value stream map (VSM) is a Lean tool that captures the entire flow of materials and information required to deliver a product or service. Unlike a simple process map, a VSM distinguishes between value-added (VA) and non-value-added (NVA) time, making waste visible.

### When to Use
- When you need to quantify how much of the total lead time is actually adding value
- When prioritizing improvement efforts across an end-to-end process
- When building the case for investment in process automation or redesign

### How to Build It

**Step 1: Define the scope.** Pick one product family or service line. Map from the trigger (customer request) to the endpoint (delivery to customer).

**Step 2: Walk the process in reverse.** Start from the customer and work backward. This ensures you map what actually happens rather than what people think happens.

**Step 3: Draw process boxes.** Each box represents a process step. Below each box, add a data box with: cycle time (CT), changeover time (CO), uptime %, batch size, number of operators, defect rate.

**Step 4: Draw inventory triangles.** Between process steps, note any queues, backlogs, or inventory buffers. Convert these to time using the formula: queue time = items in queue / throughput rate.

**Step 5: Add information flow.** Draw the information flow across the top of the map: customer orders, production schedules, supplier communications. Distinguish electronic (lightning bolt arrow) from manual (straight arrow) information flow.

**Step 6: Build the timeline.** Draw a stepped timeline along the bottom. The upper steps represent NVA time (waiting, queuing). The lower steps represent VA time (actual processing). Sum each to get total lead time and total VA time.

**Step 7: Calculate process efficiency.** Process Cycle Efficiency (PCE) = VA time / Total lead time. World-class service processes achieve 20-50%. Many organizations score below 10%.

### Worked Example: Insurance Claims Processing

| Step | Cycle Time (VA) | Queue/Wait (NVA) |
|------|-----------------|-------------------|
| Receive and log claim | 10 min | 0 (trigger) |
| Wait in assignment queue | -- | 2 days |
| Initial review and triage | 20 min | -- |
| Wait for documentation | -- | 5 days |
| Detailed investigation | 45 min | -- |
| Wait for approval queue | -- | 1.5 days |
| Manager approval | 10 min | -- |
| Wait for payment processing | -- | 1 day |
| Issue payment | 5 min | -- |

**Results:**
- Total VA time: 90 minutes (1.5 hours)
- Total NVA time: 9.5 days
- Total lead time: 9.5 days + 1.5 hours, which is approximately 9.5 days
- Process Cycle Efficiency: 1.5 hours / (9.5 days x 8 hours/day) = 1.5 / 76 = 2.0%
- Interpretation: Only 2% of the total time is spent doing actual work. The remaining 98% is waiting. This is common in service processes and represents enormous improvement potential.

### Tips
- Always validate time data with actual measurements, not estimates. People consistently underestimate wait times and overestimate processing times.
- Color-code VA steps (green) and NVA steps (red) to make waste immediately visible.
- Focus future-state improvements on the largest NVA blocks first -- that is where the biggest gains are.

---

## 4. Conducting Process Mapping Workshops

### Preparation
- Invite 6-10 participants who actually perform the work (not just managers)
- Book a room with a large whiteboard or wall space. Provide sticky notes in multiple colors, markers, and tape
- Send a brief pre-read explaining the purpose, scope, and what participants should bring (data, examples, pain points)
- Designate a facilitator (to guide) and a scribe (to document)

### During the Workshop
1. **Set context (10 min):** Explain why you are mapping the process, what will be done with the output, and how participants' input will be used.
2. **Define boundaries (10 min):** Agree on start point, end point, and scope. Use the SIPOC as a framing tool.
3. **Map the process (60-90 min):** Have participants call out steps while the facilitator places sticky notes. Encourage debate -- disagreements reveal where the real process diverges from the assumed process.
4. **Add data (30 min):** For each step, estimate cycle time, wait time, error rate, and volume. Mark where data is a guess vs. measured.
5. **Identify pain points (20 min):** Ask participants to flag their top frustrations with red dots. Cluster and prioritize.
6. **Validate and close (10 min):** Walk through the entire map once more. Confirm accuracy. Document open questions and next steps.

### After the Workshop
- Digitize the map within 48 hours while memories are fresh
- Circulate for review and corrections
- Schedule follow-up interviews to fill data gaps
- Use the validated map as the baseline for improvement analysis

---

## 5. Common Process Mapping Mistakes

### Too Much Detail
Mapping every mouse click and keystroke makes the map unusable. Match the level of detail to your purpose: SIPOC for executive communication, swimlane for process analysis, detailed work instructions for training.

### Too Little Detail
Skipping steps or glossing over decision points hides the very problems you are trying to find. If a step takes more than 30 minutes or involves a decision, it probably deserves to be broken into sub-steps.

### Missing Handoffs
Handoffs between departments are where most delays and errors occur. If your map does not clearly show every time work moves from one person or team to another, you are missing the most important information.

### Skipping Measurements
A process map without time and volume data is a picture, not an analysis tool. Always attach cycle times, wait times, volumes, and error rates. Even rough estimates are better than nothing.

### Mapping the "Should Be" Instead of the "Is"
The most common mistake. People describe the official process, not what actually happens. Workarounds, shortcuts, informal approvals, and exceptions are where the real problems live. Insist on mapping reality.

### Ignoring Rework Loops
If 15% of invoices need to be corrected and resubmitted, that rework loop must appear on the map. Rework is one of the largest sources of hidden waste and cannot be improved if it is not visible.

### Not Validating with Frontline Staff
Managers often have an incomplete or outdated view of the process. Always validate the map with the people who actually do the work every day. Their perspective will reveal steps, delays, and workarounds that no one else knows about.
