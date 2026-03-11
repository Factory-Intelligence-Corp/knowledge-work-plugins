---
name: power-quality
description: Expert power quality diagnostic agent for electrical systems. Comprehensive field analysis methodology covering voltage sags/swells, harmonics, transients, power factor, grounding problems, and more. References IEEE 519, IEEE 1159, and ANSI standards. Trigger with "diagnose power quality", "power quality issue", "harmonics problem", "voltage sag", "VFD faults", "equipment tripping", "power factor", "grounding issue", or "THD analysis".
---

# Power Quality Diagnostic Agent

Expert-level power quality diagnostics for electrical systems. This skill provides a systematic, standards-based methodology for identifying, measuring, analyzing, and resolving power quality issues in commercial and industrial facilities. Works standalone with symptoms and measurements you provide, supercharged when connected to your knowledge base and document tools.

## How It Works

```
┌─────────────────────────────────────────────────────────────────┐
│                 POWER QUALITY DIAGNOSTIC AGENT                    │
├─────────────────────────────────────────────────────────────────┤
│  ALWAYS (works standalone)                                        │
│  ✓ You describe: symptoms, equipment affected, site conditions   │
│  ✓ Systematic diagnostic methodology (6-phase process)           │
│  ✓ Root cause analysis based on symptoms and measurements        │
│  ✓ IEEE 519 / IEEE 1159 / ANSI C84.1 compliance evaluation      │
│  ✓ Corrective action recommendations with cost estimates         │
│  ✓ Priority-ranked remediation plan                               │
│  ✓ Formal diagnostic report generation                           │
├─────────────────────────────────────────────────────────────────┤
│  SUPERCHARGED (when you connect your tools)                       │
│  + Knowledge base: equipment history, past diagnostics, specs    │
│  + Document storage: report templates, reference standards       │
│  + Email: send reports to clients and engineering staff           │
│  + Chat: notify team of critical findings in real-time           │
│  + Calendar: schedule follow-up measurements and maintenance     │
└─────────────────────────────────────────────────────────────────┘
```

---

## Connectors (Optional)

Connect your tools to supercharge this skill:

| Connector | What It Adds |
|-----------|--------------|
| **Knowledge base** | Equipment history, nameplate data, past diagnostic reports, site single-line diagrams |
| **Document storage** | Report templates, reference standards library, archived measurements |
| **Email** | Send completed reports to clients, distribute urgent findings |
| **Chat** | Real-time notification of critical findings, team coordination |
| **Calendar** | Schedule follow-up measurements, maintenance windows |

> **No connectors?** No problem. Describe your symptoms, paste your measurements, and tell me about the site. I'll walk you through the full diagnostic methodology.

---

## Diagnostic Methodology

### Phase 1: Initial Assessment

Gather the critical information needed to scope the diagnostic:

```
1. SYMPTOMS
   - What is happening? (equipment tripping, flickering lights, overheating,
     drive faults, premature equipment failure, nuisance breaker trips)
   - When did it start? (sudden onset, gradual, intermittent, time-of-day pattern)
   - What changed? (new equipment installed, load changes, utility work,
     construction, weather events)

2. EQUIPMENT AFFECTED
   - What equipment is experiencing problems?
   - Equipment nameplate data (voltage, current, kVA/HP rating)
   - Age and condition of affected equipment
   - Single-line diagram location (which panel, feeder, transformer)

3. SITE CONDITIONS
   - Facility type (manufacturing, commercial, data center, healthcare)
   - Voltage system (120/208V, 277/480V, 4160V, 13.8kV)
   - Service entrance configuration (utility transformer, main switchgear)
   - Known nonlinear loads (VFDs, UPS, LED lighting, welders, arc furnaces)
   - Backup power systems (generators, UPS, automatic transfer switches)

4. HISTORICAL CONTEXT
   - Previous power quality studies or reports
   - Utility power quality complaints or records
   - Equipment failure history and patterns
   - Recent electrical modifications or additions
```

### Phase 2: Measurement Planning

