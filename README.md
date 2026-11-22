# Penny Stock Radar — personal PWA

## What this build does
- Installable Android-friendly web app (PWA).
- Uses a user-provided Finnhub API token to request quotes and daily candles.
- Screens a starter watchlist against your $5 price cap and 500,000 average-volume threshold.
- Lets you add symbols and adjust the screening rules.
- Displays basic momentum/watch labels and optional browser notifications while the app is open.

## Important limitations
- This is a starter watchlist, not a complete market-wide scanner across every NYSE, NASDAQ and OTC security.
- Finnhub's free plan has request limits and data-coverage/delay restrictions. Confirm current plan terms with Finnhub.
- The API token is stored in local browser storage. Anyone with access to this browser profile may be able to retrieve it. This is intended for personal use, not public distribution.
- Scheduled checks run only while the app is open. Push alerts while closed require a server and push-notification setup.
- No brokerage integration or trade execution. Screening flags are not buy recommendations.

## Deploy (required for home-screen installation)
A PWA must be served over HTTPS (or localhost). Easiest path:
1. Create a free GitHub account and a new public repository named `penny-stock-radar`.
2. Upload `index.html`, `manifest.webmanifest`, `sw.js`, and `icon.svg` to the repository root.
3. In repository Settings → Pages, choose deploy from branch `main`, folder `/ (root)`, and save.
4. Wait for GitHub Pages to publish the HTTPS site.
5. Open the published URL in Chrome on Android → menu (⋮) → Install app or Add to Home screen.

## Data setup
1. Create a free Finnhub account at https://finnhub.io and copy your API token.
2. Open the installed app, paste the token and tap Save token.
3. Tap Scan watchlist.

The app makes sequential API calls to reduce the chance of hitting free-tier rate limits.
