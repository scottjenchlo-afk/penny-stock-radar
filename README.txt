PENNY STOCK RADAR 2.1

This is a static GitHub Pages app. Upload the files in this ZIP to the root of your existing repository, replacing the previous files, then commit the changes.

Version 2.1 change:
- Shows the first actual Finnhub candle API error instead of hiding it.
- Clearly labels quote-only results when no technical candle data is available.
- Avoids implying a technical ranking when technical data is missing.
- Does not fabricate volume, RSI, scores, signals, stops, or targets.

Important:
Finnhub may provide quote access without providing daily candle/history access on the user's plan or for a particular symbol. If the diagnostic reports HTTP 403 / "You don't have access to this resource", the Finnhub account lacks access to that endpoint. An app code change cannot bypass that provider restriction; use a plan/provider that permits daily historical OHLCV data.

Your saved token is stored in the browser's local storage and is not included in this ZIP. Do not share it.
