---
name: electrical-quotation
description: Create professional electrical service quotations with NECA labor standards, material pricing, and markup calculations. Trigger with "quote electrical work", "price this job", "create quotation for [customer]", "electrical estimate for [scope]", "how much to install [item]".
---

# Electrical Quotation Specialist

Build complete, professional electrical service quotations for Huston Electric, Inc. This skill calculates labor using NECA (National Electrical Contractors Association) labor unit standards, prices materials from the knowledge base or user input, applies configurable markups, and generates a formatted quotation document. Works standalone with manual input and NECA reference tables, supercharged when you connect your knowledge base, document generation, and CRM tools.

## Connectors (Optional)

| Connector | What It Adds |
|-----------|--------------|
| **Knowledge Base (NECA)** | Automated NECA labor unit lookups for each task |
| **Knowledge Base (Materials)** | Real-time material cost lookups from supplier pricing |
| **Knowledge Base (Past Quotes)** | Reference similar past quotations for pricing consistency |
| **Document Generation** | Generate branded PDF quotations automatically |
| **Email** | Send quotation directly to customer |
| **CRM** | Pull customer info, log quotation, track status |

> **No connectors?** No problem. Describe the scope of work and I will use NECA reference tables built into this skill and ask you for material costs. Output is formatted text you can copy into your quotation template.

---

## How It Works

```
┌──────────────────────────────────────────────────────────────────────────┐
│                    ELECTRICAL QUOTATION SPECIALIST                       │
├──────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  Step 1: PARSE REQUEST                                                   │
│  - Identify customer, location, scope of work                           │
│  - Determine quotation type (T&M, fixed price, budgetary)              │
│  - Check for special conditions (emergency, overtime, prevailing wage)  │
│                                                                          │
│  Step 2: RESEARCH (if connectors available)                             │
│  - ~~past quotations: Find similar past jobs for pricing reference      │
│  - ~~CRM: Pull customer info, site history, contact details            │
│  - ~~neca manual: Look up labor units for each task                    │
│                                                                          │
│  Step 3: BUILD LINE ITEMS                                                │
│  - Break scope into individual tasks                                    │
│  - Assign NECA labor units to each task                                 │
│  - Calculate labor hours (quantity x NECA units)                        │
│  - Price materials for each line item                                   │
│                                                                          │
│  Step 4: CALCULATE PRICING                                               │
│  - Labor: hours x labor rate ($92/hr standard)                         │
│  - Materials: cost x markup (40% standard)                             │
│  - Equipment rental (if applicable)                                     │
│  - Subtotals, sales tax, grand total                                   │
│                                                                          │
│  Step 5: GENERATE QUOTATION                                              │
│  - Format professional quotation document                               │
│  - Include terms and conditions                                         │
│  - Add NEC code references where applicable                            │
│                                                                          │
│  Step 6: DELIVER                                                         │
│  - ~~document generation: Create branded PDF                           │
│  - ~~email: Send to customer                                           │
│  - ~~CRM: Log quotation and update opportunity                         │
│  - Output to user (always)                                              │
│                                                                          │
└──────────────────────────────────────────────────────────────────────────┘
```

---

## Output Format

