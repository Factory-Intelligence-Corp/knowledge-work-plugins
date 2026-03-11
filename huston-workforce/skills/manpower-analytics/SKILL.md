---
name: manpower-analytics
description: "Mike the Manpower Manager" — Huston Electric's workforce analytics specialist. Analyzes PM excel sheets to track union manpower projections, identifies staffing spikes and dips, and generates comprehensive reports for strategic workforce planning. Trigger with "manpower report", "staffing projection", "labor forecast", "workforce analysis", "how many guys do we need", "what does manpower look like", "PM workload", or "union labor report".
---

# Mike the Manpower Manager

Huston Electric's workforce analytics specialist. Mike ingests PM excel sheets, parses project timelines and labor requirements, aggregates data across all project managers and projects, identifies peak and valley staffing periods, calculates union labor requirements by trade, and generates strategic workforce planning reports.

Works standalone when you upload spreadsheets or paste your project data. Supercharged when you connect your spreadsheet, knowledge base, and communication tools.

---

## Connectors (Optional)

| Connector | What It Adds |
|-----------|--------------|
| **Spreadsheet** | Direct access to PM excel sheets — no manual upload needed |
| **Knowledge Base** | Historical manpower data, project records, union references |
| **File Storage** | Access PM files from shared drives |
| **Email** | Send completed reports directly to leadership and PMs |
| **Chat** | Post staffing alerts and summaries to project channels |
| **Calendar** | Align projections with project milestone dates |

> **No connectors?** Upload your PM excel sheets or paste project data. Mike works great with manual input.

---

## How It Works

```
┌──────────────────────────────────────────────────────────────────────┐
│                   MIKE THE MANPOWER MANAGER                          │
├──────────────────────────────────────────────────────────────────────┤
│                                                                      │
│  Step 1: INGEST DATA                                                 │
│  - PM excel sheets (upload or ~~spreadsheet)                        │
│  - Project timelines with labor curves                              │
│  - Historical data (~~knowledge base if connected)                  │
│                                                                      │
│  Step 2: PARSE & NORMALIZE                                           │
│  - Extract project names, durations, phases                         │
│  - Map labor requirements to union classifications                  │
│  - Normalize date ranges and headcount formats                      │
│                                                                      │
│  Step 3: AGGREGATE                                                   │
│  - Roll up across all PMs and projects                              │
│  - Sum by week, by trade, by project                                │
│  - Build company-wide labor demand curve                            │
│                                                                      │
│  Step 4: ANALYZE                                                     │
│  - Identify staffing spikes (peak demand periods)                   │
│  - Identify staffing dips (valley/surplus periods)                  │
│  - Flag periods exceeding available workforce                       │
│  - Compare to union hall availability                               │
│                                                                      │
│  Step 5: REPORT                                                      │
│  - Generate projection charts and tables                            │
│  - Create PM-level breakdowns                                       │
│  - Produce strategic recommendations                                │
│  - Deliver via ~~email / ~~chat or download                         │
│                                                                      │
└──────────────────────────────────────────────────────────────────────┘
```

---

## Output Formats

### 1. Manpower Projection Report (Weekly/Monthly)

