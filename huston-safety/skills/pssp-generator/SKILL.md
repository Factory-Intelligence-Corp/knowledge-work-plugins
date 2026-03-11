---
name: pssp-generator
description: "PSSP Pete — autonomous Project-Specific Safety Plan generator for Huston Electric, Inc. Ingests project details, retrieves safety data from knowledge bases, references past PSSPs, applies OSHA/NFPA/NEC standards, performs Job Hazard Analysis, generates risk assessments, and produces complete formatted PSSPs. Trigger with 'create a PSSP', 'generate a safety plan for', 'I need a project safety plan', 'PSSP for [project]', or 'site-specific safety plan'."
---

# PSSP Pete — Safety Team

Your autonomous Project-Specific Safety Plan generator for Huston Electric, Inc. PSSP Pete ingests project details, identifies site-specific hazards, references past plans for similar projects, applies OSHA/NFPA/NEC standards, performs risk assessments, and produces a complete, formatted, ready-to-sign PSSP.

---

## Overview

Every Huston Electric project requires a Project-Specific Safety Plan (PSSP) before work begins. PSSP Pete automates the creation of these plans by:

1. **Gathering project details** — scope, location, voltage levels, duration, workforce, client requirements
2. **Identifying site-specific hazards** — electrical, environmental, physical, chemical, and situational hazards unique to the project
3. **Referencing past PSSPs** — finding similar projects in the knowledge base and applying lessons learned
4. **Applying regulatory standards** — mapping OSHA, NFPA 70E, NEC, and IEEE requirements to project specifics
5. **Generating risk assessments** — probability x severity matrix with risk rankings for all identified hazards
6. **Creating control measures** — hierarchy of controls (elimination, substitution, engineering, administrative, PPE)
7. **Formatting the complete PSSP** — ready for review, approval, and distribution

---

## How It Works

```
┌─────────────────────────────────────────────────────────────────┐
│                        PSSP PETE                                  │
├─────────────────────────────────────────────────────────────────┤
│  ALWAYS (works standalone)                                       │
│  + You provide: project details, scope, location, voltage        │
│  + Web search: local codes, client safety requirements           │
│  + Standards: OSHA, NFPA 70E, NEC, IEEE 1584                    │
│  + JHA methodology: systematic hazard identification             │
│  + Risk assessment: probability x severity matrix                │
│  + Output: complete, formatted PSSP document                     │
├─────────────────────────────────────────────────────────────────┤
│  SUPERCHARGED (when you connect your tools)                      │
│  + Knowledge base: past PSSPs, incident history, equipment       │
│    data, company SOPs, subcontractor records                     │
│  + Document storage: project specs, site drawings, client        │
│    safety requirements, contract documents                       │
│  + Email: distribute completed PSSP, notify stakeholders         │
│  + Chat: coordinate reviews, notify project teams                │
│  + Calendar: schedule PSSP review meetings, safety orientations  │
└─────────────────────────────────────────────────────────────────┘
```

---

## Connectors (Optional)

| Connector | What It Adds |
|-----------|--------------|
| **Knowledge base** | Past PSSPs for similar project types, incident history at similar sites, equipment specifications, company SOPs, subcontractor safety records |
| **Document storage** | Project specifications, site drawings, client safety manuals, contract safety requirements, arc flash studies |
| **Email** | Distribute completed PSSPs, send for client review/approval, notify subcontractors of requirements |
| **Chat** | Notify project team when PSSP is ready for review, coordinate approvals, share updates |
| **Calendar** | Schedule PSSP review meetings, project safety orientations, site safety inspections |

> **No connectors?** No problem. Provide the project details and PSSP Pete generates a complete plan using regulatory standards and best practices.

---

## Getting Started

When you invoke PSSP Pete, provide the following:

**Required:**
| Field | Description | Example |
|-------|-------------|---------|
| Project name | Name or identifier | "Maple Street Office Building" |
| Project location | Address and site description | "1200 Maple St, Suite 300, Nashville TN" |
| Scope of work | What electrical work is being performed | "Complete electrical fit-out including power distribution, lighting, fire alarm" |
| Voltage levels | Maximum voltage on the project | "277/480V 3-phase, 120/208V 3-phase" |
| Project duration | Estimated start and end dates | "March 2026 - September 2026" |

**Helpful if you have it:**
| Field | Description |
|-------|-------------|
| Client name | General contractor or building owner |
| Client safety requirements | Any client-specific safety rules beyond OSHA |
| Estimated workforce | Number of Huston Electric workers on site |
| Subcontractors | Any electrical subcontractors on the project |
| Special conditions | Confined spaces, elevated work, live work, hazmat areas |
| Site drawings/specs | Upload project documents for more specific hazard identification |
| Past similar project | "This is like the Oak Avenue project we did last year" |

---

## Output Format — Complete PSSP

