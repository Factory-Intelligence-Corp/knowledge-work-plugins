---
description: Generate a full electrical service quotation — scope of work, NECA labor units, materials, markups, terms and conditions
argument-hint: "<scope of work or job description>"
---

# /quote-electrical

> If you see unfamiliar placeholders or need to check which tools are connected, see [CONNECTORS.md](../CONNECTORS.md).

Generate a professional electrical service quotation with NECA labor calculations, material pricing, markups, tax, and terms and conditions.

## Usage

```
/quote-electrical <scope of work or job description>
```

Generate a quotation for: $ARGUMENTS

If a file is referenced: @$1

---

## How It Works

```
┌─────────────────────────────────────────────────────────────────┐
│                    QUOTE ELECTRICAL                              │
├─────────────────────────────────────────────────────────────────┤
│  STANDALONE (always works)                                       │
│  ✓ Describe the scope of work or paste job notes                │
│  ✓ NECA labor unit calculation for each task                    │
│  ✓ Material pricing (enter costs or use estimates)              │
│  ✓ Labor rate: $92/hr, material markup: 40%                    │
│  ✓ Indiana sales tax: 7% on materials                          │
│  ✓ Professional quotation with terms and conditions            │
├─────────────────────────────────────────────────────────────────┤
│  SUPERCHARGED (when you connect your tools)                      │
│  + Knowledge Base: NECA labor unit lookups, material pricing    │
│  + Past Quotations: Reference similar past jobs                │
│  + Document Generation: Branded PDF quotation                   │
│  + Email: Send quotation directly to customer                   │
│  + CRM: Pull customer info, log quotation                      │
└─────────────────────────────────────────────────────────────────┘
```

---

## What I Need From You

**Option 1: Describe the job**
Tell me what needs to be done:
```
Quote a 200A panel upgrade for Johnson Manufacturing at 456 Industrial Blvd.
Replace 100A panel, add 6 new 20A circuits, install 2 GFCI outlets in wash bay.
```

**Option 2: Paste a scope of work**
Paste the scope from a request, email, or site survey notes. I will parse it into line items.

**Option 3: List the tasks**
```
- Install 200A panel (surface mount)
- Run 200A feeder, 15 ft
- 6x 20A dedicated circuits, 75 ft average run
- 2x GFCI receptacles with weatherproof covers, 40 ft run
- Circuit labeling and testing
```

**Helpful if you have it:**
- Customer name and address
- Contact name and phone/email
- Material costs (if known)
- Special conditions (overtime, emergency, prevailing wage)
- PO number or reference number

---

## Output

The quotation includes:

1. **Header** — Quotation number, date, validity, estimator info
2. **Customer Information** — Name, contact, service address
3. **Scope of Work** — Narrative description of all work
4. **Pricing Detail** — Line items with NECA labor, hours, labor cost, material cost, line total
5. **Cost Summary** — Labor subtotal, material subtotal, equipment, permits, tax, grand total
6. **Terms and Conditions** — Validity, payment, warranty, code compliance, access, safety
7. **Acceptance Block** — Signature line, date, PO number

---

## Pricing Reference

| Parameter | Standard Value |
|-----------|---------------|
| Labor rate | $92/hr |
| Overtime rate | $138/hr (1.5x) |
| Emergency rate | $184/hr (2x) |
| Material markup | 40% |
| Equipment rental markup | 15% |
| Sales tax (IN) | 7% on materials |
| Tax on labor | No (Indiana) |
| Quotation validity | 30 days |
| Payment terms | Net 30 |
| Warranty | 1 year labor and materials |

---

## If Connectors Available

**Knowledge Base connected:**
- Automated NECA labor unit lookups for each task
- Real-time material pricing from distributor databases
- Past quotation search for pricing consistency

**Document Generation connected:**
- Branded PDF with company logo
- Professional formatting and layout
- Return document link

**Email connected:**
- Draft email to customer with quotation attached
- Or send directly if approved

**CRM connected:**
- Auto-fill customer information
- Log quotation as opportunity
- Set follow-up reminder

---

## Tips

1. **Be specific about scope** — "Install 10 duplex receptacles, new construction, average 50 ft run from panel" is much better than "install some outlets."
2. **Mention site conditions** — Finished walls, high ceilings, outdoor, hazardous areas all affect labor.
3. **Include quantities** — Every task needs a quantity for accurate pricing.
4. **Note existing conditions** — "Replace existing 100A panel" vs. "install new panel where none exists" are different scopes.
5. **Specify material preferences** — "Eaton BR series panel" vs. "any 200A panel" affects pricing.
