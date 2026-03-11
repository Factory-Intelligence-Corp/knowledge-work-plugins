---
name: financial-compliance
description: Track ongoing financial compliance requirements for Huston Electric, Inc. — insurance renewals, license expirations, bonding capacity updates, safety certifications, and regulatory deadlines. Proactively alerts on upcoming deadlines, expired items, and gaps in coverage. Trigger with "compliance check", "what's expiring", "insurance status", "license renewals", "bonding update", "are we compliant", or "compliance dashboard".
---

# Financial Compliance Tracking

Manage ongoing compliance requirements for Huston Electric, Inc. Tracks insurance policies, contractor licenses, bonding capacity, safety certifications, union agreements, and regulatory filings. Proactively surfaces upcoming deadlines, flags expired items, and recommends corrective actions.

---

## How It Works

```
+------------------------------------------------------------------+
|                  FINANCIAL COMPLIANCE TRACKER                     |
+------------------------------------------------------------------+
|  ALWAYS (works standalone)                                       |
|  * You describe: current policies, licenses, certifications      |
|  * Deadline tracking: flag items expiring in 30/60/90 days       |
|  * Gap analysis: identify missing or lapsed coverage             |
|  * Renewal checklist: step-by-step renewal instructions          |
|  * Compliance report: summary of all tracked items with status   |
+------------------------------------------------------------------+
|  SUPERCHARGED (when you connect your tools)                      |
|  + Knowledge base: pull all compliance data automatically        |
|  + Document storage: retrieve current COIs, licenses, letters    |
|  + Calendar: set renewal reminders, track filing deadlines       |
|  + Email: monitor renewal notices from carriers/agencies         |
|  + Chat: alert team to upcoming expirations and action items     |
+------------------------------------------------------------------+
```

---

## Connectors (Optional)

| Connector | What It Adds |
|-----------|--------------|
| **Knowledge base** | All compliance records — policies, licenses, certifications, safety data, deadlines |
| **Document storage** | Current and historical COIs, license copies, bonding letters, OSHA filings |
| **Calendar** | Automatic renewal reminders, filing deadline events, review meeting scheduling |
| **Email** | Incoming renewal notices from carriers, outgoing renewal requests to agents |
| **Chat** | Deadline alerts, approval requests, team notifications for lapsed items |

> **No connectors?** No problem. Describe your current policies and deadlines, or upload documents. The skill tracks everything you provide.

---

## What This Skill Tracks

### 1. Insurance Policies

| Policy Type | Key Data Tracked |
|------------|-----------------|
| General Liability | Carrier, policy #, limits (occurrence/aggregate), expiration, additional insured endorsements |
| Automobile Liability | Carrier, policy #, combined single limit, hired/non-owned, expiration |
| Umbrella / Excess | Carrier, policy #, limit, expiration, underlying policies |
| Workers Compensation | Carrier, policy #, statutory limits, employers liability, expiration |
| Professional Liability (E&O) | Carrier, policy #, limit, expiration, retroactive date |
| Pollution Liability | Carrier, policy #, limit, expiration |
| Builders Risk | Carrier, policy #, limit, per-project or blanket |
| Inland Marine / Equipment | Carrier, policy #, scheduled equipment, limit |
| Cyber Liability | Carrier, policy #, limit, expiration |

**Tracked attributes per policy:**
- Carrier name and AM Best rating
- Policy number
- Coverage limits (per occurrence, aggregate, deductible)
- Effective date and expiration date
- Agent/broker name and contact
- Premium amount and payment schedule
- Endorsements available (additional insured, waiver of subrogation, primary/non-contributory)
- Renewal status (active, renewal in progress, expired, cancelled)

### 2. Contractor Licenses

| License Type | Key Data Tracked |
|-------------|-----------------|
| State contractor license (C-10 Electrical) | License #, state, classification, expiration, bond requirement |
| State contractor license (other classifications) | Same fields per classification |
| City/county business licenses | Jurisdiction, license #, expiration |
| Specialty licenses | Type, issuing body, license #, expiration |
| Electrical certifications | Journeyman, master electrician, by state |

