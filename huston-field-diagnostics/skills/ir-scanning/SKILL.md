---
name: ir-scanning
description: Infrared scanning interpretation and reporting for electrical equipment. Analyzes thermographic data to classify severity, identify components, and generate NFPA 70B-compliant reports. Trigger with "IR scan", "infrared report", "thermal scan", "thermography", "hot spot", "temperature differential", "delta T", "thermal image", or "IR inspection".
---

# IR Scanning Interpretation Agent

Expert infrared thermography interpretation for electrical systems. This skill analyzes thermal data from infrared scans of electrical equipment — classifying severity, identifying probable causes, recommending corrective actions, and generating NFPA 70B-compliant reports. Works standalone with temperature data you provide, supercharged when connected to your knowledge base and document tools.

## How It Works

```
┌─────────────────────────────────────────────────────────────────┐
│                  IR SCANNING INTERPRETATION                       │
├─────────────────────────────────────────────────────────────────┤
│  ALWAYS (works standalone)                                        │
│  ✓ You provide: temperature data, component descriptions         │
│  ✓ Temperature differential (delta T) analysis                   │
│  ✓ Severity classification (minor, serious, critical, emergency) │
│  ✓ Probable cause identification                                 │
│  ✓ Recommended corrective actions with priority and timeline     │
│  ✓ NFPA 70B-compliant report generation                         │
│  ✓ Trend analysis when historical data is available              │
├─────────────────────────────────────────────────────────────────┤
│  SUPERCHARGED (when you connect your tools)                       │
│  + Knowledge base: equipment records, past IR scans, baselines   │
│  + Document storage: report templates, archived thermal images   │
│  + Email: distribute reports to maintenance teams and clients    │
│  + Chat: urgent notification of critical/emergency findings      │
│  + Calendar: schedule re-inspections and maintenance windows     │
└─────────────────────────────────────────────────────────────────┘
```

---

## Connectors (Optional)

| Connector | What It Adds |
|-----------|--------------|
| **Knowledge base** | Equipment records, past IR scan results, baseline temperatures, maintenance history |
| **Document storage** | Report templates, archived thermal images, equipment photos |
| **Email** | Send reports to clients, distribute critical findings to maintenance staff |
| **Chat** | Immediate notification of emergency findings, team coordination |
| **Calendar** | Schedule re-inspections, book maintenance windows for repairs |

> **No connectors?** No problem. Give me the temperature data, describe what you're looking at, and I'll classify severity and generate a complete report.

---

## Getting Started

When this skill is triggered, I need the following:

**Required:**
- Component type (breaker, bus connection, fuse, cable termination, transformer, motor, etc.)
- Measured temperature of the anomaly
- Reference temperature (similar component under similar load, or ambient)
- Load at time of inspection (percentage of rated, or actual amps)

**Helpful if you have it:**
- Equipment nameplate data (manufacturer, rating, age)
- Location in the electrical system (panel ID, breaker number, feeder)
- Ambient temperature at time of scan
- Wind conditions (outdoor equipment)
- Emissivity setting used on the IR camera
- IR camera model and lens
- Thermal images (if working in a tool that supports image analysis)
- Past IR scan data for trend comparison

---

## Temperature Differential Analysis

### Delta T Calculation

The primary metric for IR scan evaluation is the temperature differential (delta T) between the anomaly and a comparable reference:

```
Delta T = T_anomaly - T_reference

Where:
  T_anomaly   = Temperature of the suspected hot spot
  T_reference = Temperature of a similar component under similar
                load conditions (same phase, adjacent breaker,
                opposite end of same conductor)
```

### Reference Selection Priority

Use the best available reference, in this order:

1. **Same component, different phase** (e.g., Phase A vs. Phase B on same breaker) — best for 3-phase equipment
2. **Identical component, same load** (e.g., adjacent breaker of same type at similar load) — good for single-phase
3. **Same component, previous scan** (historical baseline) — useful for trend analysis
4. **Ambient temperature** (last resort) — use only when no comparable component exists

### Load Correction

Temperature rise is approximately proportional to the square of the current. When evaluating findings at less than full load, apply a correction:

