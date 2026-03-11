# Huston Electric Financial Prequalification Plugin

A financial prequalification and compliance plugin designed for [Cowork](https://claude.com/product/cowork), Anthropic's agentic desktop application — though it also works in Claude Code. Automates the filling of prequalification PDF forms, manages company financial data, tracks compliance deadlines, and maintains prequalification documentation using past submissions and company knowledge bases. Built for Huston Electric, Inc.

## Installation

```bash
claude plugins add knowledge-work-plugins/huston-finance-prequalification
```

## Commands

Explicit workflows you invoke with a slash command:

| Command | Description |
|---|---|
| `/fill-prequal` | Fill a prequalification form — upload a PDF, auto-populate fields from company data, review, and generate completed form |
| `/compliance-check` | Run a compliance audit — check insurance expirations, license renewals, bonding capacity, and safety record currency |

All commands work **standalone** (upload forms, paste data, or describe your needs) and get **supercharged** with MCP connectors.

## Skills

Domain knowledge Claude uses automatically when relevant:

| Skill | Description |
|---|---|
| `prequal-form-filler` | Specialized finance assistant that automatically fills prequal PDF forms using company knowledge base, past submissions, and financial data — with approval workflow before submission |
| `financial-compliance` | Tracks ongoing compliance requirements — insurance renewals, license expirations, bonding updates, safety certifications, and regulatory deadlines |

## Example Workflows

### Filling a Prequalification Form

```
/fill-prequal
```

Upload a prequal PDF from a general contractor or project owner. The plugin identifies all form fields, matches them against Huston Electric's company knowledge base and past completed prequals, auto-fills matching fields with confidence scores, flags anything needing human review, and presents the completed form for approval before generating the final document.

### Running a Compliance Check

```
/compliance-check
```

Scans all tracked compliance items — insurance policies, contractor licenses, bonding capacity, EMR rates, OSHA logs, union certifications — and generates a status report with upcoming deadlines, expired items, and recommended actions.

### Prequalification Research

Just ask naturally:
```
I need to prequalify for a project with Turner Construction
```

The `prequal-form-filler` skill triggers automatically, researches Turner's typical prequal requirements, and prepares the relevant company data for submission.

### Compliance Monitoring

```
What insurance policies are expiring in the next 90 days?
```

The `financial-compliance` skill checks the knowledge base and returns a prioritized list of upcoming expirations with renewal instructions.

## Standalone + Supercharged

Every command and skill works without any integrations:

| What You Can Do | Standalone | Supercharged With |
|-----------------|------------|-------------------|
| Fill prequal forms | Upload PDF, paste form fields | Knowledge base MCP, Document storage MCP |
| Track compliance | Describe requirements, upload docs | Knowledge base MCP, Calendar MCP |
| Check insurance status | Paste policy details | Knowledge base MCP, Email MCP |
| Review past submissions | Upload previous prequals | Knowledge base MCP, Document storage MCP |
| Monitor deadlines | Describe dates manually | Calendar MCP, Email MCP, Chat MCP |
| Generate reports | Describe data | Knowledge base MCP, Document storage MCP |

## MCP Integrations

> If you see unfamiliar placeholders or need to check which tools are connected, see [CONNECTORS.md](CONNECTORS.md).

Connect your tools for a richer experience:

| Category | Examples | What It Enables |
|---|---|---|
| **Knowledge Base** | Notion, Confluence, SharePoint | Company data, past prequals, financial records, safety data |
| **Document Storage** | Google Drive, Dropbox, SharePoint | PDF form storage, completed submissions, insurance certificates |
| **Email** | Gmail, Outlook | Send completed forms, receive prequal requests, renewal notices |
| **Calendar** | Google Calendar, Outlook | Compliance deadlines, renewal reminders, submission due dates |
| **Chat** | Slack, Teams | Approval notifications, deadline alerts, team coordination |

See [CONNECTORS.md](CONNECTORS.md) for the full list of supported integrations.

## Settings

Create a local settings file at `huston-finance-prequalification/.claude/settings.local.json` to personalize:

```json
{
  "company": {
    "name": "Huston Electric, Inc.",
    "ein": "XX-XXXXXXX",
    "duns": "XXXXXXXXX",
    "cage_code": "XXXXX",
    "address": {
      "street": "123 Main Street",
      "city": "Your City",
      "state": "CA",
      "zip": "90001"
    },
    "phone": "(555) 555-5555",
    "website": "https://hustonelectric.com"
  },
  "financial": {
    "bonding_capacity_single": 25000000,
    "bonding_capacity_aggregate": 75000000,
    "annual_revenue": 50000000,
    "fiscal_year_end": "12/31"
  },
  "insurance": {
    "general_liability_limit": 2000000,
    "auto_liability_limit": 1000000,
    "umbrella_limit": 10000000,
    "workers_comp_limit": 1000000
  },
  "safety": {
    "current_emr": 0.85,
    "emr_year": 2025
  },
  "contacts": {
    "cfo": {
      "name": "CFO Name",
      "email": "cfo@hustonelectric.com",
      "phone": "(555) 555-5556"
    },
    "safety_director": {
      "name": "Safety Director Name",
      "email": "safety@hustonelectric.com"
    }
  },
  "approval_workflow": {
    "require_cfo_approval": true,
    "require_safety_review": true,
    "notify_on_completion": ["cfo@hustonelectric.com", "admin@hustonelectric.com"]
  }
}
```

The plugin will ask you for this information interactively if it is not configured.
