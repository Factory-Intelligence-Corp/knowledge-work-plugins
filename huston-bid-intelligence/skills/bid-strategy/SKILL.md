---
name: bid-strategy
description: "Bid strategy analysis for Huston Electric — analyzes market conditions, competitive landscape, historical win rates, backlog capacity, and labor availability to recommend bidding strategy on specific opportunities. Provides markup guidance, risk mitigation tactics, and competitive positioning. Trigger with \"should we bid this\", \"bid strategy for\", \"analyze this opportunity\", \"what's our chance on\", \"competitive assessment\", or \"Go/No-Go on\"."
---

# Bid Strategy Analysis

Analyze market conditions, competitive landscape, historical win rates, and current capacity to recommend a comprehensive bidding strategy for specific opportunities. Goes beyond the initial Go/No-Go screening to provide markup guidance, risk mitigation, competitive positioning, and tactical recommendations.

## How It Works

```
┌─────────────────────────────────────────────────────────────────┐
│                    BID STRATEGY ANALYSIS                          │
├─────────────────────────────────────────────────────────────────┤
│  ALWAYS (works standalone via web search + your input)            │
│  ✓ Market conditions assessment for project type and location    │
│  ✓ Competitive landscape — who else is likely bidding            │
│  ✓ Backlog and capacity check — can we staff it                  │
│  ✓ Risk identification and mitigation strategy                   │
│  ✓ Markup guidance based on market and competition               │
│  ✓ Tactical bid recommendations                                  │
│  ✓ Alternate/value engineering suggestions                       │
├─────────────────────────────────────────────────────────────────┤
│  SUPERCHARGED (when you connect your tools)                       │
│  + Knowledge Base: Historical win/loss data, pricing benchmarks  │
│  + Email: GC correspondence history, relationship context        │
│  + Spreadsheet: Current backlog data, manpower allocation        │
│  + Chat: Field intelligence from PMs and superintendents         │
└─────────────────────────────────────────────────────────────────┘
```

---

## Connectors (Optional)

| Connector | What It Adds |
|-----------|--------------|
| **Knowledge Base** | Historical bid results, win/loss patterns, pricing benchmarks, GC relationship scores |
| **Email** | Correspondence history with GC/owner, previous proposal language, negotiation context |
| **Spreadsheet** | Current backlog schedule, manpower allocation, equipment availability |
| **Chat** | Field intelligence — PM and superintendent insights on GCs, sites, and competitors |
| **File Storage** | Past estimates for similar scope, plan review notes, specification analysis |

> **No connectors?** Describe the opportunity and your situation. I will analyze with web research and your input.

---

## Getting Started

When you run this skill, I will ask for context:

**Required:**
- What is the project? (name, type, location, approximate value)
- Who is the GC or owner?
- What is the bid date?

**Helpful:**
- What is your current backlog and manpower situation?
- Have you worked with this GC/owner before?
- Do you know who else is bidding?
- Any concerns or red flags you have already identified?

---

## Output Format

