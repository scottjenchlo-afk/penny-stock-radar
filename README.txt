PENNY STOCK RADAR FREE 3.0

Upload the five files in this ZIP to the ROOT of your existing GitHub Pages repository, replacing the existing files, then Commit changes.

This build uses Alpha Vantage TIME_SERIES_DAILY. It uses daily end-of-day OHLCV data only; it is not real-time or 15-minute delayed data.

Alpha Vantage currently publishes a free allowance of 25 API requests/day. The app uses a maximum of 20 new ticker requests per UTC day to leave a safety buffer. It caches each ticker's daily history in this browser, including its retrieval date. Each day it refreshes the oldest cached symbols first, while showing the last cached data for symbols still waiting. A 41-symbol watchlist therefore refreshes over multiple days.

Setup:
1. Get a free API key from https://www.alphavantage.co/support/#api-key
2. Open the app, paste the key in the Alpha Vantage API key field, and Save API key.
3. Run daily scan.
4. Do not share your API key. It is stored in this browser's local storage.

Displayed price and daily percentage change are from the latest daily bar returned by the provider. Average volume, relative volume, RSI, radar score, and planning levels are calculated from returned daily OHLCV history. The app labels older cached rows and never fabricates missing values.

This is a curated watchlist scanner, not every NYSE/NASDAQ/OTC listing. Personal research only; not investment advice or an order-execution system.
