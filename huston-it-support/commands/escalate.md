---
description: Escalate an unresolved IT issue to the Huston Electric IT team with full diagnostic context, steps already tried, and proper priority
argument-hint: "<issue summary or context from /it-help>"
---

# /escalate

> If you see unfamiliar placeholders or need to check which tools are connected, see [CONNECTORS.md](../CONNECTORS.md).

Escalate an IT issue to the Huston Electric IT team. This command gathers all the context needed for a fast resolution — issue description, steps already tried, error messages, device info, and priority level — and formats it into a clean escalation ticket.

## Usage

```
/escalate <issue summary>
```

Escalate this issue: $ARGUMENTS

If a file is referenced (e.g., screenshot): @$1

---

## How It Works

```
+-------------------------------------------------------------------+
|                        ESCALATE                                    |
+-------------------------------------------------------------------+
|  STANDALONE (always works)                                        |
|  - Gather issue details and diagnostic context                    |
|  - Determine priority level based on impact                       |
|  - Format a complete escalation ticket                            |
|  - Output the ticket text for you to copy/paste or send           |
+-------------------------------------------------------------------+
|  SUPERCHARGED (when you connect your tools)                       |
|  + Chat: Post directly to #it-support channel                     |
|  + Email: Send escalation email to IT helpdesk                    |
|  + Project Tracker: Create a Jira ticket automatically            |
|  + Knowledge Base: Attach relevant docs to the ticket             |
+-------------------------------------------------------------------+
```

---

## What I Need From You

I'll gather this information to create the escalation ticket. If we've already been troubleshooting with `/it-help`, I'll carry over the context automatically.

**Required:**
- What is the issue? (summary in your own words)
- Is this blocking your work?

**Helpful if you have it:**
- Exact error messages or screenshots
- When did it start?
- Your device (laptop model, desktop)
- Your location (which office, remote, field)
- Steps you've already tried

**I'll fill in automatically (if available):**
- Steps tried during our troubleshooting session
- Issue category
- Recommended priority level

---

## Output

### Escalation Ticket

```markdown
## IT Support Request

**Ticket ID:** [Auto-generated: IT-YYYYMMDD-HHMM]
**Submitted:** [Date and time]
**Employee:** [Name]
**Department:** [Department]
**Location:** [Office / Remote / Field]
**Priority:** [URGENT / HIGH / NORMAL / LOW]

---

### Issue Summary
[One clear sentence describing the problem]

### Detailed Description
[Full description of what's happening, including the employee's own words
and any additional context gathered during troubleshooting]

### Error Messages
[Exact error text, codes, or description of error dialogs]
[Note if screenshot is attached]

### Steps Already Tried
1. [Step] — Result: [What happened]
2. [Step] — Result: [What happened]
3. [Step] — Result: [What happened]
[All troubleshooting steps from the /it-help session, if applicable]

### Environment Details
- **Device:** [Laptop/Desktop model, or "unknown"]
- **Operating System:** [Windows 10/11, version if known]
- **Application Affected:** [Outlook, Jonas, VPN client, etc.]
- **Browser:** [Chrome/Edge/Firefox, if web-based issue]
- **Network Connection:** [Office Wi-Fi / Ethernet / VPN / Home network]
- **Recent Changes:** [Updates, moves, new equipment, or "none known"]

### Impact Assessment
- **Work Blocked:** [Yes/No]
- **Users Affected:** [Just me / My team / Multiple people / Everyone]
- **Deadline at Risk:** [Any upcoming deadlines affected]
- **Workaround Available:** [Yes — describe / No]

---

### Recommended Actions (for IT team)
[Based on troubleshooting, suggest what IT should investigate next.
For example: "Outlook profile has been repaired and credentials re-entered.
Suspect server-side connectivity issue. Check Exchange mailbox health."]

---

### Escalation Delivery Status
[Posted to #it-support — see ~~chat]
[Email sent to itsupport@hustonelectric.com — see ~~email]
[Jira ticket created: IT-1234 — see ~~project tracker]
[Ticket text output below — copy and send to IT]
```

