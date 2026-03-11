---
description: Parse bid invitation emails — extract project details, classify by union local, assess scope and complexity, flag strategic opportunities
argument-hint: "<email content or source>"
---

# /process-bids

> If you see unfamiliar placeholders or need to check which tools are connected, see [CONNECTORS.md](../CONNECTORS.md).

Parse incoming bid invitation emails, extract structured project details, classify by IBEW local jurisdiction, and flag strategic opportunities for Huston Electric.

## Usage

```
/process-bids [email content or source]
```

Process bids from: $ARGUMENTS

If a file is referenced: @$1

---

## How It Works

```
┌─────────────────────────────────────────────────────────────────┐
│                      PROCESS BIDS                                 │
├─────────────────────────────────────────────────────────────────┤
│  STANDALONE (always works)                                        │
│  ✓ Paste or forward bid invitation email content                 │
│  ✓ Upload bid documents (PDF, Word, images)                      │
│  ✓ Describe bid opportunities verbally                           │
│  ✓ Extract: project, GC, owner, location, date, scope, value    │
│  ✓ Classify by IBEW local union jurisdiction                     │
│  ✓ Assess complexity and strategic fit                           │
│  ✓ Generate Go/No-Go recommendation                              │
│  ✓ Output structured bid record ready for weekly report          │
├─────────────────────────────────────────────────────────────────┤
│  SUPERCHARGED (when you connect your tools)                       │
│  + Email: Auto-scan inbox for unprocessed bid emails             │
│  + Knowledge Base: Cross-reference GC history and past bids     │
│  + Spreadsheet: Append directly to bid tracking sheet            │
│  + Calendar: Create bid deadline and pre-bid meeting events      │
│  + Chat: Alert estimating team of new opportunities              │
└─────────────────────────────────────────────────────────────────┘
```

---

## What I Need From You

**Option A: Paste email content**
Copy and paste the full bid invitation email. I will extract all structured data automatically.

**Option B: Forward emails (if email connected)**
Tell me to scan your inbox. I will find unprocessed bid-related emails and process them all.

**Option C: Upload documents**
Upload a bid invitation PDF, plan room notification, or screenshot. I will parse the content.

**Option D: Describe the opportunity**
```
New bid from Turner Construction for the Lincoln Elementary School renovation.
Electrical scope, about $800K. Bid date March 25. Located in Oak Park, Cook County.
Pre-bid meeting March 18 at 2pm, mandatory.
```

**Option E: Multiple bids at once**
Paste multiple emails or descriptions separated by `---`. I will process each one individually.

---

## Output

For each bid processed:

```markdown
# Bid Processed: [Project Name]

---

## Extracted Details

| Field | Value |
|-------|-------|
| **Project Name** | [Name] |
| **General Contractor** | [GC Name] |
| **Owner / Client** | [Owner Name] |
| **Location** | [Address, City, County] |
| **Bid Date** | [Date, Time, Timezone] |
| **Estimated Value** | $[X] |
| **Union Local** | [IBEW Local XXX] |
| **Scope Summary** | [Electrical scope description] |
| **Pre-Bid Meeting** | [Date, Time, Location, Mandatory?] |
| **Bond Required** | [Yes/No — Bid bond / Performance bond] |
| **Prevailing Wage** | [Yes/No — Davis-Bacon / State] |
| **Plan Availability** | [Where to access plans] |
| **Contact** | [Name, Phone, Email] |

---

## Assessment

| Factor | Rating | Notes |
|--------|--------|-------|
| **Strategic Fit** | [1-5] | [Rationale] |
| **Profitability** | [1-5] | [Rationale] |
| **Capacity** | [1-5] | [Rationale] |
| **Risk** | [1-5] | [Rationale] |
| **Logistics** | [1-5] | [Rationale] |
| **Composite Score** | [X.X] | — |

---

## Recommendation: [GO / CONDITIONAL GO / NO-GO]

**Rationale:** [2-3 sentences explaining the recommendation]

**Key flags:**
- [Flag 1]
- [Flag 2]

---

## Action Items

1. [ ] [Immediate action — e.g., request plans, attend pre-bid]
2. [ ] [Assignment — e.g., assign estimator]
3. [ ] [Deadline — e.g., bid due in X days]
```

### Batch Processing Summary

When processing multiple bids at once:

