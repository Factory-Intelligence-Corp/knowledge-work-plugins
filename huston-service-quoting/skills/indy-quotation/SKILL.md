---
name: indy-quotation
description: Indianapolis-specific electrical quotation specialist using standardized $92/hr labor rate and 40% material markup. Generates both customer-facing proposals and detailed internal pricing breakdowns. Trigger with "Indy quote", "Indianapolis quotation", "quote for Indy job", "Indianapolis service estimate", "price Indy electrical work".
---

# Indianapolis Quotation Specialist

Build quotations specifically tailored for the Indianapolis, Indiana market with Huston Electric's standardized pricing. This skill uses the fixed $92/hr labor rate and 40% material markup, applies Indiana-specific tax rules (7% sales tax on materials, no tax on labor), and generates two outputs: a clean customer-facing proposal and a detailed internal pricing breakdown showing actual costs and margins. Works standalone, supercharged with knowledge base for local material pricing and past Indy-area quotations.

## Connectors (Optional)

| Connector | What It Adds |
|-----------|--------------|
| **Knowledge Base (Past Quotes)** | Reference past Indianapolis-area quotations |
| **Knowledge Base (Materials)** | Local distributor pricing (Graybar, WESCO, CED) |
| **Document Generation** | Generate branded PDF proposal |
| **CRM** | Pull Indy customer info, job history |

> **No connectors?** Describe the job. I will build both the customer proposal and internal pricing breakdown using standard Indy rates.

---

## How It Works

```
┌──────────────────────────────────────────────────────────────────────────┐
│                  INDIANAPOLIS QUOTATION SPECIALIST                      │
├──────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  Step 1: PARSE JOB REQUEST                                               │
│  - Customer, location (verify Indianapolis metro area)                 │
│  - Scope of work                                                       │
│  - Job type (service call, project, emergency)                        │
│                                                                          │
│  Step 2: BUILD LINE ITEMS                                                │
│  - NECA labor units for each task                                      │
│  - Material costs (net cost to Huston)                                 │
│  - Apply standard Indy rates:                                          │
│    - Labor: $92/hr                                                     │
│    - Material markup: 40%                                              │
│    - Sales tax: 7% (materials only)                                   │
│                                                                          │
│  Step 3: GENERATE CUSTOMER PROPOSAL                                      │
│  - Clean, professional format                                          │
│  - Lump-sum pricing (no internal cost exposure)                       │
│  - Scope, price, terms                                                 │
│                                                                          │
│  Step 4: GENERATE INTERNAL BREAKDOWN                                     │
│  - Full cost detail (labor burden, material cost, markup)             │
│  - Margin analysis per line item                                       │
│  - Job profitability summary                                           │
│  - Comparison to similar past jobs                                     │
│                                                                          │
│  Step 5: DELIVER BOTH DOCUMENTS                                          │
│  - Customer proposal (for the customer)                                │
│  - Internal breakdown (for Huston management only — NEVER SEND)      │
│                                                                          │
└──────────────────────────────────────────────────────────────────────────┘
```

---

## Standard Indianapolis Rates

These are the fixed rates for all Indianapolis-area quotations:

| Rate Category | Amount | Notes |
|--------------|--------|-------|
| **Journeyman labor rate** | $92.00/hr | Standard billable rate |
| **Overtime labor rate** | $138.00/hr | 1.5x, after 8 hrs or weekends |
| **Emergency labor rate** | $184.00/hr | 2x, after-hours emergency calls |
| **Apprentice labor rate** | $65.00/hr | When applicable |
| **Material markup** | 40% | Over net distributor cost |
| **Equipment rental markup** | 15% | Over rental cost |
| **Subcontractor markup** | 15% | Over sub invoice |
| **Indiana sales tax** | 7.00% | On materials only, NOT labor |
| **Service call minimum** | 2 hours | Minimum billable for any dispatch |
| **Trip charge** | $150.00 | If job cancelled same-day |

### Internal Cost Benchmarks

These are NOT shown to customers — used for internal margin analysis only:

| Cost Category | Amount | Notes |
|--------------|--------|-------|
| Journeyman burdened cost | ~$55-$65/hr | Wages + benefits + burden |
| Apprentice burdened cost | ~$30-$40/hr | Wages + benefits + burden |
| Vehicle cost per trip | ~$35-$50 | Fuel, wear, insurance |
| Overhead allocation | ~$15-$20/hr | Shop, tools, admin |
| Target gross margin | 25-35% | Per job |

---

## Customer Proposal Format

This is what the customer sees — clean, professional, no internal costs exposed.

