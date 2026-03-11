---
name: generator-quotation
description: Create generator installation and service quotations with sizing guidance, transfer switch selection, and budgetary or firm pricing. Trigger with "quote generator", "generator estimate", "price standby generator", "generator installation quote", "backup power quotation".
---

# Generator Quotation Specialist

Build professional generator installation and service quotations for Huston Electric, Inc. This skill covers standby generator sizing, automatic transfer switch selection, installation labor, fuel system connections, and ongoing maintenance. Supports both budgetary quotations (for planning) and firm quotations (for commitment). Works standalone with manual input, supercharged with knowledge base for past generator jobs and current equipment pricing.

## Connectors (Optional)

| Connector | What It Adds |
|-----------|--------------|
| **Knowledge Base (Past Quotes)** | Reference similar past generator installations |
| **Knowledge Base (Materials)** | Current generator and ATS pricing from distributors |
| **Document Generation** | Generate branded PDF quotation |
| **CRM** | Pull customer info, log quotation |

> **No connectors?** Describe the generator need and I will build a complete quotation using standard installation labor and ask you for equipment costs.

---

## How It Works

```
┌──────────────────────────────────────────────────────────────────────────┐
│                   GENERATOR QUOTATION SPECIALIST                        │
├──────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  Step 1: DETERMINE REQUIREMENTS                                         │
│  - Load analysis (whole-house, critical loads, full facility)          │
│  - Generator sizing (kW rating)                                        │
│  - Fuel type (natural gas, LP, diesel)                                 │
│  - Transfer switch type (automatic, manual, service-rated)             │
│                                                                          │
│  Step 2: SELECT EQUIPMENT                                                │
│  - Generator unit (brand, model, kW)                                   │
│  - Automatic transfer switch (ATS) rating and type                     │
│  - Concrete pad or mounting requirements                               │
│  - Fuel system components                                               │
│                                                                          │
│  Step 3: CALCULATE INSTALLATION LABOR                                    │
│  - Site preparation (pad, mounting, clearances)                        │
│  - Electrical connections (ATS, feeder, load circuits)                 │
│  - Gas/fuel piping coordination                                        │
│  - Start-up, testing, and commissioning                                │
│  - Permit and inspection coordination                                  │
│                                                                          │
│  Step 4: BUILD QUOTATION                                                 │
│  - Budgetary format (range pricing for planning)                       │
│  - Firm format (fixed price for commitment)                            │
│  - Include all equipment, labor, and ancillary costs                   │
│                                                                          │
│  Step 5: GENERATE AND DELIVER                                            │
│  - Format quotation document                                           │
│  - Include generator-specific terms and warranty                       │
│  - Note permit, gas, and inspection requirements                       │
│                                                                          │
└──────────────────────────────────────────────────────────────────────────┘
```

---

## Generator Sizing Guide

| Application | Typical Size | Notes |
|-------------|-------------|-------|
| Residential — critical loads only | 10-14 kW | Furnace, fridge, sump, some lights |
| Residential — whole house (small) | 16-20 kW | Up to 200A service |
| Residential — whole house (large) | 22-26 kW | Large homes, 200A+ service |
| Small commercial | 25-50 kW | Office, small retail |
| Medium commercial | 50-150 kW | Restaurant, mid-size facility |
| Large commercial / industrial | 150-500+ kW | Warehouse, manufacturing, data center |

**Sizing calculation:**
```
1. List all loads to be powered (in watts or amps)
2. Apply demand factors per NEC 220
3. Add 20-25% safety factor
4. Select next standard generator size up
5. Verify fuel consumption is acceptable
```

---

## Transfer Switch Selection

| Type | Application | Typical Cost Range |
|------|-------------|-------------------|
| Service-rated ATS (200A) | Residential whole-house | $1,200-$2,500 |
| Load-center ATS (100A) | Residential critical loads | $800-$1,500 |
| Standard ATS (100-200A) | Small commercial | $2,000-$4,500 |
| Standard ATS (400-800A) | Medium commercial | $5,000-$15,000 |
| Bypass isolation ATS | Critical facilities | $8,000-$25,000 |
| Manual transfer switch | Budget / simple applications | $300-$800 |

---

## Installation Labor Standards

| Task | Labor Hours | Crew Size | Notes |
|------|-------------|-----------|-------|
| Concrete pad (pre-poured, set generator) | 2.0-4.0 | 2 | Does not include concrete work |
| Set generator on pad (small, <25 kW) | 2.0-3.0 | 2 | Includes leveling, anchoring |
| Set generator on pad (large, 25-100 kW) | 4.0-6.0 | 2-3 | May require machinery |
| Install ATS (service-rated, 200A) | 6.0-10.0 | 2 | Includes feeder rework |
| Install ATS (load-center, 100A) | 4.0-6.0 | 1-2 | Adjacent to existing panel |
| Install ATS (400A+) | 10.0-16.0 | 2-3 | Switchgear modification |
| Run feeder — generator to ATS (per 25 ft) | 1.5-2.5 | 2 | Size-dependent |
| Gas connection coordination | 1.0-2.0 | 1 | Coordinate with plumber/gas co. |
| Battery install and wiring | 0.50 | 1 | Start battery |
| Exercise timer programming | 0.50 | 1 | Weekly exercise schedule |
| Start-up and commissioning | 2.0-4.0 | 1-2 | Load test, verify ATS operation |
| Final inspection coordination | 1.0-2.0 | 1 | Meet inspector, demonstrate |
| Customer orientation | 0.50-1.0 | 1 | Explain operation, maintenance |

---

## Budgetary Quotation Format

Use this format when the customer needs a planning estimate, not a firm commitment.

