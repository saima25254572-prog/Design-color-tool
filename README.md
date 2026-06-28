# 🎨 Chroma — Color Toolkit

A free, fast, multi-page color tool website. No frameworks, no build step — just HTML, CSS, and vanilla JS.

## Features

| Page | Tool | Description |
|------|------|-------------|
| `/pages/palette.html` | Palette Generator | Generate complementary, analogous, triadic, tetradic, or monochromatic palettes. Export as CSS variables or JSON. |
| `/pages/gradient.html` | Gradient Maker | Create linear, radial, or conic gradients. Quick presets + CSS export. |
| `/pages/converter.html` | Color Converter | Convert HEX ↔ RGB ↔ HSL ↔ HSV ↔ CMYK. WCAG contrast checker included. |
| `/pages/picker.html` | Color Picker | Visual canvas picker with hue + alpha sliders. Copy HEX, RGB, HSL, RGBA, HSLA in one click. |

## Deploy to GitHub Pages

1. Push this folder to a GitHub repository.
2. Go to **Settings → Pages**.
3. Set source to `main` branch, `/ (root)`.
4. Your site will be live at `https://yourusername.github.io/your-repo-name/`

## Project Structure

```
/
├── index.html          # Home / navigation hub
├── css/
│   └── shared.css      # Shared styles (nav, buttons, cards, etc.)
└── pages/
    ├── palette.html
    ├── gradient.html
    ├── converter.html
    └── picker.html
```

## No dependencies

- Google Fonts (Space Grotesk + Space Mono) loaded via CDN
- Zero npm, zero build tools — just open `index.html`
