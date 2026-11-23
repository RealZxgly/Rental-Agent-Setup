# Rental Agent

A Windows app that turns property evaluation form submissions into revenue dashboards and branded PDF reports.

**Upload your submissions file → see every property's revenue potential → download the PDF report**

---

## Download

👉 **[Download the latest version](../../releases/latest)**. Under **Assets**, click `RentalAgentSetup.exe`.

**Requirements:** Windows 10 or 11 (uses Microsoft Edge, which comes with Windows).

---

## Install

1. Run `RentalAgentSetup.exe`.
2. If Windows shows **"Windows protected your PC"**, click **More info → Run anyway**. This appears because the app isn't code-signed; it's normal for small independent apps.
3. Click **Next → Install**. No administrator rights are needed.
4. Open **Rental Agent** from the Start menu or the desktop shortcut.

The first time, create your account on the sign-in page (see below).

---

## Signing in

The app opens on the **My NWTFI Portal** sign-in page.

- **First time:** click **Create account**, enter your work email and a password (at least 8 characters, letters and numbers), and confirm it.
- You'll then see a **recovery code** (like `4F2A-9C1B-77DE`). **Save it**: it's the only way to reset a forgotten password, and it's shown once.
- **Forgot password?** Enter your email, your recovery code and a new password. You get a new recovery code; the old one stops working.
- After 5 wrong passwords, sign-in for that email pauses for 5 minutes.
- Accounts are stored **on this computer** (`%APPDATA%\RentalAgent\users.json`). Passwords and recovery codes are stored only as salted hashes, never as text. Closing the app signs you out.
- Sign out or switch customer from **⚙ Settings** or the buttons in the top bar.

> Lost both the password and the recovery code? Close the app and delete `users.json` from `%APPDATA%\RentalAgent`, then create the account again. (This removes all accounts on that computer; your reports are not affected.)

## Choosing a customer

After signing in, pick the **customer you're working on** (NWTFI to start). You can add customers (e.g. Solara) or remove them on the same page, and switch any time with the customer button in the top bar. Switching clears whatever data was loaded.

## The portals

| Portal | Reports | What they're for |
|---|---|---|
| **Operation & Monitoring** | Lead Generation, Sales Pipeline, Social Media & Marketing Performance · *coming: Operations Board (Trello), Live Marketing (HubSpot)* | Internal dashboards to monitor marketing and operations |
| **Requesting Report** | Short Term Rental Analysis, New Hire | Reports you run for requests |
| **Financial Dashboard** | P&L Variance Review · *more coming* | Financial dashboards |

Pick a report, drop in your file, and it does the rest. **← Back** returns to the portal and clears what was loaded; nothing is saved. Each newer report has **Download the template** on its upload page and **Print / Save as PDF** on its dashboard.

---

## Short Term Rental Analysis

### 1. Upload the submissions file
Click **Launch dashboard**, then drop your file on the upload box or click **Choose File**.

- **CSV**, **Excel (.xlsx)** or **PDF**. You can select or drop **several files at once**.
- A PDF must have real text (not a scanned image), with each label next to its answer, like the CSV template.
- A file can be **one property** (labels in column A, answers in column B, like the evaluation email) or **many properties** (one row each, column names in the first row).
- Labels are matched automatically (Property Type, Bedrooms, Bathrooms, Zip Code, Amenities, Email, and so on), even if they're spelled a bit differently.
- Not sure about the layout? Click **Download the CSV template** for one example property.
- Got new submissions later? Click **+ Add files** on the overview. A submission that's already loaded (same Submission ID) is updated, not duplicated.

If you upload **one property**, its report opens straight away. Several properties open the overview first.

Nothing is saved: pressing **Home** (or closing the app) clears the loaded file. Use **⇪ Open another file** on a property to load a different one.

