---
name: schedule-builder
description: Project schedule assistant for Huston Electric. User provides project title, start date, and task list with durations. Calculates start and end dates for each task, supports weekday-only scheduling, shows schedule for approval, and produces a PDF with summary table and color-coded Gantt chart. Trigger with "build a schedule", "create a project schedule", "schedule for [project]", "Gantt chart", "project timeline", or "task schedule".
---

# Schedule Builder

Build professional project schedules with calculated dates, dependency tracking, and polished PDF output featuring summary tables and color-coded Gantt charts. Designed for electrical construction projects at Huston Electric, Inc.

Works standalone when you provide project details in conversation. Supercharged when you connect your spreadsheet, document, and email tools.

---

## Connectors (Optional)

| Connector | What It Adds |
|-----------|--------------|
| **Spreadsheet** | Import task lists from existing workbooks, export schedule data |
| **Document** | Generate formatted PDF reports with Gantt charts |
| **Email** | Send completed schedule PDFs to project team |
| **File Storage** | Save schedules to shared project folders |
| **Calendar** | Sync milestone dates to team calendars |
| **Project Tracker** | Create tasks in Jira, Asana, or similar tools |

> **No connectors?** Provide your task list in conversation. I will calculate the schedule and produce output you can copy or download.

---

## How It Works

```
┌──────────────────────────────────────────────────────────────────────┐
│                       SCHEDULE BUILDER                               │
├──────────────────────────────────────────────────────────────────────┤
│                                                                      │
│  Step 1: GATHER PROJECT DETAILS                                      │
│  - Project title                                                     │
│  - Start date                                                        │
│  - Weekday-only? (skip weekends)                                    │
│  - Hours per day (default: 8)                                       │
│                                                                      │
│  Step 2: DEFINE TASK LIST                                            │
│  - Task names                                                        │
│  - Durations (days or weeks)                                        │
│  - Dependencies (which tasks must finish first)                     │
│  - Resource assignments (optional)                                   │
│                                                                      │
│  Step 3: CALCULATE DATES                                             │
│  - Start/end dates per task                                          │
│  - Weekday-only adjustments                                         │
│  - Critical path identification                                     │
│  - Total project duration                                            │
│                                                                      │
│  Step 4: PRESENT FOR APPROVAL                                        │
│  - Schedule table (task, start, end, duration, dependencies)        │
│  - Summary statistics                                                │
│  - Ask user to confirm or adjust                                    │
│                                                                      │
│  Step 5: GENERATE PDF                                                │
│  - Summary table                                                     │
│  - Color-coded Gantt chart                                           │
│  - Critical path highlighted                                        │
│  - Deliver via ~~email / ~~file storage or download                 │
│                                                                      │
└──────────────────────────────────────────────────────────────────────┘
```

---

## Output Format

### Schedule Table (Approval View)

```markdown
# Project Schedule: [Project Title]
**Start Date:** [Date]
**Scheduling Mode:** [Weekday-Only / Calendar Days]
**Generated:** [Date]

---

## Schedule Summary

| Metric | Value |
|--------|-------|
| **Project Start** | [Date] |
| **Project End** | [Date] |
| **Total Duration** | [X] working days ([X] calendar days) |
| **Total Tasks** | [X] |
| **Critical Path Tasks** | [X] |
| **Milestones** | [X] |

---

## Task Schedule

| # | Task | Duration | Start | End | Dependencies | Resources | Critical |
|---|------|----------|-------|-----|-------------|-----------|----------|
| 1 | [Task name] | [X] days | [Date] | [Date] | — | [Trade/crew] | Yes/No |
| 2 | [Task name] | [X] days | [Date] | [Date] | 1 | [Trade/crew] | Yes/No |
| 3 | [Task name] | [X] days | [Date] | [Date] | 1 | [Trade/crew] | Yes/No |
| 4 | [Task name] | [X] days | [Date] | [Date] | 2, 3 | [Trade/crew] | Yes/No |
| 5 | [Task name] | [X] days | [Date] | [Date] | 4 | [Trade/crew] | Yes/No |

---

## Critical Path

[Task 1] → [Task 2] → [Task 4] → [Task 5]
**Critical Path Duration:** [X] working days
**Float:** Tasks not on critical path have [X] days of float

---

## Milestones

| Milestone | Date | Triggered By |
|-----------|------|-------------|
| Project Start | [Date] | — |
| [Phase complete] | [Date] | Task [X] completion |
| [Inspection] | [Date] | Task [X] completion |
| Substantial Completion | [Date] | Task [X] completion |
| Project Complete | [Date] | All tasks |

---

Does this schedule look correct? I can adjust any task durations,
dependencies, or dates before generating the final PDF.
```

