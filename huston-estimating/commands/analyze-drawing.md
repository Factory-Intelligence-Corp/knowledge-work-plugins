---
description: Analyze a floor plan, reflected ceiling plan, or electrical drawing — count fixtures by room and type, cross-reference fixture schedules, generate material and labor estimates
argument-hint: "<drawing sheet or description>"
---

# /analyze-drawing

> If you see unfamiliar placeholders or need to check which tools are connected, see [CONNECTORS.md](../CONNECTORS.md).

Analyze electrical drawings to count light fixtures by room and type, cross-reference fixture schedules, and produce material takeoffs with labor estimates. Powered by Edison the Electrical Estimator.

## Usage

```
/analyze-drawing [drawing sheet or description]
```

Analyze drawing: $ARGUMENTS

If a file is referenced: @$1

---

## How It Works

```
┌─────────────────────────────────────────────────────────────────┐
│              ANALYZE DRAWING (Edison)                             │
├─────────────────────────────────────────────────────────────────┤
│  STANDALONE (always works)                                       │
│  ✓ Upload drawing image (PNG, JPG, PDF)                         │
│  ✓ Identifies drawing type (floor plan, RCP, electrical, site)  │
│  ✓ Identifies all rooms and spaces                              │
│  ✓ Counts fixtures by type within each room                     │
│  ✓ Produces room-by-room fixture count table                    │
│  ✓ Generates fixture type summary with grand totals             │
│  ✓ Estimates material costs and labor hours                     │
├─────────────────────────────────────────────────────────────────┤
│  SUPERCHARGED (when you connect your tools)                      │
│  + Knowledge Base: fixture pricing, labor hour standards        │
│  + File Storage: pull drawings and fixture schedules            │
│  + Document Generation: formatted PDF takeoff reports           │
│  + Project Tracker: drawing revision history                    │
└─────────────────────────────────────────────────────────────────┘
```

---

## What I Need From You

**Option A: Upload a drawing**
Upload an image or PDF of the electrical drawing sheet. Best results with:
- Reflected Ceiling Plans (RCPs) — primary source for fixture counts
- Electrical Lighting Plans — fixtures with circuit routing
- Site Plans — exterior lighting
- Floor Plans — limited fixture info but useful for room identification

**Option B: Upload multiple sheets**
Upload several sheets for a complete floor or building. Edison will aggregate counts across all sheets.

**Option C: Reference a project**
```
Analyze the lighting plans for the Oakwood Apartments project
```
If ~~file storage is connected, Edison will pull the drawing set directly.

**Helpful extras:**
- Fixture schedule (upload alongside the plan for cross-referencing)
- Specification section 26 51 00 (lighting fixture types and manufacturers)
- Any addenda that changed fixture types

---

## Output

```markdown
# Fixture Takeoff: [Project Name] — [Sheet Reference]

**Drawing:** [Sheet number and title]
**Drawing Type:** [Floor Plan / RCP / Electrical Plan / Site Plan]
**Analyzed By:** Edison — Electrical Estimator
**Date:** [Date]
**Confidence Level:** [High / Medium / Low]

---

## Room-by-Room Fixture Count

### [Room Number — Room Name]

| Fixture Type | Symbol | Qty | Notes |
|-------------|--------|-----|-------|
| [Type] | [Symbol] | [X] | [Notes] |
| **Room Total** | | **[X]** | |

[Repeats for every room]

---

## Fixture Type Summary

| Type | Total Qty | Unit Cost | Extended Cost |
|------|-----------|-----------|---------------|
| [Type] | [X] | $[X] | $[X] |
| **TOTALS** | **[X]** | | **$[X]** |

---

## Fixture Schedule Cross-Reference

| Drawing Symbol | Schedule Type | Manufacturer | Catalog No. | Verified |
|---------------|---------------|-------------|-------------|----------|
| [Symbol] | [Type] | [Mfr] | [Cat#] | [Yes/No] |

---

## Material Takeoff Summary

| Category | Amount |
|----------|--------|
| Fixtures | $[X] |
| Wiring and Rough-In | $[X] |
| Material Markup | $[X] |
| **Material Total** | **$[X]** |

---

## Labor Hour Estimates

| Task | Qty | Hours/Unit | Total Hours | Extended |
|------|-----|------------|-------------|----------|
| [Task] | [X] | [X] | [X] | $[X] |
| **Labor Total** | | | **[X] hrs** | **$[X]** |

---

## Estimate Summary

| Category | Amount |
|----------|--------|
| Material | $[X] |
| Labor | $[X] |
| Overhead | $[X] |
| Profit | $[X] |
| **Total** | **$[X]** |

---

## Notes and Flags

- [Items needing estimator verification]
- [Unclear symbols or low-confidence counts]
- [Discrepancies between drawing and schedule]
```

---

## Quality Assurance

Edison performs a three-pass analysis:

1. **First Pass** — Systematic room-by-room fixture count
2. **Second Pass** — Verification (totals, symmetry, density check, emergency egress coverage)
3. **Third Pass** — Cross-reference with fixture schedule and flag discrepancies

Each room receives a confidence rating (High / Medium / Low) based on drawing clarity and symbol recognition certainty.

---

## Tips

1. **Upload high resolution** — Higher DPI means more accurate symbol recognition
2. **Include the fixture schedule** — Cross-referencing gives you manufacturer and catalog numbers
3. **Specify the sheet** — "Analyze Sheet E2.1" is more precise
4. **Upload multiple sheets** — Edison aggregates across floors and buildings
5. **Note addenda changes** — "Type C was changed to Type F in Addendum 2"
6. **Ask for specific rooms** — "Just count fixtures in the lobby and corridors"