```markdown
# PROJECT-SPECIFIC SAFETY PLAN (PSSP)

## HUSTON ELECTRIC, INC.

---

### Document Control

| Field | Value |
|-------|-------|
| **Document No.** | PSSP-[YYYY]-[XXX] |
| **Project Name** | [Project Name] |
| **Project Number** | [Project Number] |
| **Revision** | [X.X] |
| **Prepared By** | [Name / Title] |
| **Reviewed By** | [Safety Director] |
| **Approved By** | [Project Manager] |
| **Effective Date** | [Date] |
| **Review Date** | [90 days from effective or as required] |

---

### Table of Contents

1. Project Information
2. Safety Policy Statement
3. Project Safety Organization
4. Site-Specific Hazard Identification
5. Risk Assessment Matrix
6. Control Measures and Hierarchy
7. Electrical Safety Program
8. Lockout/Tagout Program
9. Arc Flash Safety
10. Personal Protective Equipment
11. Training Requirements
12. Emergency Procedures
13. Site Safety Rules
14. Subcontractor Safety Requirements
15. Incident Reporting and Investigation
16. Safety Inspections and Audits
17. Document Control and Revisions
18. Acknowledgment and Signature Pages

---

### 1. Project Information

| Field | Details |
|-------|---------|
| **Project Name** | [Name] |
| **Project Number** | [Number] |
| **Project Address** | [Full address] |
| **Client/GC** | [Client name and contact] |
| **Project Manager** | [Name, phone, email] |
| **Site Superintendent** | [Name, phone, email] |
| **Safety Director** | [Name, phone, email] |
| **Competent Person(s)** | [Names and qualifications] |
| **Scope of Work** | [Detailed description] |
| **Contract Value** | [If applicable] |
| **Start Date** | [Date] |
| **Completion Date** | [Date] |
| **Work Hours** | [Standard hours, overtime provisions] |
| **Maximum Workers on Site** | [Number] |
| **Voltage Levels** | [All voltage levels present] |
| **Available Fault Current** | [If known, for arc flash assessment] |

**Project Description:**
[Detailed narrative description of the project, including phases of work, major systems being installed, and any unique project characteristics]

---

### 2. Safety Policy Statement

Huston Electric, Inc. is committed to providing a safe and healthful workplace for all employees, subcontractors, and visitors. No job is so important and no deadline so urgent that we cannot take the time to perform our work safely.

**Our safety commitments:**
- Every worker has the right and responsibility to stop work if conditions are unsafe
- Safety is a condition of employment — compliance with this PSSP and all applicable regulations is mandatory
- All incidents, injuries, and near-misses will be reported, investigated, and corrected
- Safety training will be provided before any worker performs a new or unfamiliar task
- Regular safety inspections and audits will be conducted throughout the project
- Continuous improvement of our safety program through lessons learned

**Stop Work Authority:** Every Huston Electric employee and subcontractor has the authority and obligation to stop work immediately when an imminent danger is identified. No worker will face retaliation for exercising stop work authority.

---

### 3. Project Safety Organization

```
[Project Manager]
    ├── [Safety Director] — Overall safety program oversight
    │   ├── [Site Safety Representative] — Day-to-day safety
    │   └── [Safety Committee] — Weekly safety reviews
    ├── [Site Superintendent] — Field operations and safety compliance
    │   ├── [Foreman 1] — Crew safety leader
    │   ├── [Foreman 2] — Crew safety leader
    │   └── [Foreman N] — Crew safety leader
    └── [Subcontractor Safety Contacts]
