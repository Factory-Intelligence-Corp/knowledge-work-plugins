---
name: prequal-form-filler
description: Specialized finance assistant that automatically fills prequalification PDF forms for Huston Electric, Inc. Uses company knowledge base, past prequal submissions, and financial data to auto-populate form fields with confidence scores. Includes approval workflow before submission. Trigger with "fill this prequal", "prequalification form", "fill out this prequal form", "I need to prequalify for [project/GC]", "prequal for [company]", or "complete this prequalification".
---

# Prequal Form Filler - Finances

Automatically fill prequalification PDF forms using Huston Electric's company knowledge base, past completed submissions, and current financial data. Every field is populated with a confidence score and source citation. Fields needing human review are flagged. Nothing is submitted without explicit approval.

---

## How It Works

```
+------------------------------------------------------------------+
|                    PREQUAL FORM FILLER                            |
+------------------------------------------------------------------+
|  ALWAYS (works standalone)                                       |
|  * You upload: prequal PDF form or describe fields               |
|  * Field identification: parse all form fields and requirements  |
|  * Knowledge matching: map fields to company data                |
|  * Auto-fill: populate fields with best available data           |
|  * Confidence scoring: rate each field (high/medium/low/manual)  |
|  * Human review: flag fields needing verification                |
|  * Approval: present completed form for sign-off                 |
|  * Output: generate completed form ready for submission          |
+------------------------------------------------------------------+
|  SUPERCHARGED (when you connect your tools)                      |
|  + Knowledge base: pull company profile, financials, safety data |
|  + Document storage: retrieve past prequals, COIs, licenses      |
|  + Email: receive prequal requests, send completed packages      |
|  + Calendar: track submission deadlines                          |
|  + Chat: notify approvers, coordinate document collection        |
+------------------------------------------------------------------+
```

---

## Connectors (Optional)

Connect your tools to supercharge this skill:

| Connector | What It Adds |
|-----------|--------------|
| **Knowledge base** | Company profile, financial records, safety data, project history, key personnel, past prequal field mappings |
| **Document storage** | Past completed prequal PDFs, insurance certificates, bonding letters, financial statements, W-9, license copies |
| **Email** | Receive prequal requests directly, send completed packages, track submission confirmations |
| **Calendar** | Submission deadlines, auto-set reminders for upcoming prequals |
| **Chat** | Approval notifications, alert CFO/Safety Director when forms are ready for review |

> **No connectors?** No problem. Upload the prequal PDF and paste or describe your company data. The skill will walk you through every field.

---

## Getting Started

When you run this skill, provide what you have:

**Required:**
- Prequalification form (PDF upload, pasted text, or description of fields)

**Helpful if you have it:**
- General contractor or project owner name
- Project name and location
- Submission deadline
- Any special requirements or notes

If you have connected your knowledge base and document storage, the skill pulls all company data automatically and skips the manual questions.

---

## Detailed Process

### Step 1: Receive Prequal Form

**Accept input in any format:**
```
1. PDF upload — parse form fields, checkboxes, tables, and attachments list
2. Pasted text — extract field names and requirements from raw text
3. Description — "Turner Construction standard prequal" triggers lookup
   of known GC prequal templates
4. Photo/scan — OCR the form to extract fields
```

**If connectors available:**
```
1. Email → Search for recent prequal requests
   - Query: emails with "prequalification" or "prequal" (last 30 days)
   - Extract: attached PDFs, submission deadlines, special instructions

2. Document storage → Check for known GC templates
   - Query: "[GC Name] prequal" in document library
   - Pull: previous submissions to this same GC
```

**If no connectors:**
```
1. Ask user:
   - "Upload the prequal form or paste the fields"
   - "Who is this for? (GC name or project owner)"
   - "When is it due?"
   - "Any special notes or requirements?"

2. Accept whatever they provide and work with it
```

### Step 2: Identify Form Fields and Requirements

Parse the form to build a complete field inventory:

```yaml
field_inventory:
  - id: "company_name"
    label: "Legal Company Name"
    type: "text"
    required: true
    section: "Company Information"
    page: 1

  - id: "ein"
    label: "Federal Tax ID (EIN)"
    type: "text"
    required: true
    section: "Company Information"
    page: 1
    format: "XX-XXXXXXX"

  - id: "annual_revenue_current"
    label: "Annual Revenue (Current Year)"
    type: "currency"
    required: true
    section: "Financial Information"
    page: 3
    format: "$X,XXX,XXX"

  - id: "emr_current"
    label: "Current Experience Modification Rate"
    type: "decimal"
    required: true
    section: "Safety Record"
    page: 5
    format: "X.XX"
```