```markdown
# Bid Strategy: [Project Name]

**Prepared:** [Date]
**Bid Date:** [Date]
**GC/Owner:** [Name]
**Estimated Value:** $[X]
**Location:** [City, County] | **Union Local:** [IBEW Local]

---

## Executive Summary

[2-3 sentence recommendation: pursue aggressively, bid competitively,
bid with premium, or decline. Key rationale.]

**Recommendation:** [GO / CONDITIONAL GO / NO-GO]
**Confidence Level:** [High / Medium / Low]
**Suggested Markup Range:** [X% - Y%]

---

## Market Analysis

### Current Market Conditions
| Factor | Assessment | Impact on Strategy |
|--------|------------|-------------------|
| **Market volume** | [High/Normal/Low] | [More/fewer bidders] |
| **Sector demand** | [Growing/Stable/Declining] | [Pricing pressure] |
| **Labor availability** | [Tight/Adequate/Surplus] | [Rate implications] |
| **Material costs** | [Rising/Stable/Falling] | [Escalation risk] |
| **Interest rates** | [High/Moderate/Low] | [Project funding stability] |

### Local Market Factors
- [Union territory conditions]
- [Competing projects drawing manpower]
- [Regional economic indicators]
- [Permitting/inspection environment]

---

## Competitive Landscape

### Likely Bidders
| Competitor | Likelihood | Strengths | Weaknesses | Expected Approach |
|------------|-----------|-----------|------------|-------------------|
| [Company 1] | High | [What they do well] | [Where they struggle] | [Aggressive/Standard] |
| [Company 2] | Medium | [Strengths] | [Weaknesses] | [Approach] |
| [Company 3] | Medium | [Strengths] | [Weaknesses] | [Approach] |

### Competitive Position Assessment
- **Our advantages:** [What differentiates Huston on this project]
- **Our vulnerabilities:** [Where competitors may beat us]
- **Expected number of bidders:** [X-Y]
- **Expected spread:** [X% between low and high bidder]

---

## Historical Data

### Win/Loss with This GC
| Metric | Value |
|--------|-------|
| **Bids submitted** | [X] |
| **Wins** | [X] ([%]) |
| **Average spread (when won)** | [X%] below next bidder |
| **Average spread (when lost)** | [X%] above low bidder |
| **Last bid** | [Date] — [Won/Lost] — [Project] |
| **Relationship quality** | [Strong/Good/Neutral/Weak] |

### Similar Project History
| Project | Year | Value | Result | Margin | Lessons |
|---------|------|-------|--------|--------|---------|
| [Name] | [Year] | $[X] | [W/L] | [%] | [Key takeaway] |

---

## Capacity Assessment

### Current Backlog
| Metric | Status | Impact |
|--------|--------|--------|
| **Active projects** | [X] | [Healthy/Stretched/Overloaded] |
| **Backlog value** | $[X] | [Within/Near/Over target] |
| **Peak manpower committed** | [X] electricians | [Available/Tight] |
| **Estimating load** | [X] active bids | [Bandwidth available/Stretched] |

### Staffing Plan (if awarded)
| Role | Available | Needed | Gap |
|------|-----------|--------|-----|
| **Project Manager** | [Y/N] | [Name or hire] | [None/Hire needed] |
| **Superintendent** | [Y/N] | [Name or hire] | [None/Hire needed] |
| **Foremen** | [X] available | [X] needed | [+/- X] |
| **Journeymen** | [X] available | [X] needed | [+/- X] |
| **Apprentices** | [X] available | [X] needed | [+/- X] |

### Schedule Fit
- **Project start:** [Estimated date]
- **Project duration:** [X months]
- **Conflicts with:** [Any overlapping projects]
- **Ramp-up timing:** [When manpower peaks]

---

## Risk Assessment

### Risk Matrix
| Risk | Probability | Impact | Mitigation |
|------|-------------|--------|------------|
| [Scope growth] | [H/M/L] | [H/M/L] | [Strategy] |
| [Schedule delay] | [H/M/L] | [H/M/L] | [Strategy] |
| [Labor shortage] | [H/M/L] | [H/M/L] | [Strategy] |
| [Material escalation] | [H/M/L] | [H/M/L] | [Strategy] |
| [Payment risk] | [H/M/L] | [H/M/L] | [Strategy] |
| [Coordination issues] | [H/M/L] | [H/M/L] | [Strategy] |
| [Design incomplete] | [H/M/L] | [H/M/L] | [Strategy] |

### Bid-Specific Risks
- [Project-specific risk 1 and mitigation]
- [Project-specific risk 2 and mitigation]
- [Project-specific risk 3 and mitigation]

### Contract Risk Flags
- [ ] Liquidated damages: $[X]/day — [Acceptable/Concerning/Excessive]
- [ ] Warranty period: [X months] — [Standard/Extended]
- [ ] Retainage: [X]% — [Standard/High]
- [ ] Pay-if-paid clause: [Yes/No]
- [ ] No-damage-for-delay: [Yes/No]
- [ ] Indemnification scope: [Standard/Broad form]

---

## Pricing Strategy

### Markup Recommendation
| Component | Suggested Range | Rationale |
|-----------|----------------|-----------|
| **Overhead** | [X%] | [Based on project duration and complexity] |
| **Profit** | [X% - Y%] | [Based on competition and risk] |
| **Contingency** | [X%] | [Based on scope clarity and risk level] |
| **Escalation** | [X%] | [Based on project duration and market] |
| **Total markup** | [X% - Y%] | [Composite recommendation] |

### Pricing Tactics
1. **[Tactic 1]** — [Description and rationale]
2. **[Tactic 2]** — [Description and rationale]
3. **[Tactic 3]** — [Description and rationale]

### Value Engineering Opportunities
| VE Item | Savings Estimate | Trade-off | Recommend? |
|---------|-----------------|-----------|------------|
| [Item 1] | $[X] | [What is given up] | [Yes/No/As alternate] |
| [Item 2] | $[X] | [Trade-off] | [Yes/No/As alternate] |

### Alternate Recommendations
- **Base bid:** [Approach — as specified]
- **Alternate 1:** [Description — savings/add]
- **Alternate 2:** [Description — savings/add]

---

## Tactical Recommendations

### Pre-Bid Actions
1. [ ] [Attend pre-bid meeting — date/time]
2. [ ] [Visit site — what to look for]
3. [ ] [Contact GC estimator — build relationship]
4. [ ] [Review addenda — check for scope changes]
5. [ ] [Identify key subcontractors needed]

### Bid Day Tactics
1. [ ] [Submission timing strategy]
2. [ ] [Qualification language to include]
3. [ ] [Exclusions to clearly state]
4. [ ] [Alternates to offer]

### Post-Bid Strategy
1. [ ] [Follow-up plan if low bidder]
2. [ ] [Negotiation approach if in range]
3. [ ] [Intelligence gathering if not awarded]

---

## Decision Summary

| Factor | Score (1-5) | Weight | Weighted |
|--------|-------------|--------|----------|
| Strategic fit | [X] | 25% | [X] |
| Profitability potential | [X] | 25% | [X] |
| Capacity | [X] | 20% | [X] |
| Risk (inverse) | [X] | 20% | [X] |
| Logistics | [X] | 10% | [X] |
| **Total** | — | 100% | **[X.X]** |

**Final Recommendation:** [GO / CONDITIONAL GO / NO-GO]

**Conditions (if Conditional Go):**
- [Condition 1 that must be met]
- [Condition 2 that must be met]

**Key Success Factors (if Go):**
- [What must go right to win and profit]
- [Critical path items]
```