```

**Roles and Responsibilities:**

| Role | Safety Responsibilities |
|------|------------------------|
| **Project Manager** | Overall PSSP implementation, resource allocation, management reviews |
| **Safety Director** | PSSP development and updates, regulatory compliance, incident investigation, training oversight |
| **Site Superintendent** | Daily safety implementation, toolbox talks, hazard correction, worker compliance |
| **Foreman** | Pre-task safety briefings, crew PPE compliance, hazard identification, near-miss reporting |
| **All Workers** | Follow PSSP requirements, report hazards, participate in safety meetings, use required PPE |

---

### 4. Site-Specific Hazard Identification

#### 4.1 Electrical Hazards

| Hazard | Source | Location | Voltage/Energy |
|--------|--------|----------|----------------|
| Electric shock | [Source] | [Location] | [V/A] |
| Arc flash | [Source] | [Location] | [cal/cm2 if known] |
| Arc blast | [Source] | [Location] | [Pressure wave] |
| Induced voltage | [Source] | [Location] | [V] |
| Static electricity | [Source] | [Location] | — |
| Lightning | Outdoor work | [Areas] | — |

#### 4.2 Physical Hazards

| Hazard | Source | Location |
|--------|--------|----------|
| Falls from height | [Ladders, scaffolds, lifts, openings] | [Areas] |
| Struck by | [Overhead work, material handling, cranes] | [Areas] |
| Caught in/between | [Rotating equipment, pinch points] | [Areas] |
| Slips/trips | [Wet surfaces, uneven terrain, cords, debris] | [Areas] |
| Noise exposure | [Generators, power tools, construction activity] | [Areas] |
| Heat stress | [Hot environments, outdoor summer work] | [Areas] |
| Cold stress | [Cold environments, outdoor winter work] | [Areas] |
| Confined spaces | [Manholes, vaults, crawl spaces, attics] | [Areas] |

#### 4.3 Chemical Hazards

| Hazard | Source | Location |
|--------|--------|----------|
| Lead exposure | [Old paint, solder, batteries] | [Areas] |
| Asbestos | [Existing building materials] | [Areas] |
| Silica dust | [Concrete cutting, core drilling] | [Areas] |
| Solvents/adhesives | [Wire pulling compound, PVC cement, contact cleaner] | [Areas] |
| Battery acid | [UPS systems, emergency lighting] | [Areas] |

#### 4.4 Environmental/Situational Hazards

| Hazard | Source | Location |
|--------|--------|----------|
| Weather exposure | [Outdoor work areas] | [Areas] |
| Traffic/vehicles | [Active roadways, parking areas, loading docks] | [Areas] |
| Public interaction | [Occupied buildings, active facilities] | [Areas] |
| Multi-employer site | [Other trades working simultaneously] | [Areas] |
| Overhead utilities | [Power lines near work areas] | [Areas] |
| Underground utilities | [Buried cables, conduits near excavation] | [Areas] |

---

### 5. Risk Assessment Matrix

#### 5.1 Risk Assessment Methodology

**Probability Rating:**

| Rating | Description | Definition |
|--------|-------------|------------|
| 5 | Almost Certain | Expected to occur during the project |
| 4 | Likely | Will probably occur during the project |
| 3 | Possible | Might occur during the project |
| 2 | Unlikely | Not expected but possible |
| 1 | Rare | Could occur but highly unlikely |

**Severity Rating:**

| Rating | Description | Definition |
|--------|-------------|------------|
| 5 | Catastrophic | Fatality or permanent total disability |
| 4 | Major | Permanent partial disability or hospitalization |
| 3 | Moderate | Lost time injury, restricted duty |
| 2 | Minor | First aid, medical treatment, no lost time |
| 1 | Negligible | Near miss, no injury |

**Risk Score = Probability x Severity**

| Risk Score | Risk Level | Action Required |
|------------|------------|-----------------|
| 20-25 | **Critical** | Work must NOT proceed without additional controls — Safety Director approval required |
| 12-19 | **High** | Significant controls required — detailed JHA, specific procedures, additional PPE |
| 6-11 | **Medium** | Standard controls — follow established procedures and PPE requirements |
| 1-5 | **Low** | Routine precautions — standard safe work practices |

#### 5.2 Risk Assessment for This Project

| ID | Hazard | Probability | Severity | Risk Score | Risk Level | Primary Control |
|----|--------|-------------|----------|------------|------------|-----------------|
| H-01 | [Hazard] | [1-5] | [1-5] | [Score] | [Level] | [Control measure] |
| H-02 | [Hazard] | [1-5] | [1-5] | [Score] | [Level] | [Control measure] |
| ... | ... | ... | ... | ... | ... | ... |

---

### 6. Control Measures and Hierarchy

For each identified hazard, controls are applied using the Hierarchy of Controls:

```
┌─────────────────────────┐
│  1. ELIMINATION         │ ← Most effective
│  Remove the hazard      │
├─────────────────────────┤
│  2. SUBSTITUTION        │
│  Replace with less      │
│  hazardous alternative  │
├─────────────────────────┤
│  3. ENGINEERING         │
│  CONTROLS               │
│  Isolate/guard hazard   │
├─────────────────────────┤
│  4. ADMINISTRATIVE      │
│  CONTROLS               │
│  Procedures, training,  │
│  warning signs          │
├─────────────────────────┤
│  5. PPE                 │ ← Least effective (last resort)
│  Personal protective    │
│  equipment              │
└─────────────────────────┘
```

#### Control Measures by Hazard

| Hazard ID | Elimination | Substitution | Engineering | Administrative | PPE |
|-----------|-------------|--------------|-------------|----------------|-----|
| H-01 | [If possible] | [If possible] | [Controls] | [Procedures] | [Required PPE] |
| H-02 | [If possible] | [If possible] | [Controls] | [Procedures] | [Required PPE] |

---

### 7. Electrical Safety Program

Per NFPA 70E Article 110.5, the following electrical safety program applies to this project:

**7.1 Electrically Safe Work Condition**
- All electrical work shall be performed in an electrically safe work condition per NFPA 70E Article 120 unless an Energized Electrical Work Permit is issued
- Establishing an electrically safe work condition requires: disconnect, lockout/tagout, verify zero energy, ground (if necessary)

**7.2 Energized Electrical Work**
- Energized work is permitted ONLY when de-energizing creates greater hazard or is infeasible
- An Energized Electrical Work Permit (EEWP) must be completed per NFPA 70E 130.2(B)
- The EEWP must be approved by [Safety Director / Project Manager]
- Arc flash risk assessment and shock hazard analysis required before energized work
- Appropriate PPE category must be determined and worn

**7.3 Approach Boundaries**
Per NFPA 70E Table 130.4(E)(a) for the voltages on this project:

| Voltage | Limited Approach | Restricted Approach | Prohibited Approach |
|---------|-----------------|--------------------|--------------------|
| [V] | [Distance] | [Distance] | [Distance] |

**7.4 Working Space**
Per NEC Article 110.26, minimum working space for this project:

| Voltage | Condition | Depth | Width | Height |
|---------|-----------|-------|-------|--------|
| [V] | [1/2/3] | [Distance] | [Distance] | [Distance] |

---

### 8. Lockout/Tagout Program

Per OSHA 29 CFR 1910.147 and NFPA 70E Article 120:

**8.1 LOTO Requirements**
- Equipment-specific LOTO procedures shall be developed for all equipment on this project
- Only authorized employees shall perform LOTO
- Affected employees shall be notified before and after LOTO application/removal
- Each authorized employee shall apply their own personal lock and tag
- Locks shall not be removed by anyone other than the person who applied them (except emergency removal per company procedure)

**8.2 LOTO Equipment Required**
- [ ] Individual padlocks (one per authorized employee) — keyed differently
- [ ] Lockout hasps (multi-lock) for group lockout
- [ ] Lockout tags — "DANGER — DO NOT OPERATE"
- [ ] Circuit breaker lockout devices
- [ ] Valve lockout devices (if applicable)
- [ ] Plug lockout devices
- [ ] Group lockbox (if applicable)

**8.3 Verification**
- After LOTO, verify zero energy state by attempting to operate equipment
- Use voltage tester to verify de-energized state
- Test voltage tester on known live source before AND after verification (live-dead-live)
- Check for stored energy (capacitors, springs, gravity, pressure) and dissipate

---

### 9. Arc Flash Safety

**9.1 Arc Flash Risk Assessment**
Per NFPA 70E 130.5, an arc flash risk assessment shall be performed before any worker approaches exposed energized electrical conductors or circuit parts.

**9.2 Arc Flash PPE Requirements for This Project**

| Equipment | Voltage | PPE Category | Min Arc Rating | Arc Flash Boundary |
|-----------|---------|-------------|----------------|-------------------|
| [Equipment] | [V] | [0-4] | [cal/cm2] | [Distance] |

**9.3 Arc Flash Labels**
- All electrical equipment on this project shall have arc flash warning labels per NFPA 70E 130.5(H)
- Labels shall include: incident energy, arc flash boundary, PPE category, and approach boundaries
- Where arc flash study data is not available, the NFPA 70E Table Method shall be used

---

### 10. Personal Protective Equipment

**10.1 Minimum PPE — All Workers at All Times**
- [ ] Hard hat (ANSI Z89.1 Class E)
- [ ] Safety glasses (ANSI Z87.1)
- [ ] High-visibility vest (ANSI/ISEA 107 Class 2 minimum)
- [ ] Work boots (ASTM F2413 — EH rated)
- [ ] Long pants (no shorts)
- [ ] Shirt with sleeves (no tank tops)

**10.2 Task-Specific PPE**

| Task | Additional PPE Required |
|------|------------------------|
| Electrical work (energized) | Arc-rated clothing per PPE category, rubber insulating gloves with protectors, face shield/hood |
| Electrical work (de-energized, LOTO) | Voltage-rated gloves for verification, safety glasses |
| Overhead work | Face shield for drilling/cutting |
| Concrete cutting/drilling | Respirator (N95 minimum for silica), face shield, hearing protection |
| Elevated work (>6 ft) | Full body harness, shock-absorbing lanyard, tie-off point |
| Confined space entry | As specified in confined space permit — may include SCBA/SAR, gas monitor |
| Welding/brazing | Welding helmet, leather gloves, fire-resistant clothing |
| Battery work | Chemical splash goggles, face shield, acid-resistant gloves and apron |

**10.3 PPE Inspection**
- All PPE shall be inspected before each use
- Rubber insulating gloves: visual inspection before each use, electrical testing per ASTM F496 schedule
- Arc-rated clothing: inspect for damage, contamination, and proper arc rating
- Fall protection: inspect harness, lanyard, and connectors per manufacturer instructions
- Damaged PPE shall be removed from service immediately

---

### 11. Training Requirements

**11.1 Required Training — Before Starting Work**

| Training | Who | Frequency | Documentation |
|----------|-----|-----------|---------------|
| PSSP orientation | All workers | Project start | Sign-in sheet |
| OSHA 10-Hour Construction | All workers | Valid card | Card copy on file |
| OSHA 30-Hour Construction | Foremen and above | Valid card | Card copy on file |
| Electrical safety (qualified person) | Electricians | Annual | Training record |
| Arc flash safety | All electrical workers | Annual | Training record |
| LOTO — authorized person | Workers performing LOTO | Annual + equipment-specific | Training record |
| CPR/First Aid/AED | Minimum 1 per crew | Current certification | Card copy on file |
| Fall protection | Workers at heights >6 ft | Annual | Training record |
| Confined space entry | Workers entering confined spaces | Annual | Training record |
| Hazard communication | All workers | Initial + as needed | Training record |
| Fire extinguisher | All workers | Annual | Training record |

**11.2 Site-Specific Training**

| Training | Content | Who | When |
|----------|---------|-----|------|
| Site orientation | Site layout, emergency exits, assembly point, site rules | All | First day on site |
| [Client] safety orientation | Client-specific safety requirements | All | Before site access |
| [Hazard]-specific | [Details for project-specific hazards] | [Affected workers] | Before task |

**11.3 Ongoing Training**
- Weekly toolbox talks (documented with sign-in)
- Pre-task briefings (daily or when tasks change)
- Post-incident safety stand-downs (when incidents occur)
- New hazard awareness (when new hazards identified)

---

### 12. Emergency Procedures

**12.1 Emergency Contact Information**

| Contact | Name | Phone |
|---------|------|-------|
| Emergency Services | 911 | 911 |
| Huston Electric Safety Director | [Name] | [Phone] |
| Project Manager | [Name] | [Phone] |
| Site Superintendent | [Name] | [Phone] |
| Client/GC Safety | [Name] | [Phone] |
| Nearest Hospital | [Hospital name and address] | [Phone] |
| Poison Control | — | 1-800-222-1222 |
| Utility Emergency | [Utility name] | [Phone] |
| OSHA (reporting) | — | 1-800-321-OSHA |

**12.2 Emergency Assembly Point**
- Location: [Specific location on site, away from buildings and traffic]
- Alternate: [Backup location if primary is blocked]

**12.3 Emergency Procedures**

**Electrical Contact/Shock:**
1. Do NOT touch the victim if still in contact with energized source
2. De-energize the circuit if possible (use non-conductive device to separate if needed)
3. Call 911 immediately
4. Begin CPR/AED if victim is unresponsive and not breathing
5. Notify Huston Electric Safety Director
6. Secure the area — do not disturb the scene

**Arc Flash/Electrical Burn:**
1. Call 911 immediately
2. Move victim to safe area if still near hazard
3. Do NOT remove clothing adhered to burns
4. Cool burns with clean, cool water
5. Cover with sterile, non-fluffy dressings
6. Treat for shock — keep warm, elevate legs
7. Notify Huston Electric Safety Director

**Fire:**
1. Sound the alarm and alert all personnel
2. Call 911
3. Attempt to extinguish ONLY if safe (small, contained fire)
4. Use Class C extinguisher for electrical fires — NEVER use water
5. Evacuate to emergency assembly point
6. Account for all personnel
7. Do not re-enter until cleared by fire department

**Medical Emergency:**
1. Call 911
2. Provide first aid within your training level
3. Do NOT move the injured person unless immediate danger exists
4. Send someone to guide emergency vehicles to the scene
5. Notify Huston Electric Safety Director

**Severe Weather:**
1. Monitor weather forecasts daily
2. Suspend outdoor work when lightning is within 10 miles
3. Seek shelter in substantial building or hard-topped vehicle
4. Wait 30 minutes after last lightning/thunder before resuming outdoor work
5. Suspend work in high winds per task-specific requirements

**12.4 Emergency Equipment**

| Equipment | Location | Responsible Person |
|-----------|----------|--------------------|
| First aid kit | [Location] | [Name] |
| AED | [Location] | [Name] |
| Fire extinguishers (Class ABC and C) | [Locations] | [Name] |
| Spill kit | [Location] | [Name] |
| Emergency eyewash | [Location] | [Name] |
| Rescue equipment (electrical) | [Location] | [Name] |

---

### 13. Site Safety Rules

1. **All workers** must attend site safety orientation before beginning work
2. **PPE** — minimum PPE required at all times in work areas (hard hat, safety glasses, hi-vis, EH-rated boots)
3. **Housekeeping** — keep work areas clean and organized; cords managed, scrap collected daily
4. **Reporting** — all injuries, incidents, near-misses, and hazards must be reported immediately to supervisor
5. **Impairment** — zero tolerance for drugs and alcohol; workers must report prescription medications that may cause impairment
6. **Fall protection** — required at 6 feet (construction) or as specified by client requirements
7. **LOTO** — mandatory for all equipment servicing and maintenance; no exceptions
8. **Energized work** — prohibited without an approved Energized Electrical Work Permit
9. **Ladders** — inspect before use, 3-point contact, 4:1 ratio, secured at top
10. **Excavation** — call 811 before any digging; utility locates required
11. **Barricades** — open panels, floor openings, overhead hazards must be barricaded and signed
12. **Visitors** — all visitors must check in, receive orientation, be escorted, and wear minimum PPE
13. **Cell phones** — no cell phone use while operating equipment, on ladders, or in electrical rooms
14. **Horseplay** — zero tolerance; immediate removal from site
15. **Stop work authority** — every worker has the right and responsibility to stop unsafe work

---

### 14. Subcontractor Safety Requirements

**14.1 Prequalification**
All subcontractors must provide before mobilization:
- [ ] Written safety program
- [ ] OSHA 300 logs (3 years)
- [ ] EMR (Experience Modification Rate) — must be below 1.0
- [ ] Proof of insurance (GL, WC, auto, umbrella)
- [ ] OSHA training documentation for all workers
- [ ] Competent person designations

**14.2 Subcontractor Obligations**
- Comply with this PSSP and all applicable regulations
- Attend Huston Electric project safety orientation
- Participate in weekly safety meetings
- Report all incidents, injuries, and near-misses to Huston Electric immediately
- Provide task-specific JHAs for their scope of work
- Maintain their own PPE and safety equipment
- Accept Huston Electric's right to stop their work for safety violations

**14.3 Multi-Employer Responsibilities**
Per OSHA multi-employer citation policy, Huston Electric as controlling/creating employer will:
- Communicate hazards created by our work to other employers
- Coordinate safety activities with the GC and other trades
- Correct hazards we create or control
- Ensure our subcontractors comply with OSHA standards

---

### 15. Incident Reporting and Investigation

**15.1 Reporting Requirements**

| Incident Type | Report To | When |
|---------------|-----------|------|
| Fatality | OSHA, Safety Director, PM | Within 8 hours (OSHA) |
| Hospitalization, amputation, eye loss | OSHA, Safety Director, PM | Within 24 hours (OSHA) |
| Lost time injury | Safety Director, PM | Immediately |
| Medical treatment | Safety Director, PM | Immediately |
| First aid | Supervisor, Safety Director | Same day |
| Near miss | Supervisor, Safety Director | Same day |
| Property damage | Supervisor, PM | Same day |

**15.2 Investigation**
All incidents (including near-misses) will be investigated to determine:
- Direct cause(s)
- Contributing factors
- Root cause(s)
- Corrective actions (immediate and preventive)

**15.3 Documentation**
- Incident reports completed within 24 hours
- OSHA 300 log updated within 7 days
- Corrective actions tracked to completion
- Lessons learned shared at next safety meeting

---

### 16. Safety Inspections and Audits

| Inspection Type | Frequency | Conducted By | Documentation |
|-----------------|-----------|--------------|---------------|
| Daily hazard assessment | Daily | Foreman | Daily safety log |
| Weekly site inspection | Weekly | Site Superintendent | Inspection checklist |
| Monthly safety audit | Monthly | Safety Director | Audit report |
| PPE inspection | Before each use | Individual worker | By exception (report damage) |
| LOTO audit | Quarterly | Safety Director | Audit report |
| Fire extinguisher inspection | Monthly | Designated person | Inspection tag |
| First aid kit inspection | Weekly | Designated person | Inspection log |
| Tool and equipment inspection | Before each use | User | By exception |
| Electrical test equipment | Per ASTM schedule | Designated person | Calibration/test records |

---

### 17. Document Control and Revisions

| Rev | Date | Author | Description | Approved By |
|-----|------|--------|-------------|-------------|
| 1.0 | [Date] | [Name] | Initial PSSP | [Name] |

**Review Schedule:**
- This PSSP shall be reviewed every 90 days or when:
  - Scope of work changes significantly
  - New hazards are identified
  - An incident occurs requiring procedure changes
  - Regulatory changes affect the project
  - Client requirements change

---

### 18. Acknowledgment and Signature Pages

#### 18.1 PSSP Approval

| Role | Name | Signature | Date |
|------|------|-----------|------|
| **Prepared By** | | | |
| **Safety Director** | | | |
| **Project Manager** | | | |
| **Client/GC Approval** (if required) | | | |

#### 18.2 Worker Acknowledgment

I have received, read, and understand this Project-Specific Safety Plan. I agree to comply with all requirements contained herein. I understand that I have the right and responsibility to stop work if I observe unsafe conditions.

| Name (Print) | Signature | Company | Date |
|--------------|-----------|---------|------|
| | | | |
| | | | |
| | | | |
| | | | |
| | | | |
| | | | |
| | | | |
| | | | |
| | | | |
| | | | |
```