### 2. The overview
- **KPI cards:** submissions, hot leads, pipeline revenue, average per property, average nightly rate, average lead score, local market coverage, and leads that need review.
- **Charts:** expected revenue by property, lead status, revenue range per property, and revenue by market.
- **All Submissions table:** search by name, ZIP, market or status. Click a row to open that property.

### 3. A property's evaluation
- **Property Summary:** a plain-English summary of revenue, pricing, a comparison with current income, notes, and suggested next steps.
- **KPI cards:** expected and optimized revenue, nightly rate, occupancy, owner net, lead score, market and confidence.
- **Key Numbers:** average monthly revenue and owner income, best and slowest month, break-even nights, nights needed to match today's income, revenue per bedroom, and nightly rate vs. the local market.
- **Owner & Contact:** name, email and phone with Copy buttons, timeline and submission details.
- **Lead Score Breakdown:** how many points the timeline, condition, rental rules, availability and revenue each scored.
- **How This Was Calculated:** step by step, with this property's real numbers: the local price per night, how each answer moves it, how many nights get booked, each month, and what the owner keeps after fees and costs.
- **Charts:** revenue by month, three scenarios, what shapes the nightly rate, and where each revenue dollar goes.
- **Month by Month** and **Scenario Breakdown** tables: nights, rate and revenue per month, and fees, costs and owner income per scenario.
- **Submitted Answers:** exactly what the owner filled in.
- **⬇ Download PDF report** creates the branded report and opens it.

Use **⬇ Download all PDF reports** on the overview to make a report for every property at once.

### Lead status
| Status | Meaning |
|---|---|
| **HOT** | Score 70+, contact first |
| **WARM** | Score 45–69, follow up this week |
| **NURTURE** | Under 45, add to the follow-up list |
| **INVESTOR** | Mentions buying or investing |
| **Manual review** | Missing answers, or short-term rentals not allowed |

### How the estimate works
Short-term rental (Airbnb-style): guests pay per night. The app starts from the real local average price per night for that number of bedrooms (from the ZIP code), adjusts it for property type, bathrooms, size, amenities and condition, estimates how many nights get booked, then adds it up by month and year. What the owner earns today is shown only for comparison and does not change the estimate.

### Local market data
When a submission includes a **ZIP code**, the evaluation uses that area's short-term rental averages (AirDNA) and its busy season. Florida markets peak in winter, for example. ZIPs outside the built-in market list use U.S. averages, and the evaluation says so.

---

## Lead Generation

One dashboard for the whole journey. Every contact is at one step:

| Step | Meaning |
|---|---|
| **Lead** | A request, form, call, email or referral came in. Stages: *New* (not contacted yet), *Attempted Contact* (no reply yet). |
| **Active Lead** | They replied: Susan is in communication with them. Stages: *Contacted*, *Nurturing* (not ready yet), *Appointment Set*. |
| **Prospect** | They want to discuss a contract; handed to Kyle. Stages: *Meeting Scheduled*, *Needs Analysis*, *Proposal Sent*, *Negotiation*. |
| **Client** | The contract is signed. |
| **Closed** | No response after several tries, not interested, lost, or not a fit (with the reason). |

**Tiles**
- *Where every contact is now:* **Total Managed Contacts** (everyone in the file), **Leads**, **Active Leads**, **Prospects** (with potential and weighted value), **Clients**, **Closed**.
- *How contacts move from step to step* (each tile shows its own math, e.g. "22 of 41 active leads"):
  - **Lead → Active lead** = contacts that ever replied ÷ all contacts
  - **Active lead → Prospect** = contacts that ever became prospects ÷ those that became active
  - **Prospect → Client** = clients ÷ contacts that ever became prospects
  - **Overall: Lead → Client** = clients ÷ all contacts
  - Closed contacts still count for the steps they reached before closing. "About N days" is the average time between step dates.
- *Outreach:* **Emails sent**, **Calls made**, **Follow-ups done**, **Replies** and reply rate (needs the Emails Sent / Calls / Follow-ups / Replies columns).

