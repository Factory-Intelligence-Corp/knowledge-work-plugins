# Huston Bid Intelligence Plugin

A bid tracking and analysis plugin primarily designed for [Cowork](https://claude.com/product/cowork), Anthropic's agentic desktop application — though it also works in Claude Code. Built for Huston Electric, Inc. to transform chaotic bid invitation emails into organized, union-based Excel intelligence reports that drive Tuesday strategy meetings. Works standalone with email forwarding and your input, supercharged when you connect your email, spreadsheet tools, and knowledge base.

## Installation

```bash
claude plugins add knowledge-work-plugins/huston-bid-intelligence
```

## Commands

Explicit workflows you invoke with a slash command:

| Command | Description |
|---|---|
| `/process-bids` | Parse bid invitation emails — extract project details, classify by union local, assess scope and complexity, flag strategic opportunities |
| `/bid-report` | Generate the weekly Excel intelligence report — organized by union territory, with Go/No-Go recommendations and priority rankings for Tuesday meetings |

All commands work **standalone** (forward emails, paste bid details, or upload documents) and get **supercharged** with MCP connectors.

## Skills

Domain knowledge Claude uses automatically when relevant:

| Skill | Description |
|---|---|
| `bid-email-analysis` | Huston Bid Intel Agent — transforms bid invitation emails into organized union-based Excel intelligence reports for Tuesday strategy meetings |
| `bid-strategy` | Bid strategy analysis — analyzes market conditions, competitive landscape, historical win rates, and backlog capacity to recommend Go/No-Go decisions |

## Example Workflows

### Processing Incoming Bids

```
/process-bids
```

Forward bid invitation emails or paste their content. Get structured extraction of project name, GC/owner, location, bid date, scope, estimated value, and union jurisdiction. Each bid is classified, assessed, and ready for the weekly report.

### Tuesday Strategy Meeting Report

```
/bid-report
```

Generate a comprehensive Excel report organized by union local territory. Includes all active bid opportunities with Go/No-Go recommendations, priority rankings, and strategic notes. Designed for printing or screen-sharing at Tuesday morning meetings.

### Quick Bid Assessment

Just ask naturally:
```
We just got invited to bid on the new Jefferson County courthouse renovation. What do you think?
```

The `bid-strategy` skill triggers automatically, researches the project, assesses fit with Huston's capabilities, and provides a Go/No-Go recommendation with rationale.

### Competitive Landscape Check

```
Who else is likely bidding on the Mercy Hospital expansion?
```

The `bid-strategy` skill analyzes known competitors in that union territory and project type, referencing historical bid results.

## Standalone + Supercharged

Every command and skill works without any integrations:

| What You Can Do | Standalone | Supercharged With |
|-----------------|------------|-------------------|
| Parse bid emails | Forward/paste email content | Email MCP (Gmail, Outlook) |
| Generate Excel reports | Manual data entry, paste bids | Spreadsheet MCP (Google Sheets) |
| Track bid history | Describe past bids | Knowledge Base MCP (Notion, Confluence) |
| Assess opportunities | Describe the project | Email + Knowledge Base MCPs |
| Tuesday meeting prep | Upload/paste bid list | All MCPs combined |
| Document generation | Text output | Document + Spreadsheet MCPs |

## MCP Integrations

> If you see unfamiliar placeholders or need to check which tools are connected, see [CONNECTORS.md](CONNECTORS.md).

Connect your tools for a richer experience:

| Category | Examples | What It Enables |
|---|---|---|
| **Email** | Gmail, Microsoft 365 | Auto-pull bid invitation emails, plan room notifications, addenda |
| **Spreadsheet** | Google Sheets, Microsoft 365 | Generate and update Excel/Sheets bid tracking reports |
| **Knowledge Base** | Notion, Confluence | Store bid history, win/loss data, contractor notes, lessons learned |
| **Chat** | Slack, Teams | Share bid alerts, coordinate estimating team, distribute reports |
| **Calendar** | Google Calendar, Microsoft 365 | Track bid due dates, pre-bid meetings, Tuesday strategy meetings |
| **File Storage** | Google Drive | Store bid documents, plans, specifications, addenda |

See [CONNECTORS.md](CONNECTORS.md) for the full list of supported integrations.

## Settings

Create a local settings file at `huston-bid-intelligence/.claude/settings.local.json` to personalize:

```json
{
  "company": {
    "name": "Huston Electric, Inc.",
    "licenses": ["Electrical Contractor", "Low Voltage", "Fire Alarm"],
    "bonding_capacity": 5000000,
    "service_territory": "Greater Metropolitan Area"
  },
  "union_locals": [
    {
      "local": "IBEW Local 134",
      "territory": "City of Chicago and Cook County",
      "jurisdiction_notes": "Primary territory"
    },
    {
      "local": "IBEW Local 701",
      "territory": "DuPage, Kane, Kendall, Will Counties",
      "jurisdiction_notes": "Secondary territory"
    }
  ],
  "strategic_priorities": {
    "target_sectors": ["Healthcare", "Education", "Municipal", "Data Centers"],
    "min_project_value": 100000,
    "max_project_value": 10000000,
    "preferred_gc_relationships": ["Turner Construction", "Walsh Group", "Pepper Construction"],
    "avoid_gc": []
  },
  "meeting_schedule": {
    "strategy_meeting": "Tuesday 8:00 AM",
    "report_deadline": "Monday 5:00 PM"
  },
  "team": {
    "estimators": ["Name1", "Name2"],
    "project_managers": ["Name1", "Name2"],
    "superintendent": "Name"
  }
}
```

The plugin will ask you for this information interactively if it is not configured.
