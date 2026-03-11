---
name: contract-generation
description: Generate professional one-time service contracts with scope of work, pricing, signature blocks, warranty terms, and legal provisions for Huston Electric, Inc. Trigger with "generate contract", "create service contract", "produce contract for [customer]", "turn this quote into a contract", "service agreement for [job]".
---

# Contract Generation Agent

Produce professional service contracts for Huston Electric, Inc. This skill converts accepted quotations into binding service contracts with detailed scope, pricing schedules, warranty provisions, insurance requirements, legal terms, and signature blocks. Handles one-time service contracts, ongoing service agreements, and maintenance contracts. Works standalone with manual input, supercharged with document generation for branded PDFs and CRM for customer records.

## Connectors (Optional)

| Connector | What It Adds |
|-----------|--------------|
| **Document Generation** | Generate branded, formatted PDF contracts |
| **CRM** | Pull customer info, link contract to opportunity |
| **Email** | Send contract to customer for signature |
| **Knowledge Base (Past Quotes)** | Reference accepted quotation for contract details |

> **No connectors?** Provide the job details or reference a quotation and I will produce a complete contract in text format you can copy into your template.

---

## How It Works

```
┌──────────────────────────────────────────────────────────────────────────┐
│                      CONTRACT GENERATION AGENT                          │
├──────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  Step 1: GATHER CONTRACT DETAILS                                         │
│  - Customer information (name, address, contact)                       │
│  - Reference quotation number (if applicable)                          │
│  - Scope of work (from quotation or new description)                  │
│  - Contract value and payment schedule                                 │
│  - Start date and estimated completion                                 │
│                                                                          │
│  Step 2: DETERMINE CONTRACT TYPE                                         │
│  - One-time service (fixed scope, fixed price)                        │
│  - Time and material (hourly rate + materials at cost + markup)       │
│  - Service agreement (recurring, defined term)                        │
│  - Maintenance contract (EMP-based, annual)                           │
│                                                                          │
│  Step 3: ASSEMBLE CONTRACT SECTIONS                                      │
│  - Cover page and parties                                              │
│  - Scope of work                                                       │
│  - Pricing and payment                                                 │
│  - Schedule and milestones                                             │
│  - Warranty and guarantees                                             │
│  - Insurance and indemnification                                      │
│  - General terms and conditions                                       │
│  - Signature blocks                                                    │
│                                                                          │
│  Step 4: GENERATE AND DELIVER                                            │
│  - Format contract document                                            │
│  - ~~document generation: Create branded PDF                          │
│  - ~~email: Send to customer for review/signature                     │
│  - ~~CRM: Log contract, update opportunity status                     │
│                                                                          │
└──────────────────────────────────────────────────────────────────────────┘
```

---

## Contract Types

### One-Time Service Contract

For defined scope, single-occurrence jobs. Most common for service work.

### Time and Material (T&M) Contract

For jobs where scope is uncertain. Defines rates and markup, not total price.

### Service Agreement

For recurring services over a defined term (e.g., quarterly maintenance).

### Maintenance Contract

Based on an accepted EMP proposal, covering ongoing maintenance for a defined term.

---

## Output Format — One-Time Service Contract

