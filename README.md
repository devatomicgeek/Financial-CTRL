# Financial CTRL v0.6

Updated from v0.5 without changing Firebase configuration or financial calculations.

## Updates
- Minimalist SVG bell replaces the old notification symbol.
- Individual dismiss (X) and CLEAR ALL controls for in-site notifications.
- Dismissed alert keys saved in the existing user Firestore document, so dismissal persists after refresh and syncs across devices.
- Card and loan reminders use month-specific keys, allowing new monthly reminders. Bill alerts are keyed to their bill month.
- Dismissal does not change bill/payment status or any financial amount.

## Upgrade
Export a JSON backup, replace `index.html` on GitHub Pages, and refresh. Keep the current Firestore rules. Test clearing alerts and synchronization on your devices.

Live Firebase integration is not tested by the offline build.
