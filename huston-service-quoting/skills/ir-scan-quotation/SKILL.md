---
name: ir-scan-quotation
description: Create infrared scanning service quotations for electrical equipment thermal imaging surveys. Trigger with "quote IR scan", "infrared scan quotation", "thermal imaging quote", "price IR survey", "electrical thermography quote".
---

# IR Scan Quotation Specialist

Build professional infrared (IR) scanning service quotations for Huston Electric, Inc. Infrared thermography identifies hot spots in electrical equipment before they cause failures, fires, or downtime. This skill covers equipment surveys, panel scanning, reporting, and follow-up repair quotations. Works standalone with manual input, supercharged with knowledge base for past IR scan jobs and standard pricing.

## Connectors (Optional)

| Connector | What It Adds |
|-----------|--------------|
| **Knowledge Base (Past Quotes)** | Reference pricing from similar IR scan jobs |
| **Document Generation** | Generate branded PDF quotation and IR reports |
| **CRM** | Pull customer info, track annual scan schedules |

> **No connectors?** Describe the facility and equipment count. I will build a quotation using standard IR scan pricing.

---

## How It Works

```
┌──────────────────────────────────────────────────────────────────────────┐
│                   IR SCAN QUOTATION SPECIALIST                          │
├──────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  Step 1: ASSESS FACILITY                                                 │
│  - Number and type of electrical panels                                │
│  - Switchgear, MCCs, transformers, disconnects                        │
│  - Number of buildings / locations                                     │
│  - Voltage levels (120/208, 277/480, medium voltage)                  │
│                                                                          │
│  Step 2: DETERMINE SCAN SCOPE                                            │
│  - Full facility survey vs. targeted panels                           │
│  - Load requirements (equipment must be under load)                   │
│  - Access and scheduling (production hours, off-hours)                │
│  - PPE and arc flash requirements                                     │
│                                                                          │
│  Step 3: CALCULATE PRICING                                               │
│  - Base fee per scan visit                                             │
│  - Per-panel / per-equipment charges                                   │
│  - Report generation and delivery                                     │
│  - Travel time (if applicable)                                        │
│                                                                          │
│  Step 4: GENERATE QUOTATION                                              │
│  - Detailed scope of scan services                                    │
│  - Pricing breakdown                                                   │
│  - Report deliverables description                                    │
│  - Scheduling and access requirements                                 │
│                                                                          │
└──────────────────────────────────────────────────────────────────────────┘
```

---

## IR Scan Pricing Standards

### Per-Panel Pricing Model

| Equipment Type | Price Per Unit | Scan Time | Notes |
|---------------|---------------|-----------|-------|
| Distribution panel (120/208V) | $75-$125 | 15-20 min | Includes all breakers |
| Distribution panel (277/480V) | $100-$150 | 15-25 min | Higher voltage, more detail |
| Main switchboard | $150-$250 | 20-30 min | Multiple sections |
| Motor control center (MCC) | $200-$400 | 30-60 min | Per MCC lineup |
| Transformer (dry type) | $75-$125 | 10-15 min | Connections and body |
| Transformer (oil-filled) | $100-$175 | 15-20 min | Includes bushing scan |
| Disconnect switch | $40-$60 | 5-10 min | Each disconnect |
| Bus duct (per section) | $50-$100 | 10-15 min | Per accessible section |
| Medium voltage switchgear | $250-$500 | 30-45 min | 5kV-15kV class |
| Generator/ATS | $100-$200 | 15-25 min | Transfer switch connections |

### Minimum Charges

| Service | Minimum | Notes |
|---------|---------|-------|
| IR scan visit (local, <25 mi) | $500 | Includes first 4 panels |
| IR scan visit (remote, 25-75 mi) | $750 | Includes travel, first 4 panels |
| IR scan visit (distant, >75 mi) | $1,000+ | Travel + per-panel |
| Report generation | Included | Standard report with all scans |
| Emergency/priority scan | 1.5x standard | Within 48 hours |

---

## Report Deliverables

Every IR scan quotation includes the following report:

```
IR SCAN REPORT CONTENTS:
1. Executive summary with overall facility condition rating
2. Equipment inventory — all items scanned with location
3. Thermal images — each piece of equipment, annotated
4. Findings table:
   - Location and equipment ID
   - Phase/connection with anomaly
   - Temperature reading (absolute and delta-T)
   - Severity classification (Minor / Intermediate / Serious / Critical)
   - Recommended action and priority
5. Comparison to previous scan (if annual program)
6. Priority repair recommendations with estimated costs
7. Thermographer certification and camera calibration info
```

### Severity Classifications (NETA/NFPA 70B)