**Categorize all fields into sections:**

| Section | Typical Fields |
|---------|---------------|
| Company Information | Legal name, DBA, address, phone, fax, website, EIN, DUNS, CAGE code, year established, type of organization, state of incorporation |
| Officers and Ownership | President/CEO, VP, Secretary, Treasurer, owners with percentages, minority/women-owned status |
| Financial Information | Annual revenue (3 years), current assets, current liabilities, net worth, working capital, bank references, line of credit |
| Bonding | Bonding company, agent, single project limit, aggregate limit, current bonded backlog, largest bond ever obtained |
| Insurance | General liability limits, auto liability, umbrella/excess, workers comp, professional liability, pollution liability, carrier names, policy numbers, expiration dates |
| Safety Record | EMR (3 years), OSHA 300A data (3 years), DART rates, fatalities, citations, safety program description, safety director name, drug testing program |
| Experience and Project History | Projects completed (last 5 years), project name, owner, value, completion date, scope, reference contact |
| Licenses and Certifications | State contractor licenses, electrical licenses, specialty certifications, license numbers, expiration dates, states licensed |
| Union Affiliations | Union name, local number, agreement expiration, apprenticeship program |
| Equipment | Major equipment list, fleet size, specialized equipment, owned vs. leased |
| Key Personnel | Names, titles, years with company, years in industry, certifications, education |
| References | Bank references, trade references, owner/GC references, surety references |
| Legal and Compliance | Pending litigation, bankruptcy history, contract terminations, debarment status, EEOC compliance, drug-free workplace |
| Subcontracting | Percentage self-performed, typical subcontractor trades, MBE/WBE/DBE participation |

### Step 3: Match Fields to Company Knowledge Base Data

**If knowledge base connected:**
```
1. Query company profile → match to Company Information fields
2. Query financial records → match to Financial Information fields
3. Query insurance policies → match to Insurance fields
4. Query safety database → match to Safety Record fields
5. Query project history → match to Experience fields
6. Query personnel records → match to Key Personnel fields
7. Query license database → match to Licenses fields
8. Query equipment inventory → match to Equipment fields
```

**If no knowledge base:**
```
1. Check settings.local.json for stored company data
2. Ask user for any missing critical fields
3. Accept uploaded documents (COIs, financials, etc.)
4. Parse uploaded documents for matching data
```

**Field matching logic:**
```
For each form field:
  1. Exact match — field label matches knowledge base key directly
  2. Semantic match — field label is a synonym or variant
     (e.g., "Tax ID" = "EIN" = "Federal Employer ID Number")
  3. Derived match — field can be calculated from known data
     (e.g., "Working Capital" = Current Assets - Current Liabilities)
  4. Historical match — field was answered in a past prequal
  5. No match — field requires manual input
```

### Step 4: Cross-Reference with Past Completed Prequals

**If document storage connected:**
```
1. Search for past prequal submissions
   - Query: "prequal" OR "prequalification" in completed forms folder
   - Filter: same GC/owner if possible

2. For each unmatched field:
   - Search past submissions for the same or similar field
   - Extract the previously provided answer
   - Note the date of the past submission (flag if stale)

3. For matched fields:
   - Compare current data vs. past submission
   - Flag any significant changes (revenue up/down >10%, EMR change, etc.)
   - Note: "Previously submitted X, current data shows Y"
```

**Past submission comparison logic:**
```
For each field with both current and historical data:
  - If values match: confidence = HIGH
  - If minor difference (<5%): confidence = HIGH, note change
  - If moderate difference (5-15%): confidence = MEDIUM, flag for review
  - If major difference (>15%): confidence = LOW, require manual confirmation
  - If historical only (no current source): confidence = LOW, flag as "from past submission — verify current"
```

### Step 5: Auto-Fill Matching Fields

Populate each field with the best available data and assign a confidence score:

