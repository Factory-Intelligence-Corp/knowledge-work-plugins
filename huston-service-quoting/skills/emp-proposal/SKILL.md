---
name: emp-proposal
description: Create comprehensive Electrical Maintenance Program (EMP) proposals for recurring preventive maintenance service, budgetary planning, and facility electrical system management. Trigger with "EMP proposal", "maintenance program quote", "preventive maintenance plan", "create maintenance proposal", "annual electrical maintenance budget".
---

# EMP (Electrical Maintenance Program) Proposal

Build comprehensive Electrical Maintenance Program proposals for Huston Electric, Inc. An EMP is a recurring service agreement covering preventive maintenance, inspections, testing, and emergency response for a customer's electrical infrastructure. This skill creates detailed proposals with scope, schedules, budgets, and deliverables for facilities of any size. Works standalone with facility descriptions, supercharged with knowledge base for past EMP proposals and standard service packages.

## Connectors (Optional)

| Connector | What It Adds |
|-----------|--------------|
| **Knowledge Base (Past Quotes)** | Reference similar EMP proposals for pricing and scope |
| **Knowledge Base (Materials)** | Maintenance supply pricing |
| **Document Generation** | Generate branded PDF proposal |
| **CRM** | Pull customer info, facility history, existing agreements |

> **No connectors?** Describe the facility and I will build a comprehensive EMP proposal using standard maintenance schedules and industry best practices.

---

## How It Works

```
┌──────────────────────────────────────────────────────────────────────────┐
│                       EMP PROPOSAL GENERATOR                            │
├──────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  Step 1: FACILITY ASSESSMENT                                             │
│  - Building size, type, and age                                        │
│  - Electrical system inventory (panels, switchgear, transformers)      │
│  - Generator and emergency systems                                     │
│  - Lighting systems (interior, exterior, emergency/exit)              │
│  - Special systems (fire alarm, security, data)                       │
│                                                                          │
│  Step 2: DEFINE SERVICE TIERS                                            │
│  - Basic: Annual inspections and IR scans                             │
│  - Standard: Quarterly visits, PM tasks, IR scans                     │
│  - Premium: Monthly visits, full PM, priority emergency response      │
│                                                                          │
│  Step 3: BUILD MAINTENANCE SCHEDULE                                      │
│  - Monthly tasks (visual inspections, testing)                        │
│  - Quarterly tasks (cleaning, tightening, IR scan)                    │
│  - Semi-annual tasks (testing, calibration)                           │
│  - Annual tasks (full survey, load testing, arc flash update)         │
│                                                                          │
│  Step 4: CALCULATE ANNUAL BUDGET                                         │
│  - Scheduled maintenance labor                                         │
│  - Materials and consumables                                           │
│  - IR scanning services                                                │
│  - Emergency response allocation                                      │
│  - Contingency for unplanned repairs                                  │
│                                                                          │
│  Step 5: GENERATE PROPOSAL                                               │
│  - Executive summary with value proposition                            │
│  - Detailed scope by service tier                                     │
│  - Annual maintenance calendar                                        │
│  - Budget breakdown with monthly/quarterly/annual view                │
│  - Terms and renewal provisions                                       │
│                                                                          │
└──────────────────────────────────────────────────────────────────────────┘
```

---

## Facility Assessment Checklist

Gather this information to build an accurate EMP proposal:

```
ELECTRICAL SYSTEM INVENTORY:
  [ ] Main service size and voltage (e.g., 800A 277/480V)
  [ ] Number of distribution panels and locations
  [ ] Number of branch circuit panels and locations
  [ ] Switchgear / switchboard count
  [ ] Transformer count and sizes
  [ ] Motor control centers (MCCs)
  [ ] Variable frequency drives (VFDs)
  [ ] Disconnects (quantity estimate)
  [ ] Generator(s) — size, fuel type, age
  [ ] Automatic transfer switch(es)
  [ ] UPS systems

LIGHTING SYSTEMS:
  [ ] Interior lighting type (LED, fluorescent, HID)
  [ ] Exterior lighting (parking lot, building, signage)
  [ ] Emergency lighting units (quantity)
  [ ] Exit signs (quantity)
  [ ] Lighting controls (photocells, timers, occupancy sensors)

SPECIAL SYSTEMS:
  [ ] Fire alarm system (type, age, monitoring)
  [ ] Security/access control
  [ ] Data/telecom rooms
  [ ] Parking lot lighting / bollards
  [ ] Specialty equipment (kitchen, medical, manufacturing)

FACILITY INFO:
  [ ] Building square footage
  [ ] Number of floors
  [ ] Building age
  [ ] Number of buildings / locations
  [ ] Tenant or owner-occupied
  [ ] Operating hours
```