```markdown
# HUSTON ELECTRIC, INC.
## BUDGETARY GENERATOR QUOTATION

**Quotation #:** HE-GEN-[YYYY]-[NNNN]
**Date:** [Date]
**Prepared By:** [Estimator Name]

** * * BUDGETARY ESTIMATE — NOT A FIRM QUOTATION * * **

This budgetary quotation is provided for planning and budgeting purposes only.
A firm quotation will be provided after site survey and final equipment selection.

---

### PROJECT OVERVIEW

| | |
|---|---|
| **Customer:** | [Company/Name] |
| **Location:** | [Address] |
| **Application:** | [Residential / Commercial / Industrial] |
| **Generator Size:** | [X] kW |
| **Fuel Type:** | [Natural Gas / LP / Diesel] |
| **Transfer Type:** | [Automatic / Manual] |

---

### BUDGETARY PRICING

| Component | Estimated Range |
|-----------|----------------|
| Generator unit ([brand] [X] kW) | $[low] — $[high] |
| Automatic transfer switch ([X]A) | $[low] — $[high] |
| Concrete pad | $[low] — $[high] |
| Electrical installation labor | $[low] — $[high] |
| Feeder cable and conduit | $[low] — $[high] |
| Gas piping (by others) | $[low] — $[high] |
| Permits and inspections | $[low] — $[high] |
| **BUDGETARY TOTAL** | **$[low] — $[high]** |

---

### NOTES

1. This budgetary estimate is based on typical installations of this size.
2. Actual pricing may vary based on site conditions, equipment selection, and code requirements.
3. Gas piping is typically performed by a licensed plumber and is quoted separately.
4. Concrete pad work is typically by a concrete contractor and may be quoted separately.
5. A site survey is required before a firm quotation can be provided.
6. Equipment lead times are currently [X] weeks — early ordering recommended.

### NEXT STEPS

To proceed toward a firm quotation:
1. Schedule a site survey (no charge)
2. Finalize equipment selection
3. Receive firm quotation within [X] business days of survey
```

---

## Firm Quotation Format

```markdown
# HUSTON ELECTRIC, INC.
## GENERATOR INSTALLATION QUOTATION

**Quotation #:** HE-GEN-[YYYY]-[NNNN]
**Date:** [Date]
**Valid Until:** [Date + 30 days]
**Prepared By:** [Estimator Name]

---

### CUSTOMER INFORMATION

| | |
|---|---|
| **Customer:** | [Company/Name] |
| **Site Address:** | [Address] |

---

### SCOPE OF WORK

[Detailed description of generator installation scope]

---

### EQUIPMENT

| Item | Description | Cost |
|------|-------------|------|
| Generator | [Brand] [Model] [kW] [Fuel] | $[X.XX] |
| Transfer Switch | [Brand] [Model] [Rating]A ATS | $[X.XX] |
| Battery | Start battery with rack | $[X.XX] |
| Pad | [Pre-cast / Poured] concrete pad | $[X.XX] |
| **Equipment Total** | | **$[X.XX]** |

### INSTALLATION LABOR

| Task | Hours | Cost |
|------|-------|------|
| Set and anchor generator | [X.X] | $[X.XX] |
| Install ATS | [X.X] | $[X.XX] |
| Feeder — gen to ATS | [X.X] | $[X.XX] |
| Circuit modifications | [X.X] | $[X.XX] |
| Start-up and commissioning | [X.X] | $[X.XX] |
| **Labor Total** ([X.X] hrs @ $[rate]/hr) | | **$[X.XX]** |

### ADDITIONAL COSTS

| Item | Cost |
|------|------|
| Electrical permit | $[X.XX] |
| Gas piping (by others / included) | $[X.XX] |
| **Additional Total** | **$[X.XX]** |

---

### COST SUMMARY

| Category | Amount |
|----------|--------|
| Equipment | $[X.XX] |
| Installation Labor | $[X.XX] |
| Additional Costs | $[X.XX] |
| Subtotal | $[X.XX] |
| Sales Tax (7% on equipment/materials) | $[X.XX] |
| **GRAND TOTAL** | **$[X.XX]** |

---

### GENERATOR-SPECIFIC TERMS

1. Equipment warranty per manufacturer terms (typically 5-year limited).
2. Installation warranty: 1 year on all Huston Electric labor.
3. Gas piping must be installed by licensed plumber per local code.
4. Customer responsible for maintaining fuel supply.
5. Generator requires annual maintenance — see maintenance agreement options.
6. All work per NEC Articles 700, 701, 702 and local amendments.
7. Equipment lead time: approximately [X] weeks from order.
8. Installation scheduled [X] weeks after equipment delivery.
9. Concrete pad must cure minimum 7 days before generator placement.

### ACCEPTANCE

Customer Signature: _________________________ Date: ___________
Printed Name: _________________________

Huston Electric, Inc. | [Phone] | [License #]
```

---

## NEC Requirements for Generators

| Requirement | NEC Reference | Detail |
|-------------|---------------|--------|
| Emergency systems | Art. 700 | Legally required standby (hospitals, egress lighting) |
| Legally required standby | Art. 701 | Fire pumps, smoke control, elevators |
| Optional standby | Art. 702 | Residential and commercial backup power |
| Transfer equipment | 700.5, 701.5, 702.5 | Prevents backfeed to utility |
| Outdoor installation | 110.26 | Working clearances around equipment |
| Grounding | 250.30 | Separately derived system grounding |
| Disconnect | 445.18 | Disconnect means required |

---

## Related Skills

- **electrical-quotation** — General electrical service quotations
- **emp-proposal** — Maintenance program proposals including generator maintenance
- **contract-generation** — Service contracts for generator maintenance agreements