Determine what to measure, where, when, and for how long:

```
MEASUREMENT MATRIX

┌──────────────────┬────────────────────┬──────────────┬──────────────┐
│ Parameter        │ Measurement Point  │ Duration     │ Equipment    │
├──────────────────┼────────────────────┼──────────────┼──────────────┤
│ Voltage (RMS)    │ Service entrance   │ 7-day min    │ PQ analyzer  │
│ Voltage (RMS)    │ Affected equipment │ 7-day min    │ PQ analyzer  │
│ Current (RMS)    │ Feeder circuits    │ 7-day min    │ PQ analyzer  │
│ Harmonics (V&I)  │ Service entrance   │ 7-day min    │ PQ analyzer  │
│ Harmonics (V&I)  │ Nonlinear loads    │ Spot check   │ PQ analyzer  │
│ Transients       │ Service entrance   │ 7-day min    │ PQ analyzer  │
│ Power factor     │ Service entrance   │ 7-day min    │ PQ analyzer  │
│ Neutral-ground V │ Panel/equipment    │ Spot check   │ DMM          │
│ Ground impedance │ Ground grid/rods   │ Spot check   │ Ground tester│
│ Frequency        │ Service entrance   │ 7-day min    │ PQ analyzer  │
│ Flicker (Pst)    │ Affected circuits  │ 7-day min    │ PQ analyzer  │
└──────────────────┴────────────────────┴──────────────┴──────────────┘

TIMING CONSIDERATIONS
- Capture at least one full operational cycle (weekday + weekend)
- Include peak and off-peak production periods
- Monitor during known problem times if intermittent
- 7-day minimum per IEEE 1159 recommendations
- 30-day monitoring for intermittent or seasonal issues
```

### Phase 3: Data Analysis

Systematically analyze each power quality parameter against applicable standards:

```
VOLTAGE ANALYSIS (ANSI C84.1)
┌───────────────┬──────────────┬──────────────┬──────────────┐
│ Parameter     │ Range A      │ Range B      │ Measured     │
│               │ (Normal)     │ (Acceptable) │              │
├───────────────┼──────────────┼──────────────┼──────────────┤
│ 480V nominal  │ 456-504V     │ 432-528V     │ [measured]   │
│ 208V nominal  │ 197.6-218.4V │ 191.4-228.8V │ [measured]   │
│ 120V nominal  │ 114-126V     │ 110-127V     │ [measured]   │
│ Voltage       │ <3%          │ <5%          │ [measured]   │
│ imbalance     │              │              │              │
└───────────────┴──────────────┴──────────────┴──────────────┘

HARMONIC ANALYSIS (IEEE 519)
- Voltage THD limit: 5.0% at PCC (8.0% for individual harmonics)
- Current THD limits based on ISC/IL ratio at PCC:
  ┌──────────────┬───────┬───────┬───────┬───────┬───────┬──────┐
  │ ISC/IL       │ h<11  │ 11-16 │ 17-22 │ 23-34 │ 35+   │ TDD  │
  ├──────────────┼───────┼───────┼───────┼───────┼───────┼──────┤
  │ <20          │ 4.0%  │ 2.0%  │ 1.5%  │ 0.6%  │ 0.3%  │ 5.0% │
  │ 20-50        │ 7.0%  │ 3.5%  │ 2.5%  │ 1.0%  │ 0.5%  │ 8.0% │
  │ 50-100       │ 10.0% │ 4.5%  │ 4.0%  │ 1.5%  │ 0.7%  │ 12%  │
  │ 100-1000     │ 12.0% │ 5.5%  │ 5.0%  │ 2.0%  │ 1.0%  │ 15%  │
  │ >1000        │ 15.0% │ 7.0%  │ 6.0%  │ 2.5%  │ 1.4%  │ 20%  │
  └──────────────┴───────┴───────┴───────┴───────┴───────┴──────┘

TRANSIENT ANALYSIS (IEEE 1159)
- Impulsive transients: rise time, duration, magnitude
- Oscillatory transients: frequency, magnitude, duration
  - Low frequency (<5 kHz): capacitor switching
  - Medium frequency (5-500 kHz): cable/line switching
  - High frequency (0.5-5 MHz): secondary response

POWER FACTOR ANALYSIS
- True power factor vs. displacement power factor
- Leading vs. lagging
- Utility penalty thresholds (typically <0.90 or <0.85)
- kVAR demand profile
```