```
Estimated delta T at full load = Measured delta T x (I_rated / I_measured)^2

Example:
  Measured delta T: 15 C at 60% load
  Estimated at 100% load: 15 x (1.0 / 0.6)^2 = 15 x 2.78 = 41.7 C
  This changes a "serious" finding into a "critical" finding.
```

**Important:** Always note the load at time of inspection. A finding that looks minor at 40% load may be critical at full load.

---

## Severity Classification

### Four-Level Classification System

Based on NFPA 70B recommendations and industry best practices:

```
┌────────────┬──────────────┬────────────────────────────────────────┐
│ Severity   │ Delta T      │ Action Required                        │
├────────────┼──────────────┼────────────────────────────────────────┤
│ MINOR      │ 1-10 C       │ Monitor — schedule repair at next      │
│            │ (2-18 F)     │ available maintenance window.           │
│            │              │ Re-inspect in 12 months.                │
├────────────┼──────────────┼────────────────────────────────────────┤
│ SERIOUS    │ 11-30 C      │ Repair soon — schedule repair within   │
│            │ (20-54 F)    │ 30 days. Re-inspect monthly until       │
│            │              │ repaired. Monitor load.                 │
├────────────┼──────────────┼────────────────────────────────────────┤
│ CRITICAL   │ 31-70 C      │ Repair immediately — schedule repair   │
│            │ (56-126 F)   │ as soon as possible. Reduce load if    │
│            │              │ feasible. Re-inspect weekly.            │
├────────────┼──────────────┼────────────────────────────────────────┤
│ EMERGENCY  │ >70 C        │ Emergency action — de-energize if      │
│            │ (>126 F)     │ safe to do so. Imminent failure risk.   │
│            │              │ Do not re-energize until repaired.      │
│            │              │ Notify facility management immediately. │
└────────────┴──────────────┴────────────────────────────────────────┘
```

### Additional Severity Considerations

Escalate severity by one level if any of the following apply:

- **Safety-critical system** — emergency power, fire alarm, life safety circuits
- **High consequence of failure** — data center, continuous process, healthcare
- **Evidence of progressive deterioration** — delta T increasing scan over scan
- **Component at or above its rated temperature** — regardless of delta T
- **Load-corrected delta T exceeds next threshold** — finding is worse at full load
- **Visible damage** — discoloration, melting, arc tracking, burnt insulation

---

## Component Identification

### Common Anomaly Locations and Probable Causes

```
SWITCHGEAR AND PANELBOARDS
┌──────────────────────────────┬──────────────────────────────────────┐
│ Location                     │ Probable Cause                       │
├──────────────────────────────┼──────────────────────────────────────┤
│ Breaker line-side lug        │ Loose connection, oxidized contact   │
│ Breaker load-side lug        │ Loose connection, undersized lug     │
│ Breaker internal (body hot)  │ Internal contact degradation,        │
│                              │ overload, breaker failure             │
│ Bus connection (bolted)      │ Loose bolts, Belleville washers      │
│                              │ flattened, oxidation, plating failure│
│ Bus splice                   │ Loose splice bolts, corrosion        │
│ Neutral bar connection       │ Loose lug, overloaded neutral        │
│ Ground bar connection        │ Loose lug, corrosion                 │
│ Fuse clip                    │ Weak spring tension, oxidation,      │
│                              │ wrong fuse size                      │
│ Fuse body (entire fuse hot)  │ Overloaded, deteriorating element    │
└──────────────────────────────┴──────────────────────────────────────┘

TRANSFORMERS
┌──────────────────────────────┬──────────────────────────────────────┐
│ Location                     │ Probable Cause                       │
├──────────────────────────────┼──────────────────────────────────────┤
│ Primary termination          │ Loose connection, oxidation          │
│ Secondary termination        │ Loose connection, overload           │
│ Tank hot spot                │ Internal winding fault, core issue,  │
│                              │ cooling system failure               │
│ Cooling fans/radiators       │ Fan failure, blocked airflow,        │
│                              │ clogged radiators                    │
│ Bushing                      │ Internal insulation degradation      │
│ Tap changer                  │ Contact degradation, mechanism issue │
│ Overall elevated temperature │ Overload, harmonic heating,          │
│                              │ K-factor exceedance                  │
└──────────────────────────────┴──────────────────────────────────────┘

MOTORS AND DRIVES
┌──────────────────────────────┬──────────────────────────────────────┐
│ Location                     │ Probable Cause                       │
├──────────────────────────────┼──────────────────────────────────────┤
│ Motor terminal box           │ Loose connection, undersized leads   │
│ Motor bearing (DE or NDE)    │ Bearing failure, inadequate          │
│                              │ lubrication, misalignment            │
│ Motor winding (overall)      │ Overload, voltage imbalance,         │
│                              │ blocked ventilation, single phasing  │
│ VFD heatsink                 │ Fan failure, blocked filter,         │
│                              │ overload, ambient too high           │
│ VFD input/output terminals   │ Loose connections                    │
│ Cable termination at motor   │ Loose lug, corrosion, moisture      │
└──────────────────────────────┴──────────────────────────────────────┘

CONDUCTORS AND CONNECTIONS
┌──────────────────────────────┬──────────────────────────────────────┐
│ Location                     │ Probable Cause                       │
├──────────────────────────────┼──────────────────────────────────────┤
│ Cable termination / lug      │ Loose connection, wrong torque,      │
│                              │ oxidation, wrong lug type            │
│ Wire nut / splice            │ Loose connection, improper splice    │
│ Conductor run (mid-span)     │ Overload, undersized conductor,     │
│                              │ damaged insulation                   │
│ Cable tray / conduit hot spot│ Overloaded circuit, eddy current     │
│                              │ heating in steel conduit             │
│ Plug / receptacle            │ Loose contact, worn receptacle,      │
│                              │ backstab connection failure          │
└──────────────────────────────┴──────────────────────────────────────┘
```