**Moving a contact to the next step:** use the button on its row (**→ Active Lead**, **→ Prospect**, **✓ Contract signed**) or open it and change Step / Stage (including **Closed**). Each move is dated today. Changes made in the app aren't saved automatically: click **⬇ Download updated file** to get your file back with the new statuses and dates.

**File columns** (the template and the mock file have all of them): Lead ID, Date Created, First / Last Name, Company, Job Title, Email, Phone, City, State, Country, Lead Source, Campaign, Service Interest, Industry, **Status**, **Stage**, Assigned To, **Emails Sent**, **Calls**, **Follow-ups**, **Replies**, Last Contact, Next Follow-up, Next Step, Estimated Value, Budget, Timeline, **Active Date**, **Converted Date**, **Client Date**, **Closed Date**, Expected Close Date, Closed Reason, Notes. Only a name, company or email is required.
HubSpot lead statuses are understood too: *New / Open / Attempted to Contact* → Lead, *Connected / In Progress / Bad Timing* → Active Lead, *Open Deal* → Prospect, *Unqualified* → Closed, lifecycle *Customer* → Client.

**Lead score (0–100)** for leads and active leads, when the file has none: lead source (up to 20, referrals highest), timeline (up to 25), estimated value (up to 20), engagement (up to 25, counts only when they **reply**), contact details (up to 10). A contact with 5+ attempts and no reply is capped at 40 (cold). Hot 70+, Warm 45–69, Cold under 45.

**Needs Attention:** leads not contacted 2+ days after they came in, no reply after 5+ attempts (close it?), overdue follow-ups, no contact in 14+ days (30 for nurturing), active leads ready to become prospects, passed close dates, prospects with no next step.

---

## Sales Pipeline

Upload a CSV or Excel file with **one row per deal**. Columns are matched by name, so most CRM exports (HubSpot, Pipedrive, Salesforce, a spreadsheet) work as they are:
Deal Name, Contact, Email, Phone, Sales Rep, Stage, Value, Probability, Created Date, Expected Close Date, Last Contact, Next Step, Next Follow-up, Source, Notes. Only **Stage** and **Value** plus a deal or contact name are required.

- **KPIs:** open pipeline, weighted forecast (value × chance of closing), won, win rate, average deal size, average days to close, closing this month, deals needing attention.
- **Charts:** pipeline by stage, weighted forecast by month, by sales rep, by lead source.
- **Needs Attention:** open deals with an overdue follow-up, no contact in 14+ days, a passed close date or no next step.
- Stages are recognized from common wording (e.g. "Appointment scheduled" → Qualified, "Contract sent" → Negotiation, "Closed won" → Won). When there's no Probability column, each stage gets a standard chance of closing: New Lead 10%, Contacted 20%, Qualified 35%, Proposal Sent 55%, Negotiation 75%.

---

## New Hire

