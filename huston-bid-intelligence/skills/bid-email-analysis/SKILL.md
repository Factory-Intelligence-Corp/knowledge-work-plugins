---
name: bid-email-analysis
description: "Huston Bid Intel Agent — transforms chaotic bid invitation emails into organized union-based Excel intelligence reports for Tuesday strategy meetings. Parses bid invitations, plan room notifications, and addenda. Classifies by IBEW local jurisdiction, assesses scope and complexity, flags strategic opportunities, and generates Excel reports with Go/No-Go recommendations. Trigger with \"process bid emails\", \"new bid invitations\", \"bid intel report\", \"Tuesday meeting report\", \"what bids came in\", or \"update the bid log\"."
---

# Huston Bid Intel Agent

Transform chaotic bid invitation emails into organized, union-based Excel intelligence reports that drive Tuesday strategy meetings. This skill is the core engine for Huston Electric's bid tracking workflow.

## How It Works

```
┌─────────────────────────────────────────────────────────────────┐
│                   HUSTON BID INTEL AGENT                          │
├─────────────────────────────────────────────────────────────────┤
│  ALWAYS (works standalone)                                        │
│  ✓ Parse bid invitation emails (forwarded or pasted)             │
│  ✓ Extract: project, GC, owner, location, bid date, scope       │
│  ✓ Classify by IBEW local union jurisdiction                     │
│  ✓ Assess bid size, complexity, and strategic fit                │
│  ✓ Identify required licenses and certifications                 │
│  ✓ Flag high-priority strategic opportunities                    │
│  ✓ Generate Go/No-Go recommendation with rationale               │
│  ✓ Produce Excel report organized by union territory             │
├─────────────────────────────────────────────────────────────────┤
│  OUTPUT                                                           │
│  ✓ Excel report: union-organized bid intelligence                │
│  ✓ Strategic summary for Tuesday meetings                        │
│  ✓ Priority-ranked opportunity list                              │
│  ✓ Calendar entries for bid due dates                            │
├─────────────────────────────────────────────────────────────────┤
│  SUPERCHARGED (when you connect your tools)                       │
│  + Email: Auto-scan inbox for bid invitations                    │
│  + Spreadsheet: Write directly to Google Sheets / Excel          │
│  + Knowledge Base: Pull historical win/loss data, GC notes       │
│  + Calendar: Auto-create bid deadline events                     │
│  + Chat: Send bid alerts to estimating team                      │
│  + File Storage: Access plans and specifications                 │
└─────────────────────────────────────────────────────────────────┘
```

---

## Connectors (Optional)

| Connector | What It Adds |
|-----------|--------------|
| **Email** | Auto-scan inbox for bid invitations, plan room alerts, addenda notifications |
| **Spreadsheet** | Write formatted Excel reports directly to Google Sheets or OneDrive |
| **Knowledge Base** | Historical bid data, GC relationship scores, past project performance |
| **Calendar** | Auto-create events for bid due dates, pre-bid meetings, site walks |
| **Chat** | Push bid alerts and Tuesday report summaries to team channels |
| **File Storage** | Access uploaded plans, specs, and addenda for scope assessment |

> **No connectors?** No problem. Forward bid emails, paste content, or describe opportunities and I will process everything manually.

---

## Getting Started

When you run this skill, I will ask for what I need:

**If no email connected:**
> "Forward your bid invitation emails to me, or paste the email content here. I can handle multiple bids at once."

**If no spreadsheet connected:**
> "I will generate the Excel report as a downloadable file. Want me to format it for a specific template?"

**If no knowledge base connected:**
> "Tell me about any history you have with the GC or owner on this project. Have you bid similar work before?"

**If you have connectors:**
I will pull bid emails automatically, cross-reference with your bid history, and generate the report directly in your spreadsheet tool.

---

## Email Parsing Patterns

The agent recognizes and processes these common bid email types:

### Bid Invitations (Primary)
```
Detection patterns:
- Subject contains: "invitation to bid", "ITB", "request for proposal",
  "RFP", "bid invitation", "request for bid", "solicitation",
  "invitation for bid", "bid request"
- From addresses: known GC domains, plan room services, owner procurement
- Body contains: bid date, project name, scope of work, plan availability

Extracted fields:
- Project Name
- Bid Date / Due Date / Time
- General Contractor (GC)
- Owner / Client
- Project Location (address, city, county)
- Scope of Work (electrical, low voltage, fire alarm, etc.)
- Estimated Value (if stated or inferable)
- Pre-Bid Meeting (date, time, location, mandatory/optional)
- Plan Availability (plan room, FTP, BuildingConnected, etc.)
- Bond Requirements
- Prevailing Wage / Davis-Bacon applicability
- Addenda count
- Contact person and method
```