---

## Execution Flow

### Phase 1: Gather Project Information

```
From user or email/documents:
1. Project name, type, and description
2. GC and/or owner identity
3. Location (address, city, county)
4. Bid date and time
5. Estimated value or square footage
6. Scope of electrical work
7. Contract type (lump sum, GMP, design-build, etc.)
8. Special requirements (prevailing wage, PLA, certifications)
```

### Phase 2: Market Research

```
Web searches (always):
1. "[GC name] recent projects [location]" — GC activity level
2. "[Project type] construction [region] 2024 2025" — market trends
3. "[Location] construction projects" — competing projects
4. "electrical contractor [region]" — competitor identification
5. "[Owner name] construction projects" — owner's building program
6. "construction material prices [year]" — cost trends
7. "[Union local] labor outlook" — manpower conditions
```

### Phase 3: Historical Analysis (If Knowledge Base Connected)

```
1. Query bid history for this GC
   - Win/loss record, pricing spreads, relationship notes
2. Query similar project types
   - Pricing benchmarks per square foot or per unit
   - Lessons learned, change order patterns
3. Query competitor history
   - Who typically bids this type of work
   - Their pricing tendencies
4. Query location history
   - Previous work in area, site conditions
```

### Phase 4: Capacity Check

```
1. Review current backlog (from spreadsheet or user input)
   - Total committed value
   - Monthly manpower requirements
   - Equipment commitments
2. Assess available resources
   - PM and superintendent availability
   - Foreman and journeyman counts
   - Apprentice ratios and compliance
3. Identify conflicts
   - Overlapping project schedules
   - Geographic spread concerns
   - Estimating bandwidth
```

### Phase 5: Synthesize and Recommend

```
1. Score each decision factor (1-5)
2. Calculate weighted composite score
3. Check for automatic triggers (Go or No-Go)
4. Determine markup range based on:
   - Competition level
   - Risk assessment
   - Strategic value
   - Capacity utilization
5. Develop tactical recommendations
6. Draft strategy document
```

---

## Win Rate Improvement Framework

Track these metrics over time to improve bidding accuracy:

| Metric | Target | How to Improve |
|--------|--------|---------------|
| **Hit rate** | 20-30% | Better Go/No-Go screening |
| **Average spread** | Within 5% of low | Market intelligence, pricing calibration |
| **Bid accuracy** | Final cost within 3% of bid | Better takeoff, historical data |
| **Go/No-Go accuracy** | 80%+ of Go bids are competitive | Refine scoring criteria quarterly |
| **Strategic win rate** | 35%+ on priority targets | Relationship investment, pre-positioning |

---

## Tips

1. **Know your number before you know theirs** — Build your estimate on your costs, then adjust strategy based on competition.
2. **Relationships win ties** — When bids are close, the GC gives the work to the contractor they trust. Invest in relationships.
3. **No-Go is a strategy** — Every bid you decline frees estimating capacity for a better opportunity.
4. **Track everything** — Bid results, spreads, competitors, conditions. Data compounds over time.
5. **Pre-position on strategic targets** — Do not wait for the ITB. Build the GC relationship months before.
6. **Site visits matter** — 30 minutes on site saves hours of assumptions and thousands in contingency.
7. **Read the specifications** — Spec sections 26, 27, and 28 hide scope that plan-only takeoffs miss.
8. **Qualifications protect profit** — Clear exclusions and qualifications prevent scope creep after award.

---

## Related Skills

- **bid-email-analysis** — Parse and classify incoming bid invitations, generate the weekly Excel intelligence report