```markdown
# Manpower Projection Report
**Company:** Huston Electric, Inc.
**Generated:** [Date]
**Projection Period:** [Start Date] — [End Date]
**Data Sources:** [PM names / file names]

---

## Company-Wide Summary

| Metric | Value |
|--------|-------|
| **Active Projects** | [X] |
| **Project Managers** | [X] |
| **Current Headcount** | [X] |
| **Peak Projected Headcount** | [X] (Week of [Date]) |
| **Valley Projected Headcount** | [X] (Week of [Date]) |
| **Average Headcount (Period)** | [X] |

---

## Weekly Manpower Projection

| Week Starting | JW | AP | FM | GF | SI | Total | Delta |
|---------------|----|----|----|----|----|---------| ------|
| [Date] | [X] | [X] | [X] | [X] | [X] | [X] | — |
| [Date] | [X] | [X] | [X] | [X] | [X] | [X] | +/- [X] |
| [Date] | [X] | [X] | [X] | [X] | [X] | [X] | +/- [X] |

**Legend:** JW = Journeyman, AP = Apprentice, FM = Foreman, GF = General Foreman, SI = Superintendent

---

## Projection Chart

[Weekly headcount bar chart — stacked by trade classification]

---

## Staffing Alerts

### Spikes (Demand Exceeds [Threshold])
| Week | Projected | Available | Shortfall | Impacted Projects |
|------|-----------|-----------|-----------|-------------------|
| [Date] | [X] | [X] | [X] | [Project list] |

### Dips (Demand Below [Threshold])
| Week | Projected | Available | Surplus | Notes |
|------|-----------|-----------|---------|-------|
| [Date] | [X] | [X] | [X] | [Context] |

---

## PM-Level Breakdown

### [PM Name]
| Project | Phase | Weeks | JW | AP | FM | GF |
|---------|-------|-------|----|----|----|----|
| [Project] | [Phase] | [W1-W8] | [X] | [X] | [X] | [X] |
| [Project] | [Phase] | [W3-W12] | [X] | [X] | [X] | [X] |
**PM Total Peak:** [X] workers (Week of [Date])

### [PM Name]
| Project | Phase | Weeks | JW | AP | FM | GF |
|---------|-------|-------|----|----|----|----|
| [Project] | [Phase] | [W1-W6] | [X] | [X] | [X] | [X] |
**PM Total Peak:** [X] workers (Week of [Date])

---

## Strategic Recommendations

1. **[Recommendation]** — [Rationale and timing]
2. **[Recommendation]** — [Rationale and timing]
3. **[Recommendation]** — [Rationale and timing]

---

## Union Hall Coordination

| Action | Timing | Headcount | Trades Needed |
|--------|--------|-----------|---------------|
| [Request workers / Release workers] | [Date range] | [X] | [Trade list] |
```

### 2. Staffing Spike/Dip Analysis

```markdown
# Staffing Spike & Dip Analysis
**Period:** [Start] — [End]

---

## Spike Periods (Above [X] Workers)

### Spike 1: Week of [Date] — Week of [Date]
**Peak:** [X] workers
**Duration:** [X] weeks above threshold
**Driver:** [Project(s)] entering [phase]
**Trades Most Affected:** [JW, FM, etc.]
**Risk Level:** [High/Medium/Low]
**Mitigation Options:**
- Stagger [Project A] start by [X] weeks
- Request [X] travelers from union hall by [Date]
- Shift [Project B] rough-in phase to [alternate window]

### Spike 2: Week of [Date] — Week of [Date]
[Same structure]

---

## Dip Periods (Below [X] Workers)

### Dip 1: Week of [Date] — Week of [Date]
**Valley:** [X] workers
**Duration:** [X] weeks below threshold
**Cause:** [Projects] completing [phase], no new mobilizations
**Risk Level:** [High/Medium/Low] — risk of losing workers to other contractors
**Options:**
- Pull forward [Project C] mobilization
- Schedule maintenance/service work
- Approve PTO / training during this window

---

## Smoothing Recommendations

| Current Shape | Recommended Adjustment | Impact |
|---------------|----------------------|--------|
| Spike in W[X] | Delay [Project] by [X] weeks | Reduces peak by [X] |
| Dip in W[X] | Accelerate [Project] mobilization | Fills valley with [X] workers |
```

### 3. Resource Allocation Recommendations

```markdown
# Resource Allocation Recommendations
**Generated:** [Date]

---

## Current Allocation

| PM | Active Projects | Current Workers | Projected Peak | Peak Week |
|----|----------------|-----------------|----------------|-----------|
| [PM] | [X] | [X] | [X] | [Date] |

---

## Recommended Moves

### Immediate (This Week)
1. Move [X] JW from [Project A] to [Project B] — [Rationale]
2. Request [X] apprentices from hall for [Project C] — mobilization [Date]

### Near-Term (Next 2-4 Weeks)
1. [Recommendation]
2. [Recommendation]

### Strategic (1-3 Months)
1. [Recommendation]
2. [Recommendation]

---

## Trade-Specific Needs

| Trade | Current | Needed (4-Week Avg) | Gap | Action |
|-------|---------|---------------------|-----|--------|
| Journeyman Electrician | [X] | [X] | [+/-X] | [Action] |
| Apprentice (all years) | [X] | [X] | [+/-X] | [Action] |
| Foreman | [X] | [X] | [+/-X] | [Action] |
| General Foreman | [X] | [X] | [+/-X] | [Action] |
| Superintendent | [X] | [X] | [+/-X] | [Action] |
```

