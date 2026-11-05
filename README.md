# FINANCIAL CTRL v0.1

Static, responsive GitHub Pages personal finance dashboard. Uses Firebase Google Authentication and Cloud Firestore. No financial records are bundled with the website.

## Deployment
1. Upload `index.html`, `robots.txt`, and this README to the root of your `financial-ctrl` GitHub repository.
2. GitHub repository > Settings > Pages > Deploy from a branch > `main` / `(root)` > Save.
3. Firebase Console > Authentication > Settings > Authorized domains: add your GitHub Pages **hostname** (e.g. `yourname.github.io`, without protocol or path).
4. Visit your deployed website and sign in with Google. If you see a permissions error, this is expected while Firestore remains locked.
5. Firebase Console > Authentication > Users: copy your UID. In Firestore Database > Rules, paste the contents of `firestore.rules`, replace `YOUR_FIREBASE_UID` with your actual UID, then **Publish**. Do not commit the UID-customized rules to a public repository if you prefer not to disclose it.
6. Refresh the site. It should sync your records. Test on mobile and desktop.

**Security:** Do not publish open/test Firestore rules. The website code is public; your financial data is protected by Firestore rules. `robots.txt` and the `noindex` meta tag only discourage indexing, not access. A Firebase web API key is not a secret.

**Backups:** Export JSON regularly. Import replaces the currently signed-in user's dataset after confirmation. All financial calculations are client-side and intended for personal tracking, not bank reconciliation or financial advice.

**Version:** 0.1. The interface is a new recreation inspired by the supplied screenshots, not a copy of the old website's source code.
