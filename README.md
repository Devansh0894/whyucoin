# WHYUS.co — homepage v2

Updated homepage for **whyus.co.in**. Drop-in replacement for the current page.

## Section order

Hero → Marquee → Numbers → **Our work (the two showreels)** → Three ways to work with us → Voices → Your vision, our creation → FAQ → Footer

## What changed

- **Removed** the old two-card short-form reel block (`files/reel2.mp4`, `files/reel3.mp4`) and its 9:16 grid styling.
- **Moved** *Our work* up to the second screen — directly after the numbers, directly before *Three ways to work with us*.
- **Added** the two long-form animated reels, side by side.
- **Fixed** the supplied `whyus-cofounder-9x16-4k-MUSIC.mp4`: it was a 16:9 render letterboxed into a vertical canvas (black bars top and bottom for all 36s). Cropped back to its true 16:9 frame so both reels match.
- Nav order is now Work → Offerings → Voices → FAQ. The hero *Watch Showreel* button and the footer *Work* link both jump to the new section.

## Reel behaviour

- Click a card to play with sound.
- A **Sound on / Sound off** chip appears while a reel is playing.
- Only one reel plays at a time.
- A reel pauses itself when it scrolls out of view, so audio never plays offscreen.

## Files

| File | What it is |
| --- | --- |
| `index.html` | The full page |
| `files/showreel-brand.mp4` | Studio showreel — 1920×1080, 0:59, 6.9 MB |
| `files/showreel-cofounder.mp4` | Co-founder film — 1920×1080, 0:36, 2.8 MB |
| `files/showreel-brand-poster.jpg` | Poster frame, studio showreel |
| `files/showreel-cofounder-poster.jpg` | Poster frame, co-founder film |
| `WHYUS-homepage-v2.pdf` | Visual handoff — every section, plus the change list |
| `_preview/` | Screenshots used in the PDF. Not needed on the server. |

## To publish

Upload `index.html` and the whole `files/` folder to the site root, keeping that structure. The old `files/reel2.mp4` and `files/reel3.mp4` are no longer referenced and can be deleted.

The 4K masters are untouched in `Downloads/finals/`. The files here are H.264 web encodes with `faststart`, together under 10 MB.

## To preview locally

```bash
python -m http.server 5199 --directory "C:\Users\DELL\Downloads\whyus-site-v2"
```

Then open http://localhost:5199.