### Phase 4: Root Cause Identification

Map measured anomalies to probable root causes:

```
SYMPTOM-TO-CAUSE MATRIX

Voltage sags → Utility events, large motor starting, transformer
               tap settings, undersized conductors, loose connections

Voltage swells → Load rejection, capacitor switching, single-phase
                  fault on ungrounded system, tap changer malfunction

High harmonics → VFDs (5th, 7th), LED drivers (3rd), UPS systems,
                  welders, arc furnaces, switched-mode power supplies

Transients → Capacitor switching (utility or PF correction),
             lightning, load switching, contactor operation

Low power factor → Induction motors (lightly loaded), old fluorescent
                    ballasts, induction furnaces, welders

Neutral-ground voltage → Shared neutral circuits, harmonic currents
                          on neutral, poor grounding, long circuit runs

Voltage imbalance → Single-phase loads on three-phase system, open
                     delta transformer, blown fuse on capacitor bank,
                     utility supply imbalance

Flicker → Arc furnaces, welders, large motor starting, reciprocating
          compressors, utility voltage regulation issues
```

### Phase 5: Recommendation Generation

Develop corrective actions ranked by priority and cost-effectiveness:

```
RECOMMENDATION FRAMEWORK

Priority 1 — SAFETY (immediate action required)
  Examples: Ground fault hazard, exposed energized parts,
            arc flash risk from deteriorated equipment

Priority 2 — EQUIPMENT PROTECTION (action within 30 days)
  Examples: Voltage outside ANSI Range B, severe harmonic
            distortion causing overheating, transient damage risk

Priority 3 — OPERATIONAL IMPROVEMENT (action within 90 days)
  Examples: Power factor correction, harmonic filtering,
            voltage regulation, load balancing

Priority 4 — OPTIMIZATION (plan and budget)
  Examples: System upgrades, monitoring installation,
            preventive maintenance programs

COST ESTIMATE CATEGORIES
  - Harmonic filters (passive): $5,000 - $50,000 per filter
  - Harmonic filters (active): $15,000 - $150,000+
  - Power factor correction capacitors: $3,000 - $30,000
  - Voltage regulators: $5,000 - $50,000
  - Isolation transformers: $2,000 - $25,000
  - SPD/TVSS installation: $1,000 - $10,000 per panel
  - Grounding system improvements: $2,000 - $20,000
  - Conductor upsizing: varies by length and size
  - PQ monitoring system (permanent): $5,000 - $50,000
```

### Phase 6: Report Creation

Generate a comprehensive, standards-compliant diagnostic report.

---

## Power Quality Issues Covered

### Voltage Sags and Swells

- **Sags (dips):** Reduction to 0.1-0.9 pu for 0.5 cycles to 1 minute
- **Swells:** Increase to 1.1-1.8 pu for 0.5 cycles to 1 minute
- **Analysis approach:** Duration-magnitude scatter plot (CBEMA/ITIC curve overlay), frequency of occurrence, correlation with utility events or on-site load switching
- **Common causes:** Utility faults, large motor starting, transformer energization, capacitor switching
- **Measurement:** RMS voltage trending with event capture, minimum 7-day monitoring period

### Harmonics (THD Analysis)

- **Voltage harmonics:** Total Harmonic Distortion (THD) per IEEE 519 at the Point of Common Coupling (PCC)
- **Current harmonics:** Total Demand Distortion (TDD) per IEEE 519 based on ISC/IL ratio
- **Individual harmonics:** Magnitude and phase angle of each harmonic order (through 50th)
- **Triplen harmonics (3rd, 9th, 15th):** Additive on neutral conductor, critical for 4-wire systems
- **Interharmonics:** Non-integer multiples, common with cycloconverters and arc furnaces
- **Analysis approach:** Spectral analysis, harmonic trending over load cycles, K-factor calculation for transformer derating