---

## Recommended Actions by Finding Type

### Loose Connection (Most Common — ~70% of IR Findings)

```
Corrective Action:
1. De-energize and lock out/tag out (LOTO)
2. Remove conductor from terminal
3. Clean contact surfaces (wire brush, contact cleaner)
4. Inspect for damage (pitting, discoloration, deformation)
5. Replace lug if damaged or discolored
6. Apply oxide inhibitor (for aluminum conductors — always)
7. Re-terminate with calibrated torque wrench to manufacturer specs
8. Re-energize and verify with IR scan under load

Torque Specifications (Reference — always use manufacturer's values):
  #14-#10 AWG: 20-25 in-lb
  #8-#6 AWG: 35-45 in-lb
  #4-#2 AWG: 45-60 in-lb
  #1-2/0 AWG: 60-80 in-lb
  3/0-4/0 AWG: 80-100 in-lb
  250-500 kcmil: 100-200 in-lb (varies by manufacturer)
```

### Overloaded Circuit

```
Corrective Action:
1. Verify actual load current vs. circuit rating
2. Determine cause of overload (added loads, failed equipment)
3. Options:
   a. Reduce load — redistribute to other circuits
   b. Upsize conductor — if conduit fill allows
   c. Upsize breaker — only if conductor supports it
   d. Add new circuit — for permanent load growth
4. Re-inspect after corrective action under full load
```

### Deteriorating Component (Breaker, Fuse, Contact)

```
Corrective Action:
1. Replace the component
2. Inspect adjacent components for similar deterioration
3. Evaluate if environmental factors contributed (moisture,
   corrosion, contamination, vibration)
4. Consider upgrading to higher-quality components if pattern
   of repeated failure exists
5. Re-inspect after replacement under load
```

---

## NFPA 70B Maintenance Standards Reference

### Applicable Sections

- **NFPA 70B Chapter 11:** Thermographic surveys of electrical equipment
- **Frequency recommendations:**
  - Annual IR scans for general electrical equipment
  - Semi-annual for critical systems and high-reliability facilities
  - Quarterly for equipment with known issues or aging infrastructure
  - After major maintenance or modifications
  - Before and after planned shutdowns

### NFPA 70B Thermographic Survey Requirements