---

## Execution Flow

### Step 1: Gather Project Details

**If connectors available:**
```
1. Knowledge base → Search for project record
   - Pull: project scope, location, client, workforce size
   - Pull: client-specific safety requirements

2. Document storage → Find project documents
   - Pull: specifications, drawings, contract safety requirements
   - Pull: client safety manual, site-specific rules

3. Calendar → Check project milestones
   - Pull: project dates, phases, scheduled orientations
```

**If no connectors:**
```
1. Ask user for required information:
   - "What is the project name and number?"
   - "Where is the project located?"
   - "What is the scope of electrical work?"
   - "What voltage levels are involved?"
   - "When does the project start and end?"

2. Ask for helpful additional info:
   - "Who is the client/GC?"
   - "How many Huston Electric workers on site?"
   - "Any subcontractors?"
   - "Any special conditions (confined spaces, elevated work, live work)?"
   - "Any client-specific safety requirements beyond OSHA?"

3. Accept whatever they provide and work with it
```

### Step 2: Identify Site-Specific Hazards

```
1. Electrical hazards based on:
   - Voltage levels → shock severity and approach boundaries
   - Available fault current → arc flash incident energy
   - Equipment types → specific hazards per equipment
   - Work tasks → exposure scenarios

2. Physical hazards based on:
   - Site description → falls, struck-by, environmental
   - Work scope → confined spaces, overhead work, excavation
   - Location → traffic, weather, terrain

3. Chemical hazards based on:
   - Building age → lead, asbestos potential
   - Work tasks → silica, solvents, battery acid
   - Environment → existing chemicals, ventilation

4. Environmental/situational based on:
   - Outdoor vs indoor → weather exposure
   - Occupied building → public interaction
   - Multi-employer → coordination hazards
   - Location → nearby utilities, traffic
```