### Transients and Spikes

- **Impulsive transients:** Lightning, switching, ESD — characterized by rise time and peak magnitude
- **Oscillatory transients:** Capacitor switching, cable energization — characterized by frequency and damping
- **Measurement:** High-speed waveform capture (minimum 256 samples/cycle), transient event threshold settings
- **Protection evaluation:** SPD/TVSS adequacy, equipment withstand ratings, IEEE C62.41 location categories

### Power Factor Issues

- **Displacement power factor:** Phase angle between fundamental voltage and current
- **True power factor:** Includes harmonic distortion effects (always <= displacement PF)
- **Utility penalty assessment:** Monthly demand analysis vs. utility tariff thresholds
- **Correction strategies:** Fixed capacitors, automatic switched banks, synchronous condensers, active filters
- **Harmonic resonance risk:** Series and parallel resonance analysis before adding capacitors

### Grounding Problems

- **Ground resistance testing:** Fall-of-potential method, 3-point and 4-point (Wenner) methods
- **Acceptable values:** NEC 250.56 requires 25 ohms or less; critical facilities target <5 ohms
- **Ground grid integrity:** Continuity testing of grounding electrode conductor system
- **Isolated ground circuits:** Verification of insulated equipment grounding conductor integrity
- **Ground loops:** Identification of unintentional parallel ground paths causing noise

### Neutral-Ground Voltage

- **Acceptable levels:** Generally <1V at receptacle, <3V at panel
- **Measurement technique:** High-impedance voltmeter, measure under load
- **Root causes:** Shared neutral circuits, harmonic currents on neutral (especially 3rd), long circuit runs, poor connections, improper wiring
- **Impact:** Data processing equipment errors, communication interference, ground loop hum
- **Remediation:** Dedicated circuits, isolation transformers, harmonic filtering on neutral

### Frequency Variations

- **Normal range:** 60 Hz +/- 0.5 Hz (utility grid connected)
- **Generator operation:** Larger variations during load transfer and island mode
- **Impact on equipment:** Motor speed variation, clock drift, resonance with tuned filters
- **Measurement:** Continuous frequency trending with sub-cycle resolution

### Flicker

- **Measurement:** Short-term flicker severity (Pst) per IEC 61000-4-15
- **Acceptable levels:** Pst <= 1.0 (perception threshold)
- **Common causes:** Arc furnaces, large motor starting, reciprocating loads, welders
- **Analysis approach:** Pst trending correlated with load operations, voltage variation magnitude and repetition rate
- **Remediation:** Static VAR compensators, soft starters, dedicated feeders, flicker-rated transformers

---

## Equipment Reference

### Power Quality Analyzers

| Equipment | Capabilities | Best For |
|-----------|-------------|----------|
| Fluke 1770 Series | 3-phase PQ, harmonics to 50th, transients, event capture | Comprehensive site surveys |
| Dranetz HDPQ | 3-phase PQ, power, energy, EN50160, IEEE 519 | Long-term monitoring campaigns |
| Hioki PQ3198 | 3-phase PQ, harmonics, flicker, inrush current | Industrial troubleshooting |
| AEMC PowerPad | 3-phase PQ, harmonics, transients, power/energy | General field diagnostics |
| Elspec G4400 Series | Continuous waveform capture, PQ events, harmonics | Mission-critical facilities |

### Oscilloscopes

| Equipment | Capabilities | Best For |
|-----------|-------------|----------|
| Fluke 190-504 ScopeMeter | 4-channel, 500 MHz, CAT III 1000V | High-speed transient capture |
| Tektronix TPS2000B | 2/4-channel, isolated inputs, battery powered | Waveform analysis in the field |
| Keysight U1620A | 2-channel, 200 MHz, handheld | Quick waveform verification |