```
SURVEY PREPARATION
- Equipment should be under normal operating load (minimum 40% of rated)
- Panels and enclosures should be opened or covers removed
  (follow NFPA 70E arc flash requirements)
- Allow equipment to reach thermal equilibrium (minimum 1 hour under load)
- Document ambient conditions (temperature, humidity, wind)
- Verify IR camera calibration and emissivity settings

SURVEY DOCUMENTATION
- Date and time of inspection
- Equipment identification and location
- Ambient temperature and conditions
- Load at time of inspection
- IR camera model, serial number, emissivity setting
- Thermal image of each anomaly
- Visual image of each anomaly (for component identification)
- Reference temperature measurement point
- Severity classification and recommended action

SURVEY SCOPE (per NFPA 70B)
- Service entrance equipment
- Main switchgear and switchboards
- Distribution panelboards
- Motor control centers
- Transformers (dry-type and liquid-filled)
- Bus duct and plug-in units
- Disconnects and safety switches
- Automatic transfer switches
- Capacitor banks
- Large motors and motor connections
- UPS systems
- Generator connections and transfer equipment
```

---

## Report Format

### IR Inspection Report Template

```markdown
# Infrared Thermographic Inspection Report

**Client:** [Company Name]
**Site:** [Facility Address]
**Prepared by:** [Thermographer Name], [Certification Level]
**Date of Inspection:** [Date]
**Report No:** [HE-IR-YYYY-XXXX]

---

## Inspection Parameters

| Parameter | Value |
|-----------|-------|
| **IR Camera** | [Model, Serial Number] |
| **Lens** | [Focal length] |
| **Emissivity Setting** | [0.XX] |
| **Reflected Temperature** | [XX C / XX F] |
| **Ambient Temperature** | [XX C / XX F] |
| **Humidity** | [XX%] |
| **Wind** | [Calm / Light / Moderate — for outdoor] |
| **Load Condition** | [XX% of rated / XX Amps measured] |
| **Certification** | [Level I / II / III Thermographer, Cert #] |

---

## Executive Summary

[2-3 paragraph summary for facility management. Include total findings
count by severity, most urgent items requiring immediate attention, and
overall assessment of electrical system thermal health.]

### Findings Summary

| Severity | Count | Action Required |
|----------|-------|-----------------|
| Emergency | [X] | De-energize immediately |
| Critical | [X] | Repair as soon as possible |
| Serious | [X] | Repair within 30 days |
| Minor | [X] | Schedule at next maintenance window |
| **Total** | **[X]** | |

---

## Detailed Findings

### Finding [#]: [Component Description]

| Field | Value |
|-------|-------|
| **Equipment** | [Panel/MCC/Switchgear ID] |
| **Component** | [Breaker / Bus / Fuse / Connection / etc.] |
| **Location** | [Building, Floor, Room, Panel ID] |
| **Phase** | [A / B / C / Neutral] |
| **Anomaly Temperature** | [XX.X C / XX.X F] |
| **Reference Temperature** | [XX.X C / XX.X F] |
| **Delta T** | [XX.X C / XX.X F] |
| **Load at Time of Scan** | [XX% of rated / XX Amps] |
| **Load-Corrected Delta T** | [XX.X C (at 100% load)] |
| **Severity** | [MINOR / SERIOUS / CRITICAL / EMERGENCY] |

**Thermal Image:**
[Thermal image with temperature scale, measurement markers, and
component labels — or description of thermal pattern observed]

**Visual Image:**
[Corresponding visual photograph for component identification]

**Probable Cause:** [Loose connection / Overload / Component
degradation / etc.]

**Recommended Action:** [Specific corrective action with timeline]

**Priority:** [Immediate / 30 days / Next maintenance window / Monitor]

---

[Repeat for each finding]

---

## Equipment Inspected — No Exceptions Found

| Equipment ID | Description | Location | Load | Status |
|--------------|-------------|----------|------|--------|
| [ID] | [Description] | [Location] | [XX%] | Normal |
| [ID] | [Description] | [Location] | [XX%] | Normal |

---

## Recommendations Summary

| # | Equipment | Finding | Severity | Action | Timeline |
|---|-----------|---------|----------|--------|----------|
| 1 | [ID] | [Brief description] | [Level] | [Action] | [When] |
| 2 | [ID] | [Brief description] | [Level] | [Action] | [When] |

---

## Re-Inspection Schedule

| Finding # | Equipment | Severity | Re-Inspect By |
|-----------|-----------|----------|---------------|
| [#] | [ID] | Critical | [Date — within 1 week] |
| [#] | [ID] | Serious | [Date — within 30 days] |
| [#] | [ID] | Minor | [Date — next annual scan] |

---

## Appendices

### Appendix A: Thermal Images (Full Resolution)
### Appendix B: Equipment Single-Line Diagram
### Appendix C: Inspection Route / Equipment List
### Appendix D: Thermographer Certification
### Appendix E: Camera Calibration Certificate
```

