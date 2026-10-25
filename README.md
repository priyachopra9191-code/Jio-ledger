# Jio Ledger PWA V1

## Included
- Installable Progressive Web App (PWA)
- Local browser storage
- Dashboard and live recalculated charts
- Create, read, update, duplicate and delete transactions
- Create, edit, rename and delete account definitions
- Separate IPO, special-category, share-trading and adjustment records
- Editable IPO calendar
- JSON full backup and restore
- CSV import/export (CSV opens in Excel)
- Offline cache after first load

## Run locally
A PWA needs HTTPS or localhost; opening `index.html` directly as a `file://` URL will not enable installation or service worker caching.

If Python is installed, run in this folder:
`python -m http.server 8000`
Then open `http://localhost:8000` in a browser.

## Install on Android
1. Host the folder on an HTTPS static host (for example GitHub Pages or Netlify).
2. Open the hosted URL in Chrome on Android.
3. Use Chrome menu > Install app / Add to Home screen.

## Data
All ledger data stays in the browser's local storage. It does not sync across devices. Use Data & Backup > Download full JSON backup regularly. Restoring replaces the current local dataset.

## Data quality note
The starter ledger uses the details available in the prior conversation. Some historical application-level buy mappings were not retained, so those are represented as adjustment/opening records with notes rather than fabricated per-application values. Review the opening rows and reconcile against your original ledger before using the portal for formal accounting.