---

## Service Tier Definitions

### Tier 1 — Basic (Annual)

| Service | Frequency | Description |
|---------|-----------|-------------|
| Infrared scan | Annual | Full facility IR thermographic survey |
| Panel inspections | Annual | Visual inspection of all panels |
| Emergency/exit light test | Annual | 90-minute discharge test per NFPA 101 |
| Generator exercise | Annual | Load bank test and annual service |
| Report delivery | Annual | Condition report with recommendations |
| Emergency response | Standard rates | No priority dispatch |

### Tier 2 — Standard (Quarterly)

All Tier 1 services plus:

| Service | Frequency | Description |
|---------|-----------|-------------|
| Infrared scan | Semi-annual | Full facility IR scan twice per year |
| Panel maintenance | Quarterly | Torque connections, clean, inspect |
| Emergency/exit light test | Semi-annual | 30-min test semi-annual + 90-min annual |
| Generator service | Quarterly | Oil, filter, belts, coolant, exercise |
| Lighting maintenance | Quarterly | Replace failed lamps, clean fixtures |
| Condition reporting | Quarterly | Status report with trending data |
| Emergency response | Priority | 4-hour response guarantee |

### Tier 3 — Premium (Monthly)

All Tier 2 services plus:

| Service | Frequency | Description |
|---------|-----------|-------------|
| Infrared scan | Quarterly | Full IR scan four times per year |
| Facility walk-through | Monthly | Visual inspection of all systems |
| Panel maintenance | Quarterly | Full PM with torque and cleaning |
| Generator service | Monthly | Full monthly service and exercise |
| Lighting maintenance | Monthly | Same-visit lamp and fixture repair |
| On-call emergency | 24/7 | 2-hour response guarantee |
| Annual arc flash update | Annual | Label updates, study review |
| Dedicated account manager | Ongoing | Single point of contact |

---

## Maintenance Task Details

### Quarterly Panel Maintenance

```
SCOPE PER PANEL:
  1. De-energize panel (if customer-approved)
  2. Remove panel cover
  3. Visual inspection:
     - Bus bars for discoloration, pitting
     - Wire insulation for heat damage
     - Breaker condition and alignment
     - Neutral/ground bar connections
  4. Torque all connections to manufacturer specifications
  5. Verify breaker operation (toggle test)
  6. Clean interior (vacuum debris, dust)
  7. Replace panel cover
  8. Update panel schedule/directory if needed
  9. Document findings with photos

ESTIMATED TIME PER PANEL: 30-60 minutes
LABOR: 0.50-1.00 hours per panel
```

### Emergency/Exit Light Testing (NFPA 101)

```
MONTHLY (30-second functional test):
  - Activate test button on each unit
  - Verify illumination
  - Document results

ANNUAL (90-minute discharge test):
  - Disconnect AC power to each unit
  - Run on battery for 90 minutes
  - Verify illumination maintained for full duration
  - Replace failed batteries
  - Document results

LABOR PER UNIT: 0.10 hrs (monthly) / 0.25 hrs (annual)
```

### Generator Maintenance Schedule

```
MONTHLY:
  - Visual inspection
  - Check oil level
  - Check coolant level
  - Battery voltage check
  - Exercise under load (if possible) for 30+ minutes
  - Record run hours

QUARTERLY:
  - All monthly items
  - Change oil and filter
  - Check/replace air filter
  - Inspect belts and hoses
  - Test battery specific gravity
  - Check fuel system
  - Exercise with building load

ANNUAL:
  - All quarterly items
  - Replace coolant (per manufacturer schedule)
  - Replace spark plugs (gas units)
  - Inspect exhaust system
  - Load bank test (per NFPA 110)
  - ATS functional test
  - Update maintenance log
```

---

## Output Format

