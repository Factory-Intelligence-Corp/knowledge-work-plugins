---
name: bid-checklist
description: "Bid Checklist Filler Agent — scan plans and specifications to systematically fill out a bid checklist for electrical estimators. Reviews general conditions, electrical scope, fire alarm, low voltage, and site work categories. Flags items needing estimator attention. Trigger with \"fill out the bid checklist\", \"check this spec against our checklist\", \"bid checklist for this project\", \"review the specs for bid items\", or \"what's in scope for this bid\"."
---

# Bid Checklist Filler Agent

Scans construction plans and specifications to systematically fill out a comprehensive electrical bid checklist. Reviews every relevant specification section, identifies scope items, flags ambiguities, and produces a completed checklist that ensures nothing is missed in the estimate.

## How It Works

```
┌─────────────────────────────────────────────────────────────────┐
│                 BID CHECKLIST FILLER                              │
├─────────────────────────────────────────────────────────────────┤
│  ALWAYS (works standalone with uploaded documents)               │
│  ✓ Systematic plan review across all drawing sheets             │
│  ✓ Specification parsing by CSI division                        │
│  ✓ Scope identification for all electrical disciplines          │
│  ✓ Checklist fill-in with source references                     │
│  ✓ Flag system for items needing estimator attention            │
│  ✓ Inclusion/exclusion tracking                                 │
│  ✓ Addenda and alternate review                                 │
├─────────────────────────────────────────────────────────────────┤
│  SUPERCHARGED (when you connect your tools)                      │
│  + Knowledge Base: standard Huston checklists, past bid notes   │
│  + File Storage: pull specs and plans from project folders      │
│  + Document Generation: formatted PDF checklist for bid package │
│  + Project Tracker: RFI log, addenda tracking                   │
└─────────────────────────────────────────────────────────────────┘
```

---

## Getting Started

Upload project documents and tell the agent what you need:

- "Fill out the bid checklist for this project"
- "Check this spec against our standard checklist"
- "What electrical scope is in this spec?"
- "Review Division 26 for bid items"
- "Is fire alarm in our scope for this project?"

The agent will review every relevant section and produce a completed checklist with source references.

---

## Connectors (Optional)

| Connector | What It Adds |
|-----------|--------------|
| **Knowledge Base** | Huston Electric standard checklist templates, past bid notes for similar projects, common specification traps |
| **File Storage** | Direct access to project specification PDFs, drawing sets, addenda, bid forms |
| **Document Generation** | Formatted PDF bid checklist for inclusion in bid package, printable review copies |
| **Project Tracker** | RFI tracking, addenda list, scope clarification history, bid due dates |

> **No connectors?** Upload your specs and plans directly. The agent works with whatever documents you provide.

---

## Systematic Plan Review Process

The agent reviews drawings in this order:

```
1. Cover Sheet / Drawing Index
   - Identify all electrical sheets in the set
   - Note drawing scale and general notes
   - Check for addenda references

2. General Notes Sheets (E0.x)
   - Electrical legends and abbreviations
   - General notes and requirements
   - Panel schedules
   - Fixture schedules
   - Equipment schedules

3. Site Plans (E1.x / C series)
   - Site lighting (poles, bollards, wall packs)
   - Underground conduit and feeders
   - Exterior receptacles and disconnects
   - Utility service entrance

4. Floor Plans — Lighting (E2.x)
   - All fixture types and counts (uses drawing-analysis skill)
   - Switching and dimming
   - Emergency and exit lighting
   - Lighting control systems

5. Floor Plans — Power (E3.x)
   - Receptacles (standard, dedicated, special purpose)
   - Equipment connections
   - Motor connections
   - Panel locations and feeders

6. Floor Plans — Systems (E4.x / E5.x)
   - Fire alarm devices and wiring
   - Low voltage / data / telecom
   - Security and access control
   - AV systems

7. Single Line Diagrams (E6.x)
   - Service entrance
   - Distribution equipment
   - Generator and transfer switch
   - Transformer requirements

8. Details and Schedules (E7.x+)
   - Mounting details
   - Riser diagrams
   - Panel schedules
   - Load calculations
```