```markdown
# SERVICE CONTRACT

## HUSTON ELECTRIC, INC.

---

### CONTRACT NUMBER: HE-CTR-[YYYY]-[NNNN]
### DATE: [Date]
### REFERENCE QUOTATION: [Quote # if applicable]

---

## 1. PARTIES

**Contractor:**
Huston Electric, Inc.
[Address]
[City, State ZIP]
Phone: [Phone]
License #: [License Number]

**Customer:**
[Customer Name]
[Customer Address]
[City, State ZIP]
Phone: [Phone]
Contact: [Contact Name], [Title]

---

## 2. SCOPE OF WORK

Huston Electric, Inc. ("Contractor") shall furnish all labor, materials, tools, and
equipment necessary to perform the following work at [Service Address]:

[Detailed scope of work — transferred from quotation or described in detail]

2.1. **Included in this contract:**
  - [Specific inclusion 1]
  - [Specific inclusion 2]
  - [Specific inclusion 3]

2.2. **Not included in this contract:**
  - [Specific exclusion 1]
  - [Specific exclusion 2]
  - [Specific exclusion 3]

2.3. **Work by others:**
  - [Work customer or other contractors are responsible for]

---

## 3. CONTRACT PRICE AND PAYMENT

3.1. **Contract Price:** $[Total Amount]

3.2. **Payment Schedule:**

| Milestone | Amount | Due |
|-----------|--------|-----|
| Upon contract execution | $[X.XX] ([X]%) | At signing |
| Upon substantial completion | $[X.XX] ([X]%) | Net 30 from completion |
| [Additional milestone] | $[X.XX] ([X]%) | [Terms] |

3.3. **Payment Terms:** Net 30 from date of invoice. Late payments subject to 1.5%
monthly interest charge.

3.4. **Change Orders:** Any work beyond the scope defined in Section 2 requires a
written change order signed by both parties. Change orders will be priced at
$[rate]/hr for labor plus materials at cost plus [X]%.

---

## 4. SCHEDULE

4.1. **Commencement:** Work shall commence on or about [Start Date], subject to
material availability and scheduling.

4.2. **Estimated Completion:** [Completion Date or Duration]

4.3. **Work Hours:** Standard work hours are Monday through Friday, 7:00 AM to
3:30 PM. Overtime or weekend work, if required by Customer, will be billed
at overtime rates ($[rate]/hr).

4.4. **Delays:** Contractor shall not be liable for delays caused by material
shortages, weather, acts of God, or conditions beyond Contractor's control.

---

## 5. WARRANTY

5.1. **Labor Warranty:** Contractor warrants all workmanship for a period of one (1)
year from the date of substantial completion.

5.2. **Material Warranty:** Materials are warranted per manufacturer's terms and
conditions. Contractor will assist Customer with manufacturer warranty claims
during the warranty period.

5.3. **Warranty Exclusions:** This warranty does not cover damage caused by misuse,
abuse, neglect, unauthorized modification, or acts of God.

5.4. **Warranty Service:** To request warranty service, contact Contractor at [Phone]
during normal business hours. Warranty claims will be addressed within [X]
business days.

---

## 6. INSURANCE AND INDEMNIFICATION

6.1. **Contractor Insurance:** Contractor maintains the following insurance:
  - General Liability: $[X,000,000] per occurrence
  - Workers Compensation: Per statutory requirements
  - Automobile Liability: $[X,000,000] per occurrence
  - Umbrella/Excess: $[X,000,000]

6.2. **Certificates of Insurance:** Available upon request.

6.3. **Indemnification:** Each party shall indemnify the other against claims arising
from the indemnifying party's negligence or willful misconduct.

---

## 7. GENERAL TERMS AND CONDITIONS

7.1. **Permits and Inspections:** [Contractor / Customer] shall obtain and pay for
all necessary permits. Contractor shall coordinate required inspections.

7.2. **Code Compliance:** All work shall be performed in accordance with the current
National Electrical Code (NEC), NFPA 70, and all applicable state and local codes
and amendments.

7.3. **Access:** Customer shall provide Contractor with reasonable access to all work
areas during the project duration. Delays caused by restricted access may result
in additional charges.

7.4. **Site Conditions:** If concealed or unknown conditions are encountered that
differ materially from those indicated in this contract, the contract price
and schedule shall be equitably adjusted by change order.

7.5. **Cancellation:** Either party may cancel this contract with [30] days written
notice. Customer shall pay for all work completed and materials procured
through the date of cancellation.

7.6. **Dispute Resolution:** Any disputes arising from this contract shall first be
addressed through good-faith negotiation. Unresolved disputes shall be
submitted to mediation in [County], Indiana.

7.7. **Governing Law:** This contract shall be governed by the laws of the State of
Indiana.

7.8. **Entire Agreement:** This contract, including any referenced quotation and
change orders, constitutes the entire agreement between the parties.

7.9. **Safety:** Contractor shall comply with all applicable OSHA regulations and
maintain a safe working environment. Customer shall notify Contractor of any
known hazards at the work site.

7.10. **Lien Rights:** Contractor reserves all lien rights under Indiana Code
32-28-3 (Mechanic's Lien Statute).

---

## 8. ACCEPTANCE AND SIGNATURES

By signing below, Customer accepts the terms of this contract and authorizes Huston
Electric, Inc. to proceed with the work described herein.

**CUSTOMER:**

Signature: _________________________ Date: ___________
Printed Name: _________________________
Title: _________________________
Company: _________________________

**CONTRACTOR — HUSTON ELECTRIC, INC.:**

Signature: _________________________ Date: ___________
Printed Name: _________________________
Title: _________________________

---

Huston Electric, Inc.
[Address] | [Phone] | [Email]
License #: [License Number]
```

---

## T&M Contract Pricing Section Variation

When the contract is time-and-material rather than fixed price, replace Section 3 with:

```markdown
## 3. RATES AND PRICING

3.1. **Labor Rates:**
| Classification | Standard Rate | Overtime Rate | Emergency Rate |
|----------------|---------------|---------------|----------------|
| Journeyman Electrician | $92/hr | $138/hr | $184/hr |
| Apprentice | $65/hr | $97.50/hr | $130/hr |
| Helper | $50/hr | $75/hr | $100/hr |

3.2. **Materials:** Materials furnished at cost plus 40% markup.

3.3. **Equipment Rental:** Equipment furnished at cost plus 15% markup.

3.4. **Not-to-Exceed Amount:** $[X.XX] (if applicable — work will not exceed this
amount without written authorization from Customer).

3.5. **Billing:** [Weekly / Bi-weekly / Monthly] invoices with detailed time and
material documentation.

3.6. **Payment Terms:** Net 30 from date of invoice.
```

---

## Service Agreement Term Section Variation

For recurring service agreements, add:

```markdown
## TERM AND RENEWAL

- **Initial Term:** [1 / 2 / 3] year(s) commencing [Start Date].
- **Renewal:** Automatically renews for successive one-year terms unless either party
  provides 60 days written notice of non-renewal.
- **Price Adjustment:** Annual price adjustment of up to [3]% for renewed terms.
- **Early Termination:** [60] days written notice required. Customer responsible for
  services rendered through termination date.
```

---

## Contract Generation Checklist

Before generating a contract, verify:

```
REQUIRED INFORMATION:
  [ ] Customer legal name (as it should appear on contract)
  [ ] Customer address
  [ ] Customer contact name and title (signing authority)
  [ ] Service address (if different from customer address)
  [ ] Scope of work (from quotation or new description)
  [ ] Contract value
  [ ] Payment terms and schedule
  [ ] Start date
  [ ] Estimated completion date
  [ ] Permit responsibility (contractor or customer)
  [ ] Any special conditions or customer requirements

CONTRACTOR INFORMATION:
  [ ] Company legal name
  [ ] Address
  [ ] License number
  [ ] Authorized signer name and title
  [ ] Insurance certificate availability
```

---

## Related Skills

- **electrical-quotation** — Create the quotation that precedes the contract
- **sign-quotation** — Sign-specific quotations for contract conversion
- **generator-quotation** — Generator quotations for contract conversion
- **emp-proposal** — Maintenance program proposals for service agreement contracts