```yaml
filled_fields:
  - id: "company_name"
    value: "Huston Electric, Inc."
    confidence: "HIGH"
    source: "Company Profile — Knowledge Base"
    notes: null

  - id: "annual_revenue_2025"
    value: "$48,750,000"
    confidence: "HIGH"
    source: "Financial Records — 2025 Annual Report"
    notes: "Matches past Turner prequal (submitted 03/2025)"

  - id: "emr_2024"
    value: "0.82"
    confidence: "MEDIUM"
    source: "Past Prequal — McCarthy (submitted 09/2024)"
    notes: "From past submission. Verify with current NCCI letter."

  - id: "largest_project_completed"
    value: null
    confidence: "MANUAL"
    source: null
    notes: "No matching data found. Requires manual input."
```

**Confidence levels:**

| Level | Meaning | Action |
|-------|---------|--------|
| **HIGH** | Current data from verified source (knowledge base, recent financials) | Auto-fill, no review needed |
| **MEDIUM** | Data from past submission or secondary source, may need verification | Auto-fill, flag for review |
| **LOW** | Data from old submission (>12 months) or derived/calculated value | Auto-fill with warning, require confirmation |
| **MANUAL** | No matching data found in any source | Leave blank, flag for manual input |

### Step 6: Flag Fields Needing Human Review

Generate a review list organized by urgency:

```markdown
## Fields Requiring Review

### MUST COMPLETE (no data available)
- [ ] Largest single project completed in last 5 years (Page 4, Field 12)
- [ ] Bank reference contact name and phone (Page 6, Field 3)
- [ ] List of current projects with remaining value (Page 4, Field 15)

### VERIFY (data from past submissions)
- [ ] EMR 2024: 0.82 (source: past McCarthy prequal, Sep 2024)
- [ ] Workers Comp Policy #: WC-2024-887431 (source: past COI, may have renewed)
- [ ] DART Rate 2024: 1.2 (source: past OSHA log submission)

### REVIEW CHANGES (current data differs from past submissions)
- [ ] Annual Revenue 2025: $48.75M (was $42.1M in last submission — 15.8% increase)
- [ ] Bonding Aggregate: $75M (was $60M — capacity increased)
- [ ] Number of employees: 385 (was 342 — 12.6% increase)

### INFORMATIONAL (auto-filled, high confidence)
- Company Name: Huston Electric, Inc. [HIGH]
- EIN: XX-XXXXXXX [HIGH]
- Address: 123 Main Street, City, ST 90001 [HIGH]
- (... all other HIGH confidence fields listed for transparency)
```

### Step 7: Present for Approval

Present the completed form in a structured review format:

```markdown
## Prequal Form Review: [GC/Owner Name]

**Form:** [Form title/name]
**Due Date:** [Submission deadline]
**Prepared:** [Today's date]

---

### Completion Summary

| Status | Count | Percentage |
|--------|-------|-----------|
| Auto-filled (HIGH confidence) | 47 | 68% |
| Auto-filled (needs verification) | 12 | 17% |
| Manually completed by user | 8 | 12% |
| Remaining blank | 2 | 3% |
| **Total fields** | **69** | **100%** |

---

### Section-by-Section Review

[Each section with all fields, values, confidence, and sources]

---

### Approval

**Before I generate the final document, please confirm:**

1. [ ] All flagged fields have been reviewed
2. [ ] Financial data is current and accurate
3. [ ] Insurance information matches current COIs
4. [ ] Safety data matches current OSHA logs
5. [ ] Project references are approved for use
6. [ ] Authorized signer is identified

**Who should sign this form?**
- [ ] President/CEO
- [ ] CFO
- [ ] Other: ___________
```

**If chat connector available:**
```
Send approval request to configured approvers:
- Message: "Prequal form for [GC Name] is ready for review.
  47/69 fields auto-filled. 12 fields need verification.
  Due date: [date]. Please review and approve."
- Channel: #finance or direct message to CFO
```

### Step 8: Generate Completed Form

After approval, generate the final output:

```
1. Populate the original PDF form with approved values
2. Generate a clean summary document with all fields and sources
3. Compile the submission package:
   - Completed prequal form
   - Current Certificate of Insurance (COI)
   - Bonding capacity letter
   - EMR verification letter
   - Financial statements (if required)
   - W-9
   - License copies
   - Safety program summary
   - Project experience matrix
   - Key personnel resumes
4. Save completed package to document storage
5. Update knowledge base with new submission record
```

---