| Classification | Delta-T | Action Required | Timeframe |
|---------------|---------|-----------------|-----------|
| **Minor** | 1-10 deg C above baseline | Monitor, schedule repair at convenience | 6-12 months |
| **Intermediate** | 10-25 deg C above baseline | Repair at next scheduled outage | 1-3 months |
| **Serious** | 25-40 deg C above baseline | Repair as soon as possible | 1-4 weeks |
| **Critical** | >40 deg C above baseline or >100 deg C | Immediate action required | Immediate |

---

## Output Format

```markdown
# HUSTON ELECTRIC, INC.
## INFRARED SCANNING SERVICE QUOTATION

**Quotation #:** HE-IR-[YYYY]-[NNNN]
**Date:** [Date]
**Valid Until:** [Date + 30 days]
**Prepared By:** [Estimator Name]

---

### CUSTOMER INFORMATION

| | |
|---|---|
| **Customer:** | [Company/Name] |
| **Facility:** | [Facility Name / Address] |
| **Contact:** | [Contact Name / Phone / Email] |

---

### SCOPE OF SERVICES

Huston Electric, Inc. will perform a comprehensive infrared thermographic survey
of the following electrical equipment at the above facility:

**Equipment to be scanned:**
| # | Equipment | Location | Voltage | Qty |
|---|-----------|----------|---------|-----|
| 1 | [Panel/Switchgear] | [Building/Room] | [V] | [X] |
| 2 | [Panel/Switchgear] | [Building/Room] | [V] | [X] |

**Total equipment items:** [X]

**Survey includes:**
- Infrared thermal imaging of all accessible electrical connections
- Digital photographs of each piece of equipment
- Temperature measurements of all connections under load
- Comparison to previous survey (if available)
- Detailed report with findings, severity ratings, and recommendations

---

### PRICING

| Item | Quantity | Unit Price | Total |
|------|----------|------------|-------|
| IR scan — distribution panels (120/208V) | [X] | $[X.XX] | $[X.XX] |
| IR scan — distribution panels (277/480V) | [X] | $[X.XX] | $[X.XX] |
| IR scan — switchboard/switchgear | [X] | $[X.XX] | $[X.XX] |
| IR scan — transformers | [X] | $[X.XX] | $[X.XX] |
| IR scan — disconnects | [X] | $[X.XX] | $[X.XX] |
| IR scan — MCC lineups | [X] | $[X.XX] | $[X.XX] |
| Report generation and delivery | 1 | Included | Included |
| Travel (if applicable) | — | — | $[X.XX] |
| **TOTAL** | | | **$[X.XX]** |

---

### REQUIREMENTS AND SCHEDULING

1. **Load requirement:** Equipment must be under normal operating load during the scan.
   Minimum 40% of rated load is required for meaningful thermal data.
2. **Access:** All panel covers and equipment doors must be accessible. Covers will be
   removed and replaced by Huston Electric during the scan.
3. **Escort:** Customer to provide an escort familiar with equipment locations.
4. **Arc flash:** Customer to provide arc flash study and PPE requirements for equipment
   rated above 240V. If no arc flash study exists, Huston Electric will use NFPA 70E
   Table 130.7(C)(15)(a) default categories.
5. **Scheduling:** Scans should be performed during normal production hours when equipment
   is under load. Off-hours scans are available at premium rates if equipment load
   can be maintained.
6. **Report delivery:** Written report delivered within [5-10] business days of scan.

---

### IR-SPECIFIC TERMS

1. This quotation covers infrared scanning and reporting only.
2. Repairs identified during scanning are quoted separately.
3. Camera: [FLIR/equivalent] thermal imaging camera, calibrated annually.
4. Thermographer: Level [I/II] certified per ASNT SNT-TC-1A.
5. Findings classified per NETA MTS and NFPA 70B severity standards.
6. Annual scanning programs available at discounted rates — ask about EMP proposals.

### ACCEPTANCE

Customer Signature: _________________________ Date: ___________
Printed Name: _________________________

Huston Electric, Inc. | [Phone] | [License #]
```

---

## Annual IR Scan Programs

For repeat customers, offer annual scan programs at discounted pricing:

```
ANNUAL PROGRAM PRICING:
  Single scan: Standard pricing
  Annual program (1 scan/year): 10% discount
  Semi-annual program (2 scans/year): 15% discount
  Quarterly program (4 scans/year): 20% discount

  Programs include:
  - Year-over-year trending and comparison reports
  - Priority scheduling
  - Discounted repair pricing for identified issues
  - Compliance documentation for insurance
```

---

## Related Skills

- **electrical-quotation** — Quote repairs identified during IR scans
- **emp-proposal** — Include IR scanning in Electrical Maintenance Programs
- **contract-generation** — Annual IR scan service contracts