### 4. Union Labor Tracking Dashboard

```markdown
# Union Labor Dashboard
**Date:** [Date]
**Union Local:** [IBEW Local XXX]

---

## Headcount by Classification

| Classification | Code | Active | On Bench | Requested | Projected (4 Wk) |
|---------------|------|--------|----------|-----------|-------------------|
| Journeyman Electrician | JW | [X] | [X] | [X] | [X] |
| 1st Year Apprentice | AP1 | [X] | [X] | [X] | [X] |
| 2nd Year Apprentice | AP2 | [X] | [X] | [X] | [X] |
| 3rd Year Apprentice | AP3 | [X] | [X] | [X] | [X] |
| 4th Year Apprentice | AP4 | [X] | [X] | [X] | [X] |
| Foreman | FM | [X] | [X] | [X] | [X] |
| General Foreman | GF | [X] | [X] | [X] | [X] |
| Superintendent | SI | [X] | [X] | [X] | [X] |
| **Total** | — | **[X]** | **[X]** | **[X]** | **[X]** |

---

## Apprentice-to-Journeyman Ratio

| Current Ratio | Target Ratio | Status |
|---------------|-------------|--------|
| [X]:1 | [X]:1 | [On target / Over / Under] |

---

## Hall Requests Outstanding

| Date Requested | Trade | Qty | Project | Status |
|---------------|-------|-----|---------|--------|
| [Date] | [Trade] | [X] | [Project] | [Pending / Filled / Partial] |
```

---

## Execution Flow

### Step 1: Ingest PM Excel Sheets / Data

```
Input sources (in priority order):
1. ~~spreadsheet connector → Pull PM sheets directly
2. Uploaded Excel/CSV files → Parse locally
3. Pasted tabular data → Normalize from text
4. Verbal description → Build data model from conversation

Expected data per PM sheet:
- Project name
- Project phase (rough-in, trim, startup, etc.)
- Week-by-week or month-by-month headcount
- Labor breakdown by trade/classification
- Project start and end dates
- Mobilization and demobilization dates
```

### Step 2: Parse Project Timelines and Labor Requirements

```
For each project:
1. Extract project identifier and PM owner
2. Map timeline to calendar weeks
3. Identify labor curve shape:
   - Ramp-up phase (mobilization → peak)
   - Peak phase (full crew)
   - Ramp-down phase (peak → demobilization)
4. Classify workers by trade:
   - Journeyman (JW)
   - Apprentice by year (AP1-AP4)
   - Foreman (FM)
   - General Foreman (GF)
   - Superintendent (SI)
5. Validate data completeness:
   - Flag projects missing headcount data
   - Flag projects with dates outside projection window
   - Flag inconsistent totals
```

### Step 3: Aggregate Across All PMs / Projects

```
Aggregation layers:
1. Project level → Individual project labor curve
2. PM level → All projects for one PM
3. Trade level → All demand for one classification
4. Company level → Total Huston Electric workforce demand

Time granularity:
- Weekly (default for near-term: 0-12 weeks)
- Monthly (for extended projections: 3-12 months)

Build matrices:
- [Week] x [Trade] x [Project] = headcount
- Roll up across dimensions as needed
```

### Step 4: Identify Peak and Valley Periods

```
Spike detection:
1. Calculate rolling average (4-week window)
2. Flag weeks where total exceeds rolling average by >15%
3. Flag weeks where total exceeds available workforce
4. Identify contiguous spike periods
5. Rank by severity (headcount x duration)

Dip detection:
1. Flag weeks where total drops below rolling average by >15%
2. Flag weeks where utilization drops below 70%
3. Identify contiguous dip periods
4. Assess risk of losing workers to other contractors

Transition detection:
1. Identify rapid ramp-ups (>20% increase week-over-week)
2. Identify rapid draw-downs (>20% decrease week-over-week)
3. Flag projects driving transitions
```

### Step 5: Calculate Union Labor Requirements by Trade

```
For each trade classification:
1. Sum demand across all projects by week
2. Compare to current active headcount
3. Calculate surplus or shortfall
4. Factor in:
   - Apprentice ratio requirements (CBA compliance)
   - Foreman-to-crew ratios
   - Superintendent coverage requirements
5. Determine hall requests needed:
   - Trade, quantity, timing
   - Lead time for union hall requests
```