```markdown
# HUSTON ELECTRIC, INC.
## SERVICE QUOTATION

**Quotation #:** HE-[YYYY]-[NNNN]
**Date:** [Date]
**Valid Until:** [Date + 30 days]
**Prepared By:** [Estimator Name] | [Phone] | [Email]

---

### CUSTOMER INFORMATION

| | |
|---|---|
| **Customer:** | [Company/Name] |
| **Contact:** | [Contact Name] |
| **Address:** | [Service Address] |
| **Phone:** | [Phone] |
| **Email:** | [Email] |
| **PO #:** | [If provided] |

---

### SCOPE OF WORK

[Narrative description of the work to be performed, including location details,
access requirements, and any special conditions.]

---

### PRICING DETAIL

| # | Description | Qty | Unit | NECA Labor Units | Labor Hrs | Labor Cost | Material Cost | Line Total |
|---|-------------|-----|------|------------------|-----------|------------|---------------|------------|
| 1 | [Task description] | [X] | EA | [X.X] | [X.X] | $[X.XX] | $[X.XX] | $[X.XX] |
| 2 | [Task description] | [X] | EA | [X.X] | [X.X] | $[X.XX] | $[X.XX] | $[X.XX] |
| 3 | [Task description] | [X] | EA | [X.X] | [X.X] | $[X.XX] | $[X.XX] | $[X.XX] |

---

### COST SUMMARY

| Category | Amount |
|----------|--------|
| **Total Labor** ([X.X] hrs @ $[rate]/hr) | $[X.XX] |
| **Total Materials** (cost + [X]% markup) | $[X.XX] |
| **Equipment Rental** | $[X.XX] |
| **Permits** | $[X.XX] |
| **Subtotal** | $[X.XX] |
| **Sales Tax** ([X]% on materials) | $[X.XX] |
| **GRAND TOTAL** | **$[X.XX]** |

---

### TERMS AND CONDITIONS

1. **Validity:** This quotation is valid for 30 days from the date above.
2. **Payment Terms:** Net 30 from date of invoice.
3. **Warranty:** One (1) year warranty on labor and materials from date of completion.
4. **Permits:** [Included / Not included — customer responsibility].
5. **Work Hours:** Standard hours are Monday-Friday, 7:00 AM - 3:30 PM. Overtime rates apply outside these hours.
6. **Change Orders:** Additional work beyond this scope requires a written change order.
7. **Access:** Customer shall provide clear access to all work areas. Delays caused by restricted access may result in additional charges.
8. **Code Compliance:** All work performed in accordance with the current National Electrical Code (NEC) and local amendments.
9. **Insurance:** Huston Electric, Inc. maintains general liability and workers compensation insurance. Certificates available upon request.
10. **Cancellation:** 24-hour notice required for scheduled work. Same-day cancellations subject to a trip charge.

---

### ACCEPTANCE

By signing below, Customer authorizes Huston Electric, Inc. to proceed with the work described above at the quoted price.

Customer Signature: _________________________ Date: ___________

Printed Name: _________________________

Title: _________________________

PO Number: _________________________

---

Huston Electric, Inc.
[Address] | [Phone] | [License #]
```

---

## Execution Flow

### Step 1: Parse Request

```
Input patterns:
- "Quote a 200A panel upgrade at 123 Main St for Acme Corp"
  → Customer: Acme Corp, Location: 123 Main St, Scope: 200A panel upgrade
- "How much to install 20 duplex receptacles in a new office?"
  → Scope: 20 duplex receptacles, Type: new construction
- "Price this job: replace 100A panel, add 4 circuits, install 2 ceiling fans"
  → Scope: panel replacement + circuits + ceiling fans (multi-task)
- "Budgetary quote for lighting retrofit, 50 fixtures"
  → Type: budgetary, Scope: lighting retrofit 50 fixtures
```

**Determine quotation type:**
- **Fixed Price** — Standard; firm commitment with defined scope
- **Time & Material (T&M)** — When scope is uncertain; quote hourly rate + material markup
- **Budgetary** — For planning purposes; clearly marked as estimate, not a firm commitment
- **Emergency** — After-hours or urgent; emergency labor rates apply

### Step 2: Research Materials and Past Quotes

**If knowledge base connected:**
```
1. ~~past quotations: Search for similar scope of work
   - Pull: pricing from comparable past jobs
   - Use as: sanity check on current pricing

2. ~~neca manual: Look up labor units for each task
   - Query: task description (e.g., "install duplex receptacle")
   - Pull: NECA labor unit value

3. ~~material pricing: Look up current costs
   - Query: each material item
   - Pull: current distributor pricing
```

**If no knowledge base:**
```
1. Use NECA reference tables in this skill (see below)
2. Ask user for material costs they cannot provide
3. Use industry-standard estimates where appropriate
```

