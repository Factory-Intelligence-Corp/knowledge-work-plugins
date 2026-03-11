---
description: Fill a prequalification form — upload a PDF, auto-populate fields from company data, review flagged fields, and generate a completed form ready for submission
argument-hint: "<prequal PDF or form description>"
---

# /fill-prequal

> If you see unfamiliar placeholders or need to check which tools are connected, see [CONNECTORS.md](../CONNECTORS.md).

Fill a prequalification form by auto-populating fields from Huston Electric's company knowledge base, past submissions, and current financial data. Every field gets a confidence score and source citation. Nothing is submitted without your approval.

## Usage

```
/fill-prequal <PDF upload or form description>
```

Process this prequal form: $ARGUMENTS

If a file is referenced: @$1

---

## How It Works

```
+------------------------------------------------------------------+
|                       FILL PREQUAL                               |
+------------------------------------------------------------------+
|  STANDALONE (always works)                                       |
|  * Upload prequal PDF or describe the form fields                |
|  * Identify all form fields and requirements                     |
|  * Match fields to company data (settings or user input)         |
|  * Auto-fill with confidence scores (HIGH/MEDIUM/LOW/MANUAL)     |
|  * Flag fields needing human review or manual completion         |
|  * Present completed form for approval                           |
|  * Generate final submission package                             |
+------------------------------------------------------------------+
|  SUPERCHARGED (when you connect your tools)                      |
|  + Knowledge base: company profile, financials, safety, projects |
|  + Document storage: past prequals, COIs, bonding letters        |
|  + Email: receive prequal requests, send completed packages      |
|  + Calendar: track submission deadlines                          |
|  + Chat: notify approvers when form is ready for review          |
+------------------------------------------------------------------+
```

---

## What I Need From You

**Option 1: Upload the prequal PDF**
Upload the PDF form. I will parse all fields, checkboxes, tables, and attachment requirements, then auto-fill from company data.

**Option 2: Paste the form fields**
Copy and paste the field names or questions from the prequal form. I will match each one to company data and fill them in.

**Option 3: Name the GC or project owner**
Tell me who the prequal is for (e.g., "Turner Construction standard prequal"). If I have a past submission to this GC, I will use it as a starting template and update with current data.

**Option 4: Describe the requirements**
Tell me what information they are asking for: "They want company info, 3 years of financials, insurance, safety records, and 5 project references." I will gather and organize all the data.

---

## Output

### Completed Form Summary

```markdown
## Prequal Form: [GC/Owner Name]

**Form:** [Form title]
**Project:** [Project name if known]
**Due Date:** [Submission deadline]
**Prepared:** [Today's date]

---

### Completion Summary

| Status | Count | % |
|--------|------:|---:|
| Auto-filled (HIGH confidence) | XX | XX% |
| Auto-filled (verify recommended) | XX | XX% |
| Needs manual input | XX | XX% |
| **Total fields** | **XX** | **100%** |

---

### Fields Needing Your Input

**MUST COMPLETE (no data available):**
1. [ ] [Field name] — [Page/Section reference]
2. [ ] [Field name] — [Page/Section reference]

**VERIFY (auto-filled from past submission):**
1. [ ] [Field name]: [Value] — Source: [Past prequal, date]
2. [ ] [Field name]: [Value] — Source: [Past prequal, date]

**CHANGED (current data differs from last submission):**
1. [ ] [Field name]: [New value] (was [Old value], [% change])

---

### All Fields by Section

#### Company Information
| Field | Value | Confidence | Source |
|-------|-------|-----------|--------|
| Legal Name | Huston Electric, Inc. | HIGH | Company Profile |
| EIN | XX-XXXXXXX | HIGH | Company Profile |
| ... | ... | ... | ... |

#### Financial Information
| Field | Value | Confidence | Source |
|-------|-------|-----------|--------|
| Revenue 2025 | $48,750,000 | HIGH | Financial Records |
| ... | ... | ... | ... |

[Continue for all sections]

---

### Submission Package Checklist

- [ ] Completed prequal form
- [ ] Certificate of Insurance (COI)
- [ ] Bonding capacity letter
- [ ] EMR verification letter (NCCI)
- [ ] Financial statements
- [ ] W-9
- [ ] License copies
- [ ] Safety program summary
- [ ] Project experience list
- [ ] Key personnel resumes
- [ ] [Any additional attachments required by this form]

---

### Approval

Please review the above and confirm:
1. [ ] All flagged fields reviewed and completed
2. [ ] Financial data is current
3. [ ] Insurance matches current COIs
4. [ ] Authorized to submit

Ready to generate the final package?
```

---

## If Connectors Available

**Knowledge base connected:**
- Automatically pull company profile, financial data, safety records, project history, key personnel, and license information
- Cross-reference with past prequal submissions to the same GC
- Use past field mappings to improve auto-fill accuracy

**Document storage connected:**
- Retrieve the most recent COI, bonding letter, financial statements, W-9, and license copies
- Check for past submissions to the same GC/owner
- Save completed package to the prequal submissions folder

**Email connected:**
- Search for the original prequal request email
- Extract submission deadline and special instructions
- Draft submission email with completed package attached

**Calendar connected:**
- Set a reminder for the submission deadline
- Block time for review if the deadline is within 5 business days

**Chat connected:**
- Notify CFO when the form is ready for financial review
- Notify Safety Director when safety data needs verification
- Alert admin when the approved form is ready for submission

---

## Data Validation

Before generating the final form, the following checks run automatically:

**Financial consistency:**
- Working capital = Current assets - Current liabilities
- Revenue trend is reasonable year-over-year
- Bonded backlog does not exceed aggregate capacity

**Insurance currency:**
- All policy expiration dates are in the future
- Coverage limits meet this GC's minimum requirements (if known)
- Policy numbers match current COI on file

**Safety accuracy:**
- EMR is from current or most recent NCCI letter
- TRIR and DART calculations are mathematically correct
- Incident counts match OSHA 300A data

**License validity:**
- All listed licenses are current and not expired
- License classifications cover the project scope
- Licenses cover the project jurisdiction

---

## Tips

1. **Upload the actual PDF** — Parsing the real form is more accurate than describing the fields
2. **Name the GC** — If we have a past submission to this GC, it dramatically improves auto-fill
3. **Mention the deadline** — Helps prioritize and set appropriate reminders
4. **Flag special requirements** — Some GCs require specific endorsements, higher limits, or proprietary forms
5. **Review changed fields carefully** — When current data differs significantly from a past submission, double-check the new values