---

## Execution Flow

### Step 1: Gather Inspection Data

**If connectors available:**
```
1. Knowledge base → Search for equipment records
   - Pull: equipment inventory for the site
   - Pull: past IR scan results for baseline comparison
   - Pull: maintenance history and known issues

2. Document storage → Search for reference files
   - Pull: report template
   - Pull: site single-line diagram
   - Pull: previous IR reports for this facility
```

**If no connectors:**
```
1. Ask thermographer:
   - "What equipment did you scan?"
   - "What temperature readings did you get?"
   - "What was the reference temperature?"
   - "What was the load at time of inspection?"
   - "What is the ambient temperature?"
   - "What camera and emissivity did you use?"

2. Accept whatever data they provide
```

### Step 2: Classify Each Finding

```
For each anomaly reported:
1. Calculate delta T (anomaly - reference)
2. Apply load correction if less than full load
3. Classify severity (minor / serious / critical / emergency)
4. Check for escalation factors (safety-critical, trend, rated temp)
5. Identify probable cause based on component type and pattern
6. Determine recommended corrective action
7. Assign timeline based on severity
```

### Step 3: Trend Analysis (if historical data available)

```
1. Compare current readings to past scans
2. Calculate rate of temperature increase
3. Identify components trending toward higher severity
4. Flag any components that were previously repaired but returned
5. Note new findings not present in prior scans
```

### Step 4: Generate Report

```
1. Compile all findings into NFPA 70B-compliant format
2. Sort findings by severity (emergency first)
3. Write executive summary for facility management
4. Include all measurement data and thermal descriptions
5. Generate recommendations summary table
6. Create re-inspection schedule

If connectors available:
7. Save report to document storage
8. Email report to client and internal distribution
9. Log findings in knowledge base
10. Schedule re-inspections via calendar
11. If emergency/critical findings: notify team via chat
```

---

## IR Camera Settings Guide

### Emissivity Reference Values

```
COMMON ELECTRICAL MATERIALS
┌────────────────────────────┬──────────────┐
│ Material                   │ Emissivity   │
├────────────────────────────┼──────────────┤
│ Oxidized copper            │ 0.65 - 0.78  │
│ Polished copper            │ 0.02 - 0.07  │
│ Oxidized aluminum          │ 0.20 - 0.33  │
│ Anodized aluminum          │ 0.77 - 0.85  │
│ Painted metal (any color)  │ 0.90 - 0.95  │
│ Electrical tape (black)    │ 0.95 - 0.97  │
│ Plastic / rubber insulation│ 0.90 - 0.95  │
│ Porcelain insulator        │ 0.85 - 0.92  │
│ Oxidized steel             │ 0.70 - 0.85  │
│ Galvanized steel           │ 0.23 - 0.28  │
│ Glass (thick)              │ 0.85 - 0.92  │
│ Concrete                   │ 0.92 - 0.97  │
└────────────────────────────┴──────────────┘

BEST PRACTICES
- Use electrical tape targets on low-emissivity surfaces
- Allow tape to reach thermal equilibrium (minimum 10 minutes)
- Adjust emissivity for each material type
- Note emissivity setting used for each measurement
- When in doubt, use 0.95 for painted or insulated surfaces
```

### Minimum Detectable Temperature Difference

The accuracy of the finding depends on camera capability and conditions:

- Modern IR cameras: +/- 2 C or +/- 2% of reading
- Environmental factors: wind, solar loading, reflected heat sources
- Distance: spatial resolution decreases with distance (IFOV matters)
- Focus: out-of-focus images understate temperature differences

---

## Common Pitfalls in IR Scanning Interpretation

