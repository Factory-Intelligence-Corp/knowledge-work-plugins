---
description: Produce a one-time service contract with scope, pricing, signature blocks, warranty, and legal terms
argument-hint: "<job details or quotation reference>"
---

# /generate-contract

> If you see unfamiliar placeholders or need to check which tools are connected, see [CONNECTORS.md](../CONNECTORS.md).

Generate a professional service contract for Huston Electric, Inc. with scope of work, pricing schedule, warranty, insurance, general terms, and signature blocks.

## Usage

```
/generate-contract <job details or quotation reference>
```

Generate a contract for: $ARGUMENTS

If a file is referenced: @$1

---

## How It Works

```
┌─────────────────────────────────────────────────────────────────┐
│                    GENERATE CONTRACT                             │
├─────────────────────────────────────────────────────────────────┤
│  STANDALONE (always works)                                       │
│  ✓ Describe the job or reference an accepted quotation          │
│  ✓ One-time service, T&M, or service agreement formats         │
│  ✓ Scope of work, inclusions, and exclusions                   │
│  ✓ Pricing and payment schedule                                 │
│  ✓ Warranty, insurance, and indemnification                    │
│  ✓ General terms and conditions                                 │
│  ✓ Dual signature blocks (customer and contractor)              │
├─────────────────────────────────────────────────────────────────┤
│  SUPERCHARGED (when you connect your tools)                      │
│  + Knowledge Base: Reference accepted quotation details         │
│  + Document Generation: Branded PDF contract                    │
│  + Email: Send contract for review/signature                    │
│  + CRM: Link contract to customer record and opportunity       │
└─────────────────────────────────────────────────────────────────┘
```

---

## What I Need From You

**Option 1: Reference a quotation**
```
Generate contract for accepted quotation HE-2026-0147,
Johnson Manufacturing, 200A panel upgrade.
```

**Option 2: Describe the job**
```
Create a contract for Acme Corp at 123 Industrial Way.
Scope: Install new 400A service, two 200A panels, 30 circuits.
Price: $18,500. Payment: 50% at signing, 50% at completion.
Start date: April 1. Duration: 2 weeks.
```

**Option 3: Specify contract type**
```
T&M contract for ongoing electrical repairs at Smith Warehouse.
Not-to-exceed $25,000. Rates: $92/hr standard, 40% material markup.
Term: 6 months.
```

**Required information:**
- Customer legal name and address
- Contact name with signing authority
- Scope of work
- Contract price or rate structure
- Payment terms
- Start date and estimated duration

---

## Output

The contract includes:

1. **Parties** — Contractor and customer legal names, addresses
2. **Scope of Work** — Detailed description with inclusions and exclusions
3. **Contract Price and Payment** — Amount, schedule, change order provisions
4. **Schedule** — Start date, completion estimate, work hours
5. **Warranty** — Labor and material warranty terms
6. **Insurance and Indemnification** — Coverage types and amounts
7. **General Terms** — Permits, code compliance, access, cancellation, disputes, governing law
8. **Signature Blocks** — Customer and contractor with date lines

---

## Contract Types

| Type | When to Use | Pricing Structure |
|------|-------------|-------------------|
| **Fixed Price** | Defined scope, firm commitment | Lump sum or milestones |
| **Time & Material** | Uncertain scope | Hourly rates + material markup |
| **Service Agreement** | Recurring services | Monthly/quarterly/annual |
| **Not-to-Exceed T&M** | Semi-defined scope | T&M with cap amount |

---

## Tips

1. **Get the legal name right** — The customer name on the contract must be the legal entity, not a trade name.
2. **Define exclusions clearly** — What is NOT included prevents scope disputes later.
3. **Specify change order process** — Written approval required before additional work begins.
4. **Payment schedule protects cash flow** — For large jobs, require a deposit at signing.
5. **Review before sending** — Always review the generated contract before sending to the customer. Adjust terms as needed for the specific situation.