```markdown
# Bid Processing Summary — [Date]

**Bids processed:** [X]
**Total estimated value:** $[X]

| # | Project | GC | Value | Bid Date | Local | Recommendation |
|---|---------|----|----|----------|-------|----------------|
| 1 | [Name] | [GC] | $[X] | [Date] | [Local] | GO |
| 2 | [Name] | [GC] | $[X] | [Date] | [Local] | CONDITIONAL |
| 3 | [Name] | [GC] | $[X] | [Date] | [Local] | NO-GO |

---

**Immediate Actions:**
1. [ ] [Most urgent action]
2. [ ] [Second action]
3. [ ] [Third action]

**Ready for Tuesday report:** [Yes — X new bids added / No — needs review]
```

---

## Processing Logic

### Step 1: Identify Email Type

```
Classify the input:
- Bid invitation (from GC or owner)
- Plan room notification (from service like BuildingConnected, iSqFt)
- Addendum notice (update to existing bid)
- Bid result (tabulation or award notice)
- Other (forward to user for manual classification)

Priority:
- Bid invitations with dates within 14 days → URGENT
- New bid invitations → NORMAL
- Addenda on tracked bids → HIGH (may change recommendation)
- Bid results → LOG (record for historical data)
```

### Step 2: Extract Structured Data

```
Parse email content for:

1. Project identification
   - Project name (from subject or body)
   - Project number (if referenced)
   - Building type / sector classification

2. Parties
   - General Contractor name and contact
   - Owner / Client name
   - Architect / Engineer (if mentioned)

3. Location
   - Street address
   - City and state
   - County (critical for union classification)
   - Zip code

4. Timeline
   - Bid date and time (with timezone)
   - Pre-bid meeting date/time/location
   - Estimated construction start
   - Estimated construction duration

5. Scope
   - Electrical divisions referenced (Division 26, 27, 28)
   - Scope narrative / description
   - Inclusions and exclusions
   - Special systems (fire alarm, low voltage, security, AV)

6. Requirements
   - Bid bond amount or percentage
   - Performance and payment bond
   - Prevailing wage / Davis-Bacon
   - License requirements
   - Insurance requirements
   - Prequalification requirements
   - MBE/WBE/DBE goals

7. Plans and specifications
   - Where to access (plan room, FTP, email attachment)
   - Plan room service name and link
   - Deposit requirements
   - Access credentials needed
```

### Step 3: Classify and Assess

```
1. Map location → IBEW local jurisdiction
2. Score complexity (5 factors, 1-5 scale)
3. Check license requirements against company credentials
4. Check bonding requirements against capacity
5. Run Go/No-Go decision matrix
6. Calculate priority ranking score
7. Assign recommendation with rationale
```

### Step 4: Output and Store

```
1. Display structured bid record
2. If spreadsheet connected → append to bid tracking sheet
3. If calendar connected → create bid deadline event
4. If chat connected → post alert to estimating channel
5. If knowledge base connected → create bid record entry
6. Queue for inclusion in Tuesday report
```

---

## Handling Ambiguity

| Situation | Approach |
|-----------|----------|
| **No bid date listed** | Flag as "BID DATE TBD" — ask user to follow up with GC |
| **No value indicated** | Estimate from scope description, building type, and square footage |
| **GC not identified** | Check if owner-direct bid; ask user for clarification |
| **Location unclear** | Search for project name or owner to determine location |
| **Scope vague** | Extract what is available, flag "SCOPE NEEDS CLARIFICATION" |
| **Multiple trades** | Filter to electrical scope only, note other trades for context |
| **Duplicate bid** | Check against existing tracked bids, merge or update if duplicate |

---

## If Email Connected

When ~~email is available, I will:

1. **Scan inbox** for emails matching bid invitation patterns
2. **Filter** by subject line keywords and known sender domains
3. **Exclude** already-processed emails (track by message ID)
4. **Process** each matching email through the extraction pipeline
5. **Group** related emails (invitation + addenda) by project
6. **Report** count of new bids found and processed

Scanning frequency: On-demand when you run `/process-bids`, or as part of the Tuesday report preparation workflow.

---

## Tips

1. **Process daily** — Run this command each morning to catch overnight bid invitations before deadlines pass.
2. **Include the full email** — Headers and footers often contain GC contact info and legal requirements that body text omits.
3. **Batch processing is fine** — Paste multiple emails separated by `---` and I will handle them all.
4. **Flag addenda separately** — If you receive an addendum on a tracked bid, mention the original project name so I can update rather than create a duplicate.
5. **Review before Tuesday** — Process all bids by Monday afternoon so the Tuesday meeting report is complete and accurate.
