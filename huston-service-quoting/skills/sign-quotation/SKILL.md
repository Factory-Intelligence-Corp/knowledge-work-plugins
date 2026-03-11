---
name: sign-quotation
description: Create sign installation and maintenance quotations with travel time calculations, lift equipment pricing, and sign-specific labor standards. Trigger with "quote sign work", "sign installation quote", "price sign job at [location]", "sign maintenance quotation", "bid on sign project".
---

# Sign Quotation Specialist

Build professional sign installation and maintenance quotations for Huston Electric, Inc. This skill handles the unique requirements of sign work including travel time calculations, lift/crane equipment, sign-specific labor standards, weather considerations, and permit requirements. Works standalone with manual input, supercharged when you connect your knowledge base for past sign quotations and material pricing.

## Connectors (Optional)

| Connector | What It Adds |
|-----------|--------------|
| **Knowledge Base (Past Quotes)** | Reference similar past sign jobs for pricing consistency |
| **Knowledge Base (Materials)** | Sign-specific material pricing (transformers, ballasts, LED drivers, neon) |
| **Document Generation** | Generate branded PDF quotation |
| **CRM** | Pull customer info, log quotation |

> **No connectors?** Describe the sign job and I will build a complete quotation using sign industry labor standards and your material cost input.

---

## How It Works

```
┌──────────────────────────────────────────────────────────────────────────┐
│                      SIGN QUOTATION SPECIALIST                          │
├──────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  Step 1: PARSE SIGN REQUEST                                              │
│  - Sign type (channel letters, monument, pylon, cabinet, LED, neon)    │
│  - Work type (new install, repair, maintenance, retrofit, removal)     │
│  - Location and travel distance from shop                               │
│  - Sign dimensions, height, mounting method                            │
│                                                                          │
│  Step 2: CALCULATE TRAVEL TIME                                           │
│  - Distance from shop to job site                                       │
│  - Round-trip drive time at billable rate                               │
│  - Number of trips required (survey, install, final)                   │
│                                                                          │
│  Step 3: DETERMINE EQUIPMENT NEEDS                                       │
│  - Bucket truck / boom lift / crane requirements                       │
│  - Lift rental costs and duration                                       │
│  - Traffic control or flagging needs                                   │
│                                                                          │
│  Step 4: BUILD LINE ITEMS                                                │
│  - Sign-specific labor (install, wire, connect, test)                  │
│  - Electrical labor (circuits, disconnects, conduit)                   │
│  - Materials (sign components, electrical, mounting hardware)          │
│  - Equipment rental                                                     │
│  - Permits and inspections                                              │
│                                                                          │
│  Step 5: ASSESS BID OPPORTUNITY                                          │
│  - Review scope for completeness                                        │
│  - Flag risks (height, access, structural, permit timeline)            │
│  - Compare to similar past jobs if available                           │
│  - Recommend bid/no-bid based on feasibility                           │
│                                                                          │
│  Step 6: GENERATE QUOTATION                                              │
│  - Format professional quotation with sign-specific terms              │
│  - Include weather/scheduling contingencies                            │
│  - Add permit and inspection notes                                     │
│                                                                          │
└──────────────────────────────────────────────────────────────────────────┘
```

---

## Travel Time Calculations

Travel time is billable labor time for sign work, as jobs are frequently remote.

```
TRAVEL CALCULATION:
  one_way_distance = miles from shop to job site
  one_way_time = one_way_distance / average_speed (use 45 mph for mixed driving)
  round_trip_time = one_way_time x 2
  billable_travel_hours = round_trip_time (rounded up to nearest 0.5 hr)
  travel_cost = billable_travel_hours x labor_rate x number_of_crew

  Number of trips:
  - Survey/site visit: 1 trip (1 person)
  - Installation: 1-3 trips (2-3 person crew)
  - Final inspection: 1 trip (1 person)

VEHICLE CHARGE (if applicable):
  Bucket truck: $150/day or $75/half day
  Service van: $50/trip

Example:
  Job site: 45 miles from shop
  One-way time: 45 miles / 45 mph = 1.0 hour
  Round trip: 2.0 hours
  2-person crew: 2.0 hrs x 2 people x $92/hr = $368.00 travel labor
  Bucket truck: $150/day
  Total travel cost for install day: $518.00
```