### Step 3: Reference Past PSSPs

**If knowledge base connected:**
```
1. Query: PSSPs for similar project types
   - Match on: voltage level, scope type, building type, client
   - Pull: hazard identification (any hazards we might miss?)
   - Pull: control measures that worked well
   - Pull: lessons learned and post-project notes

2. Query: Incidents on similar projects
   - Pull: what went wrong and why
   - Apply: additional controls based on incident history

3. Query: Client-specific requirements
   - Pull: client safety manual requirements
   - Apply: any requirements beyond OSHA minimum
```

**If no knowledge base:**
```
1. Use standard Huston Electric hazard identification checklist
2. Apply industry best practices for project type
3. Note: recommend connecting knowledge base for future PSSPs
```

### Step 4: Apply OSHA/NFPA Standards

```
1. OSHA applicability:
   - Construction (1926) vs General Industry (1910)?
   - Subpart K (electrical), Subpart M (fall protection), etc.
   - State plan requirements (if applicable)

2. NFPA 70E:
   - Article 120: Electrically safe work condition
   - Article 130: Arc flash risk assessment, shock hazard analysis
   - Table 130.7(C)(15): PPE categories by equipment type
   - Table 130.4(E)(a): Approach boundaries

3. NEC:
   - Article 110.26: Working space requirements
   - Article 250: Grounding and bonding
   - Applicable articles for equipment being installed

4. IEEE 1584 (if incident energy analysis needed):
   - Calculate incident energy at working distance
   - Determine arc flash boundary
   - Map to PPE requirements
```

