# Connectors

## How tool references work

Plugin files use `~~category` as a placeholder for whatever tool the user connects in that category. For example, `~~spreadsheet` might mean Google Sheets, Microsoft Excel Online, or any other spreadsheet tool with an MCP server.

Plugins are **tool-agnostic** — they describe workflows in terms of categories (knowledge base, spreadsheet, email, etc.) rather than specific products. The `.mcp.json` pre-configures specific MCP servers, but any MCP server in that category works.

## Connectors for this plugin

| Category | Placeholder | Included servers | Other options |
|----------|-------------|-----------------|---------------|
| Calendar | `~~calendar` | Google Calendar, Microsoft 365 | — |
| Chat | `~~chat` | Slack | Microsoft Teams |
| Document generation | `~~document` | Microsoft 365 (Word, PowerPoint) | Google Docs |
| Email | `~~email` | Gmail, Microsoft 365 | — |
| File storage | `~~file storage` | Google Drive | OneDrive, Dropbox, Box |
| Knowledge base | `~~knowledge base` | Notion, Atlassian (Confluence) | Guru, Coda |
| Project tracker | `~~project tracker` | Atlassian (Jira) | Linear, Asana, Monday.com |
| Spreadsheet | `~~spreadsheet` | Google Sheets, Microsoft 365 (Excel) | Smartsheet, Airtable |

## Connector details

### Knowledge Base (`~~knowledge base`)

Used to store and retrieve workforce planning documents, historical manpower data, project records, and PM reference information. The manpower-analytics skill queries the knowledge base for historical labor trends and project timelines when generating projections.

**What it enables:**
- Pull historical manpower data for trend analysis
- Access PM project records and labor plans
- Retrieve union labor classification references
- Store generated reports for future reference

### Spreadsheet (`~~spreadsheet`)

The primary data source for manpower analytics. PM excel sheets containing project timelines, labor requirements, and staffing plans are ingested through this connector.

**What it enables:**
- Direct access to PM excel/spreadsheet files
- Read project labor data without manual upload
- Write projection results back to shared workbooks
- Auto-refresh data for recurring reports

### Document Generation (`~~document`)

Used to produce formatted reports, schedule PDFs, and presentation-ready workforce planning documents.

**What it enables:**
- Generate formatted PDF schedule reports with Gantt charts
- Create polished manpower projection documents
- Build presentation slides for leadership briefings
- Produce printable schedule boards

### Email (`~~email`)

Send completed reports, share projections with stakeholders, and distribute schedule updates to project teams.

**What it enables:**
- Email manpower reports to leadership
- Distribute schedule PDFs to project teams
- Send staffing alerts to PMs
- Share weekly/monthly projection summaries

### File Storage (`~~file storage`)

Access project files stored in cloud drives, including PM spreadsheets, historical reports, and reference documents.

**What it enables:**
- Access PM spreadsheet files from shared drives
- Store generated reports in team folders
- Retrieve historical workforce data files
- Organize reports by project or period

### Chat (`~~chat`)

Share reports and alerts through team messaging platforms.

**What it enables:**
- Post staffing alerts to project channels
- Share schedule updates with teams
- Notify PMs of upcoming labor spikes
- Distribute weekly manpower summaries

### Calendar (`~~calendar`)

Track project milestones and coordinate scheduling with team availability.

**What it enables:**
- Align schedules with project milestones
- Check PM availability for resource planning
- Set reminders for report generation deadlines
- Coordinate mobilization dates

### Project Tracker (`~~project tracker`)

Connect to project management tools for task tracking and milestone management.

**What it enables:**
- Sync schedule tasks with project tracker
- Track project phase completion
- Link manpower needs to project milestones
- Monitor task dependencies across projects