## Common Prequal Form Fields Reference

### Company Information
| Field | Example Value | Typical Source |
|-------|--------------|----------------|
| Legal company name | Huston Electric, Inc. | Company Profile |
| DBA / Trade name | Huston Electric | Company Profile |
| Mailing address | 123 Main St, City, ST 90001 | Company Profile |
| Physical address | Same or different | Company Profile |
| Phone / Fax | (555) 555-5555 | Company Profile |
| Website | hustonelectric.com | Company Profile |
| EIN (Federal Tax ID) | XX-XXXXXXX | Company Profile |
| DUNS Number | XXXXXXXXX | Company Profile |
| CAGE Code | XXXXX | Company Profile |
| Year established | 1985 | Company Profile |
| Type of organization | Corporation | Company Profile |
| State of incorporation | California | Company Profile |
| Number of employees | 385 | HR Records |
| Annual payroll | $28,500,000 | Financial Records |

### Financial Data
| Field | Example Value | Typical Source |
|-------|--------------|----------------|
| Annual revenue (current year) | $48,750,000 | Financial Statements |
| Annual revenue (prior year) | $42,100,000 | Financial Statements |
| Annual revenue (2 years prior) | $38,600,000 | Financial Statements |
| Current assets | $15,200,000 | Balance Sheet |
| Current liabilities | $8,400,000 | Balance Sheet |
| Net worth | $12,500,000 | Balance Sheet |
| Working capital | $6,800,000 | Calculated |
| Line of credit | $5,000,000 | Bank Reference |
| Bank name | First National Bank | Bank Reference |

### Bonding
| Field | Example Value | Typical Source |
|-------|--------------|----------------|
| Bonding company | Liberty Mutual | Bonding Letter |
| Bonding agent | Smith & Associates | Bonding Letter |
| Single project limit | $25,000,000 | Bonding Letter |
| Aggregate limit | $75,000,000 | Bonding Letter |
| Current bonded backlog | $32,000,000 | Project Records |
| Largest bond obtained | $18,500,000 | Project Records |

### Insurance
| Field | Example Value | Typical Source |
|-------|--------------|----------------|
| General liability carrier | Hartford | COI |
| GL policy number | GL-2025-443291 | COI |
| GL each occurrence limit | $1,000,000 | COI |
| GL general aggregate | $2,000,000 | COI |
| GL expiration date | 06/30/2026 | COI |
| Auto liability carrier | Hartford | COI |
| Auto liability limit | $1,000,000 | COI |
| Umbrella carrier | Zurich | COI |
| Umbrella limit | $10,000,000 | COI |
| Workers comp carrier | State Fund | COI |
| WC statutory limits | Statutory | COI |
| WC employers liability | $1,000,000 | COI |
| Professional liability | $2,000,000 | COI |
| Pollution liability | $1,000,000 | COI |

### Safety Records
| Field | Example Value | Typical Source |
|-------|--------------|----------------|
| EMR (current year) | 0.85 | NCCI Letter |
| EMR (prior year) | 0.82 | NCCI Letter |
| EMR (2 years prior) | 0.88 | NCCI Letter |
| OSHA recordable incidents | 4 | OSHA 300A |
| OSHA total hours worked | 750,000 | OSHA 300A |
| TRIR (Total Recordable Incident Rate) | 1.07 | Calculated |
| DART rate | 0.80 | OSHA 300A |
| Fatalities (last 5 years) | 0 | Safety Records |
| OSHA citations (last 5 years) | 0 | Safety Records |
| Safety director name | John Smith | Personnel Records |
| Drug testing program | Yes — pre-employment, random, post-incident | Safety Program |

### Experience and Project History
| Field | Example Value | Typical Source |
|-------|--------------|----------------|
| Project name | ABC Medical Center Electrical | Project Records |
| Project owner | ABC Healthcare Systems | Project Records |
| Project location | Los Angeles, CA | Project Records |
| Contract value | $8,500,000 | Project Records |
| Completion date | March 2025 | Project Records |
| Scope of work | Complete electrical including power, lighting, fire alarm, low voltage | Project Records |
| GC / CM | Turner Construction | Project Records |
| Reference name and phone | Jane Doe, (555) 123-4567 | Project Records |
| Percentage self-performed | 85% | Project Records |

