# Pixel Player — My Sunflower Haru

A retro / brutalist "pixel" music player card. Single-page static site built with
plain HTML + [Tailwind CSS (CDN)](https://tailwindcss.com/) and vanilla JavaScript.

## Features

- 8-bit / brutalist pixel UI with a bottom nav (Groove / Stash / World / Gear)
- Play / pause with a live progress bar you can click to seek
- **Working volume controls**: `–` / `+` buttons, a clickable & draggable volume meter,
  Arrow Up / Down keyboard shortcuts, and a live `VOL %` readout (mutes to `volume_off` at 0%)
- Now playing: **My Sunflower Haru**

## Files

| File            | Purpose                                  |
| --------------- | ---------------------------------------- |
| `index.html`    | The entire app (markup + styles + JS)    |
| `music.mp3`     | The audio track                          |
| `IMG_2221.jpeg` | Pixel-art album cover                    |
| `netlify.toml`  | Netlify deploy configuration             |

## Run locally

It's a static site, so any static file server works:

```bash
# Option A: Python
python3 -m http.server 8000

# Option B: Node
npx serve .
```

Then open <http://localhost:8000>.

> Browsers block audio autoplay, so playback starts after you press the play button.

## Deploy to Netlify (one click)

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/SmtTheSE/retromusic-card)

Because this is a static site with no build step, Netlify publishes the repository root
directly (see `netlify.toml`). No environment variables or build command are needed.

### Manual deploy (alternative)

1. Go to <https://app.netlify.com/start>.
2. Connect the `SmtTheSE/retromusic-card` repository.
3. Leave the build command empty and set the publish directory to `.` (already set in `netlify.toml`).
4. Click **Deploy**.