### Plan Room Notifications
```
Detection patterns:
- From: iSqFt, BuildingConnected, Dodge, SmartBidNet, PlanHub,
  ConstructConnect, BidClerk, Reed Construction
- Subject contains: "new project", "project match", "bid opportunity",
  "plans available"

Extracted fields:
- Project name and number
- Plan room link
- Bid date
- GC (if listed)
- Location
- CSI divisions relevant to electrical
```

### Addenda Notifications
```
Detection patterns:
- Subject contains: "addendum", "addenda", "revision", "amendment",
  "bid date change", "updated bid date"
- References a previously tracked project

Actions:
- Update bid date if changed
- Flag scope changes affecting electrical
- Note new specification sections
- Alert if addendum affects Go/No-Go recommendation
```

### Bid Results / Awards
```
Detection patterns:
- Subject contains: "bid results", "award", "notice of award",
  "apparent low bidder", "bid tabulation"

Actions:
- Record result against tracked bid
- Update win/loss history for GC and project type
- Extract competitor pricing for market intelligence
- Note spread between bids for future estimating
```

---

## Union Classification Methodology

Every bid is classified by IBEW local union jurisdiction based on project location. This determines labor rates, work rules, manpower availability, and strategic considerations.

### Classification Process

```
1. Extract project address from bid invitation
2. Determine county and municipality
3. Map to IBEW local jurisdiction
4. Pull jurisdiction-specific data:
   - Labor rates (journeyman, apprentice, foreman)
   - Work rules and conditions
   - Manpower availability assessment
   - Travel/subsistence requirements
   - Any special agreements or project labor agreements (PLAs)
```

### Jurisdiction Mapping (Configured per Installation)

The plugin ships with a configurable jurisdiction map. Example structure:

```yaml
jurisdictions:
  - local: "IBEW Local 134"
    territory:
      counties: ["Cook"]
      cities: ["Chicago"]
    notes: "Primary territory — strongest manpower, best relationships"
    labor_rate_tier: "Tier 1"

  - local: "IBEW Local 701"
    territory:
      counties: ["DuPage", "Kane", "Kendall", "Will", "Grundy"]
      cities: []
    notes: "Suburban territory — growing market, good availability"
    labor_rate_tier: "Tier 2"

  - local: "IBEW Local 461"
    territory:
      counties: ["McLean", "Livingston", "Woodford", "Ford"]
      cities: ["Bloomington", "Normal"]
    notes: "Downstate — travel considerations, limited projects"
    labor_rate_tier: "Tier 3"
```

### Impact on Go/No-Go

Union classification directly influences the bid decision:

| Factor | Favorable | Unfavorable |
|--------|-----------|-------------|
| **Territory** | Primary service area | Outside normal range, travel costs |
| **Manpower** | Adequate supply for project size | Shortage in local, competing projects |
| **Relationships** | Established with local leadership | No relationship, unfamiliar work rules |
| **Rates** | Competitive in market | Rates above non-union competition |
| **PLAs** | PLA project (union advantage) | Open shop project in union territory |

---

## Bid Size and Complexity Assessment

### Size Classification

| Category | Estimated Value | Typical Characteristics |
|----------|----------------|------------------------|
| **Small** | Under $250K | Single trade, short duration, 1-2 electricians |
| **Medium** | $250K - $1M | Multi-phase, 3-6 month duration, crew of 4-8 |
| **Large** | $1M - $5M | Complex coordination, 6-12 months, multiple crews |
| **Major** | Over $5M | Multi-year, dedicated PM, bonding considerations |

### Complexity Scoring

