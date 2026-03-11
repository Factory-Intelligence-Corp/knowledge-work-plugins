# Connectors

## How tool references work

Plugin files use `~~category` as a placeholder for whatever tool the user connects in that category. For example, `~~knowledge base` might mean Notion, Confluence, or any other knowledge base with an MCP server.

Plugins are **tool-agnostic** — they describe workflows in terms of categories (knowledge base, email, document storage, etc.) rather than specific products. The `.mcp.json` pre-configures specific MCP servers, but any MCP server in that category works.

## Connectors for this plugin

| Category | Placeholder | Included servers | Other options |
|----------|-------------|-----------------|---------------|
| Knowledge base | `~~knowledge base` | Notion, Atlassian (Confluence) | Guru, Coda, Slite |
| Document storage | `~~document storage` | Google Drive, Microsoft 365 | Dropbox, Box, SharePoint |
| Email | `~~email` | Gmail, Microsoft 365 | — |
| Chat | `~~chat` | Slack | Microsoft Teams |
| Calendar | `~~calendar` | Google Calendar | Microsoft 365 |
| Project tracker | `~~project tracker` | Atlassian (Jira) | Linear, Asana, Monday.com |

## How connectors enhance field diagnostics

### Knowledge base (`~~knowledge base`)
- Store and retrieve equipment maintenance histories
- Access past diagnostic reports for trend analysis
- Maintain equipment inventories with nameplate data
- Reference site-specific single-line diagrams and panel schedules
- Store standard operating procedures for diagnostic workflows

### Document storage (`~~document storage`)
- Save generated diagnostic reports (PDF, HTML)
- Access report templates and company letterhead
- Store thermal images alongside IR reports
- Maintain a library of reference standards (IEEE, NFPA)
- Archive completed work orders and client deliverables

### Email (`~~email`)
- Send completed diagnostic reports to clients
- Distribute urgent findings to maintenance teams
- Forward critical IR findings with recommended immediate actions
- Send internal summaries to engineering staff for review

### Chat (`~~chat`)
- Notify team of critical findings in real-time
- Coordinate with on-site personnel during diagnostics
- Share preliminary results before formal report is complete
- Request peer review of complex diagnostic scenarios

### Calendar (`~~calendar`)
- Schedule follow-up inspections based on findings
- Book maintenance windows for corrective actions
- Set reminders for re-inspection of monitored conditions
- Coordinate multi-day diagnostic campaigns