---

## Specification Parsing Methodology

### Relevant CSI Divisions

| Division | Title | What to Look For |
|----------|-------|-----------------|
| **01** | General Requirements | Permit fees, temporary power, as-built requirements, O&M manuals, commissioning |
| **26** | Electrical | Core electrical scope — all sections |
| **27** | Communications | Data cabling, telecom, AV — check if in electrical scope |
| **28** | Electronic Safety & Security | Fire alarm, access control, security cameras — check if in electrical scope |
| **23** | HVAC | Mechanical equipment connections, VFDs, controls wiring — coordination |
| **25** | Integrated Automation | Building automation system (BAS) wiring and devices |
| **31** | Earthwork | Underground duct bank, trenching requirements |
| **33** | Utilities | Utility coordination, primary service, transformer pad |

### Specification Review Checklist

For each relevant specification section:

```
1. Read "PART 1 — GENERAL"
   - Scope of work (what is included/excluded)
   - Related sections and coordination requirements
   - Quality assurance and submittals required
   - Warranty requirements

2. Read "PART 2 — PRODUCTS"
   - Specified manufacturers (basis of design)
   - Approved substitutions
   - Material and equipment requirements
   - Special testing or listing requirements

3. Read "PART 3 — EXECUTION"
   - Installation requirements
   - Testing and commissioning
   - Special procedures or sequences
   - Cleanup and protection requirements
```

---

## Checklist Categories

### Category 1: General / Project-Wide

| Item | Status | Source | Notes |
|------|--------|-------|-------|
| Permit fees included? | [YES/NO/VERIFY] | [Spec section] | [Notes] |
| Temporary power and lighting? | [YES/NO/VERIFY] | [Spec section] | [Notes] |
| As-built drawings required? | [YES/NO/VERIFY] | [Spec section] | [Notes] |
| O&M manuals required? | [YES/NO/VERIFY] | [Spec section] | [Notes] |
| Commissioning participation? | [YES/NO/VERIFY] | [Spec section] | [Notes] |
| Bonding and insurance requirements? | [YES/NO/VERIFY] | [Spec section] | [Notes] |
| Liquidated damages clause? | [YES/NO/VERIFY] | [Spec section] | [Notes] |
| Prevailing wage / Davis-Bacon? | [YES/NO/VERIFY] | [Spec section] | [Notes] |
| Submittals — how many copies? | [NUMBER] | [Spec section] | [Notes] |
| Warranty period? | [DURATION] | [Spec section] | [Notes] |
| Retainage percentage? | [PERCENT] | [Spec section] | [Notes] |

### Category 2: Service and Distribution

| Item | Status | Source | Notes |
|------|--------|-------|-------|
| Utility service entrance? | [YES/NO/VERIFY] | [Sheet/Spec] | [Voltage, amperage] |
| Main switchboard? | [YES/NO/VERIFY] | [Sheet/Spec] | [Size, type] |
| Distribution panels? | [YES/NO/VERIFY] | [Sheet/Spec] | [Quantity, sizes] |
| Branch circuit panels? | [YES/NO/VERIFY] | [Sheet/Spec] | [Quantity, sizes] |
| Transformer(s)? | [YES/NO/VERIFY] | [Sheet/Spec] | [kVA, voltage] |
| Generator? | [YES/NO/VERIFY] | [Sheet/Spec] | [Size, fuel type] |
| Automatic transfer switch? | [YES/NO/VERIFY] | [Sheet/Spec] | [Size, type] |
| UPS system? | [YES/NO/VERIFY] | [Sheet/Spec] | [kVA rating] |
| Surge protection? | [YES/NO/VERIFY] | [Sheet/Spec] | [Type, locations] |
| Grounding system? | [YES/NO/VERIFY] | [Sheet/Spec] | [Type, test required?] |

