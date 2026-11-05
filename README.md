# Financial CTRL v0.2

## What changed since v0.1

- Transaction / Movement form now reacts to the selected transaction type.
- Expense / Purchase shows **Paid from**, description, category, optional notes, amount, date and status. **Destination account** is hidden for expenses.
- Income / Refund shows **Receive into** instead of a payment source.
- Transfer shows both source and destination and an optional transfer fee.
- Balance adjustment shows the destination account, without a payment source.
- Unused controls are disabled so hidden values are not submitted.
- Added **Groceries** and **Subscriptions** expense categories.
- Version label updated to v0.2.

## Upgrade from v0.1

1. **Export a JSON backup** from the v0.1 menu first.
2. Replace only `index.html` in the root of your existing GitHub Pages repository, then commit.
3. Keep your existing Firebase project, Google Authentication configuration and **published restrictive Firestore rules**. Do not reset Firestore.
4. Reload the published website after GitHub Pages redeploys. The existing Firestore document path and data shape are unchanged.
5. Test an expense and a transfer, including their resulting account balances and transaction history.

## Files

- `index.html` - single-file responsive dashboard with Firebase SDK imported from the official CDN.
- `robots.txt` - discourages indexing, not an access-control mechanism.
- `firestore.rules` - example per-UID isolation rules. **Do not overwrite your already-published single-owner UID rules with these more general example rules** unless you intentionally want each authenticated user to have a separate workspace.

## Notes

The website requires an internet connection for Firebase. Google Sign-In and live Firestore sync must be tested on the deployed GitHub Pages origin. This is an incremental update, not a complete audit of the financial calculation engine. Keep backups and validate transactions before relying on the app for financial decisions.
