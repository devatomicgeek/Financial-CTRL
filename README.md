# Financial CTRL v0.3

## Changes from v0.2

Transfer between accounts now supports **two separate fees**:

- **Sender fee**: deducted from the sending account in addition to the transfer amount.
- **Receiver fee**: deducted from the amount credited to the receiving account.
- Transfer preview shows source deduction, net received, and combined fees.
- Both fees are included in monthly expenses; the transferred principal is not income or expense.
- Editing or deleting a transfer recalculates both accounts and monthly expenses.
- Existing v0.2 transfers remain compatible: missing `receiverFee` is treated as zero.
- Planned transfers affect projected balances only until confirmed.

### Example

Transfer 1,000 Credits from NEXUS_01 to NEXUS_02 with sender fee 5 and receiver fee 2:
- NEXUS_01: -1,005
- NEXUS_02: +998
- Monthly expenses: +7
- Combined account balance change: -7

## Upgrade

1. Export a JSON backup from your live v0.2 site before changing anything.
2. Upload **only `index.html`** from this package to your existing GitHub Pages repository root, replacing the old file.
3. Commit, wait for deployment, and hard-refresh the site.
4. Keep your existing Firebase project and **already published single-owner UID Firestore rules**. Do not replace them with the generic example included here.
5. Test one transfer, edit its fees, then delete it; verify balances and monthly expenses after each operation and after a reload.

## Files

- `index.html` - single-file dashboard (Firebase config unchanged)
- `robots.txt` - discourages indexing, does not secure the site
- `firestore.rules` - generic example for per-user data; **not** a replacement for your current stricter UID-locked rules
- `README.md` - these notes

## Caution

The existing app's broader financial logic has not been fully audited. Live Google login and Firestore synchronization must be verified on your published domain. Always retain a backup before upgrading.