### PDF Output

```markdown
## PDF Contents

Page 1: Cover Page
- Project title
- Huston Electric, Inc. logo area
- Prepared by / date
- Project summary

Page 2: Schedule Table
- Full task list with dates, durations, dependencies
- Critical path tasks highlighted in bold
- Milestones marked with diamond symbols

Page 3+: Gantt Chart
- Color-coded horizontal bar chart
- Time axis (weeks) across the top
- Tasks listed vertically on the left
- Bars colored by category/trade:
  - Blue: General / Mobilization
  - Red: Critical path tasks
  - Green: Rough-in / Installation
  - Orange: Overhead / Cable pull
  - Purple: Trim / Devices
  - Teal: Startup / Commissioning
  - Gray: Punch list / Closeout
- Dependency arrows between tasks
- Milestone diamonds on timeline
- Today-line marker (vertical red dashed line)
- Weekend shading (if weekday-only mode)
```

---

## Execution Flow

### Step 1: Gather Project Details

```
Required:
1. Project Title — "Downtown Office TI" or "ABC Manufacturing Plant"
2. Start Date — "April 1, 2026" or "next Monday"
3. Weekday-Only? — Skip Saturdays and Sundays (default: yes)

Optional:
4. Hours Per Day — Default 8 hours
5. Project Type — New construction, TI, service, etc.
6. Working Calendar — Standard or custom (e.g., 4x10 schedule)

If user provides incomplete info, ask:
- "What's the project name?"
- "When does it start?"
- "Should I skip weekends in the schedule? (Most projects do)"
```

### Step 2: Parse Task List with Durations

```
Accept input in multiple formats:

Format A: Simple list
"Mobilization - 3 days
Rough-in underground - 10 days
Pull wire overhead - 5 days
Trim and devices - 8 days
Startup - 3 days"

Format B: With dependencies
"1. Mobilization (3 days)
2. Underground rough-in (10 days, after 1)
3. Wall rough-in (15 days, after 1)
4. Overhead conduit (8 days, after 2, 3)
5. Wire pull (5 days, after 4)
6. Trim and devices (10 days, after 5)
7. Startup and testing (3 days, after 6)"

Format C: From spreadsheet
- Import task list from ~~spreadsheet
- Map columns: task name, duration, predecessor, resources

Format D: Template-based
- "Use the standard TI schedule template"
- "Base it on a typical new construction project"
- Apply standard Huston Electric task templates
```

### Step 3: Calculate Dates (Weekday-Only Option)

```
Date calculation algorithm:

IF weekday_only = true:
  For each task:
    1. Set start_date = max(project_start, predecessor_end + 1 business day)
    2. If start_date falls on Saturday → move to Monday
    3. If start_date falls on Sunday → move to Monday
    4. Calculate end_date:
       - Count forward [duration] business days from start_date
       - Skip Saturdays and Sundays
       - Skip holidays (if holiday calendar provided)
    5. Record: task, start_date, end_date, duration_business_days, duration_calendar_days

IF weekday_only = false:
  For each task:
    1. Set start_date = max(project_start, predecessor_end + 1 day)
    2. Calculate end_date = start_date + duration - 1
    3. Record: task, start_date, end_date, duration_days

Holiday handling:
  - Default: No holidays skipped (user can provide list)
  - Common holidays: New Year's, Memorial Day, July 4th,
    Labor Day, Thanksgiving (+ day after), Christmas
  - Ask user: "Should I skip any holidays?"

Dependency resolution:
  - Finish-to-Start (FS): Default — successor starts after predecessor ends
  - Start-to-Start (SS): Successor starts when predecessor starts (+ lag)
  - Finish-to-Finish (FF): Successor ends when predecessor ends (+ lag)
  - Lag: Add [X] days between dependency and start
  - Lead: Overlap by [X] days (negative lag)
```

### Step 4: Present for Approval

```
Show the user:
1. Complete schedule table with calculated dates
2. Project duration summary
3. Critical path identification
4. Any warnings:
   - Tasks with zero float (schedule risk)
   - Very long tasks that could be broken down
   - Unusual durations (e.g., 1-day task followed by 60-day task)
   - Weekend/holiday impacts on timeline

Ask for confirmation:
"Does this schedule look correct? I can:
 - Adjust any task durations
 - Change dependencies
 - Add or remove tasks
 - Move the start date
 - Switch between weekday-only and calendar days

Once approved, I'll generate the PDF with Gantt chart."
```