### Licenses and Certifications
| Field | Example Value | Typical Source |
|-------|--------------|----------------|
| State contractor license # | C-10 #XXXXXXX | License Records |
| License classification | Electrical Contractor | License Records |
| License expiration | 03/31/2027 | License Records |
| States licensed in | CA, NV, AZ | License Records |
| Specialty certifications | NETA, BICSI, LEED | Personnel Records |

### Union Affiliations
| Field | Example Value | Typical Source |
|-------|--------------|----------------|
| Union name | IBEW | Company Profile |
| Local number | Local 11 | Company Profile |
| Agreement expiration | 06/30/2027 | Union Agreement |
| Apprenticeship program | Yes — IBEW/NECA JATC | Company Profile |

### Equipment
| Field | Example Value | Typical Source |
|-------|--------------|----------------|
| Major equipment description | Bucket trucks, cable pullers, generators | Equipment List |
| Fleet size | 45 vehicles | Equipment List |
| Specialized equipment | 2 x 500 MCM cable pullers, medium voltage test equipment | Equipment List |
| Owned vs. leased | 80% owned, 20% leased | Equipment List |

### Key Personnel
| Field | Example Value | Typical Source |
|-------|--------------|----------------|
| Name | Michael Johnson | Personnel Records |
| Title | Vice President of Operations | Personnel Records |
| Years with company | 18 | Personnel Records |
| Years in industry | 25 | Personnel Records |
| Certifications | PE, LEED AP, NFPA 70E Qualified | Personnel Records |
| Education | BS Electrical Engineering, USC | Personnel Records |

---

## Output Format

The completed form package includes:

### 1. Completed Form with Confidence Scores

Each field annotated with:
- **Value** — The populated answer
- **Confidence** — HIGH / MEDIUM / LOW / MANUAL
- **Source** — Where the data came from (knowledge base record, past prequal, user input)
- **Last verified** — Date the source data was last confirmed
- **Notes** — Any caveats or change flags

### 2. Fields Needing Manual Review

A prioritized checklist:
- Fields with no data (must be completed manually)
- Fields with stale data (past submissions older than 12 months)
- Fields with significant changes from past submissions
- Fields where multiple conflicting sources exist

### 3. Source Citations

For every auto-filled field:
```
Field: Annual Revenue 2025
Value: $48,750,000
Source: Financial Records > 2025 Annual Income Statement
Retrieved: 2026-03-11
Confidence: HIGH
Past submission: $42,100,000 (Turner Prequal, 03/2025) — 15.8% increase
```

### 4. Comparison with Previous Submissions

Side-by-side comparison when a past submission to the same GC/owner exists:

| Field | Previous (03/2025) | Current | Change |
|-------|-------------------|---------|--------|
| Annual Revenue | $42,100,000 | $48,750,000 | +15.8% |
| EMR | 0.82 | 0.85 | +0.03 |
| Employees | 342 | 385 | +12.6% |
| Bonding Aggregate | $60,000,000 | $75,000,000 | +25% |
| Backlog | $28,000,000 | $32,000,000 | +14.3% |

---

## Approval Workflow

### Standard Approval Flow

```
Form Auto-Filled
     |
     v
Review Flagged Fields
     |
     v
User Completes Manual Fields
     |
     v
Present Summary for Review
     |
     v
CFO Review (if financial data included)
     |
     v
Safety Director Review (if safety data included)
     |
     v
Final Approval by Authorized Signer
     |
     v
Generate Completed Package
     |
     v
Archive to Document Storage + Update Knowledge Base
```

### Approval notifications (if chat connected)

```
1. When form is ready for review:
   → Notify CFO: "Prequal for [GC] ready for financial review"
   → Notify Safety Director: "Prequal for [GC] ready for safety review"

2. When approved:
   → Notify admin: "Prequal for [GC] approved. Ready for submission."

3. When submitted:
   → Notify team: "Prequal package for [GC] submitted. Due date: [date]."
```

---

## Data Validation Checks

Before generating the final form, validate:

### Financial Consistency
- [ ] Working capital = Current assets - Current liabilities
- [ ] Net worth is consistent with balance sheet
- [ ] Revenue trend is reasonable (no unexplained >50% swings)
- [ ] Bonded backlog does not exceed aggregate bonding capacity
- [ ] Line of credit is from a verified institution

