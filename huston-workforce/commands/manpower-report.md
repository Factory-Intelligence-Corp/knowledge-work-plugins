---
description: Generate a manpower projection report — upload PM excel sheets, analyze union labor staffing levels across projects, identify spikes and dips, get strategic workforce planning recommendations
argument-hint: "<period or PM name>"
---

# /manpower-report

> If you see unfamiliar placeholders or need to check which tools are connected, see [CONNECTORS.md](../CONNECTORS.md).

Generate a comprehensive manpower projection report for Huston Electric. Analyzes PM excel sheets, aggregates labor demand across all projects, identifies staffing spikes and dips by trade classification, and produces strategic workforce planning recommendations.

## Usage

```
/manpower-report [period or PM name]
```

Generate a manpower report for: $ARGUMENTS

If a file is referenced: @$1

---

## How It Works

```
┌──────────────────────────────────────────────────────────────────────┐
│                      MANPOWER REPORT                                 │
├──────────────────────────────────────────────────────────────────────┤
│  STANDALONE (always works)                                           │
│  ✓ Upload PM excel sheets or CSV exports                            │
│  ✓ Or paste project labor data manually                             │
│  ✓ Aggregate headcount across all PMs and projects                  │
│  ✓ Identify staffing spikes and dips by week                        │
│  ✓ Break down labor by union classification (JW, AP, FM, GF, SI)   │
│  ✓ Calculate trade-specific needs and ratios                        │
│  ✓ Generate strategic recommendations                               │
├──────────────────────────────────────────────────────────────────────┤
│  SUPERCHARGED (when you connect your tools)                          │
│  + Spreadsheet: Pull PM sheets directly — no upload needed          │
│  + Knowledge Base: Historical trends and project records            │
│  + Email: Send completed report to leadership                       │
│  + Chat: Post summary and alerts to Slack/Teams channels            │
└──────────────────────────────────────────────────────────────────────┘
```

---

## What I Need From You

### Step 1: Your Labor Data

**Option A: Upload PM Excel Sheets**
Upload the excel files from your project managers. Each sheet should contain project-level labor projections by week, ideally broken down by trade classification.

**Option B: Upload a CSV**
Export or consolidate your PM data into a CSV. I need at minimum:
- Project name
- PM name
- Week (or date range)
- Headcount (total or by trade)

Helpful if you have:
- Trade breakdown (JW, AP, FM, GF, SI)
- Project phase (rough-in, trim, startup, etc.)
- Mobilization and demobilization dates

**Option C: Paste your data**
```
PM: John Smith
  - Downtown Office TI: 8 JW, 2 AP, 1 FM — weeks 1-12
  - Airport Terminal: 15 JW, 4 AP, 2 FM, 1 GF — weeks 3-20
PM: Sarah Johnson
  - Hospital Wing B: 20 JW, 5 AP, 3 FM, 1 GF, 1 SI — weeks 1-24
  - School Renovation: 6 JW, 2 AP, 1 FM — weeks 8-16
```

**Option D: Describe your situation**
"We have 5 PMs running 12 active projects. Total workforce is about 120 people. We're concerned about a spike in June when three big projects overlap."

### Step 2: Your Parameters

- **Projection period**: How many weeks out? (default: 12 weeks)
- **Specific PM focus**: All PMs or a specific PM? (default: all)
- **Report type**: Full report, spike/dip analysis only, or PM breakdown? (default: full)
- **Current headcount**: How many workers do you have today? (helps identify gaps)

---

## Output

