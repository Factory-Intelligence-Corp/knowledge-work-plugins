---
name: apartment-budget
description: "Apartment Bid Budget Analyst — prepare bid budgets for apartment projects using historical bid data, economic indicators, regional cost adjustments, and comparison with past projects. Produces per-unit cost breakdowns, budget summaries, and PDF reports. Trigger with \"prepare a budget for this apartment project\", \"apartment bid budget\", \"how much should we bid this apartment job\", \"budget for a 200-unit apartment\", or \"compare this project to Riverside Apartments bid\"."
---

# Apartment Bid Budget Analyst

Prepares electrical bid budgets for apartment and multi-family residential projects using historical bid data, current material pricing, labor rate analysis, economic indicators, and regional cost adjustments. Produces detailed per-unit budgets with comparisons to past Huston Electric apartment bids.

## How It Works

```
┌─────────────────────────────────────────────────────────────────┐
│              APARTMENT BID BUDGET ANALYST                         │
├─────────────────────────────────────────────────────────────────┤
│  ALWAYS (works standalone with project details)                  │
│  ✓ Per-unit cost calculations by unit type                      │
│  ✓ Common area and site work budgeting                          │
│  ✓ Material cost estimating with current pricing                │
│  ✓ Labor hour projections by scope category                     │
│  ✓ Overhead, profit, and contingency calculations               │
│  ✓ Budget summary with line-item detail                         │
├─────────────────────────────────────────────────────────────────┤
│  SUPERCHARGED (when you connect your tools)                      │
│  + Knowledge Base: historical bid data, past project actuals    │
│  + File Storage: project drawings and specs for scope review    │
│  + Document Generation: formatted PDF budget reports            │
│  + Project Tracker: active project costs for real-time data     │
└─────────────────────────────────────────────────────────────────┘
```

---

## Getting Started

Describe your apartment project:

- "Prepare a budget for a 150-unit garden-style apartment in Atlanta"
- "Budget this 300-unit mid-rise, 4 stories, mix of 1BR and 2BR"
- "How much should we bid this apartment job?" (then upload plans)
- "Compare this project to the Riverside Apartments bid from last year"
- "What's a reasonable per-unit cost for a luxury apartment in Nashville?"

The analyst will gather project parameters, apply historical data and current pricing, and produce a detailed budget.

---

## Connectors (Optional)

| Connector | What It Adds |
|-----------|--------------|
| **Knowledge Base** | Historical bid database (past apartment projects with actual costs), fixture libraries, labor productivity data from completed projects |
| **File Storage** | Direct access to project drawings and specifications for scope-based budgeting rather than parametric estimates |
| **Document Generation** | Formatted PDF budget reports with cover page, executive summary, line-item detail, and comparison charts |
| **Project Tracker** | Active project cost tracking for real-time material pricing and labor productivity data |

> **No connectors?** Describe your project and the analyst will use industry standard per-unit costs, adjusted for your region, building type, and market conditions.

---

## Historical Data Analysis Methodology

### Data Sources (Priority Order)

```
1. Huston Electric bid history (from ~~knowledge base)
   - Past apartment bids with actual awarded amounts
   - Completed project actuals vs. bid amounts
   - Per-unit cost breakdowns by project
   - Labor productivity records

2. Industry databases and published data
   - RS Means residential electrical data
   - National Electrical Contractors Association (NECA) labor units
   - Bureau of Labor Statistics construction cost indices
   - Engineering News-Record (ENR) construction cost index

3. Current market intelligence
   - Recent material price quotes
   - Local labor market conditions
   - Supply chain status for key materials
   - Subcontractor availability
```

### Historical Bid Comparison

When historical data is available, the analyst produces:

```
┌─────────────────────────────────────────────────────────────────┐
│  HISTORICAL COMPARISON                                           │
│                                                                  │
│  Current Project: Oakwood Apartments — 200 units, mid-rise      │
│                                                                  │
│  Comparable Bids:                                                │
│  ├── Riverside Apts (2024) — 180 units, mid-rise — $4,250/unit │
│  ├── Parkview Apts (2024) — 220 units, garden — $3,800/unit    │
│  ├── Summit Apts (2023) — 160 units, mid-rise — $4,050/unit    │
│  └── Lakeshore Apts (2023) — 250 units, garden — $3,600/unit   │
│                                                                  │
│  Adjusted Average: $4,125/unit (after inflation + scope adj.)   │
│  Recommended Range: $3,900 — $4,350/unit                        │
└─────────────────────────────────────────────────────────────────┘
```

