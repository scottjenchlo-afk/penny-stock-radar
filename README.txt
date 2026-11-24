PENNY STOCK RADAR 2.0 — UPGRADE

FILES
- index.html: Finnhub quote scan, optional candle-based technical screen, ranking and risk-plan estimates
- manifest.webmanifest: installable app metadata
- sw.js: version 2 cache; network-first app updates; Finnhub requests are never cached
- icon.svg: existing radar icon

UPDATE YOUR EXISTING GITHUB PAGES APP
1. Open https://github.com/scottjenchlo-afk/penny-stock-radar
2. Open the repository's root folder.
3. For each of these four files (index.html, manifest.webmanifest, sw.js, icon.svg), open the file, choose the edit/pencil or upload replacement workflow, and replace it with the matching file from this ZIP. Easiest: Add file > Upload files, select all four files from the extracted penny_stock_radar folder, and choose to overwrite the existing files when GitHub prompts.
4. Commit changes to the main branch.
5. Wait for GitHub Pages to publish.
6. On Android Chrome, open the site, reload it, and if the installed app still shows the old version, close it fully and reopen. The service worker cache version is bumped to v2.

WHAT CHANGED
- Keeps the green radar design and existing Finnhub token stored in this browser.
- Keeps the starter watchlist and adds a curated expanded watchlist plus custom ticker import.
- Fetches quotes for the selected watchlist, then attempts daily candles for up to 12 under-cap symbols to reduce API usage.
- If candle access is available, estimates 20-session average volume, relative volume, RSI(14), 20-day average and ATR-based reference stop/target levels.
- If Finnhub denies candle access, the app labels the data unavailable and does not invent volume or technical signals.
- Scores are screening scores, not buy recommendations. No trades are placed.

LIMITATIONS
- This is a watchlist scanner, not a full-market scan of every NYSE/NASDAQ/OTC symbol.
- Finnhub free plans can restrict historical candle access, quote coverage and request rates. Quote-only access does not verify average volume or technical setups.
- A browser-stored API token is visible to anyone with access to this device/browser. Use only a token appropriate for a personal client-side app.
- Reference stops/targets are formula-based estimates, not guaranteed execution prices or investment advice.
