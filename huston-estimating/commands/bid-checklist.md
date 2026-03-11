---
description: Scan plans and specifications — fill out a bid checklist, flag items needing estimator attention, verify scope coverage
argument-hint: "<project name or description>"
---

# /bid-checklist

> If you see unfamiliar placeholders or need to check which tools are connected, see [CONNECTORS.md](../CONNECTORS.md).

Systematically review project plans and specifications to fill out a comprehensive electrical bid checklist. Identifies scope items, flags ambiguities, and ensures nothing is missed in the estimate.

## Usage

```
/bid-checklist [project name or description]
```

Fill bid checklist for: $ARGUMENTS

If a file is referenced: @$1

---

## How It Works

```
┌─────────────────────────────────────────────────────────────────┐
│                    BID CHECKLIST                                  │
├─────────────────────────────────────────────────────────────────┤
│  STANDALONE (always works)                                       │
│  ✓ Upload specs and/or drawings                                 │
│  ✓ Systematic review of all relevant CSI divisions              │
│  ✓ Checklist fill-in with source references                     │
│  ✓ Flag items needing estimator attention (VERIFY status)       │
│  ✓ Inclusion/exclusion tracking for bid letter                  │
│  ✓ Addenda and alternate review                                 │
├─────────────────────────────────────────────────────────────────┤
│  SUPERCHARGED (when you connect your tools)                      │
│  + Knowledge Base: standard Huston checklists, past bid notes   │
│  + File Storage: pull specs and plans from project folders      │
│  + Document Generation: formatted PDF checklist report          │
│  + Project Tracker: RFI log, addenda tracking                   │
└─────────────────────────────────────────────────────────────────┘
```

---

## What I Need From You

**Option A: Upload specifications**
Upload the project specification PDF (full project manual or just the electrical divisions). The agent will parse every relevant section.

**Option B: Upload specifications + drawings**
Upload both for the most thorough review. The agent will cross-reference drawings against specs to catch discrepancies.

**Option C: Upload a bid form or scope summary**
If you have a bid form listing alternates, allowances, and unit prices, upload it alongside the specs.

**Option D: Reference a project**
```
Fill the bid checklist for the Oakwood Apartments project
```
If ~~file storage is connected, the agent will pull project documents directly.

**Helpful context:**
- "Fire alarm may or may not be in our scope — please verify"
- "This is a K-12 school project"
- "Check if prevailing wage applies"

---

## Output

```markdown
# Bid Checklist: [Project Name]

**Project:** [Name]
**Bid Date:** [Date]
**Documents Reviewed:** [List]
**Addenda Incorporated:** [List]

---

## Summary

| Category | Items | Included | Excluded | Verify |
|----------|-------|----------|----------|--------|
| General / Project-Wide | [X] | [X] | [X] | [X] |
| Service and Distribution | [X] | [X] | [X] | [X] |
| Interior Lighting | [X] | [X] | [X] | [X] |
| Exterior / Site Lighting | [X] | [X] | [X] | [X] |
| Power / Receptacles | [X] | [X] | [X] | [X] |
| Fire Alarm | [X] | [X] | [X] | [X] |
| Low Voltage / Data | [X] | [X] | [X] | [X] |
| Security / Access Control | [X] | [X] | [X] | [X] |
| Special Systems | [X] | [X] | [X] | [X] |
| **TOTALS** | **[X]** | **[X]** | **[X]** | **[X]** |

---

## Items Requiring Estimator Attention

| # | Item | Category | Issue | Source | Cost Impact |
|---|------|----------|-------|--------|-------------|
| 1 | [Item] | [Cat] | [Issue] | [Ref] | [High/Med/Low] |

---

[Full category-by-category checklist with status, source, and notes]

---

## Exclusions for Bid Letter

- [Item 1 — not in electrical scope per [reference]]
- [Item 2 — by others per [reference]]

## Assumptions for Bid Qualification

- [Assumption 1]
- [Assumption 2]
```

---

## Checklist Categories

The agent reviews nine scope categories:

1. **General / Project-Wide** — Permits, temp power, as-builts, O&M, commissioning, prevailing wage
2. **Service and Distribution** — Switchgear, panels, transformers, generators, transfer switches
3. **Interior Lighting** — All fixture types, controls, sensors, emergency lighting
4. **Exterior / Site Lighting** — Poles, bollards, wall packs, underground conduit
5. **Power / Receptacles** — Standard, GFI, dedicated circuits, floor boxes, equipment connections
6. **Fire Alarm** — FACP, detection devices, notification, monitoring
7. **Low Voltage / Data** — Backbone, horizontal cabling, data outlets, WAPs
8. **Security / Access Control** — Card readers, cameras, door hardware
9. **Special Systems** — Lightning protection, solar, BAS, nurse call, AV

---

## Flag System

| Flag | Meaning | Action |
|------|---------|--------|
| **INCLUDED** | Clearly in electrical scope | Price it |
| **EXCLUDED** | Clearly by others | List in bid exclusions |
| **VERIFY** | Ambiguous or conflicting | Estimator must review |

---

## Tips

1. **Upload the full spec** — Non-electrical divisions often contain electrical scope (HVAC connections, kitchen equipment)
2. **Include all addenda** — Addenda frequently change electrical scope
3. **Upload the bid form** — Captures alternates, allowances, and unit prices
4. **Mention the project type** — Helps the agent know what code requirements to look for
5. **Flag known concerns** — "I think data might not be in our scope" focuses attention