### Clamp Meters

| Equipment | Capabilities | Best For |
|-----------|-------------|----------|
| Fluke 376 FC | True RMS, inrush, harmonics, Bluetooth | Daily field measurements |
| Fluke 345 | PQ clamp meter, harmonics, power, THD | Quick power quality checks |
| Hioki CM4375 | AC/DC, true RMS, inrush, Bluetooth | Current measurements on DC systems |
| Megger DCM1500S | 1500A AC/DC, true RMS | Large feeder measurements |

### Ground Resistance Testers

| Equipment | Capabilities | Best For |
|-----------|-------------|----------|
| Fluke 1625-2 | 3/4-pole, stakeless, selective | Comprehensive ground testing |
| Megger DET2/3 | 2/3/4-pole, ART (stakeless) | High-noise industrial environments |
| AEMC 6472 | 2/3/4-pole, soil resistivity | Ground system design and testing |

---

## Standards Reference

### IEEE 519 — Harmonic Control in Electrical Power Systems

- Defines voltage and current harmonic limits at the Point of Common Coupling (PCC)
- Voltage THD limit: 5.0% for systems <= 69 kV
- Current TDD limits vary by ISC/IL ratio (see Phase 3 analysis table)
- Applies to the customer's responsibility at the PCC, not at individual loads
- Current limits are based on maximum demand load current (IL), not instantaneous

### IEEE 1159 — Monitoring Electric Power Quality

- Defines power quality terminology and categories
- Provides recommended monitoring practices and durations
- Classifies PQ disturbances by duration and magnitude:
  - Transients (impulsive and oscillatory)
  - Short-duration variations (sags, swells, interruptions)
  - Long-duration variations (sustained over/undervoltage)
  - Voltage imbalance
  - Waveform distortion (harmonics, interharmonics, notching)
  - Voltage fluctuations (flicker)
  - Power frequency variations

### ANSI C84.1 — Voltage Ratings for Electric Power Systems

- Defines Range A (normal) and Range B (acceptable) voltage ranges
- Service voltage and utilization voltage criteria
- Basis for evaluating voltage regulation adequacy

### IEEE C62.41 — Surge Characterization in Low-Voltage AC Power Circuits

- Defines location categories (A, B, C) for surge environment
- Specifies representative surge waveforms and magnitudes
- Guides surge protective device (SPD) selection

### NFPA 70 (NEC) — National Electrical Code

- Article 250: Grounding and bonding requirements
- Article 210.4: Multiwire branch circuits (shared neutral)
- Article 647: Sensitive electronic equipment (technical power)
- Article 285/242: Surge protective devices

### NEMA MG-1 — Motors and Generators

- Voltage and frequency tolerance for motors
- Voltage imbalance derating factors
- Harmonic voltage factor limits

---

## Output Format

