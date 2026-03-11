# Connectors

## How tool references work

Plugin files use `~~category` as a placeholder for whatever tool the user connects in that category. For example, `~~knowledge base` might mean Notion, Confluence, SharePoint, or any other knowledge management tool with an MCP server.

Plugins are **tool-agnostic** — they describe workflows in terms of categories (knowledge base, document storage, email, etc.) rather than specific products. The `.mcp.json` pre-configures specific MCP servers, but any MCP server in that category works.

## Connectors for this plugin

| Category | Placeholder | Included servers | Other options |
|----------|-------------|-----------------|---------------|
| Knowledge base | `~~knowledge base` | Notion, Atlassian (Confluence) | SharePoint, Guru, Coda |
| Document storage | `~~document storage` | Google Drive, Microsoft 365 (SharePoint/OneDrive) | Box, Dropbox |
| Email | `~~email` | Gmail, Microsoft 365 (Outlook) | — |
| Chat | `~~chat` | Slack | Microsoft Teams |
| Calendar | `~~calendar` | Google Calendar | Microsoft 365 (Outlook Calendar) |

## What each connector enables

### Knowledge Base (`~~knowledge base`)

Stores and retrieves safety documentation, past PSSPs, company policies, OSHA logs, incident history, and equipment data.

**Used by:**
- **safety-specialist**: Retrieves past safety procedures, company safety policies, incident history, equipment specifications, and regulatory interpretations specific to Huston Electric.
- **pssp-generator**: Pulls past PSSPs for similar project types, site-specific hazard data, company standard operating procedures, and historical risk assessments.

**Example data stored:**
- Completed PSSPs organized by project type and location
- OSHA 300 logs and incident records
- Equipment-specific LOTO procedures
- Arc flash study results and incident energy data
- Safety meeting minutes and training records
- Company safety manual and policies
- Subcontractor prequalification records

### Document Storage (`~~document storage`)

Stores generated safety documents, templates, completed forms, and training materials.

**Used by:**
- **safety-specialist**: Saves generated safety procedures, LOTO templates, PPE selection guides, and safety meeting materials. Retrieves equipment manuals and manufacturer safety data sheets.
- **pssp-generator**: Saves completed PSSPs, retrieves project specifications, site drawings, and client safety requirements.

**Example documents:**
- PSSP templates and completed plans
- LOTO procedure forms
- Arc flash warning labels
- Safety meeting presentation materials
- Training sign-in sheets
- Incident report forms
- JHA (Job Hazard Analysis) worksheets

### Email (`~~email`)

Sends safety communications, incident notifications, and training reminders.

**Used by:**
- **safety-specialist**: Distributes safety alerts, sends incident notifications to management, distributes safety meeting minutes, and sends training completion reminders.
- **pssp-generator**: Sends completed PSSPs to project managers, distributes safety plans to subcontractors, and notifies stakeholders of plan updates.

### Chat (`~~chat`)

Real-time safety team coordination and incident communication.

**Used by:**
- **safety-specialist**: Posts safety alerts to team channels, coordinates incident response, shares safety meeting reminders, and facilitates safety discussions.
- **pssp-generator**: Notifies project teams when PSSPs are ready for review, coordinates plan approvals, and shares updates.

### Calendar (`~~calendar`)

Schedules and tracks safety-related events.

**Used by:**
- **safety-specialist**: Schedules safety meetings, training sessions, safety inspections, equipment testing dates, and compliance audit reminders.
- **pssp-generator**: Schedules PSSP review meetings, tracks project safety milestones, and sets reminders for plan updates.