### Step 3: Calculate Labor Using NECA Manual

**NECA labor units represent the decimal hours to complete one unit of work under standard conditions.**

```
Labor Hours = Quantity x NECA Labor Unit

Example:
  10 duplex receptacles x 0.45 labor units each = 4.5 labor hours
```

**Adjustment factors (apply as multipliers to NECA base units):**

| Condition | Factor |
|-----------|--------|
| Standard new construction | 1.00 |
| Existing construction (open walls) | 1.10 |
| Existing construction (finished walls) | 1.30-1.50 |
| Height above 10 ft | 1.10-1.25 |
| Height above 15 ft | 1.25-1.50 |
| Confined space | 1.30-1.50 |
| Outdoor work | 1.10-1.20 |
| Hazardous environment | 1.25-1.50 |
| After-hours/weekend | 1.00 (rate changes, not units) |

### Step 4: Look Up Material Pricing

```
Material Cost = Distributor/Supplier Cost (net cost to us)
Quoted Material Price = Material Cost x (1 + Markup Percentage)

Standard markup: 40%
Example:
  Panel cost: $450.00
  Quoted price: $450.00 x 1.40 = $630.00
```

**Always include:**
- Main equipment (panels, fixtures, devices)
- Wire and cable (calculate footage + 10% waste)
- Conduit and fittings (if required)
- Boxes, covers, connectors
- Fasteners and mounting hardware
- Miscellaneous consumables (tape, wire nuts, labels)

### Step 5: Apply Markups and Rates

```
LABOR CALCULATION:
  Total Labor Hours x Labor Rate = Total Labor Cost
  Standard rate: $92/hr
  Overtime rate: $138/hr (1.5x)
  Emergency rate: $184/hr (2x)

MATERIAL CALCULATION:
  Total Material Cost (net) x 1.40 = Total Material Price (quoted)

EQUIPMENT RENTAL (if applicable):
  Rental cost x 1.15 = Quoted equipment cost (15% markup)

SUBCONTRACTOR (if applicable):
  Sub cost x 1.15 = Quoted sub cost (15% markup)

TAX:
  Materials are taxable (7% Indiana sales tax)
  Labor is NOT taxable in Indiana

GRAND TOTAL:
  Labor + Materials (with markup) + Equipment + Permits + Tax
```

### Step 6: Generate Formatted Quotation

```
1. Assemble all line items into pricing table
2. Calculate all subtotals and totals
3. Write scope of work narrative
4. Apply terms and conditions
5. Add NEC code references where applicable
6. Format using output template above
```

### Step 7: Create Document and Deliver

```
If ~~document generation available:
  1. Generate branded PDF with company logo and formatting
  2. Return document link

If ~~email available:
  1. Attach PDF to email
  2. Draft cover message to customer
  3. Send or create draft for review

If ~~CRM available:
  1. Create quotation record
  2. Link to customer/opportunity
  3. Set follow-up reminder

Always:
  1. Output formatted quotation text to user
  2. Include internal pricing notes (cost vs. quoted)
```

---

## NECA Labor Unit Reference Guide

Common electrical tasks and their approximate NECA labor units (decimal hours per unit). These are baseline values — apply adjustment factors from Step 3 for site conditions.

### Panels and Switchgear

| Task | NECA Unit | Notes |
|------|-----------|-------|
| Install 100A panel (surface) | 4.50 | Does not include circuits |
| Install 200A panel (surface) | 6.00 | Does not include circuits |
| Install 400A panel (surface) | 8.50 | Does not include circuits |
| Install 100A panel (flush) | 5.50 | Add 1.0 for cutting opening |
| Install 200A panel (flush) | 7.00 | Add 1.0 for cutting opening |
| Connect panel feeder (per wire) | 0.30 | Size-dependent; base is #1 AWG |
| Install breaker (1-pole) | 0.25 | Bolt-on; add 0.10 for plug-on |
| Install breaker (2-pole) | 0.35 | Bolt-on |
| Install breaker (3-pole) | 0.50 | Bolt-on |

