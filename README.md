MY BILLS — INSTALLABLE WEB APP PACKAGE (v3)

UPLOAD INSTRUCTIONS FOR GITHUB PAGES
1. Extract this ZIP on your computer.
2. Upload the CONTENTS of this folder to the root of your existing GitHub repository, replacing the older index.html, manifest.webmanifest, and sw.js. Include the icons folder and its two PNG files. Do not upload the ZIP itself.
3. Commit the changes. GitHub Pages should publish from main / (root).
4. Open https://YOUR-USERNAME.github.io/my-bills/ in Chrome on Android. Refresh the page after deployment. Use Chrome's menu and look for Install app or the equivalent install option; wording varies by device/browser.

INCLUDED
- index.html: bill tracker
- manifest.webmanifest: app identity and install metadata
- sw.js: offline caching service worker
- icons/: 192px and 512px install icons

IMPORTANT LIMITATIONS
- This improves installability but cannot guarantee that every browser/device will offer installation. Browser requirements and menu wording vary.
- Data remains local to each browser/device. Installing the app does not synchronize bills. Use Export Backup / Import Backup to transfer a copy. Do not place backups in a public repository.
- Notifications are checked while the app is open. This package does not provide guaranteed scheduled reminders while closed.
- The app is free to host on GitHub Pages in a public repository, but repository source files are publicly visible. Never upload private bill backups or credentials.


## Payment and History fixes (v4)
- Fully paid one-time bills are moved to History.
- Fully paid installment plans reduce the tracked plan balance and move to History at $0.00.
- Paid recurring bills advance to their next due date and reset the current-cycle payment fields.
- New recurring bills no longer create duplicate future bill entries.
- Existing local browser data key remains `myBillsFreeV1`; export a backup before replacing files.

## Revolving credit and recurring installment rollover (v5)
- Credit-card payments now satisfy the cycle when the entered payments reach the configured minimum payment; if no minimum is entered, the planned monthly payment is used as the threshold.
- When the credit-card threshold is met, the due date advances by the selected recurrence and the next cycle's paid-this-cycle amount resets to zero. The unpaid card balance remains tracked; the recorded payment is applied against that balance.
- Recurring installment plans advance to their next due date after the scheduled installment has been paid, while retaining the remaining plan balance. They move to History only when the plan balance reaches zero.
- Completed cycle payments are retained in each bill's `paymentHistory` data when exported. Existing payment history is preserved when editing a bill.


## Account type behavior

- **Recurring fixed payment / regular bill** (car payment, insurance, utilities): remains active. When the scheduled amount is paid, the current cycle is recorded and the due date advances according to its recurrence. The next cycle payment amount resets.
- **Credit card / revolving account**: remains active and carries any remaining statement balance forward. The cycle advances when the entered minimum payment is met; if no minimum is entered, the planned payment is the threshold.
- **Payoff installment plan** (Afterpay, Klarna, etc.): each payment reduces the remaining plan balance. The due date advances after the scheduled installment is met. The plan is moved to History only when its remaining balance reaches $0.00.

Existing `regular`, `credit`, and `installment` saved bill type values are retained for compatibility with existing browser data.