```
Complexity factors (scored 1-5 each):

1. Scope diversity
   - Single discipline (power only) = 1
   - Power + lighting = 2
   - Full electrical + low voltage = 3
   - Full electrical + fire alarm + security + AV = 4
   - Full MEP coordination responsibility = 5

2. Technical requirements
   - Standard commercial = 1
   - Healthcare / clean room = 3
   - Data center / mission critical = 4
   - Hazardous location / explosion-proof = 5

3. Schedule pressure
   - Normal phasing = 1
   - Accelerated schedule = 3
   - Fast-track / design-build = 4
   - Occupied renovation with shutdowns = 5

4. Coordination complexity
   - Single GC, standard coordination = 1
   - Multiple primes / CM at-risk = 3
   - Owner-direct with self-coordination = 4
   - Multi-phase occupied renovation = 5

5. Regulatory/certification requirements
   - Standard permits = 1
   - Special inspections required = 2
   - LEED / green building = 3
   - OSHPD / healthcare authority = 4
   - Federal / security clearance = 5

Total score:
  5-10: Low complexity
  11-17: Moderate complexity
  18-20: High complexity
  21-25: Very high complexity
```

---

## Required Licenses and Certifications Check

For each bid, the agent checks whether Huston Electric holds the required credentials:

```
License/certification matrix:

- Electrical Contractor License (state)
- Low Voltage Contractor License
- Fire Alarm Installation License
- Security System License
- Generator Installation Certification
- Medium Voltage Certification
- Renewable Energy / Solar Certification
- OSHA 30 (superintendent requirement)
- Confined Space Entry Certification
- Asbestos Awareness (renovation work)
- NFPA 70E Arc Flash Training
- Prevailing Wage Compliance History
- Bonding Capacity (vs. project requirement)
- Insurance Limits (vs. project requirement)
- EMR (Experience Modification Rate) threshold
- Prequalification status with owner/GC
```

Flags are raised when:
- A required license is not held
- Bonding requirement exceeds capacity
- Insurance limits need endorsement
- Prequalification is required but not on file
- EMR exceeds GC threshold

---

## Go/No-Go Decision Criteria

Each bid receives a recommendation: **Go**, **Conditional Go**, or **No-Go**, with detailed rationale.

### Decision Matrix

```
SCORING (each factor rated 1-5):

Strategic Fit (weight: 25%)
  - Aligns with target sectors?
  - Relationship with GC/owner?
  - Project type Huston excels at?
  - Visibility/reference value?

Profitability Potential (weight: 25%)
  - Market conditions (how many bidders?)
  - Scope clarity (well-defined = better pricing)
  - Change order potential
  - Payment terms and owner reputation

Capacity (weight: 20%)
  - Current backlog vs. available manpower
  - Estimating bandwidth to prepare bid
  - Supervision availability
  - Equipment/tool requirements

Risk (weight: 20%)
  - Schedule risk
  - Scope ambiguity
  - Owner/GC payment history
  - Liquidated damages exposure
  - Warranty requirements

Logistics (weight: 10%)
  - Distance from office/yard
  - Union jurisdiction familiarity
  - Parking/staging/access
  - Material storage

THRESHOLDS:
  Score 4.0-5.0 → GO (strong opportunity)
  Score 3.0-3.9 → CONDITIONAL GO (bid with caveats)
  Score 2.0-2.9 → NO-GO (unfavorable, document why)
  Score 1.0-1.9 → HARD NO-GO (do not pursue)
```

### Automatic No-Go Triggers

These conditions override the scoring matrix:

- Required license not held and cannot be obtained before bid date
- Bonding requirement exceeds capacity with no path to increase
- Project conflicts with existing contractual obligations
- Owner on "do not bid" list
- Insufficient time to prepare competitive estimate
- Scope requires specialty not in Huston's capabilities

### Automatic Go Triggers

These conditions elevate the recommendation regardless of score:

- Repeat client with strong relationship and profitable history
- Strategic project that opens new market sector
- Project Labor Agreement (PLA) that limits non-union competition
- Pre-negotiated or sole-source opportunity

---

## Output Format

### Excel Report (Primary Output)

The weekly report is an Excel workbook with the following structure:

#### Sheet 1: Bid Intelligence Summary

```
Columns:
A: Priority Rank (1, 2, 3...)
B: Project Name
C: General Contractor
D: Owner / Client
E: Location (City, County)
F: Bid Date
G: Estimated Value
H: Union Local
I: Scope Summary
J: Complexity Score (L/M/H/VH)
K: Go/No-Go Recommendation
L: Key Notes / Flags
M: Assigned Estimator
N: Status (New / In Progress / Submitted / Result)

Formatting:
- Header row: Bold, dark background, white text
- Go recommendations: Green background on column K
- Conditional Go: Yellow background on column K
- No-Go: Red background on column K
- Bid dates within 7 days: Bold red text in column F
- Bid dates today: Red background on column F
- Rows grouped by Union Local (column H)
- Alternating row shading for readability
- Column widths auto-fitted to content
- Freeze panes on row 1 and column B
```