---

## Priority Determination

I'll recommend a priority level based on what you tell me:

```
Is this a SECURITY issue?
(phishing clicked, malware suspected, account compromised)
  |-- Yes --> URGENT
  |
  v
Are MULTIPLE people affected?
  |-- Yes --> HIGH
  |
  v
Is your work COMPLETELY BLOCKED? (can't do your job)
  |-- Yes --> HIGH
  |
  v
Is your work PARTIALLY affected? (slow, annoying, workaround exists)
  |-- Yes --> NORMAL
  |
  v
Is this a question, feature request, or nice-to-have?
  |-- Yes --> LOW
```

| Priority | Description | Expected IT Response |
|----------|-------------|---------------------|
| **URGENT** | Security incident or complete system outage | Immediate — IT responds right away |
| **HIGH** | Work is blocked, no workaround, or multiple users affected | Within 1 hour |
| **NORMAL** | Work is affected but workaround exists, single user | Within 4 hours |
| **LOW** | Non-urgent question, feature request, minor inconvenience | Within 1 business day |

You can override my recommendation — just tell me what priority you think it should be.

---

## Escalation Flow

```
/escalate invoked
  |
  v
Was /it-help used first?
  |-- Yes --> Carry over: issue description, category,
  |           steps tried, error messages
  |-- No --> Ask for issue details
  |
  v
Gather any missing information
  - Employee name and department
  - Device and environment details
  - Impact assessment
  |
  v
Determine priority
  |
  v
Format escalation ticket
  |
  v
Deliver the ticket
  |
  |-- Chat connected? --> Post to #it-support channel
  |-- Email connected? --> Send to IT helpdesk email
  |-- Project tracker connected? --> Create Jira ticket
  |-- Nothing connected? --> Output formatted ticket text
  |                          "Copy this and send to your IT team,
  |                           or forward to itsupport@hustonelectric.com"
  |
  v
Confirm delivery
  - "Your ticket has been submitted. Here's what to expect..."
  - Include expected response time based on priority
  - Offer tips for what to do while waiting
```

---

## If Connectors Available

**Chat connected (e.g., Slack):**
- Post the formatted ticket directly to #it-support
- Tag the IT team or on-call person (if configured)
- The employee gets a link to the Slack message for tracking

**Email connected (e.g., Microsoft 365):**
- Send the ticket as an email to the IT helpdesk address
- CC the employee so they have a copy
- Attach any screenshots or error logs

**Project Tracker connected (e.g., Jira):**
- Create a support ticket with all fields populated
- Set priority, assignee (if configured), and labels
- Return the ticket number and link to the employee

**Knowledge Base connected (e.g., Notion, Confluence):**
- Attach relevant documentation to the ticket
- Reference known issues or prior resolutions for IT team context
- Link to network diagrams or configuration docs if relevant

---

## After Escalation

Once your ticket is submitted, here's what to expect:

| Priority | Expected Response | What to Do While Waiting |
|----------|-------------------|--------------------------|
| **URGENT** | Immediately | Stay available — IT will reach out. If security issue, stay off the affected device. |
| **HIGH** | Within 1 hour | Try the workaround if one was suggested. Stay near your device. |
| **NORMAL** | Within 4 hours | Continue working with the workaround. IT will reach out when ready. |
| **LOW** | Within 1 business day | No action needed — IT will get to it. |

If you haven't heard back within the expected time, follow up in #it-support or reply to the escalation email.

---

## Tips

1. **Use /it-help first** — If we troubleshoot together first, the escalation ticket will be much more detailed, which means IT can resolve it faster.
2. **Include screenshots** — A picture of the error is worth a thousand words. Share a screenshot or photo if you can.
3. **Be specific about impact** — "I can't send emails to clients and I have a proposal due at 3pm" helps IT prioritize better than "email isn't working."
4. **One issue per ticket** — If you have multiple problems, escalate each separately. This helps IT track and resolve each one.
5. **Don't duplicate** — If you've already reported the issue in Slack or email, let me know so I don't create a duplicate ticket.