### Step 5: Generate PDF with Gantt Chart

```
PDF generation:
1. Build summary table (formatted for print)
2. Build Gantt chart:
   - X-axis: Calendar weeks (Monday start)
   - Y-axis: Task list (top to bottom)
   - Bars: Colored by task category
   - Width: Proportional to duration
   - Arrows: Show dependencies
   - Diamonds: Show milestones
3. Add header/footer:
   - Project title, company name
   - Generated date, page numbers
4. Export as PDF

Delivery options:
- Download directly
- Send via ~~email to project team
- Save to ~~file storage in project folder
- Post to ~~chat channel
```

---

## Dependency Handling

### Dependency Types

| Type | Code | Meaning | Example |
|------|------|---------|---------|
| Finish-to-Start | FS | B starts after A finishes | Wire pull starts after conduit is done |
| Start-to-Start | SS | B starts when A starts | Inspection starts when rough-in starts |
| Finish-to-Finish | FF | B finishes when A finishes | Cleanup finishes when punch list finishes |
| FS + Lag | FS+X | B starts X days after A finishes | Concrete pour starts 3 days after forms (cure time) |
| FS + Lead | FS-X | B starts X days before A finishes | Trim can start 2 days before rough-in ends (overlap) |

### Dependency Resolution Rules

```
1. Parse dependencies from user input
2. Build task dependency graph
3. Check for circular dependencies → Error if found
4. Topological sort to determine calculation order
5. Forward pass: Calculate earliest start/end dates
6. Backward pass: Calculate latest start/end dates
7. Float = Latest Start - Earliest Start
8. Critical path = Tasks where Float = 0
```

### Critical Path

```
The critical path is the longest sequence of dependent tasks.
Any delay on a critical path task delays the entire project.

Identification:
1. Forward pass → Earliest Start (ES), Earliest Finish (EF)
2. Backward pass → Latest Start (LS), Latest Finish (LF)
3. Total Float = LS - ES (or LF - EF)
4. Critical path tasks have Total Float = 0

Reporting:
- Mark critical path tasks with a flag in the schedule table
- Highlight critical path bars in red on the Gantt chart
- Show critical path sequence in summary
- Calculate total critical path duration
```

---

## Weekday vs. Calendar Day Calculations

### Weekday-Only Mode (Default)

```
- Counts only Monday through Friday
- A "5-day task" starting Monday ends Friday
- A "5-day task" starting Wednesday ends Tuesday (next week)
- Weekends shown as gaps on Gantt chart (shaded gray)
- Optional: Skip holidays too

Best for:
- Most construction projects
- Union labor schedules (standard 5-day work week)
- Office/commercial projects
```

### Calendar Day Mode

```
- Counts all days including weekends
- A "5-day task" starting Monday ends Friday
- A "5-day task" starting Wednesday ends Sunday
- No gaps on Gantt chart
- Useful for duration-based milestones

Best for:
- Cure times (concrete, paint)
- Equipment lead times
- Permit review periods
- Procurement timelines
```

### Hybrid Mode

```
Some tasks are calendar-day based even in weekday-only projects:
- Concrete cure time: 7 calendar days (not 7 work days)
- Permit review: 14 calendar days
- Equipment delivery: Lead time in calendar days

Mark these tasks as "calendar day" and they will be calculated
differently from the standard weekday-only tasks.
```

---

## Gantt Chart Formatting

### Color Scheme (Trade-Based)

| Color | Category | Example Tasks |
|-------|----------|---------------|
| Steel Blue | Mobilization / General | Site setup, temporary power, layout |
| Crimson Red | Critical Path | Any task on the critical path |
| Forest Green | Rough-In / Installation | Conduit, rough-in wiring, panel install |
| Orange | Overhead / Cable Pull | Cable tray, overhead conduit, wire pull |
| Purple | Trim / Finish | Devices, plates, fixtures, labels |
| Teal | Startup / Commissioning | Testing, energization, punch list |
| Slate Gray | Administrative | Inspections, submittals, closeout |
| Gold | Milestones | Diamond markers for key dates |

### Layout

