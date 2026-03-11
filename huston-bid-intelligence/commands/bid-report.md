---
description: Generate the weekly Excel intelligence report — organized by union territory, with Go/No-Go recommendations and priority rankings for Tuesday strategy meetings
argument-hint: "<week or date range>"
---

# /bid-report

> If you see unfamiliar placeholders or need to check which tools are connected, see [CONNECTORS.md](../CONNECTORS.md).

Generate a comprehensive bid intelligence report for Huston Electric's Tuesday strategy meeting. Produces an Excel workbook organized by union territory with Go/No-Go recommendations, priority rankings, and strategic summaries.

## Usage

```
/bid-report [week or date range]
```

Generate bid report for: $ARGUMENTS

If a file is referenced: @$1

---

## How It Works

```
┌─────────────────────────────────────────────────────────────────┐
│                       BID REPORT                                  │
├─────────────────────────────────────────────────────────────────┤
│  STANDALONE (always works)                                        │
│  ✓ Upload CSV or paste your current bid list                     │
│  ✓ Describe active bid opportunities                             │
│  ✓ Reference bids processed via /process-bids                    │
│  ✓ Generate formatted Excel workbook (4 sheets)                  │
│  ✓ Strategic summary document for meeting discussion             │
│  ✓ Priority-ranked opportunity list                              │
│  ✓ Bid calendar with upcoming deadlines                          │
├─────────────────────────────────────────────────────────────────┤
│  SUPERCHARGED (when you connect your tools)                       │
│  + Spreadsheet: Write directly to Google Sheets / Excel Online   │
│  + Knowledge Base: Pull bid history, update with new entries     │
│  + Email: Include bids processed since last report               │
│  + Calendar: Sync bid deadlines to team calendar                 │
│  + Chat: Distribute report summary to team channel               │
└─────────────────────────────────────────────────────────────────┘
```

---

## What I Need From You

**Option A: Use processed bids**
If you have been running `/process-bids` throughout the week, I will compile all processed bids into the report automatically.

**Option B: Upload a CSV or spreadsheet**
Upload your existing bid tracking spreadsheet. I will analyze, enrich, and reformat into the standard Tuesday report.

**Option C: Paste your bid list**
```
1. Lincoln Elementary Renovation — Turner Construction — Oak Park, Cook County
   Bid date: March 25 — Est. $800K — Full electrical

2. Mercy Hospital Wing Addition — Walsh Group — Naperville, DuPage County
   Bid date: March 28 — Est. $2.5M — Electrical + low voltage + fire alarm

3. Oakbrook Data Center — Owner Direct — Oak Brook, DuPage County
   Bid date: April 5 — Est. $4M — Critical power and cooling infrastructure
```

**Option D: Describe your pipeline**
"We have 8 active bids this week. Three in Cook County, two in DuPage, and three downstate. The biggest is a $4M data center. We also got results back on two bids from last week."

---

## Output

### Excel Workbook Structure

The report generates a workbook with four sheets:

#### Sheet 1: Bid Intelligence Summary

All active bids in a single view, sorted by priority rank:

```
| Priority | Project Name | GC/Owner | Location | Bid Date | Est. Value | Union Local | Scope Summary | Complexity | Go/No-Go | Notes | Estimator | Status |
```

Formatting:
- Go = green highlight on recommendation column
- Conditional Go = yellow highlight
- No-Go = red highlight
- Bid dates within 7 days = bold red text
- Bid dates past = strikethrough with red background
- Grouped by recommendation (Go first, then Conditional, then No-Go)
- Frozen header row and first two columns
- Auto-fitted column widths
- Print area set for landscape tabloid

#### Sheet 2: By Union Territory

Same data reorganized by IBEW local jurisdiction:

```
--- IBEW Local 134 (Cook County / Chicago) ---
| Project | GC | Bid Date | Value | Scope | Go/No-Go |
Subtotal: X bids, $X total value

--- IBEW Local 701 (DuPage / Suburban) ---
| Project | GC | Bid Date | Value | Scope | Go/No-Go |
Subtotal: X bids, $X total value

[Additional locals as applicable]

GRAND TOTAL: X bids, $X total value
```