### Insurance Currency
- [ ] All policy expiration dates are in the future
- [ ] Coverage limits meet or exceed GC/owner requirements
- [ ] Policy numbers match current COI on file
- [ ] Additional insured endorsements available if required
- [ ] Waiver of subrogation available if required

### Safety Data Accuracy
- [ ] EMR is from the current or most recent NCCI letter
- [ ] TRIR calculation: (Recordable incidents x 200,000) / Total hours worked
- [ ] DART calculation: (DART cases x 200,000) / Total hours worked
- [ ] No fatalities unreported
- [ ] OSHA citation history is complete and accurate

### License Verification
- [ ] All listed licenses are current (not expired)
- [ ] License classifications match the project scope
- [ ] Licenses cover the project's geographic jurisdiction

### Project History
- [ ] Reference contact information is current
- [ ] Project values are accurate
- [ ] Completion dates are correct
- [ ] No projects listed that resulted in litigation or disputes (unless disclosed)

### Personnel Data
- [ ] Key personnel are still employed
- [ ] Certifications are current
- [ ] Years of experience are accurate

---

## Configuration

### Company Financial Data

Store in `settings.local.json` or knowledge base:

```json
{
  "financial": {
    "revenue": {
      "2025": 48750000,
      "2024": 42100000,
      "2023": 38600000
    },
    "current_assets": 15200000,
    "current_liabilities": 8400000,
    "net_worth": 12500000,
    "working_capital": 6800000,
    "line_of_credit": 5000000,
    "bank_name": "First National Bank",
    "bank_contact": "Robert Thompson",
    "bank_phone": "(555) 555-9900",
    "fiscal_year_end": "12/31"
  }
}
```

### Insurance Information

```json
{
  "insurance": {
    "general_liability": {
      "carrier": "Hartford",
      "policy_number": "GL-2025-443291",
      "each_occurrence": 1000000,
      "general_aggregate": 2000000,
      "expiration": "2026-06-30",
      "agent": "ABC Insurance Agency",
      "agent_phone": "(555) 555-7700"
    },
    "auto_liability": {
      "carrier": "Hartford",
      "policy_number": "AL-2025-887321",
      "combined_single_limit": 1000000,
      "expiration": "2026-06-30"
    },
    "umbrella": {
      "carrier": "Zurich",
      "policy_number": "UMB-2025-112233",
      "each_occurrence": 10000000,
      "aggregate": 10000000,
      "expiration": "2026-06-30"
    },
    "workers_comp": {
      "carrier": "State Compensation Insurance Fund",
      "policy_number": "WC-2025-998877",
      "statutory": true,
      "employers_liability": 1000000,
      "expiration": "2026-01-01"
    },
    "professional_liability": {
      "carrier": "CNA",
      "policy_number": "PL-2025-665544",
      "limit": 2000000,
      "expiration": "2026-03-31"
    },
    "pollution_liability": {
      "carrier": "Indian Harbor",
      "policy_number": "POL-2025-334455",
      "limit": 1000000,
      "expiration": "2026-06-30"
    }
  }
}
```

### Bonding Capacity

```json
{
  "bonding": {
    "surety_company": "Liberty Mutual",
    "agent": "Smith & Associates Surety",
    "agent_phone": "(555) 555-8800",
    "single_project_limit": 25000000,
    "aggregate_limit": 75000000,
    "current_bonded_backlog": 32000000,
    "largest_bond_obtained": 18500000,
    "bonding_letter_date": "2026-01-15",
    "bonding_letter_expiration": "2027-01-15"
  }
}
```

---

## Tips for Better Results

1. **Keep the knowledge base current** — Update financial data after each fiscal year closes, update insurance after each renewal, update safety after each OSHA reporting period
2. **Save completed prequals** — Every submission improves future auto-fill accuracy by expanding the field mapping database
3. **Use consistent field names** — When storing data in the knowledge base, use the standard field names from this skill to ensure reliable matching
4. **Upload COIs promptly** — When insurance renews, upload the new certificate immediately so policy numbers, limits, and dates stay current
5. **Review EMR annually** — Request the updated NCCI experience modification letter each year and update the knowledge base
6. **Maintain project references** — Periodically verify that reference contacts are still at the listed phone numbers and willing to serve as references

---

## Related Skills

- **financial-compliance** — Track ongoing compliance requirements, insurance renewals, license expirations, and bonding updates
