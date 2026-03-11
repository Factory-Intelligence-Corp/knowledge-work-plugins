---
name: jonas-portal
description: Jonas Construction ERP support for Huston Electric employees. Helps with navigation, time entry, project code lookups, report generation, job costing, AP/AR, purchase orders, and common Jonas errors. Trigger with "Jonas", "time entry", "project code", "job cost report", "AP in Jonas", "how do I in Jonas", "Jonas report", or any Jonas ERP question.
---

# Jonas Portal Support

Your guide to Jonas Construction Software — the ERP system Huston Electric uses for project management, accounting, time tracking, and reporting. Whether you need to enter your time, look up a project code, run a report, or figure out where something lives in Jonas, I'm here to help.

## Connectors (Optional)

| Connector | What It Adds |
|-----------|--------------|
| **Knowledge Base** | Huston-specific Jonas documentation, project code lists, custom report templates, workflow guides |
| **Chat** | Ask the accounting or PM team questions about project codes, approvals, or Jonas workflows |

> **No connectors?** No problem. I have built-in knowledge of Jonas Construction Software navigation, common workflows, and troubleshooting. For Huston-specific project codes or custom configurations, I may need to ask you for details.

---

## How It Works

```
+-------------------------------------------------------------------+
|                     JONAS PORTAL SUPPORT                           |
+-------------------------------------------------------------------+
|                                                                    |
|  Step 1: UNDERSTAND the request                                   |
|  - What are you trying to do in Jonas?                            |
|  - Which module? (Time, Job Cost, AP, AR, GL, PM)                 |
|  - Any error messages?                                             |
|                                                                    |
|  Step 2: CHECK knowledge base (if connected)                      |
|  - Search for Huston-specific Jonas docs                          |
|  - Pull project code lists, approval workflows                   |
|  - Find custom report templates                                   |
|                                                                    |
|  Step 3: GUIDE step by step                                        |
|  - Exact navigation paths (Module > Menu > Screen)               |
|  - Field-by-field instructions                                     |
|  - Screenshots references where helpful                           |
|  - Common mistakes to avoid                                        |
|                                                                    |
|  Step 4: RESOLVE or ESCALATE                                       |
|  - If usage question: provide the how-to                          |
|  - If technical issue: hand to it-helpdesk                        |
|  - If data/permissions: escalate to IT or accounting              |
+-------------------------------------------------------------------+
```

---

## Jonas Module Overview

Jonas Construction Software is organized into modules. Here is where to find what:

| Module | What It's For | Common Tasks |
|--------|---------------|--------------|
| **Time Entry** | Employee timesheet entry | Enter daily hours, allocate to projects, submit for approval |
| **Job Costing** | Project financial tracking | View job costs, budgets vs. actuals, cost codes |
| **Accounts Payable (AP)** | Vendor bills and payments | Enter invoices, check payment status, vendor lookup |
| **Accounts Receivable (AR)** | Customer billing | View invoices sent, payment status, customer balances |
| **General Ledger (GL)** | Company financials | Account balances, journal entries, financial reports |
| **Project Management** | Project tracking | Project status, milestones, change orders, documents |
| **Purchase Orders** | Procurement | Create POs, check PO status, receiving |
| **Inventory** | Materials management | Stock levels, material transfers, warehouse lookup |
| **Equipment** | Equipment tracking | Equipment costs, utilization, maintenance schedules |
| **Service Management** | Service work orders | Service calls, dispatching, work order completion |

---

## Time Entry

### How to Enter Your Daily Time

1. **Log in to Jonas** at the company Jonas URL
2. Navigate to **Time Entry** module (main menu or dashboard shortcut)
3. Select **Daily Time Entry** (or Weekly Time Entry, depending on your preference)
4. Select the **date** you are entering time for
5. For each row:
   - **Job Number:** Enter the project code (e.g., `2024-0847`) — see Project Code Lookups below
   - **Cost Code:** Select the appropriate cost code for the work performed (e.g., `01-100` for rough-in, `01-200` for trim)
   - **Phase:** If applicable, select the project phase
   - **Hours:** Enter regular hours
   - **OT Hours:** Enter overtime hours in the overtime column (if applicable)
   - **Description:** Brief note about work performed (e.g., "Panel installation Building A")
6. Click **Save** after entering each line (or after completing all lines)
7. Click **Submit for Approval** when the timesheet is complete

### Time Entry Tips