#### Sheet 3: Strategic Dashboard

Summary statistics and charts:

```
PIPELINE OVERVIEW
- Total active bids: X
- Total pipeline value: $X
- Bids due this week: X ($X)
- Go recommendations: X ($X)
- Conditional Go: X ($X)
- No-Go: X ($X)
- Hit rate (trailing 90 days): X%

BY SECTOR
| Sector | Bids | Value | % of Pipeline |
| Healthcare | X | $X | X% |
| Education | X | $X | X% |
[etc.]

BY GC (Top 10)
| GC | Active Bids | Total Value | Historical Win Rate |
[Ranked by total value]

WEEK-OVER-WEEK
- New bids received: X (vs. X last week)
- Bids submitted: X
- Results received: X (X wins, X losses)
- Average project size: $X (vs. $X last week)
```

#### Sheet 4: Bid Calendar

Timeline view of all upcoming deadlines:

```
THIS WEEK
| Day | Project | GC | Value | Pre-Bid? | Estimator | Status |

NEXT WEEK
[Same format]

WEEKS 3-4
[Same format]

BEYOND 4 WEEKS
[Same format]

PRE-BID MEETINGS
| Date | Time | Project | Location | Mandatory? | Attendee |
```

---

### Strategic Summary Document

A printable/shareable summary for the Tuesday meeting:

```markdown
# Huston Electric — Bid Intelligence Report
## Week of [Date]

### This Week at a Glance
- New bids received: X projects, $X estimated value
- Bids due this week: X projects
- Recommended to pursue: X of X new opportunities
- Top opportunity: [Name] — $X — [Why]
- Bids submitted last week: X
- Results received: X wins ($X), X losses

---

### Priority Opportunities (Go Recommendations)

#### 1. [Project Name] — $[Value]
- GC: [Name] | Owner: [Name]
- Location: [City, County] | Local: [IBEW Local]
- Bid Date: [Date] ([X days away])
- Scope: [Summary]
- Why pursue: [Strategic rationale]
- Risks: [Key concerns]
- Estimator: [Assigned or TBD]

[Repeat for each Go recommendation, ranked by priority]

---

### Needs Discussion (Conditional Go)

| Project | Value | GC | Issue |
|---------|-------|----|-------|
| [Name] | $X | [GC] | [What the team needs to decide] |

---

### Declined (No-Go)

| Project | Value | GC | Reason |
|---------|-------|----|--------|
| [Name] | $X | [GC] | [Brief rationale] |

---

### Recent Results

| Project | GC | Our Bid | Result | Winner | Spread |
|---------|----|----|--------|--------|--------|
| [Name] | [GC] | $X | Won/Lost | [Winner] | X% |

---

### Action Items

1. [ ] [Person]: [Action] — [Deadline]
2. [ ] [Person]: [Action] — [Deadline]
3. [ ] [Person]: [Action] — [Deadline]

---

### Market Notes
- [Trend or observation]
- [Competitor intelligence]
- [Upcoming large projects]
```

---

## Generation Logic

### Step 1: Gather All Active Bids

```
Sources (in priority order):
1. Bids processed via /process-bids this week
2. Existing bid tracking spreadsheet (if connected)
3. Knowledge base bid records (if connected)
4. User-provided list or CSV upload
5. Email scan for any unprocessed invitations (if connected)

Deduplication:
- Match by project name + GC + bid date
- Merge records, keeping most complete data
- Flag conflicts for user review
```

### Step 2: Validate and Enrich

```
For each bid:
1. Verify bid date has not passed (flag if expired)
2. Confirm all required fields are populated
3. Fill gaps where possible:
   - Estimate value from scope if missing
   - Look up GC contact from previous bids
   - Confirm union local from location
4. Update status:
   - New (just received, not yet assessed)
   - In Progress (estimator working on it)
   - Submitted (bid turned in, awaiting result)
   - Won / Lost / No Bid (final dispositions)
5. Re-run Go/No-Go if new information available
```

