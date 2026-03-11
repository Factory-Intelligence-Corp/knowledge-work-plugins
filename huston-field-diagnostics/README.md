# Huston Field Diagnostics Plugin

A field diagnostics and testing plugin primarily designed for [Cowork](https://claude.com/product/cowork), Anthropic's agentic desktop application — though it also works in Claude Code. Provides power quality analysis, infrared scanning interpretation, and comprehensive field diagnostic methodology for electrical systems. Works standalone with your field data and measurements, supercharged when you connect your knowledge base, document generation, and communication tools.

## Installation

```bash
claude plugins add knowledge-work-plugins/huston-field-diagnostics
```

## Commands

Explicit workflows you invoke with a slash command:

| Command | Description |
|---|---|
| `/diagnose-power` | Run a power quality diagnostic — input symptoms and measurements, get root cause analysis, corrective actions, and a formal report |
| `/ir-report` | Generate an infrared scanning report — input thermal data or images, get severity classification, component analysis, and maintenance recommendations |

All commands work **standalone** (paste measurements, describe symptoms, or upload data files) and get **supercharged** with MCP connectors.

## Skills

Domain knowledge Claude uses automatically when relevant:

| Skill | Description |
|---|---|
| `power-quality` | Power quality diagnostic agent — voltage sags/swells, harmonics, transients, power factor, grounding issues, IEEE 519/1159 compliance |
| `ir-scanning` | Infrared scanning interpretation — thermal image analysis, severity classification, component identification, NFPA 70B compliance |

## Example Workflows

### Diagnosing a Power Quality Issue

```
/diagnose-power
```

Describe symptoms (equipment tripping, flickering lights, drive faults) or paste measurement data. Get a structured diagnostic report with root cause analysis, corrective actions with cost estimates, and priority rankings.

### After an IR Scan

```
/ir-report
```

Provide thermal data or describe findings from your infrared scan. Get a severity-classified report with temperature differentials, component identification, recommended actions, and NFPA 70B-compliant documentation.

### Investigating Equipment Failures

Just ask naturally:
```
We're seeing intermittent VFD faults on the 480V line at the Johnson Manufacturing site
```

The `power-quality` skill triggers automatically and walks you through a systematic diagnostic methodology — from initial assessment through root cause identification and remediation recommendations.

### Interpreting Thermal Findings

```
I found a 45-degree delta T on a breaker connection in MDP-1
```

The `ir-scanning` skill classifies the severity, identifies probable causes, and recommends immediate actions with appropriate urgency.

## Standalone + Supercharged

Every command and skill works without any integrations:

| What You Can Do | Standalone | Supercharged With |
|-----------------|------------|-------------------|
| Diagnose power quality | Describe symptoms, paste measurements | Knowledge base (historical data) |
| Generate diagnostic reports | Manual input of findings | Document generation MCP |
| Analyze IR scans | Describe thermal findings | Knowledge base (equipment records) |
| Create IR reports | Input temperature data | Document generation MCP |
| Track equipment history | Describe past issues | Knowledge base, project tracker |
| Communicate findings | Copy/paste output | Email, chat MCPs |

## MCP Integrations

> If you see unfamiliar placeholders or need to check which tools are connected, see [CONNECTORS.md](CONNECTORS.md).

Connect your tools for a richer experience:

| Category | Examples | What It Enables |
|---|---|---|
| **Knowledge base** | Notion, Confluence | Equipment records, historical diagnostics, maintenance logs |
| **Document storage** | Google Drive, Microsoft 365 | Report templates, past reports, reference documents |
| **Email** | Gmail, Microsoft 365 | Send reports to clients, internal distribution |
| **Chat** | Slack, Teams | Team coordination, urgent findings notification |
| **Calendar** | Google Calendar | Schedule follow-up inspections, maintenance windows |

See [CONNECTORS.md](CONNECTORS.md) for the full list of supported integrations.

## Settings

Create a local settings file at `huston-field-diagnostics/.claude/settings.local.json` to personalize:

```json
{
  "technician": {
    "name": "Your Name",
    "title": "Field Service Engineer",
    "certifications": ["Level II Thermographer", "NFPA 70E Qualified"],
    "license_number": "HE-XXXX"
  },
  "company": {
    "name": "Huston Electric, Inc.",
    "address": "Your Office Address",
    "phone": "Your Office Phone",
    "report_logo_path": "/path/to/logo.png"
  },
  "defaults": {
    "voltage_system": "480V 3-phase",
    "standards": ["IEEE 519", "IEEE 1159", "NFPA 70B"],
    "report_format": "pdf",
    "severity_thresholds": {
      "ir_minor_delta_t": 10,
      "ir_serious_delta_t": 30,
      "ir_critical_delta_t": 70,
      "thd_voltage_limit": 5.0,
      "thd_current_limit": 20.0
    }
  },
  "equipment": {
    "power_analyzer": "Fluke 1770 Series",
    "ir_camera": "FLIR T640",
    "clamp_meter": "Fluke 376 FC"
  }
}
```

The plugin will ask you for this information interactively if it's not configured.