**Tracked attributes per license:**
- License number
- Issuing authority (state, county, city)
- Classification or type
- Issue date and expiration date
- Renewal requirements (CEUs, fees, bond)
- Status (active, pending renewal, expired, suspended)
- States/jurisdictions covered
- Qualifying individual (RME/RMO name)
- Bond requirements associated with the license

### 3. Bonding

| Item | Key Data Tracked |
|------|-----------------|
| Bonding capacity letter | Single project limit, aggregate limit, issue date, expiration |
| Current bonded backlog | Total bonded amount across active projects |
| Available capacity | Aggregate limit minus current backlog |
| Individual project bonds | Project name, bond amount, bond #, obligee, status |
| Bid bonds outstanding | Project name, bid amount, bid date, status |

**Renewal triggers:**
- Bonding letter older than 12 months
- Backlog approaching aggregate capacity (>80%)
- Financial statements older than fiscal year end + 120 days
- Surety company requests updated financials

### 4. Safety Certifications and Records

| Item | Key Data Tracked |
|------|-----------------|
| EMR (Experience Modification Rate) | Current and 3-year history, NCCI letter date |
| OSHA 300A Summary | Annual posting requirement (Feb 1 - Apr 30), recordable incidents, hours worked |
| OSHA 300 Log | Ongoing incident log, retention period (5 years) |
| TRIR (Total Recordable Incident Rate) | Calculated annually and rolling 3-year |
| DART Rate | Days Away, Restricted, or Transferred — calculated annually |
| Safety program documentation | Written safety program, last review date |
| Drug testing program | Program type, MRO name, collection site, last audit |
| OSHA 10/30 certifications | Employee certifications, expiration tracking |
| First aid/CPR certifications | Employee certifications, expiration dates |
| Confined space certifications | Employee certifications, expiration dates |
| Arc flash / NFPA 70E training | Employee certifications, renewal dates |

### 5. Union and Labor Compliance

| Item | Key Data Tracked |
|------|-----------------|
| Collective bargaining agreements | Union local, agreement dates, expiration |
| Apprenticeship program | JATC affiliation, active apprentices, ratio compliance |
| Prevailing wage certifications | Certified payroll requirements, DIR registration |
| DIR registration | Registration #, expiration, public works eligibility |
| Fringe benefit payments | Fund names, payment schedule, current status |

### 6. Regulatory Filings

| Filing | Frequency | Deadline |
|--------|-----------|----------|
| OSHA 300A posting | Annual | Feb 1 - Apr 30 |
| OSHA 300A electronic submission | Annual | March 2 |
| EEO-1 Report | Annual | Varies (typically March-April) |
| State contractor license renewal | Biennial | Varies by state |
| DIR registration renewal | Annual | Anniversary date |
| Business license renewals | Annual | Varies by jurisdiction |
| Workers comp audit | Annual | 60 days after policy expiration |
| Financial statement preparation | Annual | Within 120 days of fiscal year end |
| Tax filings (federal/state) | Annual/Quarterly | Various |

---

## Compliance Dashboard Output

```markdown
# Compliance Dashboard: Huston Electric, Inc.
**Generated:** [Date]
**Period:** [Current quarter/year]

---

## Status Summary

| Category | Total Items | Current | Expiring (90 days) | Expired | Action Needed |
|----------|------------|---------|--------------------|---------|--------------:|
| Insurance | 8 | 6 | 2 | 0 | 2 |
| Licenses | 5 | 4 | 0 | 1 | 1 |
| Bonding | 3 | 2 | 1 | 0 | 1 |
| Safety Certs | 12 | 10 | 1 | 1 | 2 |
| Union/Labor | 4 | 4 | 0 | 0 | 0 |
| Regulatory | 6 | 5 | 1 | 0 | 1 |
| **TOTAL** | **38** | **31** | **5** | **2** | **7** |

---

## CRITICAL: Immediate Action Required

### EXPIRED
| Item | Expired On | Days Overdue | Action |
|------|-----------|-------------|--------|
| [Item name] | [Date] | [X days] | [Renewal steps] |

### EXPIRING IN 30 DAYS
| Item | Expires On | Days Remaining | Action |
|------|-----------|---------------|--------|
| [Item name] | [Date] | [X days] | [Renewal steps] |

---

## UPCOMING: 31-90 Days

| Item | Expires On | Days Remaining | Action |
|------|-----------|---------------|--------|
| [Item name] | [Date] | [X days] | [Start renewal process] |

---

## ALL CURRENT: No Action Needed

| Item | Category | Expires On | Days Remaining |
|------|----------|-----------|---------------|
| [Item name] | Insurance | [Date] | [X days] |
| ... | ... | ... | ... |
```

