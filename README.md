**[▶ Open App](https://archaeoscan.github.io/MapRuler/MapRuler.html)**


# MapRuler

**MapRuler** is a lightweight, browser-based tool for calibrating and measuring distances and areas on historical maps, architectural plans, and other scanned documents with a known scale.

No installation required — just open `MapRuler.html` in any modern browser.

---

## Features

- 📐 **Calibrate** using any known reference length (e.g. a scale bar)
- 📏 **Measure distances** between two or more points
- 🔲 **Measure areas** by drawing a polygon
- 🖼️ **Load images** via file dialog or paste (Ctrl+V / Cmd+V)
- 🔍 **Zoom & Pan** with mouse wheel and drag
- 💾 **Export** all measurements as JSON
- Works entirely offline — no server, no data upload

---

## Workflow

1. **Load an image** — click *Load image* or paste with Ctrl+V / Cmd+V
2. **Calibrate** — select the *Calibrate* tool, click two points on a known reference (e.g. scale bar), enter the real-world length and unit
3. **Measure** — switch to *Distance* or *Area*, click to place points, double-click to finish
4. **Export** — click *↓ Export* to save all measurements as a JSON file

> 💡 You can change the real-world length after placing calibration points — the calibration updates automatically.

---

## Keyboard Shortcuts

| Key | Action |
|-----|--------|
| Ctrl+V / Cmd+V | Paste image from clipboard |
| Double-click | Finish distance or area measurement |
| Mouse wheel | Zoom in/out |
| Middle mouse / drag (no tool) | Pan |

---

## Export Format

Measurements are exported as JSON:

```json
{
  "calibration": {
    "unitsPerPixel": 0.123,
    "unit": "m"
  },
  "measurements": [
    { "type": "distance", "pixels": 342.5, "real": "42.1 m" },
    { "type": "area", "pixels2": 15234, "real": "230.5 m²" }
  ]
}