#### Sheet 2: By Union Territory

```
Separate sections for each IBEW local:

--- IBEW Local 134 (Cook County / Chicago) ---
[Filtered rows from Sheet 1 for Local 134 territory]
Subtotal: [count] bids, $[total estimated value]

--- IBEW Local 701 (Suburban) ---
[Filtered rows from Sheet 1 for Local 701 territory]
Subtotal: [count] bids, $[total estimated value]

[Additional locals as configured]
```

#### Sheet 3: Strategic Dashboard

```
Summary statistics:
- Total active bids: [count]
- Total estimated pipeline value: $[sum]
- Bids due this week: [count] / $[value]
- Go recommendations: [count] / $[value]
- Conditional Go: [count] / $[value]
- No-Go: [count] / $[value]

By sector:
- Healthcare: [count] / $[value]
- Education: [count] / $[value]
- Municipal: [count] / $[value]
- Commercial: [count] / $[value]
- Industrial: [count] / $[value]
- Other: [count] / $[value]

By GC (top 10):
- [GC Name]: [count] bids, $[total value], [win rate if known]

Trend indicators:
- Bids received this week vs. last week
- Average estimated project size trend
- Go rate percentage trend
```

#### Sheet 4: Bid Calendar

```
Calendar view of upcoming bid dates:
- This week: [list with key details]
- Next week: [list]
- 2-4 weeks out: [list]
- Beyond 4 weeks: [list]

Pre-bid meetings scheduled:
- [Date] [Time] [Project] [Location] [Mandatory?]
```

### Strategic Summary (for Tuesday Meeting)

```markdown
# Huston Electric — Bid Intelligence Report
## Week of [Date]

---

### This Week at a Glance

- **New bids received:** [X] projects, $[total] estimated value
- **Bids due this week:** [X] projects
- **Recommended to pursue:** [X] of [total] new opportunities
- **Top opportunity:** [Project Name] — $[Value] — [Why it matters]

---

### Priority Opportunities (Go Recommendations)

#### 1. [Project Name] — $[Estimated Value]
- **GC:** [Name] | **Owner:** [Name]
- **Location:** [City, County] | **Local:** [IBEW Local]
- **Bid Date:** [Date]
- **Why pursue:** [2-3 sentence strategic rationale]
- **Key risks:** [Primary risk factors]
- **Assigned to:** [Estimator name]

#### 2. [Project Name] — $[Estimated Value]
[Same structure]

#### 3. [Project Name] — $[Estimated Value]
[Same structure]

---

### Conditional Opportunities (Needs Discussion)

These bids have merit but require team discussion:

| Project | Value | GC | Issue to Discuss |
|---------|-------|----|-----------------|
| [Name] | $[X] | [GC] | [Capacity concern / scope ambiguity / etc.] |

---

### Declined Opportunities (No-Go)

| Project | Value | GC | Reason |
|---------|-------|----|--------|
| [Name] | $[X] | [GC] | [Brief rationale] |

---

### Action Items

1. [ ] [Estimator]: Begin takeoff on [Project] — bid due [Date]
2. [ ] [PM]: Attend pre-bid meeting for [Project] — [Date/Time]
3. [ ] [Management]: Decision needed on [Conditional project]
4. [ ] [Admin]: Request plans for [Project] from [Plan Room]

---

### Market Notes

- [Any notable market trends observed this week]
- [New GCs entering the market]
- [Large projects coming to market soon]
- [Competitor intelligence from bid results]
```

### Priority Ranking Methodology

Opportunities are ranked using a weighted composite score:

```
Priority Score = (Strategic Fit x 0.30) + (Value x 0.25) +
                 (Win Probability x 0.25) + (Timing x 0.20)

Strategic Fit:
  5 = Target sector + preferred GC + primary territory
  4 = Target sector + known GC
  3 = Good scope fit, new GC relationship opportunity
  2 = Marginal fit, outside core competency
  1 = Poor fit, outside service area

Value:
  5 = Over $5M (major project)
  4 = $1M - $5M (large project)
  3 = $500K - $1M (medium-large project)
  2 = $250K - $500K (medium project)
  1 = Under $250K (small project)

Win Probability:
  5 = Sole source / pre-negotiated
  4 = Strong GC relationship + limited competition
  3 = Competitive but well-positioned
  2 = Highly competitive, many bidders
  1 = Long shot, unfamiliar territory

Timing:
  5 = Fills schedule gap perfectly
  4 = Good timing with current backlog
  3 = Manageable with existing commitments
  2 = Tight — would strain resources
  1 = Conflicts with existing commitments
```

