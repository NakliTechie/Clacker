# Clacker

Browser-native split-flap display. Type a message, pick a style, watch it flip.

🪧 **Try it now →** https://naklitechie.github.io/Clacker/

Clacker is part of the **NakliTechie** series of browser-native tools: single-file apps that run entirely on your device. No server. No dependencies. No install.

---

## Features

- **Split-flap animation** — Each tile cycles through random characters before landing, with a staggered column-by-column cascade — exactly like a real departure board.
- **Mechanical sound** — Click sounds generated in real-time via the Web Audio API. Each flip has a slightly randomised pitch and timing for an authentic clatter.
- **6 colour presets** — Classic (white on black), Airport (amber), Matrix (green), Neon (violet), Chalk (inverted), Sunrise (orange).
- **10 font choices** — Impact (default), Arial, Arial Black, Verdana, Tahoma, Trebuchet MS, Georgia, Times New Roman, Courier New, Comic Sans.
- **Multiple slides** — Separate messages with `---` on its own line. Auto-cycle flips through them at a configurable interval.
- **Auto-cycle** — Board animates through slides automatically. Default interval: 30 seconds. Configurable from 5 to 600 seconds.
- **Fullscreen mode** — Board scales to fill the screen. One keypress in, one keypress out.
- **Blank row support** — Empty lines in your message render as blank rows on the board.
- **Responsive** — Board scales down on smaller viewports automatically.

---

## Board

6 rows × 22 columns = 132 characters per slide. Each character is rendered on an individual split-flap tile with a physical hinge line, depth gradient, and scan-line overlay on the frame.

---

## Keyboard shortcuts

| Key | Action |
|-----|--------|
| `Enter` | Run animation |
| `Shift + Enter` | New line in message |
| `F` | Toggle fullscreen |
| `Esc` or double-click | Exit fullscreen |

---

## Multiple slides

Separate slides with `---` on its own line:

```
GATE A14  LONDON
DEPARTURE 09:30

DELAYED

STATUS BOARDING
---
CLACKER

SPLIT FLAP DISPLAY
IN YOUR BROWSER
```

Enable **Auto-cycle** to have the board flip through slides automatically. The green indicator dot in the controls shows the countdown to the next slide.

---

## Running locally

No build step. No dependencies. Just open the file:

```bash
# Option 1: open directly
open index.html

# Option 2: serve with Python
python3 -m http.server 8000
# Then visit: http://localhost:8000
```

---

## Tech stack

| Concern | Solution |
|---------|----------|
| Tile animation | CSS 3D `rotateX` keyframes with `perspective` |
| Sound | Web Audio API — generated noise buffer, no files |
| Layout | CSS Grid, 22 cols × 6 rows |
| Text wrapping | ~40 lines of vanilla JS |
| Fullscreen | Native `requestFullscreen()` API |
| Dependencies | Zero — pure HTML, CSS, JS |

---

## Why browser-native?

A real Vestaboard costs $995, needs Wi-Fi, an account, and a companion app. Clacker runs in a browser tab. Press `F` and it fills your screen.

Built for ambient displays, presentations, digital signage, or just the satisfaction of watching characters clack into place.

---

## Part of the NakliTechie series

| Tool | What it does |
|------|--------------|
| [**BabelLocal**](https://github.com/NakliTechie/BabelLocal) | Offline translation — 200 languages, NLLB model |
| [**StripLocal**](https://github.com/NakliTechie/StripLocal) | EXIF metadata stripper — nothing leaves the browser |
| [**GambitLocal**](https://github.com/NakliTechie/GambitLocal) | Chess vs Stockfish — correspondence mode via URL |
| [**VoiceVault**](https://github.com/NakliTechie/VoiceVault) | Audio transcription — Whisper, offline-first |
| [**KingMe**](https://github.com/NakliTechie/KingMe) | English draughts — custom minimax AI, zero deps |
| [**SnipLocal**](https://github.com/NakliTechie/SnipLocal) | Background remover — RMBG-1.4, passport mode |
| **Clacker** | Split-flap display — browser-native, offline |

---

**Built by [Chirag Patnaik](https://github.com/NakliTechie)**