---

## Sign-Specific Labor Standards

| Task | Labor Hours | Crew Size | Notes |
|------|-------------|-----------|-------|
| **Channel letter install (per letter)** | 0.75-1.50 | 2 | Depends on size and mounting |
| **Channel letter repair (per letter)** | 0.50-1.00 | 1-2 | LED/neon replacement |
| **Monument sign install** | 4.00-8.00 | 2-3 | Depends on size, base prep |
| **Pylon sign install** | 8.00-16.00 | 2-3 | Includes pole, electrical |
| **Cabinet sign install (small <4x8)** | 3.00-5.00 | 2 | Wall or pole mount |
| **Cabinet sign install (large >4x8)** | 5.00-10.00 | 2-3 | May require crane |
| **LED retrofit (per sign face)** | 2.00-4.00 | 1-2 | Remove old, install LED modules |
| **Neon repair (per section)** | 1.00-2.00 | 1 | Glass handling, transformer |
| **Sign removal** | 2.00-6.00 | 2-3 | Disconnect, remove, patch |
| **Electrical connection (new circuit)** | 2.00-4.00 | 1-2 | From panel to sign location |
| **Disconnect switch install** | 1.00-1.50 | 1 | Required per NEC 600.6 |
| **Photocell/timer install** | 0.50-1.00 | 1 | Automatic on/off control |
| **Ballast/driver replacement** | 0.75-1.50 | 1 | Per unit |
| **Sign survey/site assessment** | 1.00-2.00 | 1 | Measure, photo, assess |

---

## Bid Opportunity Analysis

For competitive bid situations, evaluate before quoting:

```
BID ASSESSMENT CHECKLIST:
  [ ] Is the scope clearly defined? (sign type, size, location, mounting)
  [ ] Do we have equipment access? (lift height, site restrictions)
  [ ] Are permits obtainable? (sign permits, electrical permits, variances)
  [ ] Is the timeline realistic? (lead times for sign fabrication, permit processing)
  [ ] Is the customer creditworthy? (sign jobs can be large investments)
  [ ] Do we have the manpower? (sign work requires experienced crews)
  [ ] Are there structural concerns? (wall/pole capacity, wind load)
  [ ] What is our win probability? (relationship, competition, pricing)

RISK FLAGS:
  - Height > 30 ft: Crane likely needed, cost escalation
  - No existing electrical: Add full circuit run to scope
  - Historic district: Special permit requirements, restrictions
  - Multi-tenant: Landlord approval required
  - Road frontage: Traffic control, possible lane closure permit
```

---

## Project Feasibility Assessment

| Factor | Low Risk | Medium Risk | High Risk |
|--------|----------|-------------|-----------|
| **Height** | Under 15 ft | 15-30 ft (bucket truck) | Over 30 ft (crane) |
| **Access** | Open parking lot | Limited access, side street | Rooftop, interior courtyard |
| **Structural** | Existing mounting points | Wall-mount with backing | New pole/pylon foundation |
| **Permits** | Standard sign permit | Variance needed | Zoning change required |
| **Electrical** | Existing circuit nearby | Circuit run under 100 ft | New panel or service needed |
| **Timeline** | 4+ weeks | 2-4 weeks | Under 2 weeks (rush) |

---

## Output Format

