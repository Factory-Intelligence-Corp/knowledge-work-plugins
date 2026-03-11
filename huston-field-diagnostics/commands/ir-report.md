---
description: Generate an infrared scanning report — input thermal data or findings, get severity classification, component analysis, and NFPA 70B-compliant maintenance recommendations
argument-hint: "<thermal findings, temperature data, or scan description>"
---

# /ir-report

> If you see unfamiliar placeholders or need to check which tools are connected, see [CONNECTORS.md](../CONNECTORS.md).

Generate a professional infrared thermographic inspection report. Input your thermal findings and get severity classification, probable cause identification, corrective actions, and NFPA 70B-compliant documentation.

## Usage

```
/ir-report <thermal findings, temperature data, or scan description>
```

Generate IR report for: $ARGUMENTS

If a file is referenced: @$1

---

## How It Works

```
┌─────────────────────────────────────────────────────────────────┐
│                        IR REPORT                                  │
├─────────────────────────────────────────────────────────────────┤
│  STANDALONE (always works)                                        │
│  ✓ Input temperature data or describe thermal findings           │
│  ✓ Delta T calculation and load correction                      │
│  ✓ Severity classification (minor / serious / critical / emerg) │
│  ✓ Probable cause identification by component type               │
│  ✓ Corrective actions with timeline                              │
│  ✓ NFPA 70B-compliant report ready for client delivery          │
│  ✓ Re-inspection schedule based on severity                      │
├─────────────────────────────────────────────────────────────────┤
│  SUPERCHARGED (when you connect your tools)                       │
│  + Knowledge base: past scans for trending, equipment records    │
│  + Document storage: branded templates, image archives           │
│  + Email: send report to client and maintenance teams            │
│  + Chat: urgent alert for critical/emergency findings            │
│  + Calendar: schedule re-inspections and maintenance             │
└─────────────────────────────────────────────────────────────────┘
```

---

## What I Need From You

**Option A: Structured temperature data**
```
Site: ABC Manufacturing, Building 2
Date: March 10, 2026
Camera: FLIR T640, emissivity 0.95
Ambient: 24 C
Load: ~75% of rated

Finding 1: MDP-1, Main breaker Phase B line-side lug
  Anomaly: 89 C, Reference (Phase A): 42 C, Delta T: 47 C

Finding 2: Panel LP-3A, Breaker #12 (20A, 1-pole)
  Anomaly: 51 C, Reference (Breaker #14): 38 C, Delta T: 13 C

Finding 3: Transformer T2, secondary Phase C terminal
  Anomaly: 78 C, Reference (Phase A): 45 C, Delta T: 33 C
```

**Option B: Describe your findings**
```
Did an IR scan at the Johnson plant today. Found a really hot
connection on the main breaker in MDP-1 — Phase B line side was
about 47 degrees hotter than Phase A. Also found a warm breaker
in a lighting panel and a hot transformer terminal. Plant was
running at about 75% load.
```

**Option C: Upload a file**
Reference a CSV, spreadsheet, or scan report:
```
/ir-report @ir-scan-results.csv
```

**Option D: Single finding for quick classification**
```
/ir-report 45 C delta T on a 400A breaker connection at 80% load
```

---

## Output

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
| **IR Camera** | [Model] |
| **Emissivity** | [Setting] |
| **Ambient Temperature** | [XX C / XX F] |
| **Load Condition** | [XX% of rated] |
| **Certification** | [Level and cert number] |

---

## Executive Summary

[Non-technical summary: how many findings by severity,
most urgent items, overall system assessment, and recommended
next steps for facility management.]

### Findings Summary

| Severity | Count | Action Required |
|----------|-------|-----------------|
| Emergency | [X] | De-energize immediately |
| Critical | [X] | Repair as soon as possible |
| Serious | [X] | Repair within 30 days |
| Minor | [X] | Next maintenance window |
| **Total** | **[X]** | |

---

## Detailed Findings

### Finding [#]: [Component — e.g., "MDP-1, Main Breaker Phase B"]

| Field | Value |
|-------|-------|
| **Equipment** | [Panel / Switchgear ID] |
| **Component** | [Breaker / Bus / Fuse / Connection] |
| **Location** | [Building, Room, Panel] |
| **Phase** | [A / B / C] |
| **Anomaly Temp** | [XX.X C] |
| **Reference Temp** | [XX.X C] |
| **Delta T** | [XX.X C] |
| **Load** | [XX%] |
| **Load-Corrected Delta T** | [XX.X C at 100%] |
| **Severity** | [MINOR / SERIOUS / CRITICAL / EMERGENCY] |
| **Probable Cause** | [e.g., Loose connection, oxidized contact] |
| **Recommended Action** | [Specific corrective action] |
| **Timeline** | [Immediate / 30 days / Next maintenance window] |

[Repeat for each finding]

---

## Recommendations Summary

| # | Equipment | Severity | Action | Timeline |
|---|-----------|----------|--------|----------|
| 1 | [ID] | [Level] | [Action] | [When] |

---