---

## Execution Flow

### Step 1: Gather Compliance Data

**If connectors available:**
```
1. Knowledge base -> Query all compliance records
   - Insurance policies and expiration dates
   - License records and renewal dates
   - Bonding capacity and backlog
   - Safety certifications and training records
   - Union agreements and filing deadlines

2. Document storage -> Retrieve current documents
   - Latest COIs for each policy
   - License copies
   - Bonding capacity letter
   - OSHA logs and 300A summaries
   - NCCI EMR letter

3. Calendar -> Pull compliance-related events
   - Upcoming renewal dates
   - Filing deadlines
   - Audit dates
   - Training expiration dates

4. Email -> Search for renewal notices
   - Query: "renewal" OR "expiration" OR "policy" (last 60 days)
   - Extract: upcoming expirations, premium notices, action required
```

**If no connectors:**
```
1. Ask user:
   - "What compliance items do you want to track?"
   - "Upload any current COIs, licenses, or other documents"
   - "What are your upcoming deadlines?"

2. Check settings.local.json for stored compliance data
3. Accept whatever they provide and build the tracker
```

### Step 2: Analyze Status

```
For each tracked item:
  1. Compare expiration date to today
  2. Classify status:
     - EXPIRED: expiration date has passed
     - CRITICAL: expiring within 30 days
     - WARNING: expiring within 31-60 days
     - UPCOMING: expiring within 61-90 days
     - CURRENT: more than 90 days remaining
     - UNKNOWN: no expiration date on file

  3. Check for gaps:
     - Required coverage that has no active policy
     - Licenses needed for current project jurisdictions
     - Safety certifications required for active job sites
     - Regulatory filings that are past due

  4. Compare against GC/owner requirements:
     - Minimum coverage limits required by active contracts
     - Endorsements required (AI, WOS, primary/non-contributory)
     - Maximum EMR thresholds specified in contracts
     - License classifications required for project scopes
```

### Step 3: Generate Recommendations

```
For each action item:
  1. Identify the renewal or corrective action needed
  2. List the responsible party (agent, carrier, licensing board)
  3. Provide contact information
  4. Estimate lead time for completion
  5. Note any dependencies (e.g., financials needed before bonding renewal)
  6. Suggest calendar reminders for follow-up
```

### Step 4: Notify and Track

**If calendar connected:**
```
Create calendar events for:
  - Renewal deadlines (with 30-day and 60-day advance reminders)
  - Filing deadlines (with appropriate lead time)
  - Audit dates
  - Follow-up checks on pending renewals
```

**If chat connected:**
```
Send notifications:
  - EXPIRED items: immediate alert to CFO and responsible parties
  - CRITICAL items (30 days): weekly reminder to responsible parties
  - WARNING items (60 days): bi-weekly reminder
  - UPCOMING items (90 days): monthly reminder
```

**If email connected:**
```
Draft renewal request emails:
  - To insurance agent: "Please initiate renewal for [policy]"
  - To licensing board: renewal application instructions
  - To surety agent: "Please issue updated bonding letter"
```

---

## Renewal Checklists

### Insurance Renewal Checklist

```markdown
## Insurance Renewal: [Policy Type]

**Policy:** [Policy #] — [Carrier]
**Current Expiration:** [Date]
**Agent:** [Name] — [Phone] — [Email]

### Pre-Renewal (60-90 days before expiration)
- [ ] Contact agent to begin renewal process
- [ ] Gather updated payroll data (for WC and GL)
- [ ] Gather updated vehicle schedule (for auto)
- [ ] Gather updated equipment schedule (for inland marine)
- [ ] Review current limits against contract requirements
- [ ] Identify any coverage gaps or needed endorsements
- [ ] Compile loss runs (request from carrier if needed)

### Renewal Processing (30-60 days before expiration)
- [ ] Review renewal quotes/proposals
- [ ] Compare premiums year-over-year
- [ ] Verify limits meet all active contract requirements
- [ ] Confirm endorsements available (AI, WOS, primary/NC)
- [ ] Approve renewal terms

### Post-Renewal (immediately after binding)
- [ ] Obtain new COI from agent
- [ ] Update knowledge base with new policy details
- [ ] Upload new COI to document storage
- [ ] Distribute updated COI to all active GCs/owners requiring it
- [ ] Update prequal data with new policy numbers and dates
- [ ] Set next renewal reminder
```

