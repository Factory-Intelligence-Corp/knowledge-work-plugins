# Huston IT Support Plugin

An internal IT support plugin for Huston Electric, Inc. employees, designed for [Cowork](https://claude.com/product/cowork), Anthropic's agentic desktop application — though it also works in Claude Code. Provides first-line troubleshooting for Outlook, Jonas ERP, hardware, networking, VPN, and common software issues. Works standalone with built-in knowledge, supercharged when connected to your IT knowledge base, ticketing system, and internal chat.

## Installation

```bash
claude plugins add knowledge-work-plugins/huston-it-support
```

## Commands

Explicit workflows you invoke with a slash command:

| Command | Description |
|---|---|
| `/it-help` | Describe an IT issue and get step-by-step troubleshooting guidance |
| `/escalate` | Escalate an unresolved issue to the IT team with full context and diagnostic details |

All commands work **standalone** (describe your issue and get guidance) and get **supercharged** with MCP connectors.

## Skills

Domain knowledge Claude uses automatically when relevant:

| Skill | Description |
|---|---|
| `it-helpdesk` | General IT support — Outlook, email, VPN, printers, hardware, software, passwords, network connectivity |
| `jonas-portal` | Jonas Construction ERP support — navigation, time entry, project codes, reports, job costing, AP/AR |

## Example Workflows

### Outlook Won't Sync

```
/it-help
```

Describe your issue: "My Outlook keeps saying disconnected and won't sync new emails." Get a step-by-step troubleshooting guide covering network checks, profile repair, credential reset, and cached mode settings.

### Can't Log Into Jonas

```
/it-help
```

Just ask naturally:
```
I keep getting an error when I try to log into Jonas. It says my session expired.
```

The `jonas-portal` skill triggers automatically and walks you through session clearing, browser cache, and credential verification.

### Printer Not Working

```
My printer on the 2nd floor isn't printing. Jobs are stuck in the queue.
```

The `it-helpdesk` skill kicks in with driver troubleshooting, spooler restart instructions, and network printer verification steps.

### Need to Escalate

```
/escalate
```

When self-service troubleshooting doesn't resolve the issue, escalate with full context. The command gathers your issue description, steps already tried, error messages, and device info, then sends a properly formatted ticket to the IT team.

### Jonas Report Won't Run

```
How do I run the job cost detail report in Jonas for project 2024-0847?
```

The `jonas-portal` skill provides step-by-step navigation: module, menu path, filter setup, date ranges, and export options.

## Standalone + Supercharged

Every command and skill works without any integrations:

| What You Can Do | Standalone | Supercharged With |
|-----------------|------------|-------------------|
| Troubleshoot Outlook | Built-in guides | Knowledge base MCP |
| Fix printer issues | Step-by-step instructions | Knowledge base MCP |
| Navigate Jonas | Built-in ERP knowledge | Knowledge base MCP |
| Escalate to IT | Output ticket text to copy | Chat MCP (e.g. Slack/Teams) |
| Password reset guidance | Standard instructions | Knowledge base MCP |
| VPN troubleshooting | Common fixes | Knowledge base MCP |
| Software installation | General guidance | Knowledge base MCP |

## MCP Integrations

> If you see unfamiliar placeholders or need to check which tools are connected, see [CONNECTORS.md](CONNECTORS.md).

Connect your tools for a richer experience:

| Category | Examples | What It Enables |
|---|---|---|
| **Knowledge Base** | Notion, Confluence | IT documentation, instruction manuals, known issues database |
| **Chat** | Slack, Teams | Escalation to IT team channels, real-time support handoff |
| **Email** | Microsoft 365, Gmail | Send escalation emails, share resolution documentation |
| **Project Tracker** | Jira, Confluence | Create and track IT support tickets |

See [CONNECTORS.md](CONNECTORS.md) for the full list of supported integrations.

## Settings

Create a local settings file at `huston-it-support/.claude/settings.local.json` to personalize:

```json
{
  "employee": {
    "name": "Your Name",
    "department": "Your Department",
    "location": "Office Location (e.g., Main Office, Warehouse, Field)",
    "workstation": "Desktop / Laptop model if known"
  },
  "it_team": {
    "escalation_channel": "#it-support",
    "it_manager": "IT Manager Name",
    "helpdesk_email": "itsupport@hustonelectric.com"
  },
  "environment": {
    "domain": "hustonelectric.local",
    "vpn_provider": "Cisco AnyConnect",
    "email_platform": "Microsoft 365 / Outlook",
    "erp_system": "Jonas Construction",
    "antivirus": "Your AV product"
  }
}
```

The plugin will ask you for relevant information interactively if it is not configured.
