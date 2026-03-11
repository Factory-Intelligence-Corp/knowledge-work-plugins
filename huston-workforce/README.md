# Huston Workforce Plugin

A workforce analytics and project scheduling plugin for Huston Electric, Inc. — primarily designed for [Cowork](https://claude.com/product/cowork), Anthropic's agentic desktop application, though it also works in Claude Code. Tracks union manpower projections across project managers, identifies staffing spikes and dips, builds project schedules with Gantt charts, and generates strategic workforce planning reports. Works standalone with uploaded spreadsheets and your input, supercharged when you connect your knowledge base, spreadsheets, and communication tools.

## Installation

```bash
claude plugins add knowledge-work-plugins/huston-workforce
```

## Commands

Explicit workflows you invoke with a slash command:

| Command | Description |
|---|---|
| `/manpower-report` | Generate a manpower projection report — upload PM excel sheets, analyze staffing levels, get spike/dip analysis and strategic recommendations |
| `/build-schedule` | Build a project schedule — provide tasks with durations, get a schedule table and color-coded Gantt chart PDF |

All commands work **standalone** (upload spreadsheets, paste data, or describe your projects) and get **supercharged** with MCP connectors.

## Skills

Domain knowledge Claude uses automatically when relevant:

| Skill | Description |
|---|---|
| `manpower-analytics` | "Mike the Manpower Manager" — analyze PM excel sheets, track union manpower projections, identify staffing spikes/dips, generate workforce planning reports |
| `schedule-builder` | Build project schedules — provide tasks with durations, calculate start/end dates, generate PDF with summary table and color-coded Gantt chart |

## Example Workflows

### Weekly Manpower Report

```
/manpower-report
```

Upload PM excel sheets or paste your project labor data. Get a comprehensive manpower projection report with staffing spikes and dips identified, union labor breakdowns by trade, and strategic recommendations for workforce planning.

### Building a Project Schedule

```
/build-schedule
```

Provide a project title, start date, and task list with durations. Choose weekday-only or calendar-day calculations. Get a schedule table for review, then a polished PDF with a color-coded Gantt chart.

### Quick Manpower Check

Just ask naturally:
```
What does our manpower look like for Q3?
```

The `manpower-analytics` skill triggers automatically and analyzes your current data to produce staffing projections.

### Analyzing PM Workloads

```
Show me which PMs have the highest labor demand next month
```

The `manpower-analytics` skill breaks down labor requirements by project manager and identifies who needs additional resources.

### Creating a Schedule from Scratch

```
I need a schedule for the Downtown Office TI project starting April 1
```

The `schedule-builder` skill walks you through defining tasks, durations, and dependencies, then produces a professional schedule with Gantt chart.

## Standalone + Supercharged

Every command and skill works without any integrations:

| What You Can Do | Standalone | Supercharged With |
|-----------------|------------|-------------------|
| Manpower projections | Upload Excel/CSV, paste data | Spreadsheet MCP (Google Sheets, MS 365) |
| Staffing analysis | Describe projects and labor | Knowledge Base MCP (Notion, Confluence) |
| Build schedules | Provide task list manually | Spreadsheet MCP, Document MCP |
| Generate PDF reports | Download locally | Email MCP (Gmail, Outlook) |
| Share reports | Copy output | Chat MCP (Slack), Email MCP |
| Track labor history | Upload historical data | Knowledge Base MCP, Drive MCP |

## MCP Integrations

> If you see unfamiliar placeholders or need to check which tools are connected, see [CONNECTORS.md](CONNECTORS.md).

Connect your tools for a richer experience:

| Category | Examples | What It Enables |
|---|---|---|
| **Knowledge Base** | Notion, Confluence | Centralized labor data, PM project records, historical workforce plans |
| **Spreadsheets** | Google Sheets, Microsoft 365 | Direct access to PM excel sheets, labor tracking workbooks |
| **File Storage** | Google Drive, OneDrive | Access project files, upload/download reports |
| **Email** | Gmail, Outlook | Send completed reports, share projections with stakeholders |
| **Calendar** | Google Calendar, Outlook | Project milestone tracking, scheduling coordination |
| **Chat** | Slack, Teams | Share reports with teams, notify PMs of staffing alerts |

See [CONNECTORS.md](CONNECTORS.md) for the full list of supported integrations and how connector placeholders work.

## Settings

Create a local settings file at `huston-workforce/.claude/settings.local.json` to personalize:

```json
{
  "company": "Huston Electric, Inc.",
  "region": "Your Region",
  "union_local": "IBEW Local XXX",
  "project_managers": [
    "PM Name 1",
    "PM Name 2",
    "PM Name 3"
  ],
  "labor_categories": {
    "journeyman_electrician": { "classification": "JW", "rate_tier": "A" },
    "apprentice_1st_year": { "classification": "AP1", "rate_tier": "D" },
    "apprentice_2nd_year": { "classification": "AP2", "rate_tier": "D" },
    "apprentice_3rd_year": { "classification": "AP3", "rate_tier": "C" },
    "apprentice_4th_year": { "classification": "AP4", "rate_tier": "C" },
    "foreman": { "classification": "FM", "rate_tier": "A+" },
    "general_foreman": { "classification": "GF", "rate_tier": "S" },
    "superintendent": { "classification": "SI", "rate_tier": "S+" }
  },
  "reporting": {
    "fiscal_year_start": "January",
    "default_projection_weeks": 12,
    "workdays_per_week": 5
  },
  "schedule_defaults": {
    "weekday_only": true,
    "hours_per_day": 8,
    "gantt_color_scheme": "trade-based"
  }
}
```

The plugin will ask you for this information interactively if it is not configured.
