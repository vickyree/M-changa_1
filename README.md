# Victor Keango Wedding Fundraiser

A mobile-friendly fundraising progress page using the supplied poster artwork.

## Files
- `index.html` — fundraiser page and progress display
- `data.json` — current total and fundraiser details
- `assets/wedding-poster.png` — original supplied poster (including its QR code)
- `.github/workflows/update.yml` — deploys the site to GitHub Pages when you push changes

## Update the amount raised
1. Open `data.json` on GitHub.
2. Change the value of `raised` to the latest confirmed M-Changa total (number only, no commas).
3. Commit the change. GitHub Actions will redeploy the page automatically.

Example:
```json
{
  "raised": 45000,
  "target": 320000,
  "deadline": "2026-11-27",
  "paybill": "891300",
  "account": "154144",
  "mchanga": "https://www.mchanga.africa/fundraiser/154144"
}
```

## Publish free with GitHub Pages
1. Create a GitHub repository named `victor-wedding-320k`.
2. Upload the contents of this folder to the repository root (including the hidden `.github` folder).
3. In the repository, open **Settings → Pages** and set the build/deployment source to **GitHub Actions**.
4. Open the **Actions** tab and wait for **Deploy fundraiser site** to finish.
5. Your site URL will appear in the workflow deployment details and under **Settings → Pages**.

## Important note about automatic syncing
This project does **not** scrape M-Changa or automatically read your M-Changa balance. The site reads `data.json`. Updating that one number and committing it triggers an automatic website redeploy. True automatic balance syncing needs an official M-Changa API/feed or a separately configured trusted data source; do not share M-Changa passwords or private dashboard credentials.
