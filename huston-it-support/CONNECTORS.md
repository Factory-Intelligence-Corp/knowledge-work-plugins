# Connectors

## How tool references work

Plugin files use `~~category` as a placeholder for whatever tool the user connects in that category. For example, `~~knowledge base` might mean Notion, Confluence, or any other documentation platform with an MCP server.

Plugins are **tool-agnostic** — they describe workflows in terms of categories (knowledge base, chat, email, etc.) rather than specific products. The `.mcp.json` pre-configures specific MCP servers, but any MCP server in that category works.

## Connectors for this plugin

| Category | Placeholder | Included servers | Other options |
|----------|-------------|-----------------|---------------|
| Knowledge base | `~~knowledge base` | Notion, Atlassian (Confluence) | Guru, Slite, Tettra |
| Chat | `~~chat` | Slack | Microsoft Teams |
| Email | `~~email` | Microsoft 365, Gmail | — |
| Project tracker | `~~project tracker` | Atlassian (Jira/Confluence) | Linear, Asana, ServiceNow |

## What each connector enables

### Knowledge Base (`~~knowledge base`)

The knowledge base connector is the most impactful integration for IT support. It gives the plugin access to:

- **IT documentation** — Setup guides, configuration standards, approved software lists
- **Instruction manuals** — Step-by-step procedures for common tasks (printer setup, VPN config, etc.)
- **Known issues database** — Previously resolved issues with their solutions
- **Jonas documentation** — ERP-specific guides, project code references, report instructions
- **Network diagrams** — Office layout, printer locations, access point maps
- **Onboarding checklists** — New employee IT setup procedures
- **Vendor contact info** — ISP, hardware warranty, software license contacts

Without this connector, the plugin uses built-in general IT knowledge. With it, the plugin can reference Huston Electric-specific documentation, configurations, and known issues.

### Chat (`~~chat`)

The chat connector enables real-time escalation:

- **Post escalation tickets** — Send formatted issue reports to the #it-support channel
- **Tag IT team members** — Mention the right person based on issue category
- **Share resolution notes** — Post solutions back to the channel for team visibility
- **Search prior discussions** — Find if someone else already solved this issue

### Email (`~~email`)

The email connector supports:

- **Send escalation emails** — Email the IT team with full diagnostic context
- **Share how-to guides** — Email resolution steps to the employee for future reference
- **Forward error screenshots** — Attach relevant information to escalation emails
- **Search IT communications** — Find prior IT announcements about outages, updates, or changes

### Project Tracker (`~~project tracker`)

The project tracker connector enables formal ticket management:

- **Create support tickets** — Log issues in Jira or your ticketing system
- **Track ticket status** — Check on open IT requests
- **Link related issues** — Connect similar problems for pattern detection
- **Update tickets** — Add notes, change status, assign priority