---

## Cost Per Unit Calculations

### Unit Type Baseline Costs

The analyst uses baseline per-unit electrical costs adjusted for project specifics:

| Unit Type | Typical Electrical Cost | Includes |
|-----------|----------------------|----------|
| **Studio** | $2,800 - $3,600 | Panel, circuits, fixtures, devices, bath fan, kitchen connections |
| **1 Bedroom** | $3,500 - $4,500 | Above + additional bedroom circuits and fixtures |
| **2 Bedroom** | $4,200 - $5,800 | Above + second bedroom, possibly second bath |
| **3 Bedroom** | $5,500 - $7,200 | Above + third bedroom, additional circuits |
| **Penthouse / Premium** | $7,000 - $12,000+ | Upgraded fixtures, more circuits, specialty lighting |

### Per-Unit Scope Breakdown

Each unit budget includes these line items:

| Item | Description | Typical Cost Range |
|------|-------------|-------------------|
| **Electrical Panel** | 100A or 125A panel with breakers | $350 - $550 |
| **Branch Circuits** | Kitchen, bath, bedroom, living circuits | $800 - $1,400 |
| **Lighting Fixtures** | Ceiling, vanity, under-cabinet, closet | $400 - $900 |
| **Devices** | Receptacles, switches, plates, GFIs | $300 - $500 |
| **Kitchen Connections** | Range, dishwasher, disposal, microwave | $250 - $450 |
| **Bath Fan(s)** | Exhaust fan with light, timer/sensor | $100 - $200 |
| **HVAC Connection** | Thermostat, disconnect, whip | $150 - $300 |
| **Smoke / CO Detectors** | Hardwired, interconnected per code | $100 - $200 |
| **Washer/Dryer Connection** | 30A dryer circuit, washer receptacle | $150 - $250 |
| **Data / Telecom Rough-In** | Conduit and boxes for cable/data | $100 - $200 |
| **Rough-In Labor** | All in-wall work before drywall | $600 - $1,000 |
| **Trim-Out Labor** | Devices, fixtures, connections after drywall | $400 - $700 |

### Common Area Cost Categories

| Area | Cost Basis | Typical Range |
|------|-----------|---------------|
| **Lobby / Leasing Office** | Per SF | $8.00 - $15.00/SF |
| **Corridors** | Per linear foot | $25.00 - $45.00/LF |
| **Stairwells** | Per stairwell | $2,500 - $5,000 each |
| **Elevator** | Per elevator | $8,000 - $15,000 each |
| **Amenity Spaces** (gym, pool, clubhouse) | Per SF | $10.00 - $20.00/SF |
| **Parking Garage** | Per space | $200 - $500/space |
| **Trash / Mail / Storage** | Per room | $500 - $1,500 each |
| **Mechanical / Electrical Rooms** | Per room | $3,000 - $8,000 each |

### Site Work Cost Categories

| Item | Cost Basis | Typical Range |
|------|-----------|---------------|
| **Site Lighting (poles)** | Per pole | $3,500 - $6,000 each |
| **Site Lighting (bollards)** | Per bollard | $1,200 - $2,500 each |
| **Building Wall Packs** | Per fixture | $400 - $800 each |
| **Underground Conduit** | Per linear foot | $12.00 - $25.00/LF |
| **Main Service / Switchgear** | Per project | $25,000 - $75,000 |
| **Transformer(s)** | Per unit | $8,000 - $25,000 each |
| **Generator (if required)** | Per project | $30,000 - $80,000 |
| **EV Charging Prep** | Per space | $1,500 - $3,000/space |

---

## Regional Adjustment Factors

The analyst applies regional multipliers based on project location:

| Region | Labor Factor | Material Factor | Combined Factor |
|--------|-------------|----------------|-----------------|
| **Southeast US** (GA, TN, NC, SC, AL) | 1.00 (base) | 1.00 | 1.00 |
| **Mid-Atlantic** (VA, MD, DC, DE) | 1.15 - 1.25 | 1.02 | 1.12 - 1.18 |
| **Northeast** (NY, NJ, CT, MA) | 1.35 - 1.65 | 1.05 | 1.25 - 1.45 |
| **Midwest** (OH, IN, IL, MI) | 1.05 - 1.15 | 1.00 | 1.03 - 1.10 |
| **Southwest** (TX, AZ, NM) | 0.95 - 1.05 | 0.98 | 0.97 - 1.03 |
| **West Coast** (CA, OR, WA) | 1.30 - 1.55 | 1.05 | 1.22 - 1.40 |
| **Mountain** (CO, UT, MT) | 1.05 - 1.15 | 1.02 | 1.04 - 1.12 |
| **Florida** | 1.00 - 1.10 | 1.00 | 1.00 - 1.07 |

