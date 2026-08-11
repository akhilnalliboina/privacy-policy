# Privacy Policy — Etsy Competitor Researcher

Last updated: August 11, 2026

## Summary
Etsy Competitor Researcher extracts the **public data of an Etsy listing** (title,
price, shop name, description, tags, image URLs, ratings, etc.) from the Etsy
listing page you are currently viewing, displays it in the extension popup, and
lets you copy or export it as a CSV file. Everything runs locally in your
browser.

## Data collected
When you click **Analyze listing**, the extension reads the public listing data
that is already present on the Etsy page you are viewing. This may include:

- Listing title, URL, ID, description, price, currency, availability
- Shop name, sales count, tenure, reviews, and ship-from location
- Rating, review count, favorites, views, listing date
- Tags, materials, and product image URLs

This is the same information visible to anyone who visits the listing page. The
extension does **not** collect or request any personal information about you.

## How data is used
The data is used solely to populate the popup display and to generate CSV files
you choose to copy or download. It is not transmitted anywhere.

## Data storage
- **In-memory only.** A single analyzed listing is held in the popup for the
  lifetime of that popup session.
- **Local storage (`chrome.storage.local`).** Listings you explicitly click
  **Save listing** on are stored on your device only. Stored data never leaves
  your machine and is removed when you click **Clear**.
- **No remote servers.** The extension makes no network requests of its own. All
  extracted data originates from the Etsy page you are viewing, over Etsy's
  existing HTTPS connection.

## Permissions used
| Permission | Why it is used |
| --- | --- |
| `activeTab` | Read the URL of the current tab to confirm you are on an Etsy listing |
| `storage` | Store listings you choose to save, locally on your device |
| `downloads` | Download the CSV file when you click **Export CSV** |

## Data sharing
No data is sold, shared, or transferred to third parties. Nothing is collected
for advertising or analytics.

## Contact
For privacy questions, open an issue on this project's repository.

## Chrome Web Store listing text

### Single purpose
Analyze the current Etsy listing page and copy or export its public data as CSV.

### Permissions justification
- **activeTab:** determines whether the current page is an Etsy listing so the
  extension only runs there.
- **storage:** saves listings you explicitly store, locally on your device.
- **downloads:** saves the CSV file you export.

### Data usage
All processing is done locally in your browser. This extension collects no
personal information, sends no data to any server, and only reads the public
content of the Etsy listing page you are viewing.