```markdown
# HUSTON ELECTRIC, INC.
## SERVICE PROPOSAL

**Proposal #:** HE-INDY-[YYYY]-[NNNN]
**Date:** [Date]
**Valid Until:** [Date + 30 days]
**Prepared By:** [Estimator Name] | [Phone] | [Email]

---

### TO:
**[Customer Name]**
[Customer Address]
[City, IN ZIP]
Attn: [Contact Name]

---

### PROJECT LOCATION:
[Service Address, Indianapolis, IN ZIP]

---

### SCOPE OF WORK

Huston Electric, Inc. proposes to furnish all labor, materials, and equipment
necessary to perform the following work:

[Clear, detailed scope description in numbered list]

---

### INVESTMENT

| Description | Amount |
|-------------|--------|
| [Work package 1 — lump sum description] | $[X,XXX.XX] |
| [Work package 2 — lump sum description] | $[X,XXX.XX] |
| [Work package 3 — lump sum description] | $[X,XXX.XX] |
| **Subtotal** | **$[X,XXX.XX]** |
| Indiana Sales Tax (7%) | $[XXX.XX] |
| **TOTAL INVESTMENT** | **$[X,XXX.XX]** |

---

### TERMS

- Proposal valid for 30 days
- Payment: Net 30 from invoice date
- Warranty: One (1) year on labor and materials
- Work hours: Monday-Friday, 7:00 AM - 3:30 PM
- All work per NEC and Indiana amendments
- Permits: [Included / Not included]

---

### AUTHORIZATION

To accept this proposal, please sign below and return.

Signature: _________________________ Date: ___________
Printed Name: _________________________

Huston Electric, Inc. | Indianapolis, IN | (317) 555-0100
```

---

## Internal Pricing Breakdown Format

**CONFIDENTIAL — INTERNAL USE ONLY — DO NOT SEND TO CUSTOMER**

```markdown
# INTERNAL PRICING BREAKDOWN
## Job: [Customer] — [Location]
## Proposal #: HE-INDY-[YYYY]-[NNNN]

---

### LINE ITEM DETAIL

| # | Description | Qty | NECA Units | Labor Hrs | Labor Cost @$92 | Mat'l Net Cost | Mat'l Quoted (40%) | Line Total |
|---|-------------|-----|------------|-----------|-----------------|----------------|-------------------|------------|
| 1 | [Task] | [X] | [X.XX] | [X.X] | $[X.XX] | $[X.XX] | $[X.XX] | $[X.XX] |
| 2 | [Task] | [X] | [X.XX] | [X.X] | $[X.XX] | $[X.XX] | $[X.XX] | $[X.XX] |
| 3 | [Task] | [X] | [X.XX] | [X.X] | $[X.XX] | $[X.XX] | $[X.XX] | $[X.XX] |

---

### COST vs. PRICE SUMMARY

| Category | Our Cost | Quoted Price | Margin |
|----------|----------|-------------|--------|
| Labor ([X.X] hrs) | $[X.XX] (@ ~$60 burdened) | $[X.XX] (@ $92) | $[X.XX] |
| Materials | $[X.XX] (net) | $[X.XX] (+ 40%) | $[X.XX] |
| Equipment rental | $[X.XX] (cost) | $[X.XX] (+ 15%) | $[X.XX] |
| Vehicle / trip | $[X.XX] | Included in labor | ($[X.XX]) |
| **Totals** | **$[X.XX]** | **$[X.XX]** | **$[X.XX]** |

---

### PROFITABILITY ANALYSIS

| Metric | Value |
|--------|-------|
| Total revenue (before tax) | $[X.XX] |
| Total direct cost | $[X.XX] |
| Gross profit | $[X.XX] |
| **Gross margin** | **[X.X]%** |
| Target margin range | 25-35% |
| Status | [On target / Below target / Above target] |

---

### COMPARISON TO SIMILAR PAST JOBS

| Past Job | Date | Similar Scope | Quoted | Margin |
|----------|------|--------------|--------|--------|
| [Job reference] | [Date] | [Brief scope] | $[X.XX] | [X]% |
| [Job reference] | [Date] | [Brief scope] | $[X.XX] | [X]% |

---

### NOTES FOR MANAGEMENT

- [Any pricing concerns, competitive pressure, relationship considerations]
- [Recommended adjustments if margin is below target]
- [Risk factors — site conditions, scope uncertainty, material availability]
```

---

## Indianapolis Area Coverage

| Zone | Area | Travel Consideration |
|------|------|---------------------|
| Zone 1 (local) | Downtown, Midtown, Broad Ripple, Speedway | No additional travel charge |
| Zone 2 (metro) | Carmel, Fishers, Greenwood, Avon, Brownsburg | No additional travel charge |
| Zone 3 (extended) | Anderson, Columbus, Shelbyville, Lebanon | Add travel time to quote |
| Zone 4 (remote) | Muncie, Bloomington, Terre Haute, Richmond | Quote travel separately |

---

## Indiana-Specific Code Notes

| Topic | Indiana Rule | Notes |
|-------|-------------|-------|
| Sales tax on materials | 7% | Always applies |
| Sales tax on labor | 0% | Labor is NOT taxable in Indiana |
| Electrical license | Required | State license for electrical work |
| Permit requirements | Varies by jurisdiction | Indianapolis, Carmel, Fishers have different permit offices |
| NEC adoption | Current edition with amendments | Indiana adopts NEC with state-specific amendments |
| GFCI requirements | Per NEC 210.8 | No Indiana-specific modifications |
| Inspections | Required | Rough-in and final for most permitted work |

---

## Related Skills

- **electrical-quotation** — General electrical quotation with full NECA reference
- **sign-quotation** — Sign-specific quotations
- **generator-quotation** — Generator installation quotations
- **contract-generation** — Convert accepted proposals to contracts