### License Renewal Checklist

```markdown
## License Renewal: [License Type]

**License:** [#] — [State/Jurisdiction]
**Current Expiration:** [Date]
**Issuing Authority:** [Name] — [Website]

### Pre-Renewal (90 days before expiration)
- [ ] Verify renewal requirements (CEUs, fees, bond)
- [ ] Complete any required continuing education
- [ ] Obtain updated contractor bond (if required)
- [ ] Verify qualifying individual (RME/RMO) is still employed
- [ ] Gather required financial documentation

### Renewal Processing (30-60 days before expiration)
- [ ] Submit renewal application
- [ ] Pay renewal fee
- [ ] Submit bond (if required)
- [ ] Submit CEU documentation (if required)

### Post-Renewal (immediately after receipt)
- [ ] Update knowledge base with new license details
- [ ] Upload renewed license to document storage
- [ ] Update prequal data with new license number/dates
- [ ] Set next renewal reminder
```

### Bonding Capacity Renewal

```markdown
## Bonding Capacity Update

**Surety:** [Company] — [Agent Name]
**Current Letter Date:** [Date]
**Agent Contact:** [Phone] — [Email]

### Annual Update (within 120 days of fiscal year end)
- [ ] Prepare annual financial statements (CPA-reviewed or audited)
- [ ] Compile work-in-progress (WIP) schedule
- [ ] Update backlog report
- [ ] Update key personnel information
- [ ] Prepare business plan / revenue projections
- [ ] Submit package to surety agent
- [ ] Receive updated bonding capacity letter
- [ ] Upload new letter to document storage
- [ ] Update knowledge base with new capacity figures
```

---

## GC/Owner Requirement Mapping

Track minimum requirements specified by active general contractors and project owners:

```markdown
| GC / Owner | Min GL | Min Auto | Min Umbrella | Max EMR | Add'l Insured | WOS | Special |
|-----------|--------|----------|-------------|---------|--------------|-----|---------|
| Turner | $1M/$2M | $1M | $10M | 1.0 | Required | Required | Pollution $1M |
| McCarthy | $1M/$2M | $1M | $5M | 0.95 | Required | Required | -- |
| Skanska | $2M/$4M | $2M | $10M | 0.90 | Required | Required | Prof Liability $2M |
| DPR | $1M/$2M | $1M | $10M | 1.0 | Required | Required | Cyber $1M |
```

**Compliance check:** When any policy renews or limits change, automatically verify that new coverage still meets all active GC/owner requirements. Flag any shortfalls.

---

## Proactive Alerts

### Alert Schedule

| Timeframe | Alert Level | Frequency | Channel |
|-----------|------------|-----------|---------|
| Expired | CRITICAL | Daily until resolved | Chat + Email |
| 1-30 days | URGENT | Weekly | Chat + Email |
| 31-60 days | WARNING | Bi-weekly | Chat |
| 61-90 days | NOTICE | Monthly | Dashboard only |
| 90+ days | INFO | Quarterly review | Dashboard only |

### Alert Content

```
URGENT: Workers Compensation policy WC-2025-998877 expires in 22 days (April 2, 2026)

Action required:
1. Contact agent: Jane Smith at ABC Insurance, (555) 555-7700
2. Provide updated payroll data for renewal quote
3. Review renewal terms and approve
4. Ensure no gap in coverage — WC is required on all active job sites

Impact if lapsed:
- Cannot work on any job site without active WC coverage
- Violates contract requirements with Turner, McCarthy, Skanska, DPR
- State regulatory violation — potential fines and license suspension
```

---

## Related Skills

- **prequal-form-filler** — Automatically fill prequalification forms using the compliance data tracked by this skill
