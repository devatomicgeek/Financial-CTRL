# FINANCIAL CTRL_ v0.5

## What changed
- Centered mobile sign-in card within the device viewport; removed horizontal overflow.
- Restored heavy condensed FINANCIAL CTRL_ typography on the sign-in screen and dashboard hero.
- Improved mobile heading, subtitle, description, and section-heading weight, scale, and spacing.
- Added resilient font fallbacks if Google Fonts are unavailable.
- Kept desktop design and existing financial logic, Firebase project configuration, and Firestore document paths unchanged.

## Deployment
1. Export a JSON backup from your currently deployed site.
2. Replace the repository root `index.html` with the v0.5 version.
3. Commit and wait for GitHub Pages deployment; hard-refresh on your phone.
4. Test login, dashboard, balances, transactions, and cross-device sync.
5. Keep your currently published restrictive Firestore rules; no migration is required.

## Notes
Google Fonts (Anton and Roboto Slab) load from Google when available, with local font fallbacks. Browser and Firebase live integration tests must be completed after deployment.