```markdown
# HUSTON ELECTRIC, INC.
## ELECTRICAL MAINTENANCE PROGRAM PROPOSAL

**Proposal #:** HE-EMP-[YYYY]-[NNNN]
**Date:** [Date]
**Valid Until:** [Date + 60 days]
**Prepared For:** [Customer Name]
**Prepared By:** [Estimator Name]

---

### EXECUTIVE SUMMARY

Huston Electric, Inc. proposes a comprehensive Electrical Maintenance Program (EMP) for
[Customer] at [Facility]. This program provides scheduled preventive maintenance, infrared
thermographic surveys, emergency/exit light testing, generator maintenance, and emergency
response services to protect your electrical infrastructure, reduce unplanned downtime,
and maintain code compliance.

**Recommended Service Tier:** [Basic / Standard / Premium]

**Key Benefits:**
- Prevent electrical failures and fire hazards through scheduled maintenance
- Reduce unplanned downtime with early problem detection via IR scanning
- Maintain NFPA and NEC code compliance with documented testing
- Predictable annual budget for electrical maintenance
- Priority emergency response when issues arise
- Professional documentation for insurance and regulatory compliance

---

### FACILITY PROFILE

| | |
|---|---|
| **Facility:** | [Name and Address] |
| **Building Size:** | [X] sq ft |
| **Service Size:** | [X]A, [X]V |
| **Panels:** | [X] distribution + [X] branch |
| **Transformers:** | [X] |
| **Generator:** | [X] kW [fuel type] |
| **Emergency/Exit Lights:** | [X] units |
| **Exterior Lighting:** | [X] fixtures |

---

### PROPOSED SERVICE SCHEDULE

**[Tier Name] Program — [Frequency] Visits**

| Visit | Month | Services Performed |
|-------|-------|--------------------|
| Q1 | [Month] | [Service list] |
| Q2 | [Month] | [Service list] |
| Q3 | [Month] | [Service list] |
| Q4 | [Month] | [Service list] |

---

### ANNUAL BUDGET

| Service Category | Visits/Year | Labor Hours | Annual Cost |
|-----------------|-------------|-------------|-------------|
| Panel maintenance | [X] | [X.X] | $[X.XX] |
| IR thermographic surveys | [X] | [X.X] | $[X.XX] |
| Emergency/exit light testing | [X] | [X.X] | $[X.XX] |
| Generator maintenance | [X] | [X.X] | $[X.XX] |
| Lighting maintenance | [X] | [X.X] | $[X.XX] |
| Report generation | [X] | Included | Included |
| **Scheduled Subtotal** | | | **$[X.XX]** |
| Emergency response allocation | As needed | [X] hrs | $[X.XX] |
| Material/consumable allowance | | | $[X.XX] |
| **ANNUAL PROGRAM TOTAL** | | | **$[X.XX]** |

**Monthly equivalent:** $[X.XX]/month
**Quarterly equivalent:** $[X.XX]/quarter

---

### WHAT IS NOT INCLUDED

- Capital improvements or system upgrades
- Repairs beyond normal preventive maintenance (quoted separately when identified)
- Tenant build-out or remodel electrical work
- Fire alarm monitoring fees
- Generator fuel
- Arc flash study (available as add-on service)

---

### PROGRAM TERMS

1. **Term:** [1 / 2 / 3] year agreement with annual renewal option.
2. **Billing:** [Monthly / Quarterly / Annual] in advance.
3. **Payment Terms:** Net 30.
4. **Price Escalation:** Fixed for Year 1. Annual adjustment of up to [3]% for subsequent years.
5. **Emergency Response:** [Priority / Standard] — [2 / 4]-hour response during business hours.
6. **Cancellation:** 60-day written notice by either party.
7. **Repairs:** Work beyond PM scope quoted separately at EMP customer rates ([X]% discount on standard rates).
8. **Reporting:** [Quarterly / Monthly] condition reports delivered electronically.
9. **Insurance:** Huston Electric maintains general liability and workers compensation insurance.

### ACCEPTANCE

Customer Signature: _________________________ Date: ___________
Printed Name: _________________________
Title: _________________________

Huston Electric, Inc.
Authorized Signature: _________________________ Date: ___________

Huston Electric, Inc. | [Phone] | [License #]
```

---

## Budget Estimation Quick Reference

| Facility Type | Annual EMP Range | Notes |
|---------------|-----------------|-------|
| Small office (5,000 sq ft, 4 panels) | $2,000-$4,000 | Basic tier |
| Medium office (25,000 sq ft, 12 panels) | $5,000-$10,000 | Standard tier |
| Large office (50,000+ sq ft, 20+ panels) | $10,000-$20,000 | Standard/Premium |
| Retail (single location) | $2,000-$5,000 | Basic/Standard |
| Restaurant | $3,000-$6,000 | Equipment-heavy |
| Warehouse/distribution | $5,000-$15,000 | Size-dependent |
| Manufacturing (light) | $8,000-$20,000 | MCCs, VFDs |
| Manufacturing (heavy) | $15,000-$40,000+ | Full Premium |
| Multi-building campus | $20,000-$50,000+ | Multiple facilities |

---

## Related Skills

- **ir-scan-quotation** — Standalone IR scanning service quotations
- **generator-quotation** — Generator-specific installation and service quotations
- **electrical-quotation** — One-time service quotations for repairs identified during maintenance
- **contract-generation** — Convert accepted EMP proposals into service contracts