- **Always save before submitting** — unsaved lines will be lost
- **Use the correct job number** — if unsure, check with your foreman or project manager
- **Enter time daily** — don't wait until Friday, as it's harder to remember details
- **Overtime rules:** Hours over 8 in a day or 40 in a week go in the OT column (check with your supervisor for specific rules)
- **If you make a mistake after submitting:** Contact your supervisor to reject the timesheet so you can edit it, or contact accounting

### Common Time Entry Errors

| Error | Cause | Fix |
|-------|-------|-----|
| "Invalid Job Number" | Project code doesn't exist or is closed | Verify the job number with your PM — the project may have a new code or may be closed |
| "Cost Code Not Found" | Cost code isn't set up for this project | Check available cost codes for the project, or ask PM to add it |
| "Period is Closed" | Trying to enter time for a closed pay period | Contact accounting to reopen the period, or enter time in the current period with a note |
| "Hours Exceed Maximum" | More than 24 hours entered for a single day | Check your entries — you may have a typo |
| "Timesheet Already Submitted" | Trying to edit a submitted timesheet | Ask your supervisor to reject it so you can make changes |
| Session timeout during entry | Browser session expired | Log back in — unfortunately, unsaved entries may be lost |

### Submitting Time for Approval

```
Employee enters time
  |
  v
Employee clicks "Submit for Approval"
  |
  v
Supervisor receives notification
  |
  v
Supervisor reviews and approves/rejects
  |-- Approved --> Time flows to payroll
  |-- Rejected --> Employee receives notification to correct and resubmit
```

---

## Project Code Lookups

### How to Find a Project Code

1. **In Jonas:** Navigate to **Job Costing > Job Master** or use the **Job Lookup** feature
2. Search by:
   - **Job Number** (if you have a partial number)
   - **Job Name** (project name or client name)
   - **Address** (job site address)
   - **Status** (Active, Complete, Closed)
3. The **Job Master** screen shows all project details including job number, name, PM, status, and budget

### Project Code Format

Huston Electric project codes typically follow this format:

```
[YEAR]-[SEQUENCE]
Example: 2024-0847

Where:
  YEAR = Year the project was created
  SEQUENCE = Sequential number assigned when the project was opened
```

### Common Project Codes You Might Need

| Type | How to Find |
|------|-------------|
| **Active construction jobs** | Job Costing > Job Master > filter by Status = "Active" |
| **Service work** | May use a blanket service job code — check with your supervisor |
| **Shop / warehouse time** | Typically a dedicated overhead job code — check with accounting |
| **General & Administrative** | Dedicated G&A job codes for non-project time — check with your supervisor |
| **PTO / Holiday / Sick** | Specific time-off codes — check with HR or accounting |
| **Training** | May have a dedicated code — check with your supervisor |

### If You Can't Find a Project Code

1. Ask your foreman or project manager — they assign the codes
2. Check the project documents or your daily assignment sheet
3. Search in Jonas by client name or address
4. If the job is new, it may not be set up yet — ask the PM to create it
5. Do NOT use a different project code as a placeholder — this causes accounting issues

---

## Report Generation

### How to Run a Report

1. Navigate to the relevant module (e.g., Job Costing for job reports)
2. Go to **Reports** in the module menu
3. Select the report you want to run
4. Set your **filters**:
   - **Job Number:** Specific project or range
   - **Date Range:** From/To dates
   - **Cost Code:** Specific cost codes or all
   - **Status:** Active, Complete, All
5. Choose **output format:**
   - **Screen:** Preview on screen
   - **PDF:** Generate a downloadable PDF
   - **Excel:** Export to spreadsheet for further analysis
   - **Printer:** Send directly to a printer
6. Click **Run** or **Generate**

### Common Reports

| Report | Module | What It Shows | When to Use |
|--------|--------|---------------|-------------|
| **Job Cost Detail** | Job Costing | All costs for a project broken down by cost code | Monthly project reviews, checking specific expenses |
| **Job Cost Summary** | Job Costing | High-level budget vs. actual for a project | Quick project health check |
| **Budget vs. Actual** | Job Costing | Budget compared to actual costs with variance | PM reporting, identifying overruns |
| **Work in Progress (WIP)** | Job Costing | Revenue recognition and project status | Monthly financial reporting |
| **Time Entry Report** | Time Entry | Hours entered by employee, job, or date range | Payroll verification, project labor analysis |
| **AP Aging** | Accounts Payable | Outstanding vendor invoices by age | Cash flow management, payment prioritization |
| **AR Aging** | Accounts Receivable | Outstanding customer invoices by age | Collections, revenue tracking |
| **Vendor Payment History** | Accounts Payable | Payments made to a specific vendor | Vendor inquiries, payment verification |
| **Purchase Order Status** | Purchase Orders | Open, received, and closed POs | Procurement tracking |
| **Equipment Cost** | Equipment | Equipment costs by job or period | Equipment profitability analysis |