### Receptacles and Devices

| Task | NECA Unit | Notes |
|------|-----------|-------|
| Install duplex receptacle (new const.) | 0.45 | Includes box, device, plate |
| Install duplex receptacle (existing) | 0.70 | Open wall |
| Install duplex receptacle (finished wall) | 1.20 | Fish wire, cut-in box |
| Install GFCI receptacle | 0.55 | New construction |
| Install 20A dedicated circuit receptacle | 0.55 | New construction |
| Install 30A/50A receptacle (dryer/range) | 1.00 | Includes box and plate |
| Install single-pole switch | 0.40 | Includes box, device, plate |
| Install 3-way switch | 0.50 | Includes box, device, plate |
| Install dimmer switch | 0.55 | Includes box, device, plate |

### Lighting

| Task | NECA Unit | Notes |
|------|-----------|-------|
| Install 2x4 lay-in troffer | 0.60 | Drop ceiling, standard |
| Install 2x4 LED panel | 0.50 | Drop ceiling, lighter weight |
| Install 4ft strip light (surface) | 0.55 | Chain or surface mount |
| Install recessed can (new const.) | 0.65 | IC or non-IC rated |
| Install recessed can (existing ceiling) | 1.30 | Cut opening, fish wire |
| Install wall pack (exterior) | 1.00 | Includes junction box |
| Install ceiling fan | 1.50 | Includes fan-rated box |
| Install exit sign | 0.60 | Surface or pendant mount |
| Install emergency light (combo) | 0.75 | Battery unit + heads |

### Wire and Cable

| Task | NECA Unit | Notes |
|------|-----------|-------|
| Pull wire #14-#10 (per 100 ft) | 0.80 | In conduit |
| Pull wire #8-#6 (per 100 ft) | 1.20 | In conduit |
| Pull wire #4-#2 (per 100 ft) | 1.80 | In conduit |
| Pull wire #1/0-#4/0 (per 100 ft) | 2.80 | In conduit |
| Install MC cable #12 (per 100 ft) | 1.50 | Includes connectors |
| Install Romex NM #12 (per 100 ft) | 1.00 | Stapled, residential |

### Conduit

| Task | NECA Unit | Notes |
|------|-----------|-------|
| Install 1/2" EMT (per 100 ft) | 4.00 | Includes couplings, straps |
| Install 3/4" EMT (per 100 ft) | 4.80 | Includes couplings, straps |
| Install 1" EMT (per 100 ft) | 5.80 | Includes couplings, straps |
| Install 1/2" rigid (per 100 ft) | 7.00 | Threaded |
| Install 3/4" rigid (per 100 ft) | 8.50 | Threaded |
| Install 1" rigid (per 100 ft) | 10.00 | Threaded |
| EMT 90-degree bend (1/2"-1") | 0.15-0.30 | Hand bender |

### Miscellaneous

| Task | NECA Unit | Notes |
|------|-----------|-------|
| Install disconnect switch (fused, 60A) | 1.50 | Surface mount |
| Install disconnect switch (fused, 200A) | 3.00 | Surface mount |
| Install junction box (4x4) | 0.35 | Surface mount |
| Install motor connection (up to 5 HP) | 2.00 | Includes disconnect |
| Install motor connection (5-25 HP) | 3.50 | Includes disconnect |
| Troubleshooting (per hour) | 1.00 | Diagnostic time |
| Fire alarm device (per device) | 0.75 | Smoke/heat detector |

---

## NEC Code Compliance Notes

All quotations should reference applicable NEC articles when relevant:

| Topic | NEC Reference | Key Requirement |
|-------|---------------|-----------------|
| GFCI protection | NEC 210.8 | Required in kitchens, bathrooms, garages, outdoors, basements |
| AFCI protection | NEC 210.12 | Required in bedrooms, living rooms, and most habitable rooms |
| Panel clearance | NEC 110.26 | 36" clear in front, 30" wide, headroom to ceiling |
| Grounding | NEC 250 | All circuits must be properly grounded |
| Wire sizing | NEC 310 | Ampacity tables for conductor sizing |
| Overcurrent protection | NEC 240 | Breaker sizing per conductor ampacity |
| Service entrance | NEC 230 | Service conductor requirements |
| Emergency/standby | NEC 700/701/702 | Generator and transfer switch requirements |
| Hazardous locations | NEC 500-516 | Special equipment requirements |

**Always note:** "All work performed in accordance with the current National Electrical Code (NEC) and applicable state and local amendments."

---

## Pricing Calculation Formulas

```
FOR EACH LINE ITEM:
  labor_hours = quantity x neca_unit x adjustment_factor
  labor_cost = labor_hours x labor_rate
  material_cost_net = quantity x unit_material_cost
  material_cost_quoted = material_cost_net x (1 + material_markup_pct / 100)
  line_total = labor_cost + material_cost_quoted

QUOTATION TOTALS:
  total_labor_hours = SUM(all line item labor_hours)
  total_labor_cost = SUM(all line item labor_cost)
  total_material_net = SUM(all line item material_cost_net)
  total_material_quoted = SUM(all line item material_cost_quoted)
  equipment_rental_quoted = equipment_rental_cost x 1.15
  subtotal = total_labor_cost + total_material_quoted + equipment_rental_quoted + permits
  sales_tax = total_material_quoted x (sales_tax_pct / 100)
  grand_total = subtotal + sales_tax

INTERNAL MARGIN CHECK:
  total_cost = total_labor_cost_at_burden + total_material_net + equipment_rental_cost
  gross_margin = (grand_total - total_cost) / grand_total x 100
  Target gross margin: 25-35% for service work
```

---

## Capability by Connector

| Capability | Standalone | + Knowledge Base | + Doc Gen | + Email | + CRM |
|------------|-----------|------------------|-----------|---------|-------|
| NECA labor lookup | Reference tables | Automated lookup | Same | Same | Same |
| Material pricing | Manual entry | Automated lookup | Same | Same | Same |
| Past quote reference | None | Search history | Same | Same | Same |
| PDF generation | Text output | Text output | Branded PDF | Same | Same |
| Send to customer | Copy/paste | Copy/paste | Copy/paste | Direct send | Same |
| Customer info | Manual entry | Manual entry | Manual entry | Manual entry | Auto-pull |
| Quotation tracking | None | None | None | None | Auto-log |

---

## Company Configuration [CUSTOMIZE]

```markdown
## Company Info
- Company name: Huston Electric, Inc.
- Address: [Your Address]
- Phone: [Your Phone]
- Email: [Your Email]
- License #: [Your License Number]
- Website: [Your Website]

## Labor Rates
- Standard rate: $92/hr
- Overtime rate: $138/hr (1.5x)
- Emergency rate: $184/hr (2x)
- Apprentice rate: $65/hr
- Helper rate: $50/hr

## Markup Percentages
- Material markup: 40%
- Subcontractor markup: 15%
- Equipment rental markup: 15%

## Tax
- Indiana sales tax: 7%
- Tax on materials: Yes
- Tax on labor: No

## Quotation Defaults
- Valid for: 30 days
- Payment terms: Net 30
- Warranty: 1 year labor and materials
- NECA edition: 2024

## Estimator
- Name: [Your Name]
- Title: [Your Title]
- Direct phone: [Your Phone]
- Email: [Your Email]
```

---

## Example

**Input:** "Quote a 200A panel upgrade for Johnson Manufacturing at 456 Industrial Blvd. Replace existing 100A panel with new 200A, add 6 new 20A circuits for machinery, install 2 GFCI receptacles in the wash bay."

**Quotation Output:**

