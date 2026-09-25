# Rental Agent

A Windows desktop app that turns rental-analysis lead emails into a PDF report and emails it back to the lead, all from one window.

**Search Gmail → Generate the report → Send it**

---

## Download

👉 **[Download the latest version](../../releases/latest)**. Under **Assets**, click `RentalAgentSetup.exe`.

**Requirements:** Windows 10 or 11 and a Gmail / Google account.

---

## Install

1. Run `RentalAgentSetup.exe`.
2. If Windows shows **"Windows protected your PC"**, click **More info → Run anyway**. This appears because the app isn't code-signed.
3. Click **Next → Install**. No administrator rights are needed.
4. Open **Rental Agent** from the Start menu or the desktop shortcut.

---

## First-time sign-in

1. Click **Sign in with Google** in the top-right corner.
2. A browser tab opens. Choose your Google account.
3. If you see **"Google hasn't verified this app"**, click **Advanced → Go to Rental Agent**.
4. Allow both permissions:
   - **Read your email**, to find lead emails
   - **Send email on your behalf**, to send the report
5. Go back to the app. It shows **Signed in as your@email.com**.

You only need to do this once; the app remembers you. To use a different Gmail, click **Switch account**.

> If sign-in says **"Access blocked"**, your Google account hasn't been approved for the app yet. Contact the app administrator to be added.

---

## How to use

### 1. Find the lead email
- Type part of the email subject (default: `Free Rental Analysis`).
- Optionally, type the sender's address.
- Click **Search Gmail**. Matching emails appear newest first.

### 2. Generate the report
- Select an email, then click **Generate Report** (or double-click the email).
- The app shows the lead's details, a lead status (**HOT**, **WARM**, **INVESTOR**, or **MANUAL REVIEW**), and the 12-month revenue projection.
- **View Report** opens the PDF.
- **Reports Folder** opens all saved reports.

If an email is missing required information (address, property type, bedrooms, bathrooms, or max guests), the lead is marked **MANUAL REVIEW** and no report is created.

### 3. Email the report
- The **To** box is filled in with the lead's email automatically. You can change it.
- Edit the **Subject** and **Message** if you like.
- Click **Send Email**. The PDF is attached and sent from your Gmail account.

---

## Dark mode

Click **☾ Dark mode** / **☀ Light mode** in the top-right corner to switch themes. Your choice is remembered.

---

## Updates

The app checks for new versions each time it opens. When one is available, a yellow **⬆ Update to vX.X.X** button appears in the top-right corner.

Click it and the app downloads the update, installs it, and reopens automatically. You don't need to uninstall anything, and your sign-in, theme, and reports are kept.

The current version is shown in the bottom-right corner of the app.

---

## Where your files are

| What | Location |
|---|---|
| PDF reports | `Documents\Rental Agent Reports` |
| Sign-in and settings | `%APPDATA%\RentalAgent` |

---

## Privacy

- The app connects **only** to your own Gmail account, using Google's official sign-in.
- Your password is never seen or stored by the app.
- Emails are read and sent directly between your computer and Google. Nothing is sent to any other server.
- You can remove the app's access at any time at [myaccount.google.com/permissions](https://myaccount.google.com/permissions).

---

## Uninstall

**Settings → Apps → Installed apps → Rental Agent → Uninstall.**

Your reports in `Documents\Rental Agent Reports` are not deleted.

---

## Troubleshooting

| Problem | Fix |
|---|---|
| "Windows protected your PC" | Click **More info → Run anyway** |
| "Access blocked" on Google sign-in | Your account needs to be approved; contact the administrator |
| App says "Not signed in" again | Your sign-in expired. Click **Sign in with Google** |
| No emails found | Check the subject text matches the lead emails, or clear the **From** box |
| Report didn't open | Make sure a PDF viewer is installed (Microsoft Edge works) |

---

© All rights reserved. This software is proprietary and may not be copied, modified, or redistributed without permission.
