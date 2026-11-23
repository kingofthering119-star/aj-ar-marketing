# AJ.AR Marketing — Dairy Manager

A responsive, installable web app for milk/curd stock, supplier receipts, salesman daily sheets, editable rates and cash settlement. It works in a modern laptop/mobile browser. Open `index.html` for a basic preview; to use install/offline support, serve the repository over HTTPS (for example GitHub Pages or another static host).

## Current first version
- Daily entry by date and salesman, with editable quantities/rates and computed line amounts.
- Product equivalences shown separately: 500 ml = 0.5 L/kg per packet; no automatic change to entered sheet quantities.
- Editable salesman/product rate table and rate-change history. Saved records retain the rate entered at the time.
- Stock receipts for Priya, KNR, or a new supplier; available stock is received less saved salesman entries.
- Settlement fields for extra, return/retren, previous due, cash and coins; CSV export.
- Responsive phone/laptop UI and PWA/offline shell.

## Important data/verification notes
- Browser storage (`localStorage`) is used in this initial version. Data stays in that browser/device; this release does **not** synchronize phone and laptop. Export CSV regularly. Multi-device sync requires a secured backend and authentication before using for real accounts.
- Seeded product prices are transcribed from the photos, with Sohel's visible prices as the stated fallback. Verify uncertain or obscured figures before relying on them for accounting. Quantity examples from the photos are deliberately not imported as live stock/sales records because they appear to be separate day sheets and importing them without dates could double-count.
- The photos clearly identify Shankar, Surender, Sohel, Mahraj, Rajesh, Narsing and Saleem. Six slots remain editable placeholders. POINT is included as seen in the sheet but may be a route/location; confirm its status.
- Quantities/rates in the sheet are treated as the entered billing unit. 500 ml equivalences are informational. The exact business rule for five-packet rates/slabs is not inferred or auto-applied.

## Run locally
Serve this folder with any static HTTP server. Example: `python3 -m http.server 8000`, then open `http://localhost:8000`. For production, use HTTPS. No build step or npm dependencies are needed.
