# Guía Portada 2026

HTML mini-site that documents every block and template of the El Confidencial 2026 homepage redesign. Mirrors the Notion doc structure but allows local image embedding.

## Quick start

Open `index.html` in a browser. No build step required.

## Adding images

### 1. Design in Figma (Marshall-3)

Each section has its own page in the Marshall-3 Figma file (`MBaHuH8034s6Pg7BgvaJPc`) under "Guía Notion — …" pages. Each page contains:

- **Gray sections** — one per template/case
- **White frames inside** — Desktop (1512px), Tablet (768px), Mobile (375px), Carátula CMS (400×300)

Design your template views inside the white frames.

### 2. Export from Figma

Select the frames inside a section and export as PNG. Files will be named automatically based on the frame names (e.g., `b1_template_a_desktop.png`).

**Note:** Figma adds `.png` to the export, so files arrive as `*.png.png`. Fix with:

```bash
cd ~/Downloads/imagenes\ guia\ portada/
for f in *.png.png; do mv "$f" "${f%.png.png}.png"; done
```

### 3. Place in images folder

Copy the fixed PNGs into `guia-portada/images/`.

### 4. Wire into HTML

In `index.html`, replace the placeholder:
```html
<div class="placeholder">filename</div>
```
with:
```html
<img src="images/filename.png" alt="Description">
```

## File naming convention

```
{section}_{template}_{breakpoint}.png
```

Examples:
- `b1_template_a_desktop.png`
- `b2_c_gran_enfoque_tablet.png`
- `opinion_balcon_estandar_mobile.png`
- `corecito_template_b_carátula_cms.png`

## Structure

```
guia-portada/
├── README.md
├── index.html          # Main site (all sections in one page)
└── images/             # Exported PNGs from Figma
    ├── b1_template_a_desktop.png
    ├── b1_template_a_tablet.png
    ├── b1_template_a_mobile.png
    ├── b1_template_a_carátula_cms.png
    ├── ...
    └── opinion_superopinion_listado_mobile.png
```

## Sections

| Section | Status | Templates |
|---------|--------|-----------|
| B1 — Apertura principal | ✅ Images placed | 6 (A, B, C, C+apoyos, D, E) |
| B2 — Enfoques y análisis | 🔲 Figma ready | 12 (A through K) |
| B3 — Opinión / Eventos / Nichos | 🔲 Figma ready | 3 |
| B4 — El Corecito | ✅ Images placed | 2 (A, B) |
| Issues (B5-B9) | 🔲 Figma ready | 3 |
| Lo mejor de EC | 🔲 Figma ready | 1 |
| Secciones destacadas | 🔲 Figma ready | 2 |
| Secciones secundarias | 🔲 Figma ready | 1 |
| De compras | 🔲 Figma ready | 1 |
| Branded oro | 🔲 Figma ready | 1 |
| Opinión | ✅ Images placed | 5 |

## Figma sources

| File | Key | Purpose |
|------|-----|---------|
| Marshall-3 | `MBaHuH8034s6Pg7BgvaJPc` | Design system + guide template pages |
| Portada EC producción | `4EeCeod1E3YwUrR3ESwp42` | Production layouts with actual cases |

## Frame conventions in Figma

- Parent sections: **gray background** (`#E5E5E5`)
- Child frames: **white background** (`#FFFFFF`)
- Desktop/Tablet/Mobile frames: **24px vertical padding** + horizontal padding for white border effect
- Carátula CMS frames: **16px padding** on all sides, content centered