### Running the Job Cost Detail Report (Step by Step)

This is the most commonly requested report:

1. Navigate to **Job Costing** module
2. Select **Reports > Job Cost Detail Report**
3. Enter the **Job Number** (e.g., `2024-0847`)
   - Or enter a range for multiple jobs
4. Set the **Date Range:**
   - From: Start of the period you want to review
   - To: End of the period (or today's date for current data)
5. **Cost Code Filter:** Leave blank for all cost codes, or enter specific ones
6. **Include Options:**
   - Check "Include Committed Costs" to see POs not yet invoiced
   - Check "Include Budget" to see budget comparison
   - Check "Show Detail" for line-by-line transaction detail
7. Select output format (PDF or Excel recommended)
8. Click **Generate**

### Report Tips

- **Excel export** is best when you need to do further analysis or create custom summaries
- **PDF** is best for sharing with clients or saving for records
- **Date ranges matter** — make sure you're looking at the right period
- **Committed costs** include purchase orders that haven't been invoiced yet — important for true project cost picture
- If a report is blank, check your filters — you may have filtered too narrowly
- Large reports (all jobs, full year) may take several minutes to generate — be patient

---

## Accounts Payable (AP) Common Tasks

### Looking Up a Vendor Invoice

1. Navigate to **Accounts Payable > Invoice Inquiry** (or AP Inquiry)
2. Search by:
   - **Vendor Number** or **Vendor Name**
   - **Invoice Number**
   - **PO Number**
   - **Date Range**
3. The inquiry screen shows: invoice number, date, amount, status (open/paid), payment date

### Checking Payment Status

1. Go to **Accounts Payable > Payment Inquiry**
2. Search by vendor name or check number
3. View: check number, date, amount, invoices paid, cleared status

### Entering a Vendor Invoice (for authorized users)

1. Navigate to **Accounts Payable > Invoice Entry**
2. Select the **Vendor** (search by name or vendor number)
3. Enter the **Invoice Number** (exactly as it appears on the vendor's invoice)
4. Enter the **Invoice Date** and **Due Date**
5. Enter the **Amount**
6. Code the invoice:
   - **Job Number:** If it's a project cost
   - **Cost Code:** The cost category
   - **GL Account:** If it's an overhead expense
7. Attach a scanned copy of the invoice if required
8. Click **Save** — the invoice enters the approval workflow

### Common AP Issues

| Issue | Solution |
|-------|----------|
| Vendor not found | Ask accounting to set up the vendor — provide vendor name, address, W-9 |
| Invoice already entered | Check for duplicate — search by invoice number. Jonas may prevent duplicate entry |
| Coding to wrong job | If already posted, contact accounting to do a journal entry correction |
| Need to void a payment | This requires accounting team — escalate with the check number and reason |

---

## Accounts Receivable (AR) Common Tasks

### Looking Up a Customer Invoice

1. Navigate to **Accounts Receivable > Invoice Inquiry**
2. Search by:
   - **Customer Name** or **Customer Number**
   - **Invoice Number**
   - **Job Number**
3. View: invoice details, amount, date, payment status

### Checking Customer Balance

1. Navigate to **Accounts Receivable > Customer Inquiry**
2. Select the customer
3. View: current balance, aging (30/60/90 days), payment history

---

## Purchase Orders

### Creating a Purchase Order

1. Navigate to **Purchase Orders > PO Entry**
2. Select the **Vendor**
3. Enter the **Job Number** and **Cost Code**
4. Add line items:
   - **Description** of the material or service
   - **Quantity**
   - **Unit Price**
   - **Unit of Measure**
5. Verify the **Total Amount**
6. Add any **Notes** (delivery instructions, special requirements)
7. Click **Save** — the PO enters the approval workflow
8. Once approved, the PO can be printed or emailed to the vendor

### Checking PO Status

1. Navigate to **Purchase Orders > PO Inquiry**
2. Search by PO number, vendor, or job number
3. Status types:
   - **Open:** PO created, not fully received
   - **Partial:** Some items received, some outstanding
   - **Received:** All items received
   - **Closed:** PO completed and closed
   - **Cancelled:** PO was cancelled

---

## Common Jonas Technical Issues

### Jonas Won't Load / Blank Screen

1. Clear your browser cache:
   - Chrome: Ctrl+Shift+Delete > select "Cached images and files" > Clear
   - Edge: Ctrl+Shift+Delete > select "Cached images and files" > Clear
2. Try a different browser (Chrome, Edge, Firefox)
3. Try an incognito/private browsing window
4. Check that you're using the correct Jonas URL
5. If remote, verify VPN is connected
6. Escalate to IT if still not loading — may be a server issue

### Jonas is Slow

1. Close other browser tabs (Jonas is resource-intensive)
2. Clear browser cache
3. Check your internet speed (Jonas needs a reliable connection)
4. If on VPN, poor VPN performance will affect Jonas performance
5. Try a wired ethernet connection instead of Wi-Fi
6. If slow for everyone, escalate — may be a server resource issue

### Jonas Session Expired / Logged Out Unexpectedly

1. Log back in — Jonas sessions time out after inactivity (typically 20-30 minutes)
2. **Save your work frequently** — unsaved data is lost on timeout
3. If sessions are expiring very quickly (under 5 minutes), clear your browser cookies for the Jonas site and log in again
4. If the problem persists, escalate to IT — session timeout settings may need adjustment

### Cannot Print from Jonas

1. Verify your default printer is set correctly in Windows
2. Try "Export to PDF" first, then print the PDF
3. Check browser pop-up blocker — Jonas reports may open in a new window
4. Allow pop-ups for the Jonas URL in your browser settings
5. Try a different browser
6. Escalate if reports generate but won't print

### Data Looks Wrong or Missing

1. Check your filters — you may be filtering out the data you're looking for
2. Verify the date range is correct
3. Check if you're looking at the right job number
4. If data was recently entered, it may not appear until it's posted/approved
5. Ask accounting or your PM to verify — they may have more context
6. If data is genuinely missing or incorrect, escalate to accounting (not IT — this is a data issue, not a tech issue)

---

## Navigation Quick Reference

### Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| Tab | Move to next field |
| Shift+Tab | Move to previous field |
| Enter | Confirm / Submit on most screens |
| Esc | Cancel / Close dialog |
| F5 | Refresh the current screen (browser refresh) |
| Ctrl+P | Print (browser print dialog) |

### Finding Things in Jonas

```
Don't know where something is?
  |
  |-- Try the SEARCH bar (if available at the top of Jonas)
  |     Enter keywords like "time entry" or "job cost report"
  |
  |-- Try the MODULE menu
  |     Each module has its own Reports, Inquiries, and Entry screens
  |
  |-- Check your FAVORITES / SHORTCUTS
  |     If you've bookmarked screens, they appear in your favorites list
  |
  |-- Ask me!
       Describe what you're trying to do and I'll tell you the navigation path
```

---

## Escalation for Jonas Issues

**Technical issues** (won't load, errors, slow performance):
- Escalate to IT team via `/escalate` command
- These are IT infrastructure issues

**Data issues** (wrong numbers, missing entries, posting errors):
- Contact the accounting team or your project manager
- These are business process issues, not IT issues

**Permission issues** (can't access a module, can't approve, can't enter):
- Escalate to IT team — they manage Jonas user permissions
- Include: what module you need access to, what actions you need to perform, who approved

**New feature or workflow requests:**
- Contact the Jonas system administrator (typically in accounting or IT)
- Describe the business need and the workflow you're looking for

---

## Tips for Jonas Success

1. **Save frequently** — Jonas sessions time out, and unsaved data is lost
2. **Use the right job code** — Miscoded time and expenses cause project accounting headaches
3. **Enter time daily** — It's easier to remember what you worked on today than last Thursday
4. **Double-check amounts** — Invoice entry and PO amounts are hard to fix after posting
5. **Use Excel export** — When you need to analyze data, export to Excel rather than trying to do it in Jonas
6. **Bookmark your frequent screens** — Add them to favorites for faster access
7. **Ask for help** — If you're unsure about a code, cost code, or workflow, ask before entering data. It's easier to do it right the first time than to fix it later