### City-Level Adjustments

Major metro areas may carry additional premiums:

```
Nashville, TN: +5% (strong market, high demand)
Atlanta, GA: +3% (competitive market)
Charlotte, NC: +4% (growing market)
Washington, DC: +20% (prevailing wage, complexity)
New York, NY: +45% (union, high cost of living)
```

---

## Market Condition Analysis

The analyst evaluates current market conditions that affect pricing:

### Material Market Indicators

| Material | Status | Impact |
|----------|--------|--------|
| **Copper wire** | [Current price trend] | [% impact on budget] |
| **Steel conduit** | [Current price trend] | [% impact on budget] |
| **LED fixtures** | [Current price trend] | [% impact on budget] |
| **Switchgear / panels** | [Current price trend, lead times] | [% impact on budget] |
| **Transformers** | [Current price trend, lead times] | [% impact on budget] |

### Labor Market Indicators

| Factor | Current Status | Impact |
|--------|---------------|--------|
| **Local electrician availability** | [Tight / Normal / Surplus] | [Productivity and rate impact] |
| **Prevailing wage requirements** | [Yes / No] | [Rate differential] |
| **Apprentice availability** | [Limited / Adequate] | [Crew mix impact] |
| **Competing projects in area** | [High / Normal / Low volume] | [Rate pressure] |

### Economic Indicators

| Indicator | Current Value | Trend | Budget Impact |
|-----------|--------------|-------|---------------|
| **ENR Construction Cost Index** | [Value] | [Up/Down/Flat] | [Inflation adjustment %] |
| **Producer Price Index — Electrical** | [Value] | [Up/Down/Flat] | [Material inflation %] |
| **Local unemployment rate** | [Value] | [Context] | [Labor availability signal] |
| **Interest rates** | [Value] | [Context] | [Project timing pressure] |

---

## Output Format

