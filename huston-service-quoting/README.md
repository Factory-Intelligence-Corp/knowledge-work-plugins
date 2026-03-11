# Huston Service Quoting Plugin

A service quotation and proposal plugin primarily designed for [Cowork](https://claude.com/product/cowork), Anthropic's agentic desktop application — though it also works in Claude Code. Creates professional electrical service quotations, sign quotations, generator quotations, IR scan quotations, EMP proposals, and contracts for Huston Electric, Inc. Works standalone with your input and NECA labor standards, supercharged when you connect your knowledge base, CRM, and document generation tools.

## Installation

```bash
claude plugins add knowledge-work-plugins/huston-service-quoting
```

## Commands

Explicit workflows you invoke with a slash command:

| Command | Description |
|---|---|
| `/quote-electrical` | Generate a full electrical service quotation — scope of work, NECA labor, materials, markups, terms |
| `/quote-sign` | Generate a sign installation or maintenance quotation — travel time, lift equipment, sign-specific labor |
| `/quote-generator` | Generate a generator installation or service quotation — budgetary or firm pricing |
| `/quote-ir-scan` | Generate an infrared scanning service quotation — panel count, equipment list, report format |
| `/quote-emp` | Generate an Electrical Maintenance Program proposal — recurring service, budgetary planning |
| `/generate-contract` | Produce a one-time service contract with scope, pricing, signature blocks, and legal terms |

All commands work **standalone** (describe the job, enter quantities, or paste scope notes) and get **supercharged** with MCP connectors.

## Skills

Domain knowledge Claude uses automatically when relevant:

| Skill | Description |
|---|---|
| `electrical-quotation` | Full electrical service quotation — NECA labor units, material pricing, markup calculations, NEC compliance notes |
| `sign-quotation` | Sign installation and maintenance quotation — travel time, lift rental, sign-specific labor and materials |
| `generator-quotation` | Generator installation and service quotation — sizing, transfer switch, budgetary and firm pricing |
| `ir-scan-quotation` | Infrared scanning service quotation — thermal imaging, panel surveys, report generation |
| `emp-proposal` | Electrical Maintenance Program proposal — recurring service plans, budgetary forecasting, preventive maintenance |
| `contract-generation` | One-time service contract — scope, pricing, terms, signature blocks, legal language |
| `indy-quotation` | Indianapolis-specific quotation — standardized $92/hr labor, 40% markup, customer proposal and internal pricing breakdown |

## Example Workflows

### Quoting an Electrical Service Job

```
/quote-electrical
```

Describe the work (e.g., "200A panel upgrade for commercial office at 123 Main St") or paste a scope of work. Get a complete quotation with NECA labor calculations, material costs, markups, tax, and professional terms and conditions.

### Quoting a Sign Installation

```
/quote-sign
```

Describe the sign job (e.g., "Install two channel letter signs at new retail location, 45 minutes from shop"). Get a quotation including travel time, lift equipment, sign-specific labor, and materials.

### Generating a Generator Quote

```
/quote-generator
```

Describe the generator need (e.g., "22kW Generac whole-house generator with 200A automatic transfer switch"). Get a budgetary or firm quotation with installation labor, equipment, and permitting notes.

### IR Scan Service

```
/quote-ir-scan
```

Describe the facility (e.g., "Annual IR scan of 12 electrical panels at manufacturing plant"). Get a quotation for thermal imaging services including report deliverables.

### Creating a Maintenance Program

```
/quote-emp
```

Describe the facility and needs (e.g., "Quarterly maintenance for 50,000 sq ft office building, 8 panels, emergency lighting, generator"). Get a comprehensive EMP proposal with annual budgeting.

### Generating a Service Contract

```
/generate-contract
```

Provide the quotation details or reference a previous quote. Get a professional contract with scope, pricing schedule, terms, warranty, and signature blocks.

## Standalone + Supercharged

Every command and skill works without any integrations:

| What You Can Do | Standalone | Supercharged With |
|-----------------|------------|-------------------|
| Build electrical quotation | Describe scope, enter quantities | Knowledge Base MCP (NECA manual, past quotes) |
| Price materials | Enter costs manually or use estimates | Knowledge Base MCP (material pricing database) |
| Generate PDF quotation | Output formatted text | Document Generation MCP |
| Send quotation to customer | Copy and paste | Email MCP |
| Track quotation status | Manual notes | CRM MCP |
| Reference past quotes | Describe previous work | Knowledge Base MCP (past quotations) |
| Generate contracts | Describe terms | Document Generation MCP |

## MCP Integrations

> If you see unfamiliar placeholders or need to check which tools are connected, see [CONNECTORS.md](CONNECTORS.md).

Connect your tools for a richer experience:

| Category | Examples | What It Enables |
|---|---|---|
| **Knowledge Base** | NECA Manual, Material DB, Past Quotes | NECA labor unit lookups, real-time material pricing, past quotation reference |
| **Document Generation** | PDF/Word generator | Professional PDF quotations, contracts, proposals with company branding |
| **Email** | Gmail, Microsoft 365 | Send quotations directly to customers, track delivery |
| **CRM** | Customer database | Customer history, contact info, job records, quotation tracking |
| **Project Tracker** | Job management system | Link quotations to projects, track conversion rates |

See [CONNECTORS.md](CONNECTORS.md) for the full list of supported integrations.

## Settings

Create a local settings file at `huston-service-quoting/.claude/settings.local.json` to personalize:

```json
{
  "company": {
    "name": "Huston Electric, Inc.",
    "address": "Your Address Here",
    "city": "Indianapolis",
    "state": "IN",
    "zip": "46000",
    "phone": "(317) 555-0100",
    "email": "service@hustonelectric.com",
    "license": "Your License Number",
    "website": "www.hustonelectric.com"
  },
  "labor": {
    "standard_rate": 92,
    "overtime_rate": 138,
    "emergency_rate": 184,
    "apprentice_rate": 65,
    "helper_rate": 50
  },
  "markup": {
    "material_markup_pct": 40,
    "subcontractor_markup_pct": 15,
    "equipment_rental_markup_pct": 15
  },
  "tax": {
    "sales_tax_pct": 7,
    "tax_on_labor": false,
    "tax_on_materials": true
  },
  "quotation": {
    "validity_days": 30,
    "payment_terms": "Net 30",
    "warranty_years": 1,
    "default_neca_edition": "2024"
  },
  "estimators": [
    {
      "name": "Your Name",
      "title": "Service Manager",
      "email": "name@hustonelectric.com",
      "phone": "(317) 555-0101"
    }
  ]
}
```

The plugin will ask you for this information interactively if it is not configured.