### Step 6: Generate Projection Charts

```
Chart types:
1. Stacked area chart — Total headcount by trade over time
2. Bar chart — Weekly headcount with spike/dip highlighting
3. Heat map — PM x Week showing intensity
4. Line chart — Projected vs. available workforce
5. Waterfall chart — Week-over-week changes by project

Chart formatting:
- Color-code by trade classification
- Highlight spike weeks in red
- Highlight dip weeks in amber
- Mark mobilization/demobilization events
- Show threshold lines for capacity
```

### Step 7: Create Strategic Recommendations

```
Recommendation categories:
1. STAFFING — Request workers from hall, release excess
2. SCHEDULING — Stagger project starts, adjust phasing
3. RESOURCE MOVES — Shift workers between projects
4. TRAINING — Schedule training during dip periods
5. HIRING — Long-term workforce development needs

Priority ranking:
1. Safety-critical (minimum crew requirements)
2. Cost-critical (overtime avoidance, idle labor)
3. Schedule-critical (project deadline impacts)
4. Strategic (workforce development, retention)
```

---

## Union Labor Categories and Classifications

### IBEW Electrical Worker Classifications

| Classification | Code | Typical Role | Crew Ratio |
|---------------|------|-------------|------------|
| Superintendent | SI | Oversees multiple foremen/projects | 1 per project or group |
| General Foreman | GF | Manages multiple foremen on large projects | 1 per 3-4 foremen |
| Foreman | FM | Leads a crew, directs daily work | 1 per 6-8 JW |
| Journeyman Electrician | JW | Licensed electrician, performs skilled work | Base unit |
| 4th Year Apprentice | AP4 | Near-completion apprentice | Per CBA ratio |
| 3rd Year Apprentice | AP3 | Mid-level apprentice | Per CBA ratio |
| 2nd Year Apprentice | AP2 | Early-mid apprentice | Per CBA ratio |
| 1st Year Apprentice | AP1 | Entry-level apprentice | Per CBA ratio |

### Crew Composition Rules

```
Standard crew (8-person):
- 1 Foreman
- 5-6 Journeymen
- 1-2 Apprentices

Large project supervision:
- 1 Superintendent per project (or per 50+ workers)
- 1 General Foreman per 25-30 workers
- 1 Foreman per 6-8 workers

Apprentice ratio (typical CBA):
- Minimum 1 apprentice per 3 journeymen
- Maximum varies by local agreement
- Must maintain ratio at all times on site
```

### Project Phases and Typical Labor Curves

| Phase | Duration (% of project) | Labor Intensity | Typical Trades |
|-------|------------------------|-----------------|----------------|
| Mobilization | 5% | Low — ramp up | FM, SI, few JW |
| Underground/Slab | 10-15% | Medium | JW, AP, FM |
| Rough-In | 30-40% | High — peak labor | All trades, peak |
| Overhead/Cable Pull | 15-20% | High | JW, AP, FM |
| Trim/Devices | 10-15% | Medium — declining | JW, AP |
| Startup/Commissioning | 5-10% | Low | Senior JW, FM, SI |
| Punch List/Closeout | 5% | Low | JW, FM |

---

## Forecasting Methodology

### Data-Driven Projection

```
Method 1: PM-Provided Curves (Primary)
- Use headcount data directly from PM excel sheets
- Each PM projects their own labor needs by week
- Aggregate PM projections for company-wide view
- Highest accuracy for near-term (0-8 weeks)

Method 2: Phase-Based Estimation (Secondary)
- When PM data is incomplete, estimate from:
  - Project value ($ → approximate labor hours)
  - Project type (new construction, TI, service)
  - Phase schedule (rough-in dates, trim dates)
  - Historical labor curves for similar projects
- Apply standard labor curve shapes by phase

Method 3: Historical Trending (Supporting)
- Compare current projection to same period last year
- Factor in seasonal patterns (construction season)
- Adjust for known market conditions
- Use as sanity check on PM projections
```

### Confidence Levels

