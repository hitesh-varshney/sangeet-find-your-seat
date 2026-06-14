# Sangeet — guest lookup site

A single-page website for the Sangeet: guests scan a QR code, type their name, and see
their table, who's sitting with them, and the room map. Works on any phone. Same look and
behavior as the reception lookup site.

## Files

- `index.html` — the website. (Required on the live site.)
- `seating-data.js` — the only file that changes; each table's number and who sits there. (Required. Replace to update.)
- `README.md` — this file.

## Update when the seating changes (no code)

1. Open `Sangeet Seating Chart/sangeet-builder.html` and make your changes.
2. Click **Save site data** — it downloads a fresh `seating-data.js`.
3. In the Sangeet GitHub repo: Add file → Upload files → drag the new `seating-data.js` (same name) → Commit. The live site refreshes within about a minute.

## Deploy (separate from the reception site)

Host this folder on GitHub Pages in its OWN public repo (e.g. `sangeet-find-your-seat`) so it
gets its own URL and its own QR code. Steps: create the repo → upload `index.html` and
`seating-data.js` → Settings → Pages → deploy from branch `main`, root folder. The URL will be
`https://YOUR-USERNAME.github.io/REPO/`. Send that URL to generate the QR code and printable sign.

## Notes

- 107 guests (102 from the guest list who RSVP'd yes to the Sangeet, plus 5 Sangeet-only guests). Head table = the couple.
- The current `seating-data.js` is an auto-draft starting point — refine it in the builder and re-export.
- Fonts (Allura, Lato, Jost) load from Google Fonts; needs internet, falls back to system fonts offline.