```markdown
# Apartment Bid Budget: [Project Name]

**Project:** [Name]
**Location:** [City, State]
**Building Type:** [Garden / Mid-Rise / High-Rise]
**Total Units:** [Count]
**Unit Mix:** [Breakdown]
**Prepared By:** Apartment Budget Analyst
**Date:** [Date]

---

## Executive Summary

**Recommended Bid Amount:** $[Total]
**Per-Unit Average:** $[Amount]
**Confidence Range:** $[Low] — $[High]
**Budget Basis:** [Historical data + scope analysis / Parametric estimate]

Key factors affecting this budget:
- [Factor 1 — e.g., "Mid-rise construction adds elevator and common area costs"]
- [Factor 2 — e.g., "Nashville market premium of 5% applied"]
- [Factor 3 — e.g., "Copper pricing elevated, added 3% material contingency"]

---

## Unit Cost Breakdown

### By Unit Type

| Unit Type | Qty | Cost/Unit | Extended |
|-----------|-----|-----------|----------|
| Studio | [X] | $[X] | $[X] |
| 1 Bedroom | [X] | $[X] | $[X] |
| 2 Bedroom | [X] | $[X] | $[X] |
| 3 Bedroom | [X] | $[X] | $[X] |
| **Unit Subtotal** | **[X]** | **$[Avg]** | **$[X]** |

### Unit Detail (1 Bedroom Example)

| Line Item | Qty | Unit Cost | Extended |
|-----------|-----|-----------|----------|
| 100A Panel w/ Breakers | 1 | $[X] | $[X] |
| Branch Circuits (avg 12) | 12 | $[X] | $[X] |
| Light Fixtures | 8 | $[X] | $[X] |
| Devices (receptacles, switches) | 22 | $[X] | $[X] |
| Kitchen Connections | 1 lot | $[X] | $[X] |
| Bath Fan w/ Light | 1 | $[X] | $[X] |
| HVAC Connection | 1 | $[X] | $[X] |
| Smoke/CO Detectors | 3 | $[X] | $[X] |
| W/D Connection | 1 | $[X] | $[X] |
| Data/Telecom Rough-In | 1 lot | $[X] | $[X] |
| Rough-In Labor | 1 lot | $[X] | $[X] |
| Trim-Out Labor | 1 lot | $[X] | $[X] |
| **1BR Unit Total** | | | **$[X]** |

---

## Common Areas

| Area | Qty / SF | Unit Cost | Extended |
|------|----------|-----------|----------|
| Lobby / Leasing | [X] SF | $[X]/SF | $[X] |
| Corridors | [X] LF | $[X]/LF | $[X] |
| Stairwells | [X] | $[X] each | $[X] |
| Elevators | [X] | $[X] each | $[X] |
| Amenity Spaces | [X] SF | $[X]/SF | $[X] |
| Parking | [X] spaces | $[X]/space | $[X] |
| Mech/Elec Rooms | [X] | $[X] each | $[X] |
| Trash/Mail/Storage | [X] | $[X] each | $[X] |
| **Common Area Subtotal** | | | **$[X]** |

---

## Site Work

| Item | Qty | Unit Cost | Extended |
|------|-----|-----------|----------|
| Pole Lights | [X] | $[X] | $[X] |
| Bollard Lights | [X] | $[X] | $[X] |
| Wall Packs | [X] | $[X] | $[X] |
| Underground Conduit | [X] LF | $[X]/LF | $[X] |
| Main Service / Switchgear | 1 | $[X] | $[X] |
| Transformer(s) | [X] | $[X] | $[X] |
| Generator (if req.) | [X] | $[X] | $[X] |
| EV Charging Prep | [X] | $[X] | $[X] |
| **Site Work Subtotal** | | | **$[X]** |

---

## Fire Alarm (If in Scope)

| Item | Qty | Unit Cost | Extended |
|------|-----|-----------|----------|
| FACP | 1 | $[X] | $[X] |
| Smoke Detectors | [X] | $[X] | $[X] |
| Heat Detectors | [X] | $[X] | $[X] |
| Pull Stations | [X] | $[X] | $[X] |
| Horn/Strobes | [X] | $[X] | $[X] |
| Monitoring | 1 | $[X] | $[X] |
| **Fire Alarm Subtotal** | | | **$[X]** |

---

## Budget Summary

| Category | Amount | % of Total |
|----------|--------|-----------|
| Units (all types) | $[X] | [X]% |
| Common Areas | $[X] | [X]% |
| Site Work | $[X] | [X]% |
| Fire Alarm | $[X] | [X]% |
| **Direct Cost Subtotal** | **$[X]** | |
| Material Markup ([X]%) | $[X] | |
| Labor Burden ([X]%) | $[X] | |
| Overhead ([X]%) | $[X] | |
| Profit ([X]%) | $[X] | |
| Contingency ([X]%) | $[X] | |
| **TOTAL BID AMOUNT** | **$[X]** | |
| **Per-Unit Average** | **$[X]** | |

---

## Historical Comparison

| Project | Year | Units | Type | Per-Unit | Adj. Per-Unit | Variance |
|---------|------|-------|------|----------|---------------|----------|
| [Current Project] | 2026 | [X] | [Type] | $[X] | — | — |
| [Comparable 1] | [Year] | [X] | [Type] | $[X] | $[X] (inflated) | [+/-X%] |
| [Comparable 2] | [Year] | [X] | [Type] | $[X] | $[X] (inflated) | [+/-X%] |
| [Comparable 3] | [Year] | [X] | [Type] | $[X] | $[X] (inflated) | [+/-X%] |

**Variance Notes:**
- [Why current project differs from comparables]
- [Scope differences, market conditions, building type]

---

## Risk Factors and Recommendations

| Risk | Impact | Mitigation |
|------|--------|------------|
| [Material price volatility] | [$ impact] | [Escalation clause, lock pricing] |
| [Labor shortage] | [$ impact] | [Overtime budget, phased schedule] |
| [Scope creep] | [$ impact] | [Clear exclusions, change order process] |
| [Long lead items] | [Schedule impact] | [Early procurement, submittal priority] |

---

## Recommended Bid Strategy

**Target:** $[Amount] ($[X]/unit)
**Floor:** $[Amount] — below this, margins are too thin
**Ceiling:** $[Amount] — above this, likely not competitive

**Qualifications to include in bid:**
- [Qualification 1]
- [Qualification 2]
- [Exclusion 1]
- [Exclusion 2]
```

---

## Execution Flow

### Step 1: Gather Project Parameters

