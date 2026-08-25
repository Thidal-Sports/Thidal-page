# Thidal Sports

Static one-page site for the Thidal Sports ground in Palavedu, Avadi. Plain HTML,
CSS and JavaScript — no framework, no build step.

## Files

- `index.html` — the whole page.
- `styles.css` — all styling, dark theme driven by CSS variables (`--accent` is the green).
- `script.js` — footer year, gallery lightbox, video play/pause, active nav tab.
- `images/` — logo, gallery photos, video poster.
- `media/opening.mp4` — the opening clip (silent, logo watermark, branding fades in at the end).

## Page layout

Top to bottom:

1. **Sticky header** — logo + name on the left, pill nav tabs on the right
   (`About us`, `Facilities`, `Hours`, `Location`, `Gallery`, `Contact`). The tab
   for the section you are scrolled to is highlighted; sections carry
   `scroll-margin-top` so anchor jumps clear the header.
2. **Hero** (`#top`) — logo, "Thidal Sports", tagline and the "Book the turf" CTA.
3. **Video band** — full-width autoplaying muted loop. Native controls are off; a
   single custom play/pause button (and clicking the video) toggles playback.
4. **About us** (`#about`) — short intro plus a `.facts` list (sports, surface, lighting).
5. **Facilities** (`#facilities`) — each group is a bordered `.facility-box` holding
   its `<h3 class="facility-group">` and a grid of cards: Coaching & classes and
   Amenities are `.facility-box-full` (full width), while Practice and Events share a
   row in the two-column `.facility-boxes` grid (one column under 40rem). Cards use
   `auto-fill` columns so they keep the same width, and each is an icon + name, a
   one-line note, and a call or booking link.
6. **Opening hours** (`#hours`) — day/time rows.
7. **Location** (`#location`) — address, Google Maps directions link and an embedded map.
8. **Gallery** (`#gallery`) — mosaic of tiles; `tile-wide`, `tile-tall` and `tile-xwide`
   make some photos span extra columns/rows. Clicking a photo opens the lightbox
   (click anywhere or press Escape to close).
9. **Contact** (`#contact`) — card grid: the two phone cards stack in the first column,
   Visit (map) and Instagram sit beside them full height, with the TurfTown booking
   button below the grid.
10. **Footer** — copyright with the year filled in at runtime.

Responsive rules: the gallery drops to two columns under 52rem (shorter rows under
26rem), the contact grid collapses to one column under 40rem, and under 400px the
section scroll offset grows so a two-row header still clears the headings.

## Local preview

```bash
python3 -m http.server 8000
# open http://localhost:8000
```
