# Kellie's Weekend

Single-page itinerary for July 10–12, 2026 — Santa Fe, Park City, Las Vegas.

Open `index.html` in any browser. No build step.

## Photos

Each property displays a hero photo with a thumbnail strip; clicking a thumb swaps it into the hero.

Photos live under `assets/hotels/<slug>/` and are referenced by name from `index.html`.

```
assets/hotels/
├── ten-thousand-waves-santa-fe/        Property A · Santa Fe   (7 photos)
├── four-seasons-santa-fe/              Property B · Santa Fe   (8 photos)
├── inn-of-the-five-graces-santa-fe/    Property C · Santa Fe   (5 photos)
├── bishops-lodge-santa-fe/             Property D · Santa Fe   (4 photos)
├── waldorf-astoria-park-city/          Property A · Park City  (6 photos)
├── wynn-las-vegas/                     Property A · Las Vegas  (5 photos)
└── waldorf-astoria-las-vegas/          Property B · Las Vegas  (8 photos)
```

### Adding or replacing photos

1. Drop your file into the matching `assets/hotels/<slug>/` folder.
2. Name it `<slug>-photo-NN.<ext>` — e.g. `wynn-las-vegas-photo-06.jpg`.
3. Add a `<div class="thumb"><img alt="..." src="..."></div>` line inside that property's `.thumbs` block in `index.html`.
4. Commit & push.

Supported formats: `.jpg`, `.jpeg`, `.png`, `.webp`, `.avif`.