```markdown
# Manpower Projection Report
**Company:** Huston Electric, Inc.
**Generated:** [Date]
**Period:** [Start Date] — [End Date] ([X] weeks)
**Data Sources:** [PM names / file names]

---

## Executive Summary

**Current Headcount:** [X] workers
**Peak Projected:** [X] workers (Week of [Date]) — [+X% from current]
**Valley Projected:** [X] workers (Week of [Date]) — [-X% from current]
**Active Projects:** [X] across [X] PMs
**Key Finding:** [One-sentence summary of most important insight]

---

## Company-Wide Projection

| Week Starting | JW | AP | FM | GF | SI | Total | vs. Current |
|---------------|----|----|----|----|----|---------| ------------|
| [Date] | [X] | [X] | [X] | [X] | [X] | [X] | +/-[X] |
| [Date] | [X] | [X] | [X] | [X] | [X] | [X] | +/-[X] |
| [Date] | [X] | [X] | [X] | [X] | [X] | [X] | +/-[X] |

---

## Staffing Spikes

| Period | Peak | Current | Gap | Driver | Action Required |
|--------|------|---------|-----|--------|-----------------|
| Week of [Date] | [X] | [X] | +[X] | [Project entering peak phase] | [Request from hall / stagger starts] |

## Staffing Dips

| Period | Valley | Current | Surplus | Cause | Recommendation |
|--------|--------|---------|---------|-------|----------------|
| Week of [Date] | [X] | [X] | -[X] | [Projects completing] | [Pull forward work / schedule training] |

---

## PM-Level Summary

| PM | Active Projects | Current Workers | Peak | Peak Week | Valley | Valley Week |
|----|----------------|-----------------|------|-----------|--------|-------------|
| [PM Name] | [X] | [X] | [X] | [Date] | [X] | [Date] |

---

## Trade-Specific Needs

| Trade | Current | Avg Needed | Peak Needed | Peak Week | Action |
|-------|---------|------------|-------------|-----------|--------|
| Journeyman (JW) | [X] | [X] | [X] | [Date] | [Action] |
| Apprentice (AP) | [X] | [X] | [X] | [Date] | [Action] |
| Foreman (FM) | [X] | [X] | [X] | [Date] | [Action] |
| General Foreman (GF) | [X] | [X] | [X] | [Date] | [Action] |
| Superintendent (SI) | [X] | [X] | [X] | [Date] | [Action] |

---

## Union Hall Coordination

| Action | Timing | Trade | Qty | For Project(s) |
|--------|--------|-------|-----|-----------------|
| [Request / Release] | [Date] | [Trade] | [X] | [Project list] |

---

## Strategic Recommendations

1. **[Recommendation]** — [Rationale, timing, and expected impact]
2. **[Recommendation]** — [Rationale, timing, and expected impact]
3. **[Recommendation]** — [Rationale, timing, and expected impact]

---

## Apprentice Ratio Check

| Current Ratio (AP:JW) | Required Ratio | Status |
|------------------------|---------------|--------|
| [X]:1 | [X]:1 | [Compliant / Need [X] more AP / Over ratio] |

---

## Data Quality Notes

| Issue | Affected PMs/Projects | Impact |
|-------|----------------------|--------|
| [Missing weeks / stale data / incomplete breakdown] | [List] | [How it affects the projection] |
```

---

## Report Variations

### Quick Summary Mode

Say "quick manpower check" or "manpower summary" for an abbreviated view:

```markdown
# Manpower Summary | [Date]

**Headcount:** [X] today → Peak [X] (Week of [Date]) → Valley [X] (Week of [Date])

**Spikes:**
- [Date]: +[X] workers needed — [reason]

**Dips:**
- [Date]: -[X] surplus — [reason]

**Action Now:** [Single most important action]
```

### PM-Specific Report

Say "manpower report for [PM Name]" for a single PM deep dive:

```markdown
# PM Manpower Report: [PM Name]
**Projects:** [X] active

| Project | Phase | Workers | Weeks Remaining | Peak Week |
|---------|-------|---------|-----------------|-----------|
| [Project] | [Phase] | [X] | [X] | [Date] |

**PM Total Peak:** [X] workers (Week of [Date])
**PM Key Issue:** [What needs attention]
```

### Comparison Report

Say "compare manpower to last month" or "projection vs. actuals":

```markdown
# Projection vs. Actuals Comparison

| Week | Projected | Actual | Variance | Notes |
|------|-----------|--------|----------|-------|
| [Date] | [X] | [X] | +/-[X] | [Why different] |
```

---

## If Spreadsheet Connected

- I will pull PM sheets directly from ~~spreadsheet — no upload needed
- Auto-detect sheet format and column mapping
- Refresh data on each report run for latest projections
- Write summary data back to a consolidated tracking workbook

## If Knowledge Base Connected

- Pull historical manpower data from ~~knowledge base
- Compare current projections to historical trends
- Access union classification references and CBA ratio requirements
- Store generated reports for organizational memory

## If Email Connected

- Send the completed report directly via ~~email
- Attach PDF version for leadership
- Include executive summary in email body
- CC relevant PMs and operations staff

---

## Tips

1. **Run this weekly** — Manpower projections change constantly. A weekly report keeps leadership informed and prevents surprises.
2. **Get PM sheets early** — The report is only as good as the data. Chase PM updates before generating the report.
3. **Watch the transitions** — Spikes and dips often happen at project phase boundaries. Pay special attention to weeks where multiple projects change phase simultaneously.
4. **Coordinate hall requests with lead time** — Union halls need advance notice. Identify needs 4-6 weeks out when possible.
5. **Track actuals** — Compare projections to what actually happened. This improves PM estimating accuracy over time.
