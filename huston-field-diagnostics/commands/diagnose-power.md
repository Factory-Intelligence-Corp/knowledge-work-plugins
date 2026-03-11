---
description: Run a power quality diagnostic — input symptoms and measurements, get root cause analysis, corrective actions with cost estimates, and a formal report
argument-hint: "<symptoms, measurements, or site description>"
---

# /diagnose-power

> If you see unfamiliar placeholders or need to check which tools are connected, see [CONNECTORS.md](../CONNECTORS.md).

Run a systematic power quality diagnostic for electrical systems. Input your symptoms, measurements, or site description and get a comprehensive analysis with root cause identification, corrective actions, cost estimates, and a formal report.

## Usage

```
/diagnose-power <symptoms, measurements, or site description>
```

Diagnose power quality for: $ARGUMENTS

If a file is referenced: @$1

---

## How It Works

```
┌─────────────────────────────────────────────────────────────────┐
│                      DIAGNOSE POWER                               │
├─────────────────────────────────────────────────────────────────┤
│  STANDALONE (always works)                                        │
│  ✓ Describe symptoms or paste measurement data                   │
│  ✓ Systematic 6-phase diagnostic methodology                    │
│  ✓ Root cause analysis mapped to symptoms                       │
│  ✓ IEEE 519 / IEEE 1159 / ANSI C84.1 compliance evaluation     │
│  ✓ Corrective actions with cost estimates and priority           │
│  ✓ Formal diagnostic report ready to deliver to client          │
├─────────────────────────────────────────────────────────────────┤
│  SUPERCHARGED (when you connect your tools)                       │
│  + Knowledge base: equipment history, past diagnostics           │
│  + Document storage: report templates, archived data             │
│  + Email: send completed report to client                        │
│  + Chat: notify team of critical findings                        │
│  + Calendar: schedule follow-up measurements                     │
└─────────────────────────────────────────────────────────────────┘
```

---

## What I Need From You

**Option A: Describe symptoms**
```
VFDs on the 480V bus at Johnson Manufacturing are faulting
intermittently — overvoltage faults, usually mid-morning.
Started about two weeks ago after the utility replaced a
transformer on the pole.
```

**Option B: Paste measurement data**
```
Fluke 1770 data from MDP-1 (480/277V, 3-phase, 4-wire):
  Phase A: 487V avg, 5.2% VTHD, 312A
  Phase B: 491V avg, 4.8% VTHD, 298A
  Phase C: 478V avg, 6.1% VTHD, 325A
  Neutral current: 187A
  Power factor: 0.82
  12 voltage sag events in 7 days (lowest: 412V, 6 cycles)
  3 oscillatory transients (peaks to 780V)
```

**Option C: Upload a file**
Reference a CSV export, PQ analyzer report, or any data file:
```
/diagnose-power @power-survey-data.csv
```

**Option D: Describe the situation generally**
```
Customer is complaining about flickering lights and their
new CNC machine keeps faulting. It's a 200,000 sq ft
manufacturing plant with a 2000A 480V service. They added
six new VFDs last year.
```

---

## Output