---

## Execution Flow

### Step 1: Gather Bid Emails

**If email connected:**
```
1. Scan inbox for unprocessed bid-related emails
   - Filter by subject line patterns (see Email Parsing Patterns)
   - Filter by known sender domains (GCs, plan rooms)
   - Check for addenda on previously tracked projects
   - Mark processed emails to avoid duplicates

2. Pull email metadata and body content
   - From, To, Date, Subject
   - Full body text (HTML and plain text)
   - Attachments list (plans, specs, bid forms)
```

**If no email connected:**
```
Ask user:
1. "Forward bid invitation emails to me, or paste the content"
2. "How many new bids came in this week?"
3. "Any addenda or changes to existing bids?"

Accept:
- Pasted email text
- Forwarded email content
- Manual description of opportunities
- Uploaded bid documents (PDF, Word)
```

### Step 2: Parse and Extract

```
For each bid email:

1. Identify email type (invitation, plan room, addendum, result)

2. Extract structured fields:
   - Project Name → clean, standardized format
   - General Contractor → standardize company name
   - Owner/Client → identify end client
   - Location → full address, city, county, state
   - Bid Date → standardized date + time + timezone
   - Scope → summarize electrical scope from description
   - Estimated Value → extract or estimate from scope/size
   - Pre-Bid Meeting → date, time, location, mandatory flag
   - Bond Requirements → bid bond, performance bond, amounts
   - Prevailing Wage → yes/no, Davis-Bacon, state prevailing wage
   - Plan Availability → where to get plans, access method
   - Contact → name, phone, email for questions

3. Handle ambiguity:
   - If project name unclear → use building + location
   - If value not stated → estimate from scope description
   - If GC not clear → note "Owner Direct" or "TBD"
   - If bid date missing → flag as "Date TBD — follow up"
```

### Step 3: Classify by Union Jurisdiction

```
1. Parse project location
2. Determine county and municipality
3. Look up IBEW local from jurisdiction map
4. Pull jurisdiction-specific considerations:
   - Labor rate tier
   - Travel/subsistence requirements
   - Manpower availability notes
   - Special agreements or work rules
5. Flag if project spans multiple jurisdictions
```

### Step 4: Assess and Score

```
For each bid:

1. Run complexity scoring (5 factors, 1-5 each)
2. Check license/certification requirements
3. Run Go/No-Go decision matrix
4. Calculate priority ranking score
5. Check for automatic triggers (Go or No-Go)
6. Generate recommendation with rationale
```

### Step 5: Check Historical Data (If Knowledge Base Connected)

```
1. Search for previous bids to same GC
   - Win/loss record
   - Relationship quality notes
   - Payment history

2. Search for similar project types
   - Historical pricing benchmarks
   - Lessons learned
   - Change order experience

3. Search for location-specific history
   - Previous work in same area
   - Known site conditions
   - Local authority requirements
```

### Step 6: Generate Outputs

```
1. Build Excel workbook
   - Sheet 1: Bid Intelligence Summary (all bids, sorted by priority)
   - Sheet 2: By Union Territory (grouped by IBEW local)
   - Sheet 3: Strategic Dashboard (summary statistics)
   - Sheet 4: Bid Calendar (timeline view)
   - Apply formatting, conditional highlighting, freeze panes

2. Write strategic summary
   - This Week at a Glance
   - Priority Opportunities (Go)
   - Conditional Opportunities (discuss)
   - Declined Opportunities (No-Go)
   - Action items with assignees
   - Market notes

3. Generate priority ranking
   - Ordered list of Go recommendations
   - Composite score breakdown
   - Key differentiating factors

4. Create calendar entries (if calendar connected)
   - Bid due dates
   - Pre-bid meetings
   - Estimating deadlines (bid date minus prep time)
```

### Step 7: Distribute (If Chat Connected)