### Category 3: Interior Lighting

| Item | Status | Source | Notes |
|------|--------|-------|-------|
| Recessed fixtures? | [YES/NO/VERIFY] | [Sheet/Spec] | [Types, quantities] |
| Surface mount fixtures? | [YES/NO/VERIFY] | [Sheet/Spec] | [Types, quantities] |
| Pendant fixtures? | [YES/NO/VERIFY] | [Sheet/Spec] | [Types, quantities] |
| Decorative / specialty fixtures? | [YES/NO/VERIFY] | [Sheet/Spec] | [Types, quantities] |
| Exit signs? | [YES/NO/VERIFY] | [Sheet/Spec] | [Quantity, type] |
| Emergency lighting? | [YES/NO/VERIFY] | [Sheet/Spec] | [Battery, generator?] |
| Lighting controls / dimming? | [YES/NO/VERIFY] | [Sheet/Spec] | [System type] |
| Occupancy / vacancy sensors? | [YES/NO/VERIFY] | [Sheet/Spec] | [Quantity, type] |
| Daylight harvesting? | [YES/NO/VERIFY] | [Sheet/Spec] | [Sensors, zones] |
| Under-cabinet lighting? | [YES/NO/VERIFY] | [Sheet/Spec] | [Locations] |

### Category 4: Exterior / Site Lighting

| Item | Status | Source | Notes |
|------|--------|-------|-------|
| Parking lot pole lights? | [YES/NO/VERIFY] | [Sheet/Spec] | [Quantity, height] |
| Building-mounted wall packs? | [YES/NO/VERIFY] | [Sheet/Spec] | [Quantity] |
| Bollard lights? | [YES/NO/VERIFY] | [Sheet/Spec] | [Quantity] |
| Landscape / path lighting? | [YES/NO/VERIFY] | [Sheet/Spec] | [Quantity, type] |
| Flood lights? | [YES/NO/VERIFY] | [Sheet/Spec] | [Quantity, aim] |
| Photocell control? | [YES/NO/VERIFY] | [Sheet/Spec] | [Individual, contactor?] |
| Underground conduit for site? | [YES/NO/VERIFY] | [Sheet/Spec] | [Size, length, direct burial?] |
| Concrete pole bases? | [YES/NO/VERIFY] | [Sheet/Spec] | [By electrical or civil?] |

### Category 5: Power / Receptacles

| Item | Status | Source | Notes |
|------|--------|-------|-------|
| Standard duplex receptacles? | [YES/NO/VERIFY] | [Sheet/Spec] | [Quantity] |
| GFI receptacles? | [YES/NO/VERIFY] | [Sheet/Spec] | [Locations] |
| Dedicated circuits? | [YES/NO/VERIFY] | [Sheet/Spec] | [For what equipment?] |
| Floor boxes / poke-throughs? | [YES/NO/VERIFY] | [Sheet/Spec] | [Quantity] |
| Furniture feed / modular wiring? | [YES/NO/VERIFY] | [Sheet/Spec] | [By whom?] |
| EV charging stations? | [YES/NO/VERIFY] | [Sheet/Spec] | [Quantity, level] |
| Motor connections? | [YES/NO/VERIFY] | [Sheet/Spec] | [Quantity, HP range] |
| HVAC equipment connections? | [YES/NO/VERIFY] | [Sheet/Spec] | [List from mech. schedule] |
| Kitchen equipment connections? | [YES/NO/VERIFY] | [Sheet/Spec] | [List from food service] |

### Category 6: Fire Alarm

