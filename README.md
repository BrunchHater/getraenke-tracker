# getraenke-tracker
Static drinks tracker. Built by Emil Anuarbekov (2025) for K. St. V. Rheno-Frankonia.

## How to use

1) Open locally
- Double-click `index.html` or serve the folder with any static server.
- All pages (`index.html`, `2025-10-18.html`, etc.) sit next to `styles.css`.

2) Create a new week
- Duplicate an existing week file (e.g., copy `2025-10-18.html` to `YYYY-MM-DD.html`).
- Update the `<title>` and the big date text.
- In the top nav:
  - On previous week: right arrow `href="./YYYY-MM-DD.html"`.
  - On the new week: left arrow `href="./PREV-DATE.html"`, right arrow stays disabled until the next week exists.

3) Update weekly stats
- In the `stats` section, set:
  - **Gesamtschuld** (total), **Schwund**, **Coleur**.
  - **Inventarisierung** pills: `0R 0G 0B 0W 0S` or actual counts.

4) Update “Pflichtzahler bis AC/BC”
- In the “must pay” card, list names separated by commas.

5) Add or edit people cards
- For each person:
  - `Diese Woche`: add ring pills like `11R`, `2G`, `1B`, `1W`, `24Y` (R=red, G=yellow, B=blue, W=white, S=black; `Y` is just a pill label styled as yellow via `pill-g`).
  - `Diese Woche fällig`: computed € for this week.
  - `Gesamt fällig`: cumulative € (use green for positive, red for negative).
  - `Errinerungsgebühr`: fee in € or en dash if none.
- Keep the HTML structure identical to existing cards for consistent styling.

6) Prices legend (bottom)
- Prices are shown in the footer:
  - R = €1.20, G = €0.80, B = €1.00, W = €10.00, S = €15.00.

7) Icons and styles
- Styles: `styles.css` in the root folder.
- Inline SVG icons are embedded in the HTML; no build step is required.

8) Deploy on GitHub Pages
- Push to a public repo.
- In repository settings → Pages → Source = `main` branch, root.
- Your site will be served from `https://<user>.github.io/<repo>/`.

## Notes
- File naming: use ISO dates in filenames, e.g., `2025-10-18.html`.
- Links are relative (`./YYYY-MM-DD.html`), so all week files and `styles.css` must be siblings.
- No JavaScript is required; everything is pure HTML/CSS.

## License
CC0 1.0 Universal (public domain). You may copy, modify, distribute, and use for any purpose without permission or attribution. See <https://creativecommons.org/publicdomain/zero/1.0/>.
