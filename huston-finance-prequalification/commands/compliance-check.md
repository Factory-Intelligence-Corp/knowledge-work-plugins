---
description: Run a compliance audit — check insurance expirations, license renewals, bonding capacity, safety record currency, and regulatory filing deadlines
argument-hint: "<category or 'all'>"
---

# /compliance-check

> If you see unfamiliar placeholders or need to check which tools are connected, see [CONNECTORS.md](../CONNECTORS.md).

Run a compliance audit across all tracked items — insurance policies, contractor licenses, bonding capacity, safety certifications, union agreements, and regulatory filings. Get a prioritized status report with upcoming deadlines, expired items, and recommended actions.

## Usage

```
/compliance-check [category]
```

Categories: `all` (default), `insurance`, `licenses`, `bonding`, `safety`, `union`, `regulatory`

Run compliance check: $ARGUMENTS

---

## How It Works

```
+------------------------------------------------------------------+
|                     COMPLIANCE CHECK                             |
+------------------------------------------------------------------+
|  STANDALONE (always works)                                       |
|  * Describe your policies, licenses, and deadlines               |
|  * Upload COIs, license copies, or compliance documents          |
|  * Get a status report with expiring and expired items           |
|  * Receive prioritized action items with renewal instructions    |
|  * Generate a compliance dashboard for management review         |
+------------------------------------------------------------------+
|  SUPERCHARGED (when you connect your tools)                      |
|  + Knowledge base: pull all compliance data automatically        |
|  + Document storage: retrieve COIs, licenses, bonding letters    |
|  + Calendar: check/set renewal reminders                         |
|  + Email: search for renewal notices from carriers/agencies      |
|  + Chat: alert team to critical expirations                      |
+------------------------------------------------------------------+
```

---

## What I Need From You

**Option 1: Full audit (recommended)**
Just type `/compliance-check` — if your knowledge base is connected, I pull everything automatically and generate a full report.

**Option 2: Category-specific check**
Specify a category: `/compliance-check insurance` or `/compliance-check safety`

**Option 3: Upload documents**
Upload your current COIs, license copies, bonding letters, or OSHA logs. I will parse expiration dates and coverage details to build the compliance tracker.

**Option 4: Describe your situation**
Tell me what you want to check: "Our GL renews in April and I want to make sure we start the process on time."

---

## Output

### Compliance Report

```markdown
# Compliance Report: Huston Electric, Inc.
**Generated:** [Date]
**Scope:** [All categories / Specific category]

---

## Executive Summary

**Overall Status:** [GREEN / YELLOW / RED]

| Metric | Value |
|--------|-------|
| Total tracked items | XX |
| Current and compliant | XX (XX%) |
| Action needed (expiring/expired) | XX (XX%) |
| Most urgent item | [Item] — [expires/expired date] |

---

## CRITICAL: Immediate Action Required

### Expired Items
| Item | Category | Expired On | Days Overdue | Impact | Action |
|------|----------|-----------|-------------|--------|--------|
| [Name] | [Cat] | [Date] | [X] | [What is affected] | [Steps to resolve] |

### Expiring Within 30 Days
| Item | Category | Expires On | Days Left | Action |
|------|----------|-----------|----------|--------|
| [Name] | [Cat] | [Date] | [X] | [Steps to start renewal] |

---

## WARNING: 31-60 Days

| Item | Category | Expires On | Days Left | Action |
|------|----------|-----------|----------|--------|
| [Name] | [Cat] | [Date] | [X] | [Begin renewal process] |

---

## UPCOMING: 61-90 Days

| Item | Category | Expires On | Days Left | Action |
|------|----------|-----------|----------|--------|
| [Name] | [Cat] | [Date] | [X] | [Plan renewal] |

---

## Current: No Action Needed

| Item | Category | Expires On | Days Left |
|------|----------|-----------|----------|
| [Name] | [Cat] | [Date] | [X] |
| ... | ... | ... | ... |

---

## Category Details

### Insurance
[Detailed status of each policy with limits, carriers, and expiration]

### Licenses
[Detailed status of each license with classifications and jurisdictions]

### Bonding
[Current capacity, backlog, available capacity, letter date]

### Safety
[EMR history, OSHA data currency, certification status]

### Union / Labor
[Agreement status, DIR registration, apprenticeship compliance]

### Regulatory Filings
[Filing status, upcoming deadlines, completed filings]

---

## Action Items

| Priority | Item | Owner | Deadline | Status |
|----------|------|-------|----------|--------|
| 1 | [Action] | [Person] | [Date] | [Not started / In progress] |
| 2 | [Action] | [Person] | [Date] | [Not started / In progress] |
| ... | ... | ... | ... | ... |

---

## GC/Owner Requirement Check

| GC / Owner | Requirement | Current Status | Compliant? |
|-----------|------------|---------------|-----------|
| [GC Name] | GL $1M/$2M | $1M/$2M | Yes |
| [GC Name] | EMR < 0.95 | 0.85 | Yes |
| [GC Name] | Umbrella $10M | $10M | Yes |
| ... | ... | ... | ... |

---

## Next Compliance Review

Recommended next full review: [Date — 30 days from now]
```

---

## If Connectors Available

**Knowledge base connected:**
- Pull all compliance records — policies, licenses, certifications, deadlines
- Compare current data against GC/owner minimum requirements
- Track historical compliance status over time

**Document storage connected:**
- Retrieve current COIs, license copies, bonding letters, OSHA filings
- Verify document dates match knowledge base records
- Flag documents that need to be updated after renewals

**Calendar connected:**
- Check existing renewal reminders
- Create missing reminders for items without calendar events
- Schedule follow-up checks for items in renewal process

**Email connected:**
- Search for recent renewal notices from carriers and agents
- Search for license renewal notices from state boards
- Draft renewal initiation emails to agents/brokers

**Chat connected:**
- Send critical alerts for expired items
- Post weekly compliance summary to designated channel
- Notify specific individuals of items they are responsible for

---

## Compliance Scoring

Each category receives a compliance score:

| Score | Meaning | Criteria |
|-------|---------|----------|
| **GREEN** | Fully compliant | All items current, nothing expiring within 60 days |
| **YELLOW** | Attention needed | Items expiring within 60 days, or minor gaps |
| **RED** | Critical action required | Expired items, lapsed coverage, or items expiring within 30 days |

**Overall score** is the lowest score across all categories — one RED category makes the overall status RED.

---

## Tips

1. **Run monthly** — A monthly compliance check catches issues before they become emergencies
2. **Connect your knowledge base** — Automatic data pull means the check takes seconds instead of hours
3. **Set calendar reminders** — Let the skill create renewal reminders so nothing slips through
4. **Check after renewals** — Run `/compliance-check insurance` after any policy renewal to verify the new data is captured
5. **Review before prequals** — Run `/compliance-check` before filling any prequal form to ensure all data is current
6. **Share the report** — The compliance dashboard is designed to be shared with management, CFO, and safety director