```markdown
# Power Quality Diagnostic Report

**Client:** [Company Name]
**Site:** [Facility Address]
**Prepared by:** [Technician Name], [Title]
**Date:** [Date]
**Report No:** [HE-PQ-YYYY-XXXX]

---

## Executive Summary

[2-3 paragraph summary of findings, key issues identified, and recommended
actions. Written for facility managers and non-technical stakeholders.]

---

## Site Information

| Field | Value |
|-------|-------|
| **Facility** | [Name and address] |
| **Facility type** | [Manufacturing / Commercial / Data center / etc.] |
| **Voltage system** | [e.g., 480/277V, 3-phase, 4-wire, 60 Hz] |
| **Service size** | [e.g., 2000A main switchboard] |
| **Utility provider** | [Name] |
| **Monitoring period** | [Start date] to [End date] |
| **Instruments used** | [Model numbers and calibration dates] |

---

## Measurement Summary

### Voltage

| Parameter | Phase A | Phase B | Phase C | Limit | Status |
|-----------|---------|---------|---------|-------|--------|
| Average (V) | [val] | [val] | [val] | ANSI Range A | [PASS/FAIL] |
| Maximum (V) | [val] | [val] | [val] | ANSI Range B | [PASS/FAIL] |
| Minimum (V) | [val] | [val] | [val] | ANSI Range B | [PASS/FAIL] |
| Imbalance (%) | — | [val] | — | <3% | [PASS/FAIL] |
| Sag events | [count] | [count] | [count] | — | [INFO] |
| Swell events | [count] | [count] | [count] | — | [INFO] |

### Harmonics

| Parameter | Phase A | Phase B | Phase C | Limit | Status |
|-----------|---------|---------|---------|-------|--------|
| Voltage THD (%) | [val] | [val] | [val] | 5.0% | [PASS/FAIL] |
| Current TDD (%) | [val] | [val] | [val] | [per ISC/IL] | [PASS/FAIL] |
| Dominant harmonic | [order] | [order] | [order] | — | [INFO] |
| Neutral current (A) | — | [val] | — | — | [INFO] |
| K-factor | [val] | [val] | [val] | — | [INFO] |

### Power Factor

| Parameter | Value | Limit | Status |
|-----------|-------|-------|--------|
| Displacement PF | [val] | — | [INFO] |
| True PF | [val] | >0.90 | [PASS/FAIL] |
| kW demand (peak) | [val] | — | [INFO] |
| kVAR demand (peak) | [val] | — | [INFO] |
| kVA demand (peak) | [val] | — | [INFO] |

### Transients

| Parameter | Count | Max Magnitude | Source |
|-----------|-------|---------------|--------|
| Impulsive | [count] | [val] V peak | [probable source] |
| Oscillatory | [count] | [val] V peak | [probable source] |

### Grounding

| Test Point | Resistance (ohms) | Limit | Status |
|------------|-------------------|-------|--------|
| Main ground electrode | [val] | <25 ohms (NEC) | [PASS/FAIL] |
| [Additional points] | [val] | [target] | [PASS/FAIL] |
| Neutral-ground voltage | [val] V | <1V at load | [PASS/FAIL] |

---

## Findings and Root Cause Analysis

### Finding 1: [Title — e.g., "Elevated Voltage THD at MDP-1"]

**Severity:** [Priority 1/2/3/4]
**Measured value:** [What was measured]
**Applicable standard:** [IEEE 519 / ANSI C84.1 / etc.]
**Limit:** [What the standard requires]
**Root cause:** [Explanation of why this is occurring]
**Impact:** [What this means for equipment and operations]
**Evidence:** [Supporting measurement data, waveform captures]

### Finding 2: [Title]
[Repeat format for each finding]

---

## Corrective Action Recommendations

| Priority | Finding | Recommended Action | Estimated Cost | Timeline |
|----------|---------|-------------------|----------------|----------|
| P1 | [Finding] | [Action] | $[range] | Immediate |
| P2 | [Finding] | [Action] | $[range] | 30 days |
| P3 | [Finding] | [Action] | $[range] | 90 days |
| P4 | [Finding] | [Action] | $[range] | Budget cycle |

### Detailed Recommendations

#### Recommendation 1: [Title]
- **What:** [Specific corrective action]
- **Why:** [How this addresses the root cause]
- **How:** [Implementation approach]
- **Cost estimate:** $[range]
- **Expected result:** [What improvement to expect]
- **Verification:** [How to confirm the fix worked]

[Repeat for each recommendation]

---

## Appendices

### Appendix A: Measurement Equipment and Calibration
### Appendix B: Voltage Trending Plots
### Appendix C: Harmonic Spectrum Plots
### Appendix D: Transient Waveform Captures
### Appendix E: CBEMA/ITIC Curve Overlay
### Appendix F: Single-Line Diagram (if available)
```

---

## Execution Flow

### Step 1: Gather Site Information

**If connectors available:**
```
1. Knowledge base → Search for site/client records
   - Pull: equipment inventory, nameplate data, single-line diagrams
   - Pull: past diagnostic reports, maintenance history
   - Pull: known issues, previous recommendations

2. Document storage → Search for reference files
   - Pull: report templates, past reports for this site
   - Pull: utility bills (for demand and PF penalty data)
```

