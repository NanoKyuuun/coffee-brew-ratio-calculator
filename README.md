# Coffee Brew Ratio Calculator

Dial in the perfect coffee-to-water ratio for any brew method. Pick a method, choose your input mode, and get exact grams and millilitres — instantly.

## Features

- **4 brew methods** — Pour Over, French Press, AeroPress, Drip Machine — each with its own default ratio, grind size, temperature, and brew time
- **Two input modes** — enter the number of cups you want, or the grams of coffee you have
- **Strength slider** — Mild / Medium / Strong adjusts the ratio ±2
- **Live results** — water (ml & fl oz), coffee (g & tbsp), ratio bar, and brew guide update as you adjust
- **Copy recipe** — one-click copies the full recipe to clipboard
- **Reset** — restore defaults instantly
- **Fully responsive** — works on mobile, tablet, and desktop
- **Keyboard accessible** — full tab navigation, focus-visible indicators, ARIA roles
- **Offline-friendly** — no server required, single HTML file with CDN fonts

## Getting Started

No build step required. Open `index.html` in any modern browser.

```bash
# Local development — just open the file
open index.html

# Or serve with any static file server
npx serve .
python -m http.server 8000
```

## Architecture

Single-file vanilla HTML/CSS/JS — zero dependencies beyond Google Fonts CDN.

```
index.html    — everything: markup, styles, logic
README.md     — this file
```

### Structure inside `index.html`

| Section | What it does |
|---------|-------------|
| `<style>` | All CSS with custom properties, responsive grid, animations |
| Controls card | Method selector, cups/grams toggle, stepper inputs, strength slider |
| Results panel | Live calculations, ratio bar, brew guide pills, copy/reset actions |
| `<script>` | State management, render loop, event handlers, clipboard API |

### Key design decisions

- **No framework** — vanilla JS keeps the file small and fast. The IIFE avoids global scope pollution.
- **CSS custom properties** — theming via `--vars`, easy to tweak the palette.
- **`aria-live="polite"`** on results — screen readers announce changes without interrupting.
- **`font-variant-numeric: tabular-nums`** — numbers don't jump around when values change.

## Brew Methods

| Method | Ratio | Cup Size | Grind | Temp | Time |
|--------|-------|----------|-------|------|------|
| Pour Over | 1:15 | 250 ml | Medium-fine | 94°C / 201°F | 2:30–3:30 |
| French Press | 1:12 | 300 ml | Coarse | 96°C / 205°F | 4:00 |
| AeroPress | 1:13 | 200 ml | Medium-fine | 88°C / 190°F | 1:30–2:00 |
| Drip Machine | 1:16 | 250 ml | Medium | Auto (92–96°C) | 4:30–5:30 |

## Conversions

- 1 tbsp ≈ 5.5 g of ground coffee
- 1 fl oz ≈ 29.6 ml

## License

MIT