```markdown
# HUSTON ELECTRIC, INC.
## SERVICE QUOTATION

**Quotation #:** HE-2026-0147
**Date:** March 11, 2026
**Valid Until:** April 10, 2026
**Prepared By:** Tim Reynolds | (317) 555-0101 | tim@hustonelectric.com

---

### CUSTOMER INFORMATION

| | |
|---|---|
| **Customer:** | Johnson Manufacturing |
| **Contact:** | Mike Johnson |
| **Address:** | 456 Industrial Blvd, Indianapolis, IN |

---

### SCOPE OF WORK

Huston Electric, Inc. will furnish all labor, materials, and equipment necessary to
perform the following work at the above location:

1. Remove and dispose of existing 100A electrical panel.
2. Furnish and install new 200A, 42-space main breaker panel.
3. Reconnect all existing circuits from old panel to new panel.
4. Install new 200A feeder from existing service to new panel (approximately 15 ft).
5. Furnish and install six (6) new 20A dedicated circuits for machinery, including
   conduit, wire, receptacles, and breakers. Approximate run: 75 ft average.
6. Furnish and install two (2) GFCI duplex receptacles in wash bay area, including
   weatherproof covers and in-use covers per NEC 406.9. Approximate run: 40 ft.
7. Label all new circuits in panel directory.
8. Test all circuits and verify proper operation.

---

### PRICING DETAIL

| # | Description | Qty | NECA Units | Labor Hrs | Labor ($92/hr) | Material Cost | Line Total |
|---|-------------|-----|------------|-----------|----------------|---------------|------------|
| 1 | Remove existing 100A panel | 1 | 2.00 | 2.0 | $184.00 | $0.00 | $184.00 |
| 2 | Install 200A panel (surface) | 1 | 6.00 | 6.0 | $552.00 | $686.00 | $1,238.00 |
| 3 | Reconnect existing circuits (est. 20) | 20 | 0.30 | 6.0 | $552.00 | $70.00 | $622.00 |
| 4 | 200A feeder - #4/0 AL in 2" EMT (15ft) | 1 | 3.50 | 3.5 | $322.00 | $315.00 | $637.00 |
| 5 | 20A dedicated circuits w/ receptacle (75ft avg) | 6 | 2.00 | 12.0 | $1,104.00 | $504.00 | $1,608.00 |
| 6 | GFCI receptacle w/ WP cover (40ft run) | 2 | 1.50 | 3.0 | $276.00 | $126.00 | $402.00 |
| 7 | Circuit labeling and testing | 1 | 1.50 | 1.5 | $138.00 | $14.00 | $152.00 |

---

### COST SUMMARY

| Category | Amount |
|----------|--------|
| **Total Labor** (34.0 hrs @ $92/hr) | $3,128.00 |
| **Total Materials** (cost + 40% markup) | $1,715.00 |
| **Subtotal** | $4,843.00 |
| **Sales Tax** (7% on materials) | $120.05 |
| **GRAND TOTAL** | **$4,963.05** |

---

### TERMS AND CONDITIONS

1. This quotation is valid for 30 days from the date above.
2. Payment terms: Net 30 from date of invoice.
3. One (1) year warranty on labor and materials.
4. Permits not included — customer responsibility, or Huston Electric can pull for additional fee.
5. All work per current NEC and Indiana amendments.
6. Standard work hours: Mon-Fri, 7:00 AM - 3:30 PM.
7. Customer to provide clear access to electrical room and all work areas.

---

### ACCEPTANCE

Customer Signature: _________________________ Date: ___________
Printed Name: _________________________
Title: _________________________
PO Number: _________________________

Huston Electric, Inc. | Indianapolis, IN | (317) 555-0100 | License #XXXXXXX
```

---

## Related Skills

- **sign-quotation** — Sign installation and maintenance quotations
- **generator-quotation** — Generator installation and service quotations
- **ir-scan-quotation** — Infrared scanning service quotations
- **emp-proposal** — Electrical Maintenance Program proposals
- **indy-quotation** — Indianapolis-specific quotation with standardized rates
- **contract-generation** — Produce service contracts from accepted quotations
