---
description: Generate a complete Project-Specific Safety Plan (PSSP) for a Huston Electric, Inc. project — site-specific hazards, risk assessment, control measures, emergency procedures, training requirements, and signature pages
argument-hint: "<project name or description>"
---

# /generate-pssp

> If you see unfamiliar placeholders or need to check which tools are connected, see [CONNECTORS.md](../CONNECTORS.md).

Generate a complete, formatted Project-Specific Safety Plan (PSSP) for a Huston Electric project. The PSSP covers all 18 required sections including hazard identification, risk assessment, electrical safety program, PPE requirements, emergency procedures, and worker acknowledgment pages.

## Usage

```
/generate-pssp <project name or description>
```

Generate a PSSP for: $ARGUMENTS

If a file is referenced: @$1

---

## How It Works

```
┌─────────────────────────────────────────────────────────────────┐
│                       GENERATE PSSP                               │
├─────────────────────────────────────────────────────────────────┤
│  STANDALONE (always works)                                       │
│  + Provide project details (name, location, scope, voltage)      │
│  + Systematic hazard identification by category                  │
│  + Risk assessment with probability x severity matrix            │
│  + Hierarchy of controls for each hazard                         │
│  + OSHA, NFPA 70E, NEC compliance mapping                       │
│  + Complete 18-section PSSP document                             │
│  + Ready for review, approval, and distribution                  │
├─────────────────────────────────────────────────────────────────┤
│  SUPERCHARGED (when you connect your tools)                      │
│  + Knowledge base: past PSSPs, incident history, equipment       │
│    data, company SOPs, client requirements                       │
│  + Document storage: project specs, site drawings, client        │
│    safety manuals, arc flash studies                              │
│  + Email: distribute PSSP, request client approval               │
│  + Chat: notify project team, coordinate reviews                 │
│  + Calendar: schedule safety orientation, review meetings         │
└─────────────────────────────────────────────────────────────────┘
```

---

## What I Need From You

**Required information:**

| Field | Prompt | Example |
|-------|--------|---------|
| **Project name** | "What is the project name?" | "Maple Street Office Renovation" |
| **Location** | "Where is the project?" | "1200 Maple St, Nashville TN 37203" |
| **Scope of work** | "What electrical work is being done?" | "Complete electrical fit-out: distribution, lighting, fire alarm" |
| **Voltage levels** | "What voltage levels are on this project?" | "277/480V 3-phase, 120/208V 3-phase" |
| **Duration** | "When does the project start and end?" | "March 2026 - September 2026" |

**Helpful additional information:**

| Field | Prompt |
|-------|--------|
| **Client/GC** | "Who is the client or general contractor?" |
| **Workforce size** | "How many Huston Electric workers on site?" |
| **Subcontractors** | "Any electrical subcontractors on this project?" |
| **Special conditions** | "Any confined spaces, elevated work, live work, hazmat areas?" |
| **Client safety requirements** | "Does the client have safety requirements beyond OSHA?" |
| **Building age/condition** | "Is this a new building or renovation? Any known hazards (asbestos, lead)?" |
| **Site access** | "Any access restrictions, security requirements, or occupied building considerations?" |
| **Similar past project** | "Is this similar to a project we have done before?" |

If you do not have all the information, provide what you can. PSSP Pete will use reasonable defaults and flag items that need verification.

---

## PSSP Sections Generated

The complete PSSP includes all 18 sections:

| Section | Content |
|---------|---------|
| 1. Project Information | Names, contacts, dates, scope, voltages |
| 2. Safety Policy Statement | Huston Electric safety commitments and stop work authority |
| 3. Project Safety Organization | Org chart, roles, responsibilities |
| 4. Site-Specific Hazard Identification | Electrical, physical, chemical, environmental hazards |
| 5. Risk Assessment Matrix | Probability x severity scoring for all hazards |
| 6. Control Measures | Hierarchy of controls for each identified hazard |
| 7. Electrical Safety Program | ESWC, energized work permits, approach boundaries |
| 8. Lockout/Tagout Program | LOTO requirements, equipment, and verification |
| 9. Arc Flash Safety | Risk assessment, PPE categories, label requirements |
| 10. Personal Protective Equipment | Minimum PPE and task-specific requirements |
| 11. Training Requirements | Pre-work and ongoing training matrix |
| 12. Emergency Procedures | Contacts, assembly point, response procedures by emergency type |
| 13. Site Safety Rules | 15 site-specific safety rules |
| 14. Subcontractor Safety Requirements | Prequalification, obligations, multi-employer coordination |
| 15. Incident Reporting and Investigation | Reporting timelines, investigation process, documentation |
| 16. Safety Inspections and Audits | Inspection types, frequencies, responsibilities |
| 17. Document Control and Revisions | Revision history, review schedule |
| 18. Acknowledgment and Signature Pages | Approval signatures and worker sign-off |

---

## Output Options

**Default:** Complete PSSP in markdown format, ready for copy/paste into your document system.

**If document storage connected:** Save directly as a formatted document in your company drive.

**If email connected:** Send the completed PSSP to specified recipients for review and approval.

---

## If Connectors Available

**Knowledge base connected:**
- Search for past PSSPs on similar projects (same voltage, scope type, client, building type)
- Pull lessons learned and post-project safety notes
- Reference incident history for similar work types
- Apply company-specific requirements and SOPs
- Retrieve subcontractor safety records

**Document storage connected:**
- Pull project specifications and scope documents
- Retrieve site drawings for hazard identification
- Access client safety manual and requirements
- Save completed PSSP with proper document numbering
- Store signed acknowledgment pages

**Email connected:**
- Send completed PSSP to Safety Director for review
- Distribute approved PSSP to project team
- Send PSSP to client/GC for approval (if required)
- Notify subcontractors of safety requirements
- Send worker acknowledgment reminder

**Chat connected:**
- Notify project channel when PSSP is ready for review
- Coordinate review and approval process
- Share link to approved PSSP with project team

**Calendar connected:**
- Schedule PSSP review meeting with Safety Director and PM
- Schedule project safety orientation (required before work begins)
- Set reminders for 90-day PSSP reviews
- Schedule initial site safety inspection

---

## After Generating

Once the PSSP is generated, you can:

1. **Review and customize** — Ask to modify any section, add hazards, adjust risk scores
2. **Update for changes** — "Add confined space entry to the PSSP" or "We added a subcontractor"
3. **Generate supporting documents** — Use `/safety-procedure` for specific task procedures referenced in the PSSP
4. **Create JHAs** — Ask for Job Hazard Analyses for specific tasks within the project scope
5. **Prepare orientation** — Ask for a safety orientation presentation based on the PSSP content

---

## Tips

1. **Be specific about voltages and equipment** — "277/480V distribution with 65kAIC switchgear" produces much better hazard identification than "commercial electrical"
2. **Mention existing conditions** — Occupied building, active systems, asbestos, lead paint all significantly affect the PSSP
3. **Include client requirements** — Many GCs (Turner, Skanska, Brasfield & Gorrie) have specific safety requirements that exceed OSHA
4. **Reference past projects** — "Similar to the Oak Avenue project" helps pull relevant past PSSP data from the knowledge base
5. **Upload project documents** — Specifications and drawings help identify hazards you might not think to mention
6. **Update throughout the project** — A PSSP is a living document; run `/generate-pssp` again when scope changes or new hazards are identified
7. **Plan for phases** — If the project has distinct phases (underground, rough-in, trim, startup), mention them for phase-specific hazard identification
