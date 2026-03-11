# Huston Estimating Plugin

An electrical estimating and drawing analysis plugin primarily designed for [Cowork](https://claude.com/product/cowork), Anthropic's agentic desktop application — though it also works in Claude Code. Built for Huston Electric, Inc. estimating teams to analyze construction drawings, count fixtures, fill bid checklists, and prepare apartment bid budgets. Works standalone with uploaded drawings and your input, supercharged when you connect your knowledge base, document generation, and file storage tools.

## Installation

```bash
claude plugins add knowledge-work-plugins/huston-estimating
```

## Commands

Explicit workflows you invoke with a slash command:

| Command | Description |
|---|---|
| `/analyze-drawing` | Analyze a floor plan, reflected ceiling plan, or site plan — count fixtures by room and type, cross-reference fixture schedules, generate material and labor estimates |
| `/bid-checklist` | Scan plans and specifications — systematically fill out a bid checklist, flag items needing estimator attention, verify scope coverage |
| `/apartment-budget` | Prepare an apartment bid budget — analyze historical data, apply regional adjustments, compare with past bids, generate PDF budget report |

All commands work **standalone** (upload drawings, paste specifications, or describe your project) and get **supercharged** with MCP connectors.

## Skills

Domain knowledge Claude uses automatically when relevant:

| Skill | Description |
|---|---|
| `drawing-analysis` | Edison the Electrical Estimator — analyze floor plans, reflected ceiling plans, and electrical drawings to count fixtures by room and type, cross-reference fixture schedules, and generate material/labor estimates |
| `bid-checklist` | Bid Checklist Filler — scan plans and specifications to systematically fill out a bid checklist, flag ambiguities, and verify scope coverage for estimators |
| `apartment-budget` | Apartment Bid Budget Analyst — prepare bid budgets using historical data, economic indicators, regional cost adjustments, and comparisons with past apartment bids |

## Example Workflows

### Analyzing a Drawing

```
/analyze-drawing
```

Upload a floor plan, reflected ceiling plan, or electrical drawing. Edison identifies every room, counts fixtures by type, cross-references the fixture schedule, and produces a complete material takeoff with labor hour estimates.

### Filling a Bid Checklist

```
/bid-checklist
```

Upload project plans and specifications. The checklist agent systematically reviews every section, fills in scope items, flags items that need estimator attention, and verifies nothing is missed.

### Preparing an Apartment Budget

```
/apartment-budget
```

Describe the apartment project (unit count, location, building type). The budget analyst pulls historical bid data, applies current material pricing and regional labor adjustments, and produces a detailed per-unit budget with comparison to past projects.

### Quick Fixture Count

Just ask naturally:
```
Count the light fixtures on this floor plan
```

The `drawing-analysis` skill triggers automatically and produces a room-by-room fixture count with totals by type.

### Reviewing Specifications

```
Check this spec against our standard bid checklist
```

The `bid-checklist` skill activates and systematically reviews the uploaded specification sections against Huston Electric's standard checklist categories.

### Budget Comparison

```
How does this 200-unit project compare to the Riverside Apartments bid?
```

The `apartment-budget` skill pulls historical data and generates a side-by-side comparison with variance analysis.

## Standalone + Supercharged

Every command and skill works without any integrations:

| What You Can Do | Standalone | Supercharged With |
|-----------------|------------|-------------------|
| Count fixtures from drawings | Upload drawing image/PDF | File Storage MCP (access project drawings) |
| Fill bid checklist | Upload plans and specs | Knowledge Base MCP (standard checklists) |
| Prepare apartment budget | Describe project, paste data | Knowledge Base MCP (historical bid data) |
| Generate bid documents | Markdown output, copy/paste | Document Generation MCP (formatted PDF) |
| Cross-reference fixture schedules | Upload schedule image | File Storage MCP (project documents) |
| Compare with past projects | Describe prior bids | Knowledge Base MCP (bid history database) |
| Track project status | Describe manually | Project Tracker MCP (Procore, PlanGrid) |

## MCP Integrations

> If you see unfamiliar placeholders or need to check which tools are connected, see [CONNECTORS.md](CONNECTORS.md).

Connect your tools for a richer experience:

| Category | Examples | What It Enables |
|---|---|---|
| **Knowledge Base** | Notion, Confluence | Historical bid data, fixture libraries, pricing databases, company standards |
| **Document Generation** | Internal doc gen service | Formatted PDF bid documents, budget reports, material takeoff sheets |
| **File Storage** | SharePoint, Google Drive, Box | Access project drawings, specifications, fixture schedules directly |
| **Project Tracker** | Procore, PlanGrid | Project details, RFIs, submittals, drawing revisions |

See [CONNECTORS.md](CONNECTORS.md) for the full list of supported integrations.

## Settings

Create a local settings file at `huston-estimating/.claude/settings.local.json` to personalize:

```json
{
  "company": {
    "name": "Huston Electric, Inc.",
    "region": "Southeast US",
    "laborRate": 85.00,
    "overheadMultiplier": 1.35,
    "profitMargin": 0.10
  },
  "estimating": {
    "defaultWageRate": 42.50,
    "burdenRate": 1.55,
    "materialMarkup": 0.10,
    "contingencyPercent": 0.05,
    "defaultFixtureLibrary": "huston-standard-2024"
  },
  "apartment": {
    "defaultCostPerUnit": {
      "studio": 3200,
      "oneBedroom": 4100,
      "twoBedroom": 5400,
      "threeBedroom": 6800
    },
    "historicalBidDatabase": "huston-apartment-bids"
  },
  "output": {
    "currency": "USD",
    "laborHourPrecision": 2,
    "includeTaxInEstimates": false,
    "defaultTaxRate": 0.07
  }
}
```

The plugin will ask you for this information interactively if it is not configured.
