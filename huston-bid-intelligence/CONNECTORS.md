# Connectors

## How tool references work

Plugin files use `~~category` as a placeholder for whatever tool the user connects in that category. For example, `~~email` might mean Gmail, Outlook, or any other email client with an MCP server.

Plugins are **tool-agnostic** — they describe workflows in terms of categories (email, spreadsheet, knowledge base, etc.) rather than specific products. The `.mcp.json` pre-configures specific MCP servers, but any MCP server in that category works.

## Connectors for this plugin

| Category | Placeholder | Included servers | Other options |
|----------|-------------|-----------------|---------------|
| Calendar | `~~calendar` | Google Calendar, Microsoft 365 | — |
| Chat | `~~chat` | Slack | Microsoft Teams |
| Email | `~~email` | Gmail, Microsoft 365 | — |
| File storage | `~~file storage` | Google Drive | OneDrive, Dropbox, Box |
| Knowledge base | `~~knowledge base` | Notion | Confluence, Guru, SharePoint |
| Project tracker | `~~project tracker` | Atlassian (Jira/Confluence) | Linear, Asana, Monday.com |
| Spreadsheet | `~~spreadsheet` | Google Sheets, Microsoft 365 | — |

## Connector details

### Email (`~~email`)
The primary input channel for bid intelligence. Bid invitations, plan room notifications, addenda alerts, and GC correspondence all arrive via email. When connected, the plugin can automatically scan for new bid-related emails, extract structured data, and flag urgent deadlines.

**What it enables:**
- Auto-detect bid invitation emails by sender patterns and subject lines
- Pull email body content for structured parsing
- Monitor for addenda and bid date changes
- Track correspondence history with GCs and owners

### Spreadsheet (`~~spreadsheet`)
The primary output channel. The Tuesday strategy meeting report is an Excel-format spreadsheet organized by union local territory. When connected, the plugin can create and update tracking spreadsheets directly.

**What it enables:**
- Generate formatted Excel reports with columns, headers, and conditional formatting
- Update existing bid tracking spreadsheets with new opportunities
- Maintain historical bid log with outcomes
- Create pivot-ready data for win rate analysis

### Knowledge Base (`~~knowledge base`)
Stores institutional knowledge that makes bid decisions smarter over time. Historical bid results, GC relationship notes, project lessons learned, and subcontractor performance data all live here.

**What it enables:**
- Look up historical win/loss data against specific GCs
- Reference past project performance in similar scope
- Access estimating notes and lessons learned
- Pull contractor and subcontractor relationship history

### Chat (`~~chat`)
Enables real-time bid alerts and team coordination. When a high-priority bid comes in or a deadline changes, the team needs to know immediately.

**What it enables:**
- Send bid alerts to estimating team channel
- Distribute Tuesday meeting report summaries
- Coordinate pre-bid meeting attendance
- Share addenda notifications

### Calendar (`~~calendar`)
Tracks all time-sensitive bid activities. Bid due dates, pre-bid conferences, site visits, and the Tuesday strategy meeting itself.

**What it enables:**
- Auto-create calendar events for bid due dates
- Schedule pre-bid meeting attendance
- Block estimator time for bid preparation
- Track Tuesday strategy meeting cadence

### File Storage (`~~file storage`)
Houses bid documents, plans, specifications, and addenda. When connected, the plugin can reference plan documents for scope assessment.

**What it enables:**
- Access uploaded plans and specifications
- Store and organize bid documents by project
- Reference addenda for scope changes
- Archive bid packages for historical reference
