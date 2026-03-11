# Connectors

## How tool references work

Plugin files use `~~category` as a placeholder for whatever tool the user connects in that category. For example, `~~knowledge base` might mean a NECA manual database, a material pricing system, or any other knowledge base with an MCP server.

Plugins are **tool-agnostic** — they describe workflows in terms of categories (knowledge base, document generation, email, etc.) rather than specific products. The `.mcp.json` pre-configures specific MCP servers, but any MCP server in that category works.

## Connectors for this plugin

| Category | Placeholder | Included servers | Other options |
|----------|-------------|-----------------|---------------|
| Knowledge base (NECA manual) | `~~neca manual` | Huston Knowledge Base | Any document/PDF search MCP |
| Knowledge base (material pricing) | `~~material pricing` | Huston Knowledge Base | Supplier catalogs, distributor APIs |
| Knowledge base (past quotations) | `~~past quotations` | Huston Knowledge Base | File search, document store |
| Document generation | `~~document generation` | Huston Document Generation | Google Docs, Microsoft 365, PDF generators |
| Email | `~~email` | Gmail, Microsoft 365 | Any email MCP |
| CRM | `~~CRM` | Huston CRM | Salesforce, HubSpot, ServiceTitan, custom CRM |
| Project tracker | `~~project tracker` | — | ServiceTitan, Jira, Asana, custom job tracker |
