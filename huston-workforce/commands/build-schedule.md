---
description: Build a project schedule — provide a project title, start date, and task list with durations, get a schedule table with calculated dates and a color-coded Gantt chart PDF
argument-hint: "<project name>"
---

# /build-schedule

> If you see unfamiliar placeholders or need to check which tools are connected, see [CONNECTORS.md](../CONNECTORS.md).

Build a project schedule with calculated start and end dates, dependency tracking, critical path identification, and a polished PDF featuring a summary table and color-coded Gantt chart.

## Usage

```
/build-schedule [project name]
```

Build a schedule for: $ARGUMENTS

If a file is referenced: @$1

---

## How It Works

```
┌──────────────────────────────────────────────────────────────────────┐
│                      BUILD SCHEDULE                                  │
├──────────────────────────────────────────────────────────────────────┤
│  STANDALONE (always works)                                           │
│  ✓ Provide project title, start date, and task list                 │
│  ✓ Specify durations and dependencies                               │
│  ✓ Choose weekday-only or calendar-day scheduling                   │
│  ✓ Review calculated schedule table                                  │
│  ✓ Approve and generate PDF with Gantt chart                        │
├──────────────────────────────────────────────────────────────────────┤
│  SUPERCHARGED (when you connect your tools)                          │
│  + Spreadsheet: Import tasks from existing workbook                 │
│  + Document: Generate polished PDF with formatted Gantt chart       │
│  + Email: Send schedule PDF to project team                         │
│  + Calendar: Sync milestones to team calendars                      │
│  + File Storage: Save to project folder                             │
└──────────────────────────────────────────────────────────────────────┘
```

---

## What I Need From You

### Step 1: Project Details

Tell me:
- **Project title** — e.g., "Downtown Office TI" or "ABC Manufacturing Expansion"
- **Start date** — e.g., "April 1, 2026" or "next Monday"
- **Weekday-only?** — Skip weekends? (default: yes)
- **Any holidays to skip?** — e.g., "skip Memorial Day and July 4th"

### Step 2: Task List

**Option A: Simple list with durations**
```
Mobilization - 3 days
Underground rough-in - 10 days
Wall rough-in - 15 days
Overhead conduit - 8 days
Wire pull - 5 days
Trim and devices - 10 days
Startup - 3 days
Punch list - 5 days
```

**Option B: With dependencies**
```
1. Mobilization (3 days)
2. Underground rough-in (10 days, after 1)
3. Wall rough-in (15 days, after 1)
4. Overhead conduit (8 days, after 2, 3)
5. Wire pull (5 days, after 4)
6. Trim and devices (10 days, after 5)
7. Startup and testing (3 days, after 6)
8. Punch list (5 days, after 7)
```

**Option C: Use a template**
```
Use the standard TI schedule
Use the standard new construction schedule
```

**Option D: From a file**
Upload a spreadsheet or reference a file with your task list.

If a file is referenced: @$1

### Step 3: Optional Details

- **Resource assignments** — Which trade/crew handles each task
- **Milestones** — Key dates to highlight (inspections, substantial completion)
- **Hours per day** — Default is 8 hours
- **Working calendar** — Standard 5-day or custom (e.g., 4x10)

---

## Output

### Phase 1: Schedule Table (For Your Approval)

```markdown
# Project Schedule: [Project Title]
**Start Date:** [Date]
**Mode:** [Weekday-Only / Calendar Days]
**Holidays Skipped:** [List or None]

---

## Summary

| Metric | Value |
|--------|-------|
| **Project Start** | [Date] |
| **Project End** | [Date] |
| **Working Days** | [X] |
| **Calendar Days** | [X] |
| **Tasks** | [X] |
| **Critical Path Tasks** | [X] |

---

## Schedule

| # | Task | Duration | Start | End | Depends On | Resources | Critical? |
|---|------|----------|-------|-----|-----------|-----------|-----------|
| 1 | [Task] | [X]d | [Date] | [Date] | — | [Crew] | [Yes/No] |
| 2 | [Task] | [X]d | [Date] | [Date] | 1 | [Crew] | [Yes/No] |
| 3 | [Task] | [X]d | [Date] | [Date] | 1 | [Crew] | [Yes/No] |
| 4 | [Task] | [X]d | [Date] | [Date] | 2, 3 | [Crew] | [Yes/No] |
| 5 | [Task] | [X]d | [Date] | [Date] | 4 | [Crew] | [Yes/No] |

---

## Critical Path

[Task 1] → [Task 3] → [Task 4] → [Task 5]
**Duration:** [X] working days
**Any delay on these tasks delays the project end date.**

---

## Milestones

| Milestone | Date | After Task |
|-----------|------|-----------|
| Project Start | [Date] | — |
| Rough-In Complete | [Date] | [Task #] |
| Inspection | [Date] | [Task #] |
| Substantial Completion | [Date] | [Task #] |
| Project Complete | [Date] | [Task #] |

---

## Float Analysis

| Task | Float (Days) | Note |
|------|-------------|------|
| [Task] | 0 | Critical path — no float |
| [Task] | [X] | Can slip [X] days without affecting end date |

---

**Does this look correct?**
I can adjust task durations, dependencies, or dates.
Once you approve, I will generate the PDF with Gantt chart.
```

