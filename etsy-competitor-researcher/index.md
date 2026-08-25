# Privacy Policy — Etsy Competitor Researcher

Last updated: August 25, 2026

## Summary

Etsy Competitor Researcher captures **publicly visible Etsy listing data** (title, price, shop name, rating, review count, description, image URLs, tags, etc.) from the Etsy pages **you open yourself** — single listings, search results, category pages, and shop pages — stores it locally in a research workspace, and lets you export it as CSV or JSON. Everything runs locally in your browser.

## Data read

When you click **Capture**, the extension reads public data already present on the Etsy page you are viewing. This may include:

- Listing title, URL, ID, description, price range, currency, availability
- Shop name, rating, review count
- Category breadcrumb, tags/keywords, product image URLs

This is the same information visible to anyone who visits the page. The extension does **not** collect or request any personal information about you, and does not read sales figures, buyer information, or any non-public data.

## How data is used

The data is used solely to populate the extension's workspace view and to generate CSV/JSON files you choose to export. It is not transmitted anywhere.

## Data storage

- **Local storage (`chrome.storage.local`).** Captured listings and your language preference are stored on your device only. Stored data never leaves your machine.
- You can delete stored listings at any time via **Remove selected** or **Clear all** in the workspace; uninstalling the extension removes everything.
- Exports are written only to files you explicitly save through your browser's download dialog.

## Network activity

- The extension has **no servers and no backend**, makes no analytics or telemetry calls, and loads no remote code.
- The only network requests it ever performs are **direct fetches of Etsy page URLs triggered by your clicks**: extraction reads pages already loaded in your tabs, and the optional "Next page" button fetches the next Etsy results page URL that you explicitly request.
- Nothing is ever sent to any third party.

## Permissions used

| Permission | Why it is used |
| --- | --- |
| `activeTab` | Extract data from the current Etsy tab only when you click Capture |
| `tabs` | Read the active tab's URL to determine whether it is a supported Etsy page |
| `storage` | Store captured listings, batches, and preferences locally on your device |
| `downloads` | Write the CSV/JSON file when you click an export button |
| Host access: `www.etsy.com`, `www.etsy.de` | Content-script access limited to Etsy pages, where on-demand extraction happens |

## Data sharing

No data is sold, shared, or transferred to third parties. Nothing is collected for advertising or analytics.

## Contact

For privacy questions, open an issue on this project's repository.

## Chrome Web Store listing text

### Single purpose

Extract publicly visible Etsy listing data from pages the user opens, store it locally, and export it as CSV or JSON for seller research.

### Permissions justification

- **activeTab:** extraction runs only when the user clicks Capture, granting temporary access to the current Etsy tab.
- **tabs:** determines whether the active tab is a supported Etsy page before extracting.
- **storage:** saves captured listings and preferences locally via chrome.storage.local (never synced).
- **downloads:** writes the CSV/JSON export file the user requests.
- **Host permissions (etsy.com, etsy.de):** content scripts must read publicly rendered listing data on Etsy pages; used exclusively for the single purpose above.

### Data usage

All processing is done locally in your browser. This extension collects no personal information, sends no data to any server, and only reads the public content of Etsy pages the user is viewing.