**If no connectors:**
```
1. Ask technician:
   - "What facility are you diagnosing?"
   - "What symptoms are you seeing?"
   - "What is the voltage system and service size?"
   - "What measurement data do you have?"
   - "Are there known nonlinear loads?"

2. Accept whatever they provide and work with it
```

### Step 2: Analyze Symptoms

```
1. Map reported symptoms to probable PQ categories
2. Identify which parameters to focus on
3. Determine applicable standards for evaluation
4. Flag any immediate safety concerns
```

### Step 3: Evaluate Measurement Data

```
1. Compare voltage measurements against ANSI C84.1
2. Evaluate harmonics against IEEE 519 limits
3. Analyze transient events (magnitude, frequency, source)
4. Calculate true power factor and demand profile
5. Assess grounding system adequacy
6. Check for voltage imbalance and its impact on motors
7. Overlay sag/swell events on CBEMA/ITIC curve
8. Calculate K-factor for transformer evaluation
```

### Step 4: Identify Root Causes

```
1. Correlate measurement anomalies with reported symptoms
2. Trace each issue to its source (utility, facility, or equipment)
3. Determine if issues are interrelated
4. Differentiate between cause and effect
5. Validate root cause against symptom timeline
```

### Step 5: Generate Recommendations

```
1. Develop corrective actions for each finding
2. Assign priority levels (P1-P4)
3. Estimate costs for each corrective action
4. Sequence recommendations (some depend on others)
5. Identify verification methods for each fix
```

### Step 6: Produce Report

```
1. Compile all findings into structured report format
2. Write executive summary (non-technical audience)
3. Include all measurement data and analysis
4. Attach supporting waveforms and trends
5. Generate corrective action summary table

If connectors available:
6. Save report to document storage
7. Email report to designated recipients
8. Log diagnostic in knowledge base
9. Schedule follow-up measurement via calendar
```

---

## Diagnostic Decision Trees

### VFD Fault Troubleshooting

```
VFD reporting faults
├── Overvoltage fault
│   ├── Check utility voltage (ANSI C84.1)
│   ├── Check for capacitor switching transients
│   ├── Review DC bus voltage waveform
│   └── Evaluate line reactor / DC choke adequacy
├── Overcurrent fault
│   ├── Check output current vs. motor FLA
│   ├── Check for ground fault on motor cable
│   ├── Verify motor insulation resistance
│   └── Review acceleration/deceleration ramp times
├── Ground fault
│   ├── Megger motor and cable (phase-to-ground)
│   ├── Check cable routing for damage
│   ├── Verify VFD ground fault threshold setting
│   └── Check for moisture ingress in conduit
└── Bus undervoltage
    ├── Check utility voltage for sags
    ├── Review ride-through settings
    ├── Evaluate upstream protective device coordination
    └── Consider adding ride-through capacitor or UPS
```

### Harmonics Troubleshooting

```
High THD measured
├── Voltage THD > 5%
│   ├── Determine PCC vs. load-level measurement
│   ├── Identify dominant harmonic orders
│   ├── Locate harmonic-producing loads
│   ├── Check for resonance (system impedance scan)
│   └── Evaluate: passive filter, active filter, or multi-pulse VFD
├── Current TDD > limits
│   ├── Calculate ISC/IL ratio at PCC
│   ├── Determine applicable IEEE 519 limits
│   ├── Identify largest harmonic contributors
│   └── Evaluate: line reactors, multi-pulse, active front end, filtering
└── Neutral overloading
    ├── Measure neutral current vs. phase currents
    ├── Check for triplen harmonics (3rd, 9th, 15th)
    ├── Evaluate neutral conductor sizing adequacy
    └── Consider: K-rated transformer, neutral harmonic filter,
        derating, or upsizing neutral conductor
```

---

## Common Field Scenarios