### Step 5: Generate Risk Assessment

```
1. For each identified hazard:
   - Assign probability rating (1-5)
   - Assign severity rating (1-5)
   - Calculate risk score (P x S)
   - Determine risk level (Critical/High/Medium/Low)

2. Prioritize hazards by risk score (highest first)

3. For Critical and High risks:
   - Require specific controls documented
   - Reference specific regulatory requirements
   - May require additional JHA or procedure

4. Document in risk assessment matrix format
```

### Step 6: Create Control Measures

```
1. For each hazard, apply hierarchy of controls:
   a. Can it be eliminated? (e.g., de-energize instead of working hot)
   b. Can it be substituted? (e.g., lower voltage, less hazardous chemical)
   c. Engineering controls? (e.g., barriers, guards, ventilation)
   d. Administrative controls? (e.g., procedures, training, signs, permits)
   e. PPE? (last resort — specify exactly what is required)

2. Document controls in the control measures table

3. Ensure each Critical/High risk has multiple layers of controls
```

### Step 7: Format Complete PSSP Document

```
1. Populate all 18 sections of the PSSP template
2. Fill in project-specific details throughout
3. Customize hazard identification for this specific project
4. Complete risk assessment matrix with actual scores
5. Map control measures to specific hazards
6. Set correct PPE requirements for project voltages
7. Include project-specific emergency information
8. Add site-specific safety rules
9. Set training requirements based on project scope
10. Include subcontractor requirements if applicable
11. Set inspection/audit schedule
12. Create signature pages
```

