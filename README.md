# SVG Palette Editor (SPE)

A standalone, zero-dependency SVG color editor with real-time preview. Edit individual SVG element colors with a full color picker, toggle layer visibility, and export clean SVGs — all from a single HTML file.

## Features

- **Per-element color control** — independent picker for each SVG path/shape
- **Full color picker** — saturation/value square, hue bar, opacity slider
- **Layer visibility** — eye toggle to show/hide individual elements
- **Hover highlighting** — hover a control to glow the corresponding SVG element and dim others
- **Format switching** — cycle between hex, rgba, and hsla with inline arrows
- **Copy per field** — one-click copy of any color value in the active format
- **Multi-size preview** — see your icon at 280, 128, 64, 32, and 16px simultaneously
- **Preview backgrounds** — test against dark, mid, and light surfaces
- **Transparent support** — per-element transparency with checkerboard preview
- **Presets** — 16 built-in color themes with mini icon previews
- **SVG export** — download clean SVG with current colors and visibility
- **Editable labels** — rename layers and descriptions inline
- **Settings** — toggle hover highlighting on/off

## Usage

Open `index.html` in a browser. No build step, no install, no server.

```bash
# Clone and open
git clone https://github.com/jmynes/svg-palette-editor.git
open svg-palette-editor/index.html

# Or just download index.html and double-click it
```

## Customizing for your own SVG

The editor is currently configured for the [PUNT](https://github.com/jmynes/punt) project icon. To use it with your own SVG:

1. Extract your SVG paths into the `PATHS` object
2. Update `PuntIcon` component (rename it) with your paths
3. Adjust the `viewBox` to match your SVG
4. Update `PRESETS` with color themes for your design

Each SVG element gets its own color control — add or remove fields in the `App` component to match your SVG structure.

## Tech

Single HTML file using:
- React 18 (CDN)
- Babel standalone (CDN, for JSX)
- No other dependencies

All color conversion (hex ↔ HSV ↔ RGBA ↔ HSLA), the picker UI, and drag handling are built from scratch — no color picker library.

## License

MIT