```markdown
# Power Quality Diagnostic Report

**Client:** [Company Name]
**Site:** [Facility Address]
**Prepared by:** [Technician Name], [Title]
**Date:** [Date]
**Report No:** [HE-PQ-YYYY-XXXX]

---

## Executive Summary

[2-3 paragraph non-technical summary of findings and recommendations.
Written for facility managers who need to understand the problem and
approve corrective action budgets.]

---

## Site Information

| Field | Value |
|-------|-------|
| **Facility** | [Name and address] |
| **Voltage system** | [e.g., 480/277V, 3-phase, 4-wire] |
| **Service size** | [e.g., 2000A main switchboard] |
| **Reported symptoms** | [What prompted the diagnostic] |
| **Measurement period** | [Duration and dates] |
| **Instruments** | [Equipment used] |

---

## Measurement Summary

### Voltage (ANSI C84.1 Compliance)

| Parameter | Phase A | Phase B | Phase C | Limit | Status |
|-----------|---------|---------|---------|-------|--------|
| Average (V) | [val] | [val] | [val] | Range A | [PASS/FAIL] |
| Maximum (V) | [val] | [val] | [val] | Range B | [PASS/FAIL] |
| Minimum (V) | [val] | [val] | [val] | Range B | [PASS/FAIL] |
| Imbalance | — | [val]% | — | <3% | [PASS/FAIL] |

### Harmonics (IEEE 519 Compliance)

| Parameter | Phase A | Phase B | Phase C | Limit | Status |
|-----------|---------|---------|---------|-------|--------|
| Voltage THD | [val]% | [val]% | [val]% | 5.0% | [PASS/FAIL] |
| Current TDD | [val]% | [val]% | [val]% | [calc]% | [PASS/FAIL] |

### Power Factor and Demand

| Parameter | Value | Target | Status |
|-----------|-------|--------|--------|
| True PF | [val] | >0.90 | [PASS/FAIL] |
| kW demand | [val] | — | [INFO] |
| kVAR demand | [val] | — | [INFO] |

### Events

| Event Type | Count | Worst Case | Source |
|------------|-------|------------|--------|
| Voltage sags | [X] | [val]V, [dur] | [source] |
| Voltage swells | [X] | [val]V, [dur] | [source] |
| Transients | [X] | [val]V peak | [source] |

---

## Findings and Root Cause Analysis

### Finding 1: [Title]
**Severity:** [Priority 1-4]
**Measured:** [value]
**Standard:** [applicable standard and limit]
**Root cause:** [explanation]
**Impact:** [effect on equipment and operations]

[Repeat for each finding]

---

## Corrective Action Recommendations

| Priority | Finding | Action | Est. Cost | Timeline |
|----------|---------|--------|-----------|----------|
| P1 | [Finding] | [Action] | $[range] | Immediate |
| P2 | [Finding] | [Action] | $[range] | 30 days |
| P3 | [Finding] | [Action] | $[range] | 90 days |
| P4 | [Finding] | [Action] | $[range] | Budget cycle |

### Detailed Recommendations

#### 1. [Title]
- **What:** [Specific action]
- **Why:** [How it addresses root cause]
- **Cost:** $[range]
- **Expected result:** [Improvement to expect]
- **Verification:** [How to confirm it worked]

[Repeat for each recommendation]

---

## Next Steps

1. [ ] [Immediate action if any]
2. [ ] [Schedule corrective work]
3. [ ] [Follow-up measurement plan]
4. [ ] [Long-term monitoring recommendation]
```

---

## Diagnostic Approach

### Phase 1: Intake and Scoping

```
1. Identify reported symptoms and affected equipment
2. Determine voltage system and service configuration
3. Note any recent changes (new loads, utility work, construction)
4. Identify applicable standards for evaluation
```

### Phase 2: Data Analysis

```
1. Evaluate voltage against ANSI C84.1 Range A and B
2. Check harmonics against IEEE 519 limits at PCC
3. Analyze transient events (type, magnitude, frequency)
4. Calculate true power factor and demand profile
5. Assess voltage imbalance and its motor derating impact
6. Review event data (sags, swells, interruptions)
7. Check neutral current and neutral-ground voltage
8. Overlay voltage events on CBEMA/ITIC curve
```

### Phase 3: Root Cause Identification

```
1. Map each anomaly to probable cause
2. Correlate timing of events with load patterns
3. Trace issues to source (utility, facility, or equipment)
4. Identify interrelated issues (e.g., harmonics causing PF issues)
5. Differentiate cause from effect
```

### Phase 4: Recommendation Development

```
1. Develop specific corrective actions for each finding
2. Assign priority (P1 = safety, P2 = equipment protection,
   P3 = operational, P4 = optimization)
3. Estimate costs based on typical ranges
4. Sequence actions (dependencies and quick wins)
5. Define verification method for each fix
```

### Phase 5: Report Generation

```
1. Compile findings into structured report
2. Write executive summary for non-technical audience
3. Include all measurement data and standards evaluation
4. Generate corrective action summary table
5. Define follow-up measurement plan

If connectors available:
6. Save report to ~~document storage
7. Email report via ~~email
8. Log in ~~knowledge base
9. Schedule follow-up via ~~calendar
```

---

## If Connectors Available

**Knowledge base connected:**
- Search for past diagnostics at this facility
- Pull equipment inventory and nameplate data
- Compare current findings to historical baselines
- Access site single-line diagrams

**Document storage connected:**
- Use report template with company branding
- Archive completed report
- Store measurement data files

**Email connected:**
- Send completed report to client
- Distribute urgent findings to engineering team

**Chat connected:**
- Notify team of critical findings immediately
- Request peer review for complex scenarios

**Calendar connected:**
- Schedule follow-up measurement campaign
- Book maintenance windows for corrective work

---

## Tips

1. **More data = better diagnosis** — Even partial measurements help. Voltage-only data is better than no data.
2. **Describe what changed** — If something changed before problems started, that is almost always the root cause.
3. **Note the timing** — "Happens every morning at 7 AM" is extremely valuable diagnostic information.
4. **Include load information** — Knowing what percentage of capacity the system was at during measurements changes the analysis significantly.
5. **Mention the utility** — Utility-side issues are common and often overlooked. Include any utility correspondence or outage reports.
6. **List all nonlinear loads** — VFDs, UPS systems, LED drivers, welders, servers — these are the usual suspects for harmonics and distortion.
