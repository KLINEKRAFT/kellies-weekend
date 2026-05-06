# Kellie's Weekend

Single-page itinerary for July 10–12, 2026 — Santa Fe, Park City, Las Vegas.

## Adding hotel photos

Each property loads photos automatically from a folder under `photos/`.
Drop in **up to 5 photos per property**, named `01`, `02`, `03`, `04`, `05`
(any of `.jpg`, `.jpeg`, `.png`, `.webp`).

```
photos/
├── ten-thousand-waves/        Property A · Santa Fe
├── four-seasons-rancho/       Property B · Santa Fe
├── inn-five-graces/           Property C · Santa Fe
├── bishops-lodge/             Property D · Santa Fe
├── waldorf-park-city/         Property A · Park City
├── wynn-las-vegas/            Property A · Las Vegas
└── waldorf-las-vegas/         Property B · Las Vegas
```

### Steps

```bash
git clone https://github.com/KLINEKRAFT/kellies-weekend.git
cd kellies-weekend
git checkout claude/create-kellies-weekend-9Zm8r

# Drop your photos:
#   photos/ten-thousand-waves/01.jpg
#   photos/ten-thousand-waves/02.jpg
#   ...etc

# Preview locally:
python3 -m http.server 8000
# open http://localhost:8000

git add photos/
git commit -m "add hotel photos"
git push
```

### How it works

- `01` becomes the hero image; `02`–`05` form a thumbnail row beneath.
- If a folder is empty, the editorial SVG poster shows in its place — no broken images.
- Photos can be any aspect ratio; they're cropped to fit. Landscape works best for the hero.
- Recommended size: ~1600px wide for the hero, ~600px wide for thumbs. JPG quality 80.

### Property slugs (the folder names)

| Folder | Property |
|---|---|
| `ten-thousand-waves` | Ten Thousand Waves, Santa Fe |
| `four-seasons-rancho` | Four Seasons Rancho Encantado, Santa Fe |
| `inn-five-graces` | Inn of the Five Graces, Santa Fe |
| `bishops-lodge` | Bishop's Lodge (Auberge), Santa Fe |
| `waldorf-park-city` | Waldorf Astoria Park City |
| `wynn-las-vegas` | Wynn Las Vegas |
| `waldorf-las-vegas` | Waldorf Astoria Las Vegas |
