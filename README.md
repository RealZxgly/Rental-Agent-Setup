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

No sign-in or account is needed.

---

## Home

The app opens on your dashboards. Pick one, drop in your CSV file, and it does the rest.

| | |
|---|---|
| **NWTFI Sales & Marketing Report** | Upload submissions and see each property's evaluation |

---

## NWTFI Sales & Marketing Report

### 1. Upload the submissions file
Click **Launch dashboard**, then drop your file on the upload box or click **Choose File**.

- **CSV** or **Excel (.xlsx)**. You can select or drop **several files at once**.
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

### Local market data
When a submission includes a **ZIP code**, the evaluation uses that area's short-term rental averages (AirDNA) and its busy season. Florida markets peak in winter, for example. ZIPs outside the built-in market list use U.S. averages, and the evaluation says so.

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
| Settings (theme) | `%APPDATA%\RentalAgent` |

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
