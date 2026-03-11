# Connectors

## How tool references work

Plugin files use `~~category` as a placeholder for whatever tool the user connects in that category. For example, `~~knowledge base` might mean Notion, Confluence, or any other knowledge management tool with an MCP server.

Plugins are **tool-agnostic** — they describe workflows in terms of categories (knowledge base, document generation, file storage, etc.) rather than specific products. The `.mcp.json` pre-configures specific MCP servers, but any MCP server in that category works.

## Connectors for this plugin

| Category | Placeholder | Included servers | Other options |
|----------|-------------|-----------------|---------------|
| Knowledge base | `~~knowledge base` | Notion | Confluence, Guru, SharePoint Wiki |
| Document generation | `~~document generation` | Huston Doc Gen Service | Pandoc, LaTeX, Google Docs API |
| File storage | `~~file storage` | Microsoft 365 (SharePoint/OneDrive) | Google Drive, Box, Dropbox |
| Project tracker | `~~project tracker` | Procore, PlanGrid | Autodesk Build, Fieldwire, Buildertrend |

## Category details

### Knowledge base

Stores historical bid data, fixture libraries, pricing databases, company estimating standards, and past project records. Used by all three skills to reference Huston Electric's institutional knowledge.

**What it enables:**
- Historical apartment bid lookups for budget comparison
- Standard fixture type libraries with current pricing
- Company labor rate tables and productivity factors
- Specification interpretation guides and notes from past projects
- Standard bid checklist templates

### Document generation

Produces formatted PDF output for bid documents, budget reports, material takeoff sheets, and checklist reports. Converts the structured markdown output from skills into professional documents suitable for submission.

**What it enables:**
- Formatted PDF bid budget reports
- Printable material takeoff sheets
- Professional bid checklist documents
- Cover sheets and transmittals
- Comparison reports with charts and tables

### File storage

Provides direct access to project drawings, specifications, fixture schedules, and other construction documents stored in the company file system. Eliminates the need to manually upload files.

**What it enables:**
- Direct access to project drawing sets (floor plans, RCPs, electrical plans)
- Pull specification documents by section
- Retrieve fixture schedules and cut sheets
- Access addenda and drawing revisions
- Store completed estimates and reports back to project folders

### Project tracker

Connects to construction project management platforms for project context, RFI history, submittal logs, and drawing revision tracking.

**What it enables:**
- Current project status and phase information
- RFI history that may affect scope or pricing
- Submittal logs for approved fixtures and materials
- Drawing revision tracking to ensure estimates use latest documents
- Scope change tracking and change order history