## Re-Inspection Schedule

| # | Equipment | Severity | Re-Inspect By |
|---|-----------|----------|---------------|
| 1 | [ID] | [Level] | [Date] |

---

## Equipment Inspected — No Exceptions

[Table listing all equipment scanned that showed normal thermal patterns]

---

## Appendices

- Appendix A: Thermal Images
- Appendix B: Thermographer Certification
- Appendix C: Camera Calibration
```

---

## Classification Logic

When I receive temperature data, I apply the following process:

### Step 1: Calculate Delta T

```
Delta T = T_anomaly - T_reference

Reference priority:
1. Same component, different phase (best)
2. Identical component, same load
3. Historical baseline
4. Ambient (last resort — noted as less reliable)
```

### Step 2: Load Correction

```
If load < 100% of rated:
  Corrected Delta T = Measured Delta T x (I_rated / I_measured)^2

Example:
  Measured: 25 C delta T at 60% load
  Corrected: 25 x (1.0 / 0.6)^2 = 25 x 2.78 = 69.4 C
  Classification changes from SERIOUS to CRITICAL
```

### Step 3: Severity Classification

```
Delta T 1-10 C   → MINOR    → Monitor, repair at next window
Delta T 11-30 C  → SERIOUS  → Repair within 30 days
Delta T 31-70 C  → CRITICAL → Repair ASAP, reduce load
Delta T >70 C    → EMERGENCY → De-energize immediately
```

### Step 4: Escalation Check

```
Escalate severity by one level if:
- Safety-critical system (emergency power, life safety)
- High-consequence facility (data center, healthcare)
- Progressive deterioration (trending worse over scans)
- Component at or above manufacturer's rated temperature
- Load-corrected delta T crosses next threshold
- Visible damage (discoloration, melting, arc marks)
```

### Step 5: Cause Identification

```
Based on component type and thermal pattern:
- Single hot termination → loose connection (most common)
- Entire component hot → overload or internal degradation
- All phases elevated → overload, ambient, or ventilation
- One phase only → connection issue on that phase
- Fuse body hot → overload or deteriorating element
- Bus joint hot → loose bolts, failed plating
```

---

## If Connectors Available

**Knowledge base connected:**
- Pull past IR scan results for trending analysis
- Access equipment records (age, maintenance history, ratings)
- Compare current vs. historical temperatures
- Flag repeat offenders (same component found hot before)

**Document storage connected:**
- Use branded report template
- Archive report and thermal images
- Access previous reports for this facility

**Email connected:**
- Send completed report to client contact
- Distribute urgent findings to maintenance manager
- CC internal engineering for review

**Chat connected:**
- Immediate notification for emergency/critical findings
- Team coordination for emergency response
- Request peer review for unusual thermal patterns

**Calendar connected:**
- Schedule re-inspections based on severity
- Book maintenance windows for repairs
- Set reminders for follow-up verification scans

---

## Severity-Based Response Guide

### Emergency Findings (Delta T > 70 C)

```
IMMEDIATE ACTIONS:
1. Verbally notify facility personnel on-site
2. Recommend de-energizing if safe to do so
3. If cannot de-energize: reduce load, restrict area access
4. Document with thermal and visual images
5. Send urgent notification via ~~chat (if connected)
6. Generate preliminary report within 24 hours
7. Full report within 48 hours
```

### Critical Findings (Delta T 31-70 C)

```
URGENT ACTIONS:
1. Notify facility maintenance manager
2. Recommend repair scheduling within 1 week
3. Recommend load reduction if feasible
4. Schedule weekly re-inspection until repaired
5. Generate report within 1 week
```

### Serious Findings (Delta T 11-30 C)

```
PROMPT ACTIONS:
1. Include in formal report
2. Recommend repair within 30 days
3. Schedule monthly re-inspection until repaired
4. Monitor load conditions
5. Generate report within standard timeline
```

### Minor Findings (Delta T 1-10 C)

```
STANDARD ACTIONS:
1. Document in report
2. Schedule repair at next maintenance window
3. Re-inspect at next annual survey
4. Note as baseline for future trending
```

---

## Tips

1. **Always provide load information** — A delta T at 50% load is dramatically different from the same delta T at full load. This is the single most important variable after the temperature itself.
2. **Use phase-to-phase comparison** — For three-phase equipment, comparing Phase A to Phase B to Phase C gives you reliable references without needing external benchmarks.
3. **Note the reference clearly** — "47 C delta T" is only meaningful if I know what the reference was. Same-type component is best. Ambient is least reliable.
4. **Include equipment ratings** — A 20 C delta T on a 20A lighting panel breaker and a 20 C delta T on a 4000A main bus connection require very different responses.
5. **Mention past findings** — If this connection was hot last year too, that changes the analysis. Repeat findings suggest the root cause was not addressed.
6. **Report normal equipment too** — A complete report documents everything scanned, not just the anomalies. This proves scope and establishes baselines.
7. **Note environmental conditions** — Ambient temperature, indoor/outdoor, ventilation, solar loading — all affect interpretation.