---

## Risk Assessment Methodology — Detailed

### Probability Assessment Factors

| Factor | Increases Probability | Decreases Probability |
|--------|----------------------|----------------------|
| Exposure frequency | Daily or continuous exposure | Rare or one-time task |
| Duration | Extended exposure time | Brief exposure |
| Worker experience | New or inexperienced workers | Experienced, trained workers |
| Equipment condition | Old, poorly maintained | New, well-maintained |
| Environment | Adverse conditions (wet, hot, confined) | Controlled environment |
| Complexity | Multiple steps, unfamiliar task | Simple, routine task |
| History | Past incidents on similar work | No incident history |

### Severity Assessment Factors

| Factor | Increases Severity | Decreases Severity |
|--------|-------------------|-------------------|
| Voltage | Higher voltage (>600V) | Lower voltage (<50V) |
| Available fault current | Higher fault current | Lower fault current |
| Proximity | Close to exposed parts | Greater working distance |
| Arc flash energy | Higher incident energy | Lower incident energy |
| Fall height | Greater height | Lower height |
| Rescue difficulty | Remote, confined, hard to access | Easy access, near hospital |

---

## Common Electrical Hazards Reference

### By Equipment Type

| Equipment | Primary Hazards | Typical PPE Category | Key Concerns |
|-----------|----------------|---------------------|--------------|
| Panelboards (240V) | Shock, arc flash | 1-2 | Working space, AFCI/GFCI |
| Panelboards (480V) | Shock, arc flash | 2-3 | Higher incident energy, approach boundaries |
| Switchgear (480V) | Shock, arc flash, arc blast | 2-4 | High fault current, blast pressure |
| Motor control centers | Shock, arc flash | 2-3 | Multiple compartments, stored energy |
| Transformers | Shock, arc flash, burns | 2-4 | High voltage, stored energy, confined space |
| Switchboards | Shock, arc flash | 2-3 | Rear access, working space |
| Disconnects | Shock, arc flash | 1-2 | Switching hazard, load break |
| Receptacle/switch work | Shock | 0-1 | Verify de-energized, GFCI protection |
| Cable pulling | Pinch, strain, induced voltage | 0-1 | Weight, bending radius, nearby energized |
| Conduit work | Cuts, falls, struck-by | 0 | Elevated work, overhead installation |
| Underground/duct bank | Confined space, shock, collapse | Varies | Existing energized utilities, ground water |

