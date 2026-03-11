# Connectors

## How tool references work

Plugin files use `~~category` as a placeholder for whatever tool the user connects in that category. For example, `~~knowledge base` might mean Notion, SharePoint, Confluence, or any other knowledge base with an MCP server.

Plugins are **tool-agnostic** — they describe workflows in terms of categories (knowledge base, email, document storage, etc.) rather than specific products. The `.mcp.json` pre-configures specific MCP servers, but any MCP server in that category works.

## Connectors for this plugin

| Category | Placeholder | Included servers | Other options |
|----------|-------------|-----------------|---------------|
| Knowledge base | `~~knowledge base` | Notion, Atlassian (Confluence) | SharePoint, Guru, Coda |
| Document storage | `~~document storage` | Google Drive, Dropbox, Microsoft 365 (SharePoint/OneDrive) | Box, Egnyte |
| Email | `~~email` | Gmail, Microsoft 365 (Outlook) | -- |
| Calendar | `~~calendar` | Google Calendar, Microsoft 365 | -- |
| Chat | `~~chat` | Slack | Microsoft Teams |
| Document generation | `~~document generation` | Microsoft 365 | Google Workspace |
| Project tracker | `~~project tracker` | Atlassian (Jira) | Asana, Monday.com |

## Connector details

### Knowledge Base (`~~knowledge base`)

The knowledge base is the core connector for this plugin. It stores:

- **Company profile data** — Legal name, EIN, DUNS, CAGE code, addresses, officers, organizational structure
- **Financial records** — Annual revenue, balance sheets, income statements, bonding capacity letters
- **Past prequal submissions** — Previously completed prequalification forms with field mappings
- **Insurance certificates** — Current COIs, policy numbers, limits, expiration dates, carrier information
- **Safety records** — EMR history, OSHA 300/300A logs, DART rates, incident reports, safety programs
- **Licenses and certifications** — State contractor licenses, electrical licenses, specialty certifications
- **Project history** — Completed projects with values, owners, references, completion dates
- **Key personnel** — Resumes, certifications, years of experience, roles
- **Union affiliations** — Local union numbers, agreements, apprenticeship programs
- **Equipment lists** — Major equipment, fleet details, specialized tools

### Document Storage (`~~document storage`)

Stores and retrieves PDF forms, completed submissions, and supporting documentation:

- Incoming prequal form PDFs
- Completed and signed submissions
- Insurance certificates of insurance (COIs)
- Bonding capacity letters
- Financial statements
- W-9 forms
- Safety program documents

### Email (`~~email`)

Enables sending and receiving prequalification-related communications:

- Receive prequal form requests from GCs and project owners
- Send completed prequal packages
- Track submission confirmations
- Receive renewal and expiration notices from carriers

### Calendar (`~~calendar`)

Tracks compliance and submission deadlines:

- Insurance policy expiration dates
- License renewal deadlines
- Prequal submission due dates
- Annual safety reporting deadlines
- Bonding capacity review dates
- Financial statement preparation deadlines

### Chat (`~~chat`)

Team communication and approval workflows:

- Notify approvers when prequal forms are ready for review
- Alert team to upcoming compliance deadlines
- Coordinate document collection from multiple departments
- Share submission status updates