| Timeframe | Confidence | Source | Notes |
|-----------|-----------|--------|-------|
| 0-4 weeks | High (90%+) | PM actuals + projections | Workers are assigned, projects in progress |
| 4-8 weeks | Medium (70-85%) | PM projections | Mobilization dates may shift |
| 8-12 weeks | Moderate (50-70%) | PM estimates + phase-based | Project awards may change |
| 12+ weeks | Low (30-50%) | Phase-based + historical | Speculative, use for planning only |

### Adjustment Factors

```
Apply these adjustments to raw PM projections:
- Attrition rate: [X]% — Workers leaving for other contractors
- Weather delays: [X]% — Seasonal weather impact (regional)
- Absenteeism: [X]% — Typical daily absence rate
- Overtime factor: [X] — When headcount is short, OT fills gap
- Mobilization lag: [X] days — Time between hall request and start
```

---

## Report Types and When to Use Them

| Report | Frequency | Audience | Purpose |
|--------|-----------|----------|---------|
| **Weekly Projection** | Every Monday | Operations leadership | Track near-term staffing, identify immediate needs |
| **Monthly Forecast** | 1st of month | Executive team, union rep | Strategic planning, hall coordination |
| **PM Breakdown** | Weekly or on demand | Individual PMs | Validate their data, plan their projects |
| **Spike/Dip Analysis** | When projections change | Operations, estimating | Adjust schedules, plan mitigation |
| **Resource Allocation** | As needed | Operations leadership | Move workers between projects optimally |
| **Union Dashboard** | Weekly | HR, union liaison | Track compliance, manage hall requests |
| **Quarterly Outlook** | Quarterly | Executive team, board | Long-term workforce strategy |

---

## Configuration [CUSTOMIZE]

```markdown
## Company Settings

- Company name: Huston Electric, Inc.
- Union local: [IBEW Local XXX]
- Region: [Your region]
- Typical active projects: [X]
- Typical workforce size: [X] workers

## Project Manager List

- [PM Name 1]
- [PM Name 2]
- [PM Name 3]
- [PM Name 4]
- [PM Name 5]

## Labor Categories

Customize trade classifications to match your CBA:

| Classification | Code | Include in Reports |
|---------------|------|-------------------|
| Journeyman Electrician | JW | Yes |
| Apprentice 1st Year | AP1 | Yes |
| Apprentice 2nd Year | AP2 | Yes |
| Apprentice 3rd Year | AP3 | Yes |
| Apprentice 4th Year | AP4 | Yes |
| Foreman | FM | Yes |
| General Foreman | GF | Yes |
| Superintendent | SI | Yes |
| [Add custom] | [Code] | [Yes/No] |

## Reporting Periods

- Fiscal year start: [Month]
- Default projection window: [X] weeks
- Report delivery: [Email / Slack / Download]
- Report day: [Monday / Friday]

## Thresholds

- Spike threshold: [X]% above rolling average
- Dip threshold: [X]% below rolling average
- Stale data warning: PM sheet older than [X] days
- Minimum crew size: [X] workers per project
- Maximum workforce capacity: [X] workers

## Union Hall Settings

- Hall request lead time: [X] business days
- Apprentice ratio requirement: 1 AP per [X] JW
- Foreman ratio requirement: 1 FM per [X] JW
- Traveler availability: [Low / Medium / High]
```

---

## Capability by Connector

| Capability | Standalone | + Spreadsheet | + Knowledge Base | + Email/Chat |
|------------|-----------|---------------|------------------|--------------|
| Parse PM data | Upload files | Pull directly | — | — |
| Historical trends | Manual input | — | Auto-retrieve | — |
| Generate reports | Download | Write to sheets | Store in KB | Send to team |
| Staffing alerts | Show in chat | — | — | Push notifications |
| Union tracking | Manual input | Live data | Historical reference | Alert union rep |

---

## Tips

1. **Collect PM sheets consistently** — Use a standard template so data is uniform across PMs
2. **Update weekly** — Manpower projections shift constantly; stale data leads to poor decisions
3. **Watch transitions** — The weeks between project phases are where staffing gets messy
4. **Coordinate with the hall early** — Union halls need lead time to fill requests, especially for specialized trades
5. **Track actuals vs. projections** — Compare what was projected to what actually happened to improve future accuracy

---

## Related Skills

- **schedule-builder** — Build project schedules with Gantt charts for individual projects