### Step 3: Rank and Prioritize

```
Apply priority scoring:
Priority Score = (Strategic Fit x 0.30) + (Value x 0.25) +
                 (Win Probability x 0.25) + (Timing x 0.20)

Sort order:
1. Go recommendations — by priority score descending
2. Conditional Go — by bid date ascending (most urgent first)
3. No-Go — by value descending (document why big ones were declined)
```

### Step 4: Build Excel Workbook

```
1. Create Sheet 1 (Summary) with all bids
   - Apply conditional formatting
   - Set print area and page setup
   - Add filters on each column

2. Create Sheet 2 (By Territory)
   - Group and subtotal by IBEW local
   - Add section headers and spacing

3. Create Sheet 3 (Dashboard)
   - Calculate summary statistics
   - Build sector and GC breakdowns
   - Add week-over-week comparisons

4. Create Sheet 4 (Calendar)
   - Sort by bid date ascending
   - Group by week
   - Highlight pre-bid meetings

5. If ~~spreadsheet connected:
   - Write directly to connected spreadsheet tool
   - Update existing workbook if one exists
   - Preserve historical data in additional sheets
```

### Step 5: Generate Strategic Summary

```
1. Compile "at a glance" statistics
2. Write priority opportunity narratives (Go bids)
3. List conditional opportunities with discussion points
4. Document No-Go decisions with rationale
5. Compile recent bid results and lessons
6. Generate action items with assignees and deadlines
7. Add market observations and intelligence notes
```

### Step 6: Distribute

```
If ~~chat connected:
1. Post summary to estimating team channel
2. Tag team members on their assigned bids
3. Flag bids due within 48 hours as urgent

If ~~calendar connected:
1. Verify bid deadline events exist
2. Create missing events
3. Add pre-bid meeting events
4. Set reminders for estimating deadlines

Save report:
- Excel workbook: Huston-Bid-Report-[YYYY-MM-DD].xlsx
- Strategic summary: Huston-Bid-Summary-[YYYY-MM-DD].md
```

---

## Report Frequency

| Report | When | Content |
|--------|------|---------|
| **Weekly (Tuesday)** | Monday afternoon or Tuesday morning | Full report — all 4 sheets + strategic summary |
| **Mid-week update** | Wednesday/Thursday as needed | Delta report — new bids only, updates to existing |
| **Urgent alert** | Any time | Single-bid report for high-priority or tight-deadline opportunities |

---

## Customization

### Column Configuration

Add or remove columns from the Excel report:

```yaml
columns:
  always_show:
    - priority_rank
    - project_name
    - gc_owner
    - location
    - bid_date
    - estimated_value
    - union_local
    - scope_summary
    - go_no_go
    - notes

  optional:
    - complexity_score
    - assigned_estimator
    - status
    - pre_bid_meeting
    - bond_required
    - prevailing_wage
    - plan_source
    - sector
    - building_sf
    - contract_type
```

### Report Branding

```yaml
branding:
  company_name: "Huston Electric, Inc."
  report_title: "Weekly Bid Intelligence Report"
  logo_path: "[path to logo file]"
  header_color: "#1a365d"
  accent_color: "#2b6cb0"
  font: "Calibri"
```

---

## Tips

1. **Run Monday afternoon** — Generate the report Monday so you have time to review and add context before Tuesday morning.
2. **Process bids daily** — Use `/process-bids` throughout the week so Tuesday report generation is automatic, not a scramble.
3. **Add meeting notes** — After Tuesday meetings, update bid records with team decisions (who is estimating, final Go/No-Go, strategy notes).
4. **Track results religiously** — Log every bid result. Win/loss data is what makes future Go/No-Go decisions smarter.
5. **Archive weekly** — Keep previous weeks' reports for trend analysis and management reporting.
6. **Print landscape tabloid** — Sheet 1 is designed for 11x17 landscape printing for the conference table.