1. **Ignoring load conditions** — A 5 C delta T at 30% load is actually a 56 C delta T at full load. Always load-correct.
2. **Using ambient as reference for enclosed equipment** — Inside a panel is always warmer than ambient. Use same-type component as reference.
3. **Missing the worst phase** — Always scan all three phases. The worst connection may not be the one you initially noticed.
4. **Solar loading on outdoor equipment** — Sun-facing surfaces appear hotter. Scan outdoor equipment on overcast days or shade the equipment.
5. **Reflections mistaken for hot spots** — Low-emissivity surfaces (polished metal, bare aluminum) reflect heat from other sources. Verify with contact thermometer.
6. **Scanning through glass or plastic** — IR does not transmit through standard glass or polycarbonate windows. Use IR-transparent windows or remove covers.
7. **Failing to document "normal" equipment** — Documenting what looks normal establishes baselines and proves scope of inspection.
8. **Not correlating with electrical measurements** — An IR anomaly at a connection should prompt a voltage drop measurement to confirm resistance.

---

## Safety Considerations (NFPA 70E)

```
ARC FLASH AND SHOCK HAZARD
- All IR inspections of energized electrical equipment must comply
  with NFPA 70E
- Perform an arc flash risk assessment before opening panels
- Wear appropriate PPE based on incident energy level:
  - Category 1: 4 cal/cm2 — arc-rated shirt, safety glasses
  - Category 2: 8 cal/cm2 — arc-rated clothing, face shield
  - Category 3: 25 cal/cm2 — arc flash suit, hood
  - Category 4: 40 cal/cm2 — arc flash suit, full hood
- Use IR-transparent viewing windows where installed to avoid
  opening panel covers
- Maintain safe approach boundaries (limited, restricted, prohibited)
- Two-person rule for energized work: one person operates camera,
  one serves as safety watch
- Ensure an energized work permit is in place if required by
  facility policy
```

---

## Configuration

### Default Settings

```yaml
severity_thresholds:
  minor:
    delta_t_min_c: 1
    delta_t_max_c: 10
    action: "Monitor — repair at next maintenance window"
    reinspect: "12 months"
  serious:
    delta_t_min_c: 11
    delta_t_max_c: 30
    action: "Repair within 30 days"
    reinspect: "Monthly until repaired"
  critical:
    delta_t_min_c: 31
    delta_t_max_c: 70
    action: "Repair as soon as possible"
    reinspect: "Weekly until repaired"
  emergency:
    delta_t_min_c: 71
    action: "De-energize immediately if safe"
    reinspect: "Do not re-energize until repaired"

escalation_factors:
  - "Safety-critical system"
  - "High-consequence facility (data center, healthcare)"
  - "Progressive deterioration (trending worse)"
  - "Component at or above rated temperature"
  - "Load-corrected delta T exceeds next threshold"
  - "Visible damage or arc tracking"

camera_defaults:
  emissivity: 0.95
  reflected_temperature: "ambient"
  distance_correction: true

report:
  format: "markdown"
  include_normal_equipment: true
  include_reinspection_schedule: true
  numbering_prefix: "HE-IR"
  compliance_standard: "NFPA 70B"

inspection_frequency:
  general: "Annual"
  critical_systems: "Semi-annual"
  known_issues: "Quarterly"
  post_maintenance: "After major work"
```

---

## Tips for Better IR Interpretation

1. **Always load-correct** — The single most important adjustment. A finding at half load is four times worse at full load.
2. **Compare phase to phase** — Three-phase equipment gives you built-in references. If one phase is hot, you have two comparisons.
3. **Look for patterns** — Multiple loose connections on the same panel suggest vibration, improper torque practices, or thermal cycling issues.
4. **Check both ends of every conductor** — If one end is loose, the other end may be too. Check the source and the load.
5. **Correlate with age and maintenance** — Equipment that has never been re-torqued since installation is overdue for maintenance regardless of IR findings.
6. **Repeat findings tell a story** — If the same connection is found loose scan after scan, the root cause is not being addressed (vibration, undersized lug, thermal cycling).
7. **Document environmental conditions** — Temperature, humidity, and wind all affect readings. Without this context, the data loses value.
8. **Quantify the risk** — A 40 C delta T on a 20A lighting panel is different from a 40 C delta T on an 800A feeder breaker. Consequence matters.

---

## Related Skills

- **power-quality** — Power quality diagnostics — often performed alongside IR surveys for comprehensive electrical system assessment