Upload a CSV or Excel file with **one row per new hire**: Full Name (or First / Last Name), Position, Department, Manager, Start Date, Employment Type, Pay Rate, Pay Type (Salary / Hourly), Hours Per Week, Pay Frequency, Email, Phone, Location.
Also: **Hire Type** (*Internal* = joins our organization, *Managed* = we hire them into a client's organization), **Client Organization** and **Placement Fee** for managed hires, and **National/International** with **Country**.
Any other column answered **Yes / No / Pending / N/A or with a date** is treated as a checklist item: Offer Letter, Background Check, I-9, W-4, W-9, Direct Deposit, Emergency Contact, Handbook, Equipment, Accounts, Orientation, and so on.

- **Status:** Ready (everything done), In progress, or At risk (starts within 7 days with items missing).
- **Compliance alerts:** Form I-9 (Section 1 by the first day, Section 2 within 3 business days), Form W-4 before the first payroll, Form W-9 for contractors.
- **Internal vs. Managed:** managed hires are listed by client with placement fees and the salaries placed. They're left out of our payroll and yearly cost, because the client is their employer; their compliance alerts are labeled with the client's name.
- **National vs. International:** international hires get a work-authorization reminder (visa / work permit). Contractors outside the US give **Form W-8BEN** instead of a W-9.
- **Payroll:** yearly pay per person (hourly × hours × 52), monthly wages added, and a yearly cost including 7.65% employer FICA and contractors. State and federal unemployment taxes aren't included.
- Click a person to see their full checklist.

---

## P&L Variance Review

Upload either:
- a simple table: **Account, Category, Budget** (or **Prior Period**), **Actual**, Notes; or
- a **QuickBooks "Budget vs. Actuals"** report exported to CSV or Excel (section headings and total rows are handled automatically).

Categories: Revenue, Cost of Goods Sold, Operating Expenses, Other Income, Other Expenses.

- **Summary in plain English:** net income vs. budget, revenue, costs and the biggest drivers.
- **Charts:** budget vs. actual, net income bridge (from budget to actual, line by line), biggest variances.
- **Lines to explain:** off by at least $1,000 (or 0.5% of revenue) and 10%, or by 2% of revenue or more. Favorable means it helped profit.
- Totals are recalculated from the account lines.

---

## Social Media & Marketing Performance

Upload one or more CSV or Excel exports (Meta Business Suite, Instagram, TikTok, LinkedIn, Google Ads, or your own sheet), with **one row per post, ad or day**:
Date, Platform, Post, Post Type, Impressions, Reach, Likes, Comments, Shares, Saves (or one Engagements column), Clicks, Followers, New Followers, Spend, Leads, Revenue. Any one metric column is enough; if there's no Platform column, the platform is taken from the file name (e.g. `instagram_export.csv`).

- **What Stands Out:** the main findings in plain English: best platform, best post, best day to post, best content type, cheapest leads, return on ad spend, and the latest week or month vs. the one before.
- **KPIs:** impressions and reach, engagement rate, engagements, clicks and click-through rate, new followers, ad spend and cost per click, leads and cost per lead, return on ad spend.
- **Charts:** performance by week (or month), engagement rate by platform, what content works (by post type), best day to post, ad campaign spend and cost per lead.
- **Tables:** platforms side by side, campaign results, top 10 posts, and all posts and ads (search and filter by platform).
- Rows with spend are treated as **ads**. Ads are left out of the engagement rate and "best post", since they're paid to be seen. Return on ad spend counts only campaigns that track revenue.

---

## Dark mode

Open **Settings** (top right) and choose **Light** or **Dark**. Your choice is remembered.

---

## Updates

The app checks for new versions each time it opens. When one is available, a yellow bar appears at the top: click **Update now** and the app downloads the update, closes its window, installs the new version over the old one, and reopens. Only one copy stays installed, and your saved PDF reports are kept.

You can also use **Settings → Check for updates**.

---

## Where your files are

| What | Location |
|---|---|
| PDF reports and the CSV template | `Documents\Rental Agent Reports` |
| Settings, sign-in accounts and customers | `%APPDATA%\RentalAgent` |

---

## Privacy

Everything runs on your computer. Uploaded files and reports are never sent anywhere. The only internet connection is the update check.

---

## Uninstall

**Settings → Apps → Installed apps → Rental Agent → Uninstall.** Your reports in `Documents\Rental Agent Reports` are not deleted.

---

## Troubleshooting

| Problem | Fix |
|---|---|
| "Windows protected your PC" | Click **More info → Run anyway** |
| "Couldn't find the form's columns" | Make sure the first row has the column names, or start from the CSV template |
| Old `.xls` Excel file | In Excel, use **File → Save As** and choose **CSV** or **.xlsx** |
| A property shows "Manual review" | It's missing Property Type, Bedrooms or Email. Fill them in and upload again |
| The window didn't open | Make sure Microsoft Edge is installed (it comes with Windows), then open the app again |

---

© All rights reserved. This software is proprietary and may not be copied, modified, or redistributed without permission.