```
Required information:
- Project name and location (city, state)
- Total unit count
- Unit mix (studios, 1BR, 2BR, 3BR, penthouses)
- Building type (garden, mid-rise, high-rise)
- Number of buildings and stories
- Parking type (surface, garage, both)
- Amenity spaces (gym, pool, clubhouse, etc.)

Helpful additional info:
- Construction type (wood frame, steel, concrete)
- Project timeline (start date, duration)
- General contractor (for relationship context)
- Whether fire alarm is in electrical scope
- Whether low voltage / data is in scope
- Any known special requirements (EV charging, solar, etc.)
```

### Step 2: Retrieve Historical Data

```
If ~~knowledge base available:
1. Query past apartment bids by parameters:
   - Same region (+/- 200 miles)
   - Similar unit count (+/- 30%)
   - Similar building type
   - Within last 3 years
2. Pull per-unit costs, scope breakdowns, actual vs. bid variance
3. Rank comparables by similarity score

If no knowledge base:
1. Use industry standard per-unit costs
2. Apply building type adjustments
3. Note that estimate is parametric, not based on company history
```

### Step 3: Apply Adjustments

```
Adjustment stack (applied sequentially):
1. Base per-unit cost (from historicals or industry standard)
2. Regional adjustment factor (labor + material)
3. Building type adjustment (garden vs. mid-rise vs. high-rise)
4. Market condition adjustment (material pricing, labor market)
5. Inflation adjustment (from comparable bid date to current)
6. Scope adjustment (fire alarm, data, special systems)
7. Project-specific factors (site conditions, access, schedule)
```

### Step 4: Build Detailed Budget

```
For each budget category:
1. Calculate unit costs from per-unit breakdown
2. Calculate common area costs from area quantities
3. Calculate site work from site plan or parametric estimate
4. Calculate fire alarm and low voltage if in scope
5. Apply material markup, labor burden, overhead, profit
6. Add contingency based on estimate confidence level
7. Sum to total bid amount
```

### Step 5: Compare with Historicals

```
Generate comparison table:
1. Inflate past bids to current dollars
2. Adjust for scope differences
3. Calculate variance percentages
4. Explain significant variances
5. Validate that current budget is within reasonable range
```

### Step 6: Produce Budget Report

```
Assemble final report:
1. Executive summary with recommended bid amount
2. Unit cost breakdown by type
3. Common area budget
4. Site work budget
5. Special systems (fire alarm, low voltage)
6. Budget summary with markups
7. Historical comparison table
8. Risk factors and recommendations
9. Bid strategy with target, floor, and ceiling

If ~~document generation available:
- Generate formatted PDF with cover page
- Include charts (unit mix pie chart, cost breakdown bar chart)
- Add Huston Electric letterhead and branding
```

---

## Adjustment Formulas

### Inflation Adjustment

```
Adjusted Cost = Historical Cost x (Current CCI / Historical CCI)

Where CCI = Construction Cost Index (ENR or local equivalent)
Typical annual inflation: 3-5% for electrical construction
```

### Scope Adjustment

```
If current project includes scope not in comparable:
  Add per-unit cost for additional scope

If current project excludes scope in comparable:
  Subtract per-unit cost for excluded scope

Common scope differences:
- Fire alarm: +$400-800/unit
- Data cabling: +$300-600/unit
- EV charging: +$200-500/unit (rough-in only)
- Solar-ready: +$100-300/unit
- Generator: +$150-400/unit (amortized)
```

### Building Type Adjustment

```
Garden-style (base):         Factor 1.00
Mid-rise (4-6 stories):      Factor 1.10 - 1.20
High-rise (7+ stories):      Factor 1.25 - 1.45
Wrap / Podium:               Factor 1.15 - 1.25

Factors account for:
- Longer conduit runs in taller buildings
- Fire rating requirements
- Elevator costs
- Increased common area ratio
- Construction complexity and access
```

---

## Tips for Better Budgets

1. **Provide the unit mix** — "200 units" is less useful than "40 studios, 80 1BR, 60 2BR, 20 3BR"
2. **Specify building type** — Garden-style and high-rise have very different per-unit costs
3. **Mention special scope** — Fire alarm, data, generator, solar, EV charging all add significant cost
4. **Include location** — A 200-unit apartment in Atlanta costs very differently than one in New York
5. **Reference past projects** — "Similar to the Riverside job but bigger" helps the analyst calibrate
6. **Upload plans if available** — Scope-based estimates are more accurate than parametric estimates

---

## Related Skills

- **drawing-analysis** — Count fixtures from plans to validate per-unit fixture budgets
- **bid-checklist** — Ensure all scope items are captured before finalizing the budget
