MY BILLS — PAYMENT TYPE AND AFTERPAY FIX

FILES
- index.html: updated app. Upload this file to the ROOT of the GitHub repository, replacing the existing index.html.
- README.md: these instructions. It is optional and may also be uploaded to the repository root.

BILL TYPES
1. Regular bill: utilities, subscriptions, and one-time expenses.
2. Recurring fixed installment: car payments, insurance premiums, and personal loans. The scheduled payment completes the current cycle and advances the due date; the account remains active even when a loan balance exists.
3. Credit card / revolving account: advances to the next cycle once the minimum payment (or planned payment if no minimum is entered) is met; the card balance carries forward.
4. Payoff installment plan: Afterpay/Klarna-style plans. Payments reduce the plan balance. When it reaches $0.00, payments remaining is set to zero and the plan moves to History.

IMPORTANT
- Export a backup from the current app before replacing index.html.
- Extract this ZIP and upload index.html directly to the repository ROOT. Do not upload the ZIP itself or put index.html inside a nested folder.
- Existing local browser data uses the same storage key: myBillsFreeV1.
- GitHub Pages may take a few minutes to redeploy. Hard-refresh the app after deployment.
- This update has been syntax-checked and archive-checked, but has not been tested with your private saved bill data.