| Item | Status | Source | Notes |
|------|--------|-------|-------|
| Fire alarm in electrical scope? | [YES/NO/VERIFY] | [Spec section] | [Division 26 or 28?] |
| Fire alarm control panel (FACP)? | [YES/NO/VERIFY] | [Sheet/Spec] | [Addressable, conventional?] |
| Smoke detectors? | [YES/NO/VERIFY] | [Sheet/Spec] | [Quantity, type] |
| Heat detectors? | [YES/NO/VERIFY] | [Sheet/Spec] | [Quantity, type] |
| Pull stations? | [YES/NO/VERIFY] | [Sheet/Spec] | [Quantity] |
| Horn/strobes (notification)? | [YES/NO/VERIFY] | [Sheet/Spec] | [Quantity, ADA?] |
| Duct detectors? | [YES/NO/VERIFY] | [Sheet/Spec] | [Quantity, by whom?] |
| Sprinkler flow/tamper? | [YES/NO/VERIFY] | [Sheet/Spec] | [Wiring only?] |
| Elevator recall? | [YES/NO/VERIFY] | [Sheet/Spec] | [Wiring only?] |
| Fire alarm monitoring? | [YES/NO/VERIFY] | [Sheet/Spec] | [Cellular, dedicated line?] |

### Category 7: Low Voltage / Data / Telecom

| Item | Status | Source | Notes |
|------|--------|-------|-------|
| Data cabling in electrical scope? | [YES/NO/VERIFY] | [Spec section] | [Division 27?] |
| Backbone cabling? | [YES/NO/VERIFY] | [Sheet/Spec] | [Fiber, copper?] |
| Horizontal station cabling? | [YES/NO/VERIFY] | [Sheet/Spec] | [Cat6, Cat6A?] |
| Data outlet locations? | [YES/NO/VERIFY] | [Sheet/Spec] | [Quantity] |
| Server room / MDF / IDF? | [YES/NO/VERIFY] | [Sheet/Spec] | [Locations] |
| Cable tray? | [YES/NO/VERIFY] | [Sheet/Spec] | [By whom?] |
| WAP (wireless access points)? | [YES/NO/VERIFY] | [Sheet/Spec] | [Quantity, cabling only?] |
| Paging / intercom? | [YES/NO/VERIFY] | [Sheet/Spec] | [Type] |
| CATV / cable television? | [YES/NO/VERIFY] | [Sheet/Spec] | [Cabling only?] |

### Category 8: Security and Access Control

| Item | Status | Source | Notes |
|------|--------|-------|-------|
| Security in electrical scope? | [YES/NO/VERIFY] | [Spec section] | [Division 28?] |
| Card readers / access control? | [YES/NO/VERIFY] | [Sheet/Spec] | [Quantity, wiring only?] |
| Security cameras (CCTV)? | [YES/NO/VERIFY] | [Sheet/Spec] | [Quantity, PoE?] |
| Door contacts / REX devices? | [YES/NO/VERIFY] | [Sheet/Spec] | [Quantity] |
| Electric door hardware? | [YES/NO/VERIFY] | [Sheet/Spec] | [Mag locks, strikes?] |
| Intrusion detection? | [YES/NO/VERIFY] | [Sheet/Spec] | [Type] |

### Category 9: Special Systems

| Item | Status | Source | Notes |
|------|--------|-------|-------|
| Lightning protection? | [YES/NO/VERIFY] | [Sheet/Spec] | [By electrical?] |
| Solar / PV system? | [YES/NO/VERIFY] | [Sheet/Spec] | [kW, inverters?] |
| Energy management / BAS wiring? | [YES/NO/VERIFY] | [Sheet/Spec] | [Points, wiring only?] |
| Nurse call / patient monitoring? | [YES/NO/VERIFY] | [Sheet/Spec] | [Type] |
| AV systems? | [YES/NO/VERIFY] | [Sheet/Spec] | [Cabling, rough-in only?] |
| Electric vehicle charging? | [YES/NO/VERIFY] | [Sheet/Spec] | [Level 2, DC fast?] |

---

## Flag System

The agent uses a three-level flag system:

| Flag | Meaning | Action Required |
|------|---------|----------------|
| **INCLUDED** | Clearly in scope per specs and drawings | Price in estimate |
| **EXCLUDED** | Clearly not in electrical scope | Verify exclusion in bid |
| **VERIFY** | Ambiguous, conflicting, or unclear scope | Estimator must review before pricing |