### Phase 2: PDF Generation (After Approval)

```markdown
## PDF Contents

**Page 1 — Cover**
- Project title
- Huston Electric, Inc.
- Prepared by / date
- Project duration summary

**Page 2 — Schedule Table**
- Complete task list with dates
- Critical path tasks in bold
- Milestone rows marked with diamonds
- Color-coded by task category

**Page 3+ — Gantt Chart**
- Horizontal bar chart
- Time axis: weeks across the top
- Task axis: task names on the left
- Color-coded bars by category:
  - Blue: Mobilization / General
  - Red: Critical path tasks
  - Green: Rough-in / Installation
  - Orange: Overhead / Cable pull
  - Purple: Trim / Devices
  - Teal: Startup / Commissioning
  - Gray: Administrative / Closeout
- Dependency arrows between bars
- Milestone diamonds
- Weekend shading (weekday-only mode)
- Today marker (red dashed vertical line)
```

---

## Date Calculation Rules

### Weekday-Only (Default)

```
- Monday through Friday only
- Saturday and Sunday are skipped
- Example: 5-day task starting Monday, Jan 5
  → Ends Friday, Jan 9

- Example: 5-day task starting Thursday, Jan 8
  → Thu Jan 8, Fri Jan 9, Mon Jan 12, Tue Jan 13, Wed Jan 14
  → Ends Wednesday, Jan 14

- Example: Task starting after predecessor ends Friday, Jan 9
  → Starts Monday, Jan 12

- Holidays: Skipped if specified
  → Task spanning Memorial Day week loses one working day
```

### Calendar Days

```
- All 7 days counted
- Example: 5-day task starting Monday, Jan 5
  → Ends Friday, Jan 9

- Example: 5-day task starting Thursday, Jan 8
  → Ends Monday, Jan 12 (includes Sat + Sun)

- Best for: cure times, lead times, permit reviews
```

### Dependencies

```
Finish-to-Start (default):
  Task B starts the day after Task A ends

With lag:
  "after 3, +2 days" = Task starts 2 days after Task 3 ends

With lead (overlap):
  "after 3, -2 days" = Task starts 2 days before Task 3 ends

No dependency (parallel):
  Tasks with no predecessor start at project start
  (or at earliest possible date based on other dependencies)
```

---

## Templates

### Quick TI Schedule

Say "use TI template" to auto-populate:

```
1. Mobilization & Layout (2 days)
2. Demo Existing (3 days, after 1)
3. Underground Rough-In (5 days, after 2)
4. Wall Rough-In (12 days, after 2)
5. Panel Installation (3 days, after 3)
6. Overhead Conduit (8 days, after 4)
7. Wire Pull (5 days, after 5, 6)
8. Terminations (3 days, after 7)
9. Trim & Devices (6 days, after 8)
10. Fixtures (4 days, after 8)
11. Fire Alarm (2 days, after 9)
12. Testing & Labels (2 days, after 9, 10, 11)
13. Inspection (1 day, after 12)
14. Startup (1 day, after 13)
15. Punch List (3 days, after 14)
16. Closeout (1 day, after 15)
```

### Quick New Construction Schedule

Say "use new construction template" to auto-populate a 25-task standard new-build schedule.

---

## If Spreadsheet Connected

- Import task lists directly from ~~spreadsheet
- Map columns automatically (task, duration, predecessor)
- Export completed schedule back to a workbook
- Keep a version history of schedule changes

## If Document Connected

- Generate a polished, print-ready PDF via ~~document
- Include Gantt chart with professional formatting
- Add company branding and header/footer

## If Email Connected

- Send the PDF schedule to the project team via ~~email
- Include a summary table in the email body
- Attach the PDF for download and printing

## If Calendar Connected

- Create milestone events in ~~calendar
- Set reminders for critical path deadlines
- Share project timeline with team members

---

## Tips

1. **Define dependencies carefully** — A missing dependency can hide schedule risk and make the critical path inaccurate.
2. **Use weekday-only for crew work** — Calendar days are for things like concrete cure times and permit reviews, not labor tasks.
3. **Review before generating the PDF** — It is much easier to adjust in the approval step than to regenerate.
4. **Start with a template** — Modify a standard TI or new-build template rather than starting from a blank slate.
5. **Add buffer for inspections** — Inspections often take longer than planned. Build in a day or two of float after inspection tasks.
6. **Mark milestones** — Key dates like "rough-in complete" and "substantial completion" are useful for tracking and communication.
