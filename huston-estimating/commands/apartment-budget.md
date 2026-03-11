---
description: Prepare an apartment bid budget — analyze historical data, apply regional adjustments, compare with past bids, generate a detailed budget report
argument-hint: "<project name, unit count, or description>"
---

# /apartment-budget

> If you see unfamiliar placeholders or need to check which tools are connected, see [CONNECTORS.md](../CONNECTORS.md).

Prepare an electrical bid budget for apartment and multi-family residential projects. Uses historical bid data, current material pricing, regional labor adjustments, and economic indicators to produce detailed per-unit budgets with comparisons to past projects.

## Usage

```
/apartment-budget [project name, unit count, or description]
```

Prepare apartment budget for: $ARGUMENTS

If a file is referenced: @$1

---

## How It Works

```
┌─────────────────────────────────────────────────────────────────┐
│              APARTMENT BID BUDGET                                 │
├─────────────────────────────────────────────────────────────────┤
│  STANDALONE (always works)                                       │
│  ✓ Describe your project (units, location, building type)       │
│  ✓ Or upload project plans for scope-based budgeting            │
│  ✓ Per-unit cost breakdown by unit type                         │
│  ✓ Common area and site work budgeting                          │
│  ✓ Overhead, profit, and contingency calculations               │
│  ✓ Regional and market condition adjustments                    │
├─────────────────────────────────────────────────────────────────┤
│  SUPERCHARGED (when you connect your tools)                      │
│  + Knowledge Base: historical bid data, past project actuals    │
│  + File Storage: project drawings for scope-based estimates     │
│  + Document Generation: formatted PDF budget reports            │
│  + Project Tracker: active project cost data                    │
└─────────────────────────────────────────────────────────────────┘
```

---

## What I Need From You

**Option A: Describe the project**
```
200-unit mid-rise apartment in Nashville
Mix: 40 studios, 80 1BR, 60 2BR, 20 3BR
4 stories, wood frame, surface parking
Amenities: gym, pool, clubhouse
Fire alarm in our scope, data by others
```

**Option B: Upload project plans**
Upload drawings and/or specs. The analyst will review scope and produce a detailed budget based on actual takeoff quantities rather than parametric estimates.

**Option C: Compare with a past project**
```
Budget a 300-unit project similar to Riverside Apartments but in Atlanta instead of Nashville
```
If ~~knowledge base is connected, the analyst will pull the Riverside bid and adjust for the new parameters.

**Option D: Quick parametric estimate**
```
What should we budget per unit for a 150-unit garden-style in Charlotte?
```
The analyst will provide a range based on building type, location, and current market conditions.

---

## Output

```markdown
# Apartment Bid Budget: [Project Name]

**Project:** [Name]
**Location:** [City, State]
**Building Type:** [Garden / Mid-Rise / High-Rise]
**Total Units:** [Count]
**Unit Mix:** [Breakdown]
**Date:** [Date]

---

## Executive Summary

**Recommended Bid Amount:** $[Total]
**Per-Unit Average:** $[Amount]
**Confidence Range:** $[Low] — $[High]

---

## Unit Cost Breakdown

| Unit Type | Qty | Cost/Unit | Extended |
|-----------|-----|-----------|----------|
| Studio | [X] | $[X] | $[X] |
| 1 Bedroom | [X] | $[X] | $[X] |
| 2 Bedroom | [X] | $[X] | $[X] |
| 3 Bedroom | [X] | $[X] | $[X] |
| **Subtotal** | **[X]** | **$[Avg]** | **$[X]** |

---

## Common Areas
[Line-item detail]

## Site Work
[Line-item detail]

## Fire Alarm (if in scope)
[Line-item detail]

---

## Budget Summary

| Category | Amount | % of Total |
|----------|--------|-----------|
| Units | $[X] | [X]% |
| Common Areas | $[X] | [X]% |
| Site Work | $[X] | [X]% |
| Fire Alarm | $[X] | [X]% |
| Markups and Contingency | $[X] | [X]% |
| **TOTAL BID** | **$[X]** | |

---

## Historical Comparison
[Side-by-side with comparable past bids]

## Risk Factors
[Material, labor, schedule risks with mitigation]

## Bid Strategy
[Target, floor, ceiling with qualifications]
```

---

## Budget Methodology

The analyst follows this process:

1. **Gather parameters** — Unit count, mix, building type, location, scope
2. **Retrieve historicals** — Pull comparable past bids (from ~~knowledge base or industry data)
3. **Apply adjustments** — Region, building type, inflation, scope, market conditions
4. **Build line-item budget** — Units, common areas, site work, special systems
5. **Apply markups** — Material markup, labor burden, overhead, profit, contingency
6. **Compare with history** — Validate against past bids, explain variances
7. **Produce report** — Executive summary, detail, comparison, strategy

---

## Tips

1. **Provide the unit mix** — "200 units" is useful, but "40 studios, 80 1BR, 60 2BR, 20 3BR" is much better
2. **Specify building type** — Garden-style and high-rise have very different costs
3. **Mention scope inclusions** — Fire alarm, data, generator, solar, EV charging add significant cost
4. **Include location** — Regional labor and material costs vary significantly
5. **Reference past projects** — "Similar to Riverside but bigger" helps calibrate
6. **Upload plans for accuracy** — Scope-based estimates beat parametric estimates every time
