---
description: Generate an electrical safety procedure — LOTO procedures, arc flash protocols, PPE selection guides, emergency response plans, or general safe work procedures for Huston Electric, Inc.
argument-hint: "<task, equipment, or hazard description>"
---

# /safety-procedure

> If you see unfamiliar placeholders or need to check which tools are connected, see [CONNECTORS.md](../CONNECTORS.md).

Generate a complete electrical safety procedure document with hazard identification, regulatory references, PPE requirements, step-by-step instructions, and emergency response procedures.

## Usage

```
/safety-procedure <description of task, equipment, or hazard>
```

Generate a safety procedure for: $ARGUMENTS

If a file is referenced: @$1

---

## How It Works

```
┌─────────────────────────────────────────────────────────────────┐
│                     SAFETY PROCEDURE                              │
├─────────────────────────────────────────────────────────────────┤
│  STANDALONE (always works)                                       │
│  + Describe the task, equipment, or hazard                       │
│  + Identify applicable OSHA, NFPA 70E, NEC standards            │
│  + Perform hazard analysis for the task                          │
│  + Determine PPE requirements using NFPA 70E tables              │
│  + Generate step-by-step procedure with safety controls          │
│  + Include emergency procedures and post-work checklists         │
├─────────────────────────────────────────────────────────────────┤
│  SUPERCHARGED (when you connect your tools)                      │
│  + Knowledge base: past procedures, equipment data, company      │
│    policies, arc flash studies, incident history                 │
│  + Document storage: save procedure, retrieve equipment          │
│    manuals, manufacturer safety data                             │
│  + Email: distribute procedure to affected workers               │
│  + Chat: notify team of new/updated procedure                    │
└─────────────────────────────────────────────────────────────────┘
```

---

## What I Need From You

**Option 1: Describe the task**
Tell me what work is being performed: "Replacing a 200A breaker in a 480V panelboard" or "Installing a new 120/208V sub-panel."

**Option 2: Name the equipment**
Tell me what equipment you are working on: "Square D QED2 switchboard" or "480V MCC bucket replacement."

**Option 3: Specify the procedure type**
Tell me what type of procedure you need:
- **LOTO procedure** — "LOTO for AHU-3 supply fan disconnect"
- **Arc flash protocol** — "Arc flash PPE for 480V switchgear maintenance"
- **PPE selection guide** — "What PPE for testing 277/480V circuits?"
- **Emergency response** — "Electrical shock response procedure"
- **Safe work procedure** — "Procedure for pulling wire through energized conduit runs"

**Option 4: Upload documents**
Upload equipment manuals, arc flash study results, or existing procedures for Sparky to reference and improve.

---

## Procedure Types

### General Safe Work Procedure
Complete procedure for a specific electrical task. Includes purpose, scope, hazard identification, qualifications, PPE, tools, pre-work checklist, step-by-step instructions, emergency procedures, and post-work requirements.

### LOTO Procedure
Equipment-specific Lockout/Tagout procedure. Includes energy source identification (all types), lockout sequence, verification method (live-dead-live), stored energy dissipation, and restoration sequence.

### Arc Flash Protocol
Task-specific arc flash safety requirements. Includes PPE category determination (table method or incident energy analysis), approach boundaries, required PPE list, and arc flash label content.

### PPE Selection Guide
Complete PPE requirements for a task or equipment. References NFPA 70E tables, approach boundaries, glove class selection, and arc-rated clothing requirements.

### Emergency Response Procedure
Site or task-specific emergency response procedures. Includes shock response, arc flash burn treatment, fire response, and notification requirements.

---

## Output

The procedure document follows the format defined in the `safety-specialist` skill. Key sections include:

1. **Purpose and Scope** — What this procedure covers
2. **Applicable Standards** — OSHA, NFPA 70E, NEC, IEEE references with specific sections
3. **Hazard Identification** — Hazard/source/severity/likelihood/risk level matrix
4. **Qualifications Required** — Who can perform this work
5. **PPE Requirements** — Category, arc rating, specific items with ASTM/ANSI standards
6. **Tools and Equipment** — Voltage-rated tools, test equipment, safety devices
7. **Pre-Work Safety Checklist** — Job briefing, permits, LOTO, PPE inspection
8. **Step-by-Step Procedure** — Each step with hazards and controls identified
9. **Emergency Procedures** — Shock, burn, fire, and medical emergency response
10. **Post-Work Requirements** — Cleanup, verification, LOTO removal, documentation

---

## If Connectors Available

**Knowledge base connected:**
- Search for existing Huston Electric procedures for this task/equipment
- Pull equipment-specific data (voltage, fault current, clearing time)
- Reference arc flash study results
- Check incident history for this type of work
- Apply company-specific requirements beyond OSHA minimums

**Document storage connected:**
- Save generated procedure with company document numbering
- Retrieve equipment manuals for accurate energy source identification
- Pull manufacturer safety bulletins and recommendations

**Email connected:**
- Distribute procedure to affected workers and supervisors
- Send to Safety Director for review and approval
- Notify project team of new or updated procedure

**Chat connected:**
- Post notification of new procedure to safety channel
- Alert affected crews to review the procedure

---

## Tips

1. **Include voltage levels** — Procedures and PPE vary dramatically between 120V and 480V work
2. **Name the equipment** — "480V Square D I-Line panelboard" produces a much better procedure than "electrical panel"
3. **Describe the environment** — Indoor, outdoor, wet, confined space, elevated, occupied building
4. **Mention fault current** — If you know the available fault current, arc flash PPE selection is more precise
5. **State the condition** — Working de-energized (LOTO) vs energized makes a major difference in procedure content
6. **Flag special conditions** — Permit-required confined space, fall hazard, existing asbestos, occupied building, night work