```
Gantt chart layout specifications:

Header:
  - Project title (bold, large font)
  - Date range: [Start] — [End]
  - Legend (color key)

Time Axis (top):
  - Month labels across top
  - Week divisions (Monday-start vertical lines)
  - Day divisions (light grid, optional for short projects)
  - Today marker (vertical red dashed line)

Task Axis (left):
  - Task number
  - Task name (truncated if > 40 chars)
  - Duration in parentheses
  - Indent subtasks under phases

Bars:
  - Height: Uniform, with spacing between rows
  - Fill: Solid color per category
  - Border: Darker shade of fill color
  - Critical path bars: Red fill or red border
  - Progress fill: Optional darker overlay showing % complete

Arrows:
  - Dependency arrows connecting task bars
  - FS: Arrow from end of predecessor to start of successor
  - Thin gray lines, small arrowheads

Milestones:
  - Diamond shape on the timeline
  - Gold fill
  - Label to the right

Weekend shading:
  - Light gray vertical bands for Saturday-Sunday
  - Only in weekday-only mode
```

---

## Standard Task Templates

### Electrical Construction - Tenant Improvement (TI)

```
1. Mobilization & Layout (2-3 days)
2. Demolition of Existing (3-5 days, after 1)
3. Underground / Slab Rough-In (5-10 days, after 2)
4. Wall Rough-In — Conduit & Boxes (10-15 days, after 2)
5. Panel & Gear Installation (3-5 days, after 3)
6. Overhead Rough-In — Conduit (8-12 days, after 4)
7. Cable / Wire Pull (5-8 days, after 5, 6)
8. Terminations (3-5 days, after 7)
9. Trim — Devices & Plates (5-8 days, after 8)
10. Light Fixture Installation (3-5 days, after 8)
11. Fire Alarm Devices (2-3 days, after 9)
12. Testing & Labeling (2-3 days, after 9, 10, 11)
13. Inspections (1-2 days, after 12)
14. Startup & Energization (1-2 days, after 13)
15. Punch List (3-5 days, after 14)
16. Closeout & Demobilization (1-2 days, after 15)
```

### Electrical Construction - New Build (Ground-Up)

```
1. Mobilization & Temporary Power (3-5 days)
2. Underground Ductbank & Conduit (10-20 days, after 1)
3. Slab Conduit & Stub-Ups (5-10 days, after 2)
4. Switchgear / Transformer Pads (3-5 days, after 2)
5. Wall Rough-In — Conduit (15-25 days, after 3)
6. Panel Boards & Distribution (5-8 days, after 4)
7. Overhead Conduit & Supports (10-15 days, after 5)
8. Cable Tray Installation (5-10 days, after 7)
9. Main Feeders Pull (5-8 days, after 6, 8)
10. Branch Circuit Wire Pull (8-12 days, after 7)
11. Terminations — Panels (5-8 days, after 9, 10)
12. Motor Connections (3-5 days, after 10)
13. Fire Alarm Rough-In (5-8 days, after 5)
14. Fire Alarm Devices & Heads (3-5 days, after 13)
15. Trim — Devices & Plates (8-12 days, after 11)
16. Light Fixture Installation (5-8 days, after 11)
17. Controls & Low Voltage (5-8 days, after 11)
18. Fire Alarm Testing (2-3 days, after 14)
19. Electrical Testing & Labeling (3-5 days, after 15, 16, 17)
20. Inspections (2-3 days, after 18, 19)
21. Switchgear Energization (1-2 days, after 20)
22. Startup & Commissioning (3-5 days, after 21)
23. Punch List (5-8 days, after 22)
24. Closeout Documentation (3-5 days, after 23)
25. Demobilization (1-2 days, after 24)
```

---

## Capability by Connector

| Capability | Standalone | + Spreadsheet | + Document | + Email |
|------------|-----------|---------------|------------|---------|
| Define tasks | In conversation | Import from sheet | — | — |
| Calculate dates | Always | Always | Always | Always |
| View schedule | Table in chat | Table in chat | — | — |
| Gantt chart | Text-based | Text-based | PDF with chart | PDF attached |
| Share schedule | Copy output | Export to sheet | PDF download | Send PDF |
| Track changes | Manual | Version in sheet | — | — |

---

## Tips

1. **Start with a template** — Use a standard TI or new-build template and modify, rather than building from scratch
2. **Be realistic with durations** — Optimistic schedules fail. Add buffer for inspections, weather, and coordination
3. **Identify the critical path** — Know which tasks drive your end date so you can protect them
4. **Use weekday-only for labor scheduling** — Calendar days are for material lead times and cure times, not crew work
5. **Review before generating PDF** — Easier to fix the schedule in the approval step than to regenerate the PDF
6. **Track dependencies carefully** — Missing a dependency can hide schedule risk

---

## Related Skills

- **manpower-analytics** — Analyze workforce needs across all projects, identify staffing spikes and dips