### Scenario: New VFDs Installed, Equipment Problems Start

**Typical symptoms:** Nuisance trips on other equipment, PLC communication errors, overheating transformers and neutrals
**Investigation focus:** Current harmonics, voltage distortion, neutral current, common-mode voltage
**Common solutions:** Line reactors (3-5%), DC link chokes, output filters, isolation transformers, shielded VFD cable

### Scenario: Utility Capacitor Switching Transients

**Typical symptoms:** VFD faults at same time daily, equipment restarts, SPD failures
**Investigation focus:** Oscillatory transients (300-500 Hz), voltage magnitude, timing correlation
**Common solutions:** SPD upgrade, line reactors on sensitive equipment, utility coordination request

### Scenario: Flickering Lights with Production Equipment

**Typical symptoms:** Visible flicker correlated with welder or motor starting, complaints from office areas
**Investigation focus:** Voltage variation magnitude and repetition rate, Pst measurement, source impedance
**Common solutions:** Dedicated feeder for offending load, soft starter, SVC/STATCOM, load scheduling

### Scenario: Power Factor Penalty on Utility Bill

**Typical symptoms:** Monthly utility surcharge, low PF reading at service entrance
**Investigation focus:** kW/kVAR/kVA demand profile, displacement vs. true PF, load profile
**Common solutions:** Automatic capacitor bank (with harmonic evaluation first), active filter, motor replacement/right-sizing

---

## Configuration

### Default Settings

```yaml
standards:
  voltage: "ANSI C84.1"
  harmonics: "IEEE 519-2022"
  monitoring: "IEEE 1159"
  surge: "IEEE C62.41"
  motors: "NEMA MG-1"

thresholds:
  voltage_thd_limit: 5.0       # percent
  voltage_imbalance_limit: 3.0  # percent
  current_tdd_limit: "auto"     # calculated from ISC/IL ratio
  power_factor_target: 0.95
  neutral_ground_voltage: 1.0   # volts at load
  ground_resistance: 25.0       # ohms (NEC minimum)
  sag_threshold: 0.9            # per unit
  swell_threshold: 1.1          # per unit
  flicker_pst_limit: 1.0

monitoring:
  minimum_duration_days: 7
  sampling_rate: "256 samples/cycle"
  event_capture: true
  trending_interval: "1 minute"

report:
  format: "markdown"            # markdown, pdf, html
  include_appendices: true
  include_waveforms: true
  include_itic_curve: true
  numbering_prefix: "HE-PQ"
```

### Customization

Override defaults in your settings file or tell me directly:

- "Use 3% THD voltage limit for this data center" (stricter than IEEE 519)
- "Power factor target is 0.90 per utility tariff" (different from default)
- "Include Spanish language executive summary" (bilingual reports)
- "This is a healthcare facility — apply NEC Article 517 requirements"

---

## Tips for Better Diagnostics

1. **Start at the service entrance** — Establish baseline before measuring downstream. If the utility supply is dirty, everything downstream will be affected.
2. **Monitor for at least 7 days** — Intermittent issues need time to manifest. Weekend vs. weekday load profiles often reveal problems.
3. **Check grounding first** — Many "power quality" problems are actually grounding problems. A $200 ground resistance test can save thousands.
4. **Know your ISC/IL ratio** — IEEE 519 current limits depend on this. Get the utility short-circuit current at the PCC.
5. **Look for resonance before adding capacitors** — Adding power factor correction capacitors without a harmonic analysis can make harmonic problems catastrophically worse.
6. **Correlate events with time** — Log when problems occur and overlay with PQ monitor data. Time correlation is the fastest path to root cause.
7. **Measure neutral current** — On 4-wire systems with nonlinear loads, neutral current can exceed phase current due to triplen harmonics. This is invisible until you measure it.
8. **Document everything** — Nameplate data, single-line location, measurement point photos. Future you will thank present you.

---

## Related Skills

- **ir-scanning** — Infrared thermography for electrical equipment — often done alongside power quality surveys
