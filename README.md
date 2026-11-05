# Financial CTRL_ v0.4

Visual update based on v0.3. No ledger or Firestore schema changes.

## What's new
- Finance-bar SVG brand and `FINANCIAL CTRL_ v0.4` header.
- Lightweight CSS 3D data cube with staggered assembly, idle motion, and reduced-motion support.
- Custom theme-aware month/year picker instead of the browser-native month popup.
- Notification and account-menu popovers anchored beneath their respective buttons.
- Centered SVG plus icon in floating Add Transaction button.
- Credit card donut content centered with safer font sizing.

## Deploy
1. Export a JSON backup from the currently running v0.3 site.
2. Upload **index.html** to the root of the existing GitHub Pages repository, replacing the old file.
3. Commit and refresh after Pages deploys. Hard-refresh if necessary.
4. Keep your existing **published UID-restricted Firestore rules**. Do not replace them with the example `firestore.rules` unless you have reviewed the change.
5. Verify existing balances and transactions, and test all five visual changes on desktop and mobile.

## Security
The public Firebase web configuration is embedded in index.html as before. Authentication and Firestore rules enforce access. `robots.txt` discourages indexing but is not an access-control mechanism.

## Testing
Static code and JavaScript syntax checks can be performed offline. Real Firebase sync and browser layout must be checked on the deployed website.
