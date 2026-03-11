---
description: Generate a sign installation or maintenance quotation — travel time, lift equipment, sign-specific labor, and materials
argument-hint: "<sign job description>"
---

# /quote-sign

> If you see unfamiliar placeholders or need to check which tools are connected, see [CONNECTORS.md](../CONNECTORS.md).

Generate a professional sign installation or maintenance quotation with travel time calculations, equipment rental, sign-specific labor, and electrical connections.

## Usage

```
/quote-sign <sign job description>
```

Generate a sign quotation for: $ARGUMENTS

If a file is referenced: @$1

---

## How It Works

```
┌─────────────────────────────────────────────────────────────────┐
│                      QUOTE SIGN                                  │
├─────────────────────────────────────────────────────────────────┤
│  STANDALONE (always works)                                       │
│  ✓ Describe the sign work or paste job request                  │
│  ✓ Travel time calculation based on distance from shop          │
│  ✓ Sign-specific labor standards                                │
│  ✓ Equipment rental (bucket truck, lift, crane)                 │
│  ✓ Electrical connection and NEC 600 compliance                 │
│  ✓ Professional quotation with sign-specific terms              │
├─────────────────────────────────────────────────────────────────┤
│  SUPERCHARGED (when you connect your tools)                      │
│  + Knowledge Base: Past sign jobs, sign material pricing        │
│  + Document Generation: Branded PDF quotation                   │
│  + CRM: Customer info, sign maintenance history                │
└─────────────────────────────────────────────────────────────────┘
```

---

## What I Need From You

**Describe the sign job:**
```
Install two channel letter signs at new retail location at 789 Main St, Carmel IN.
Signs are being fabricated by customer's sign company — we're doing electrical only.
Location is 45 minutes from our shop. Signs mount at 12 ft height on storefront.
Need new 20A circuit from panel to each sign location, approximately 100 ft run each.
```

**Helpful details:**
- Sign type (channel letters, monument, pylon, cabinet, LED, neon)
- Work type (new install, repair, retrofit, removal)
- Sign dimensions and mounting height
- Distance from shop to job site
- Whether sign is supplied or we are sourcing
- Number of trips needed (survey, install, final)
- Equipment needs (bucket truck, boom lift, crane)
- Existing electrical or new circuit needed

---

## Output

The sign quotation includes:

1. **Header** — Quotation number, date, estimator
2. **Customer and Site Info** — Including distance from shop
3. **Scope of Work** — Sign work description, electrical connection details
4. **Pricing Detail** — Travel, sign labor, electrical labor, equipment, materials
5. **Cost Summary** — All subtotals, tax, grand total
6. **Sign-Specific Terms** — Weather dependency, NEC 600, permits, structural
7. **Acceptance Block** — Signature line

---

## Sign-Specific Pricing Notes

| Item | Typical Range | Notes |
|------|--------------|-------|
| Travel (round trip) | $184-$552+ | Based on distance, crew size |
| Bucket truck | $150/day | $75/half day |
| Channel letter install (per letter) | $69-$138 labor | Plus materials |
| New circuit to sign (per circuit) | $350-$750 | Distance-dependent |
| Disconnect switch (NEC 600.6) | $200-$400 | Required for each sign |
| Photocell/timer | $100-$200 | Automatic on/off |

---

## Tips

1. **Always include travel** — Sign jobs are rarely next door. Travel is billable.
2. **Count the trips** — Survey, install, and inspection are often separate visits.
3. **Check equipment needs early** — Crane rental requires advance scheduling and significantly impacts cost.
4. **Verify sign fabrication status** — If the sign is not ready, installation cannot proceed. Note lead times.
5. **NEC 600.6 disconnect** — Every sign needs a disconnect switch within sight. Do not forget this line item.