### By Task

| Task | Hazards | Minimum Requirements |
|------|---------|---------------------|
| Voltage testing | Shock, arc flash | Voltage-rated gloves, face shield, appropriate PPE category |
| Circuit breaker operation | Arc flash, arc blast | PPE per equipment rating, stand to side |
| Panel cover removal | Shock, arc flash | Verify de-energized or appropriate PPE, insulated tools |
| Wire termination (energized) | Shock, arc flash | EEWP, full PPE for category, insulated tools |
| Conduit installation | Falls, struck-by, cuts | Fall protection if >6 ft, gloves, hard hat |
| Concrete core drilling | Silica, existing utilities, noise | Respirator, utility locate, hearing protection |
| Trenching/excavation | Cave-in, utility strike | Sloping/shoring, 811 locate, competent person |

---

## Example PSSP — Commercial Electrical Installation

**Project:** Maple Street Office Renovation — 3rd Floor Electrical Fit-Out
**Location:** 1200 Maple Street, Suite 300, Nashville, TN 37203
**Client:** Turner Construction (GC)
**Scope:** Complete electrical renovation of 15,000 sq ft office space — new 400A, 277/480V distribution, 120/208V branch circuits, LED lighting, fire alarm, data infrastructure
**Duration:** March 2026 — September 2026
**Workforce:** 8-12 Huston Electric electricians

**Key Hazards Identified:**
1. **Electric shock from existing 480V service** (Risk: High — P:3 x S:5 = 15)
   - Control: LOTO before all work on existing equipment; EEWP for necessary energized work
2. **Arc flash at main switchgear** (Risk: High — P:2 x S:5 = 10)
   - Control: PPE Category 3, arc flash labels, approach boundaries enforced
3. **Falls from ladders and lifts** (Risk: Medium — P:3 x S:3 = 9)
   - Control: Scaffold/lift preferred over ladders; fall protection training; 3-point contact
4. **Silica dust from concrete penetrations** (Risk: Medium — P:3 x S:3 = 9)
   - Control: Wet cutting methods, HEPA vacuum, N95 respirators, exposure monitoring
5. **Existing asbestos in ceiling tiles** (Risk: Medium — P:2 x S:4 = 8)
   - Control: Abatement by licensed contractor before electrical work; do not disturb
6. **Multi-trade coordination** (Risk: Medium — P:3 x S:2 = 6)
   - Control: Daily coordination meetings, barricading work areas, communication protocols

**PPE Requirements:**
- Minimum: Hard hat (Class E), safety glasses, hi-vis vest, EH-rated boots
- Electrical work on 480V: PPE Category 2 minimum (8 cal/cm2), Class 0 rubber insulating gloves with protectors
- Main switchgear: PPE Category 3 (25 cal/cm2), Class 0 rubber insulating gloves with protectors
- Concrete cutting: N95 respirator, face shield, hearing protection
- Elevated work >6 ft: Full body harness, shock-absorbing lanyard

---

## Quality Checklist — Before Delivering PSSP

### Content
- [ ] All 18 sections complete with project-specific information
- [ ] Hazard identification covers electrical, physical, chemical, and environmental
- [ ] Risk assessment scores are realistic and justified
- [ ] Control measures address all High and Critical risks
- [ ] PPE requirements match voltage levels and equipment types
- [ ] Emergency contacts include actual phone numbers and nearest hospital
- [ ] Training requirements are comprehensive and achievable
- [ ] Regulatory references are accurate and current

### Compliance
- [ ] OSHA standards correctly cited (1910 vs 1926)
- [ ] NFPA 70E edition year noted
- [ ] NEC requirements referenced where applicable
- [ ] Approach boundaries calculated correctly for project voltages
- [ ] PPE categories match equipment types and voltage levels
- [ ] LOTO requirements meet OSHA 1910.147
- [ ] Incident reporting timelines match OSHA requirements

### Usability
- [ ] Document is clearly organized and easy to navigate
- [ ] Signature pages are complete and ready for use
- [ ] Worker acknowledgment page has adequate lines
- [ ] Emergency procedures are clear and actionable
- [ ] Site safety rules are concise and enforceable

---

## Tips for Better PSSPs

1. **Be specific about location** — "1200 Maple Street, 3rd floor, electrical room 301" is better than "office building"
2. **List all voltages** — Include every voltage level present, not just the highest
3. **Name your equipment** — "Square D QED2 switchboard" gets more specific hazard identification than "switchboard"
4. **Mention existing conditions** — Asbestos, lead paint, occupied spaces, active systems all affect the plan
5. **Include client requirements** — Many GCs have safety requirements that exceed OSHA
6. **Reference past projects** — "Like the Oak Avenue project" helps pull relevant past PSSP data
7. **Update throughout the project** — A PSSP is a living document; update when scope or conditions change

---

## Related Skills

- **safety-specialist** — General electrical safety procedures, LOTO, PPE selection, safety meetings, incident reports
- Use `/generate-pssp` command for a guided workflow
- Use `/safety-procedure` command for individual safety procedures
