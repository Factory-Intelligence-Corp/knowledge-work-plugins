# Huston Safety Plugin

An electrical safety compliance and documentation plugin primarily designed for [Cowork](https://claude.com/product/cowork), Anthropic's agentic desktop application — though it also works in Claude Code. Helps Huston Electric, Inc. safety personnel create safety procedures, generate Project-Specific Safety Plans (PSSPs), perform hazard analysis, ensure OSHA/NFPA compliance, and manage workplace safety documentation. Works standalone with user input and web research, supercharged when you connect your knowledge base, document storage, and communication tools.

## Installation

```bash
claude plugins add knowledge-work-plugins/huston-safety
```

## Commands

Explicit workflows you invoke with a slash command:

| Command | Description |
|---|---|
| `/safety-procedure` | Generate a safety procedure document — LOTO procedures, arc flash protocols, PPE selection guides, emergency response plans |
| `/generate-pssp` | Create a complete Project-Specific Safety Plan — site-specific hazards, risk assessment, control measures, emergency procedures |

All commands work **standalone** (describe your project, paste specifications, or upload site documents) and get **supercharged** with MCP connectors.

## Skills

Domain knowledge Claude uses automatically when relevant:

| Skill | Description |
|---|---|
| `safety-specialist` | Sparky the Safety Specialist — electrical safety procedures, OSHA compliance, NFPA 70E, arc flash analysis, LOTO, PPE, safety meetings, incident reports |
| `pssp-generator` | PSSP Pete — autonomous Project-Specific Safety Plan generator with hazard analysis, risk assessment, regulatory mapping, and complete formatted output |

## Example Workflows

### Creating a Safety Procedure

```
/safety-procedure
```

Describe the task or equipment. Get a complete safety procedure with hazard identification, required PPE, step-by-step instructions, and emergency response. References OSHA 29 CFR 1910 Subpart S, NFPA 70E, and NEC requirements.

### Generating a PSSP

```
/generate-pssp
```

Provide project details (location, scope, voltage levels, duration). Get a complete Project-Specific Safety Plan with site-specific hazards, risk assessment matrix, control measures hierarchy, emergency procedures, training requirements, and signature pages.

### Safety Meeting Preparation

Just ask naturally:
```
Prepare a safety meeting on arc flash hazards for next Tuesday
```

The `safety-specialist` skill triggers automatically and generates a complete safety meeting agenda with talking points, regulatory references, and discussion questions.

### Incident Report Assistance

```
Help me document a near-miss incident involving exposed conductors on the 3rd floor
```

The `safety-specialist` skill provides a structured incident report template with root cause analysis, corrective actions, and follow-up requirements.

### Reviewing Compliance

```
What PPE is required for working on a 480V switchgear?
```

The `safety-specialist` skill references NFPA 70E tables, arc flash boundary calculations, and PPE category requirements to provide a complete answer.

## Standalone + Supercharged

Every command and skill works without any integrations:

| What You Can Do | Standalone | Supercharged With |
|-----------------|------------|-------------------|
| Generate safety procedures | Describe the task/equipment | Knowledge base (past procedures, company standards) |
| Create PSSPs | Provide project details | Knowledge base (past PSSPs, site data), Document storage |
| Arc flash analysis | Provide system parameters | Knowledge base (equipment data, incident energy studies) |
| Safety meeting content | Describe topics | Knowledge base (past meetings, incident history) |
| Incident reports | Describe the incident | Knowledge base (prior incidents), Email (notifications) |
| LOTO procedures | Describe equipment | Knowledge base (equipment manuals, energy source data) |
| Compliance checks | Ask your question | Knowledge base (company policies, audit history) |

## MCP Integrations

> If you see unfamiliar placeholders or need to check which tools are connected, see [CONNECTORS.md](CONNECTORS.md).

Connect your tools for a richer experience:

| Category | Examples | What It Enables |
|---|---|---|
| **Knowledge Base** | Notion, Confluence, SharePoint | Past PSSPs, safety procedures, OSHA logs, incident history, company safety policies |
| **Document Storage** | Google Drive, SharePoint | Safety document templates, completed PSSPs, equipment manuals, training records |
| **Email** | Gmail, Outlook | Safety alert distribution, incident notifications, training reminders |
| **Chat** | Slack, Teams | Safety team coordination, real-time incident communication |
| **Calendar** | Google Calendar, Outlook | Safety meeting scheduling, training session tracking, inspection reminders |

See [CONNECTORS.md](CONNECTORS.md) for the full list of supported integrations.

## Settings

Create a local settings file at `huston-safety/.claude/settings.local.json` to personalize:

```json
{
  "company": {
    "name": "Huston Electric, Inc.",
    "address": "Your Company Address",
    "phone": "Your Company Phone",
    "emergency_phone": "Your Emergency Contact Number"
  },
  "safety_director": {
    "name": "Safety Director Name",
    "title": "Director of Safety",
    "email": "safety@hustonelectric.com",
    "certifications": ["CSP", "CHST", "OSHA 500"]
  },
  "defaults": {
    "osha_region": "Region IV",
    "state_plan": "Federal OSHA",
    "nfpa_70e_edition": "2024",
    "nec_edition": "2023",
    "arc_flash_standard": "IEEE 1584-2018"
  },
  "ppe_suppliers": {
    "primary": "Supplier Name",
    "account_number": "ACCT-XXXXX"
  },
  "emergency_contacts": {
    "ambulance": "911",
    "fire": "911",
    "poison_control": "1-800-222-1222",
    "utility_emergency": "Local Utility Emergency Number"
  }
}
```

The plugin will ask you for this information interactively if it is not configured.

## Regulatory References

This plugin references the following standards and regulations:

| Standard | Description |
|---|---|
| **OSHA 29 CFR 1910 Subpart S** | Electrical safety standards for general industry |
| **OSHA 29 CFR 1926 Subpart K** | Electrical safety standards for construction |
| **NFPA 70E** | Standard for Electrical Safety in the Workplace |
| **NFPA 70 (NEC)** | National Electrical Code |
| **IEEE 1584** | Guide for Performing Arc-Flash Hazard Calculations |
| **ANSI Z535** | Safety signs and colors |
| **ANSI/ISEA 125** | Conformity assessment for safety and personal protective equipment |

> **Disclaimer:** This plugin assists with safety documentation and compliance guidance. It does not replace the judgment of qualified safety professionals. All safety plans and procedures should be reviewed and approved by a competent person before implementation.