### Common reasons for VERIFY flags:

- Specification says "by electrical contractor" but no drawing detail exists
- Drawing shows devices but specification assigns them to another trade
- Specification references a CSI section not included in the project manual
- Addendum changes scope but does not update all affected sections
- "Furnished by owner, installed by electrical contractor" items
- Coordination items between trades (duct detectors, motor connections)
- Items shown on architectural drawings but not electrical drawings
- Allowance items without clear quantities

---

## Output Format

```markdown
# Bid Checklist: [Project Name]

**Project:** [Name]
**Bid Date:** [Date]
**Prepared By:** Bid Checklist Agent
**Documents Reviewed:** [List of specs and drawing sheets]
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

| # | Item | Category | Issue | Source |
|---|------|----------|-------|--------|
| 1 | [Item] | [Category] | [Why it needs attention] | [Spec/Drawing ref] |
| 2 | [Item] | [Category] | [Why it needs attention] | [Spec/Drawing ref] |

---

[Full category-by-category checklist follows]
```

---

## Execution Flow

### Step 1: Receive Documents

```
Accept project documents:
- Specification PDF (full project manual or electrical sections)
- Drawing set (full set or electrical sheets)
- Addenda documents
- Bid form or scope of work summary
- Previous bid checklist template (if available from ~~knowledge base)
```

### Step 2: Index Available Documents

```
Catalog what was received:
1. List all specification sections available
2. List all drawing sheets available
3. Identify any addenda
4. Note any missing sections or sheets
5. Flag gaps (e.g., "Division 28 not included — fire alarm scope unclear")
```

### Step 3: Review Specifications

```
For each relevant CSI division (01, 26, 27, 28, and referenced sections):
1. Read PART 1 — identify scope, related sections, submittals
2. Read PART 2 — identify specified products and materials
3. Read PART 3 — identify installation and testing requirements
4. Extract every scope item and map to checklist category
5. Note special requirements (prevailing wage, commissioning, etc.)
6. Flag ambiguities and conflicts
```

### Step 4: Review Drawings

```
For each drawing sheet:
1. Read title block — sheet number, title, scale, revision
2. Review general notes
3. Identify scope items shown on the drawing
4. Cross-reference with specification requirements
5. Note items on drawings not in specs (and vice versa)
6. Flag coordination items with other trades
```

### Step 5: Fill Checklist

```
For each checklist item:
1. Determine status: INCLUDED, EXCLUDED, or VERIFY
2. Record source reference (spec section and/or drawing sheet)
3. Add notes for quantities, special requirements, or concerns
4. Cross-reference addenda for changes
5. Check for conflicts between spec and drawings
```

### Step 6: Generate Flag Report

```
Compile all VERIFY items:
1. Describe the ambiguity or conflict
2. Cite the source documents
3. Suggest resolution (RFI, clarification, assumption)
4. Prioritize by cost impact (high, medium, low)
```

### Step 7: Produce Completed Checklist

```
Output:
1. Summary table with category totals
2. Items requiring estimator attention (prioritized)
3. Full category-by-category completed checklist
4. Exclusion list for bid letter
5. Assumptions list for bid qualification
```

---

## Tips for Better Checklists

1. **Upload the full spec** — Even non-electrical divisions contain scope that affects the electrical bid (HVAC connections, kitchen equipment, etc.)
2. **Include all addenda** — Addenda frequently change electrical scope
3. **Upload the bid form** — Some bid forms list alternates, allowances, and unit prices that need to be captured
4. **Mention the project type** — "This is a K-12 school" helps the agent know to look for specific code requirements
5. **Flag known concerns** — "I think fire alarm might not be in our scope" focuses the agent's attention

---

## Related Skills

- **drawing-analysis** — Provides fixture counts that feed into the checklist lighting section
- **apartment-budget** — Uses checklist scope items to build the apartment budget
