# Coffee Brew Ratio Calculator

Pick a method, choose your input, get exact grams & millilitres.

## Features

- 4 brew methods (Pour Over, French Press, AeroPress, Drip Machine)
- Cups mode or grams mode
- Mild / Medium / Strong strength control
- Live results: water ml, fl oz, coffee g, tbsp
- Copy recipe to clipboard
- Reset to defaults
- Fully responsive (320px → 1440px+)
- Keyboard accessible with ARIA support
- Genuinely offline — zero CDN dependencies
- Respects prefers-reduced-motion

## Usage

Open `index.html` in any browser. No build step needed.

```
npx serve .
python -m http.server 8000
```

## Architecture

Single HTML file. No dependencies.

- `calc(state)` — centralized calculation (single source of truth)
- `parseCups()` / `parseGrams()` — input validation
- System font stack (no CDN fonts)
- Clipboard API with execCommand fallback

## Brew Methods

| Method | Ratio | Cup | Grind | Temp | Time |
|--------|-------|-----|-------|------|------|
| Pour Over | 1:15 | 250ml | Medium-fine | 94°C | 2:30–3:30 |
| French Press | 1:12 | 300ml | Coarse | 96°C | 4:00 |
| AeroPress | 1:13 | 200ml | Medium-fine | 88°C | 1:30–2:00 |
| Drip | 1:16 | 250ml | Medium | 92–96°C | 4:30–5:30 |

## License

MIT