```markdown
# HUSTON ELECTRIC, INC.
## SIGN SERVICE QUOTATION

**Quotation #:** HE-SGN-[YYYY]-[NNNN]
**Date:** [Date]
**Valid Until:** [Date + 30 days]
**Prepared By:** [Estimator Name]

---

### CUSTOMER INFORMATION

| | |
|---|---|
| **Customer:** | [Company/Name] |
| **Contact:** | [Contact Name] |
| **Site Address:** | [Sign Location Address] |
| **Distance from Shop:** | [X] miles ([X] min drive) |

---

### SCOPE OF WORK

[Description of sign work including sign type, dimensions, mounting,
electrical requirements, and any special conditions.]

---

### PRICING DETAIL

| # | Description | Qty | Labor Hrs | Labor Cost | Material Cost | Line Total |
|---|-------------|-----|-----------|------------|---------------|------------|
| 1 | Travel — round trip ([X] mi, [X]-person crew) | [X] | [X.X] | $[X.XX] | — | $[X.XX] |
| 2 | [Sign work task] | [X] | [X.X] | $[X.XX] | $[X.XX] | $[X.XX] |
| 3 | [Electrical work task] | [X] | [X.X] | $[X.XX] | $[X.XX] | $[X.XX] |
| 4 | Equipment — [bucket truck/lift/crane] | [X] day | — | — | $[X.XX] | $[X.XX] |
| 5 | Sign permit | 1 | — | — | $[X.XX] | $[X.XX] |

---

### COST SUMMARY

| Category | Amount |
|----------|--------|
| **Total Labor** ([X.X] hrs @ $[rate]/hr) | $[X.XX] |
| **Total Materials** (cost + 40% markup) | $[X.XX] |
| **Equipment Rental** | $[X.XX] |
| **Permits** | $[X.XX] |
| **Travel / Vehicle** | $[X.XX] |
| **Subtotal** | $[X.XX] |
| **Sales Tax** (7% on materials) | $[X.XX] |
| **GRAND TOTAL** | **$[X.XX]** |

---

### SIGN-SPECIFIC TERMS

1. Sign fabrication is NOT included unless specified. This quotation covers electrical installation and connection only.
2. All sign work per NEC Article 600 — Electric Signs and Outline Lighting.
3. Disconnect switch required per NEC 600.6 within sight of the sign.
4. Weather-dependent work — installation may be rescheduled due to wind, rain, or lightning.
5. Crane work (if applicable) requires 48-hour advance scheduling and is weather-dependent.
6. Sign permits are the responsibility of [customer / Huston Electric — specify].
7. Structural engineering certification (if required) is not included.
8. Work at height requires OSHA-compliant fall protection; included in labor.

### ACCEPTANCE

Customer Signature: _________________________ Date: ___________
Printed Name: _________________________

Huston Electric, Inc. | [Phone] | [License #]
```

---

## Past Sign Quotation Reference

When ~~past quotations is connected, search for similar jobs to validate pricing:

```
Search criteria:
  - Sign type (channel letters, monument, pylon, cabinet)
  - Work type (install, repair, retrofit)
  - Comparable size and height
  - Similar distance from shop

Use past quotes to:
  - Validate labor hour estimates
  - Check material cost accuracy
  - Ensure pricing consistency
  - Identify commonly missed scope items
```

---

## NEC Article 600 Key Requirements

| Requirement | NEC Reference | Detail |
|-------------|---------------|--------|
| Disconnect required | 600.6 | Within sight of sign, or lockable |
| Listed signs required | 600.3 | UL or equivalent listing |
| Grounding | 600.7 | All metal parts bonded and grounded |
| Branch circuit | 600.5 | Dedicated circuit for each sign |
| Wet/damp location | 600.8 | Outdoor signs require wet-rated components |
| Wiring methods | 600.31-32 | Specific wiring requirements for sign circuits |

---

## Related Skills

- **electrical-quotation** — General electrical service quotations
- **indy-quotation** — Indianapolis-specific quotation with standardized rates
- **contract-generation** — Produce service contracts from accepted quotations