```
1. Post summary to estimating team channel
2. Tag relevant estimators on assigned bids
3. Flag urgent items (bids due within 48 hours)
4. Share link to full Excel report
```

---

## Configuration

### Company Profile

```yaml
company:
  name: "Huston Electric, Inc."
  office_address: "[Address]"
  licenses:
    - type: "Electrical Contractor"
      number: "[License #]"
      state: "[State]"
      expiration: "[Date]"
    - type: "Low Voltage"
      number: "[License #]"
      state: "[State]"
      expiration: "[Date]"
    - type: "Fire Alarm"
      number: "[License #]"
      state: "[State]"
      expiration: "[Date]"
  bonding:
    single_project_limit: 5000000
    aggregate_limit: 15000000
    bonding_company: "[Name]"
  insurance:
    general_liability: 2000000
    umbrella: 10000000
    workers_comp: "Statutory"
  emr: 0.85
  prequalifications:
    - "[Owner/GC 1]"
    - "[Owner/GC 2]"
```

### Union Locals

```yaml
union_locals:
  - local: "IBEW Local 134"
    territory_description: "City of Chicago and Cook County"
    counties: ["Cook"]
    journeyman_rate: "[Rate]"
    foreman_rate: "[Rate]"
    apprentice_ratio: "1:1"
    manpower_status: "adequate"
    relationship_quality: "strong"
    notes: "Primary territory"

  - local: "IBEW Local 701"
    territory_description: "Suburban collar counties"
    counties: ["DuPage", "Kane", "Kendall", "Will"]
    journeyman_rate: "[Rate]"
    foreman_rate: "[Rate]"
    apprentice_ratio: "1:1"
    manpower_status: "adequate"
    relationship_quality: "good"
    notes: "Growing suburban market"
```

### Strategic Priorities

```yaml
strategic_priorities:
  target_sectors:
    - name: "Healthcare"
      priority: 1
      notes: "Growth sector, high margins, repeat clients"
    - name: "Education"
      priority: 2
      notes: "Steady volume, public funding, prevailing wage"
    - name: "Data Centers"
      priority: 3
      notes: "Large projects, technical differentiation"
    - name: "Municipal"
      priority: 4
      notes: "Stable work, PLA advantage"

  preferred_gcs:
    - name: "Turner Construction"
      relationship: "strong"
      win_rate: "40%"
    - name: "Walsh Group"
      relationship: "strong"
      win_rate: "35%"
    - name: "Pepper Construction"
      relationship: "good"
      win_rate: "30%"

  avoid_list:
    gcs: []
    owners: []
    reasons: {}

  value_range:
    minimum: 100000
    sweet_spot_low: 500000
    sweet_spot_high: 5000000
    maximum: 10000000

  capacity:
    current_backlog: "[Dollar amount]"
    available_manpower: "[Number of electricians]"
    estimating_bandwidth: "[Number of bids per week]"
```

### Email Sender Whitelist

```yaml
known_senders:
  general_contractors:
    - domain: "turnerconstruction.com"
      company: "Turner Construction"
    - domain: "walshgroup.com"
      company: "Walsh Group"
    - domain: "pepperconstruction.com"
      company: "Pepper Construction"

  plan_rooms:
    - domain: "isqft.com"
      service: "iSqFt"
    - domain: "buildingconnected.com"
      service: "BuildingConnected"
    - domain: "construction.com"
      service: "Dodge Construction Network"
    - domain: "smartbidnet.com"
      service: "SmartBidNet"
    - domain: "planhub.com"
      service: "PlanHub"

  owners:
    - domain: "[owner domain]"
      name: "[Owner Name]"
```

---

## Tips

1. **Process emails daily** — Do not let bid invitations pile up. A missed bid date cannot be recovered.
2. **Update results religiously** — Win/loss data is what makes the Go/No-Go engine smarter over time.
3. **Be honest about No-Go** — Declining a bad-fit bid frees estimating time for better opportunities.
4. **Track addenda carefully** — Scope changes in addenda can flip a No-Go to a Go, or vice versa.
5. **Review the Tuesday report Monday afternoon** — Give yourself time to add context before the meeting.
6. **Calibrate union jurisdiction data** — Labor rates and manpower availability change. Update quarterly.
7. **Log competitor intel from bid results** — Every bid tabulation is market intelligence.

---

## Related Skills

- **bid-strategy** — Deep analysis of market conditions, competitive landscape, and strategic positioning for specific bid opportunities
