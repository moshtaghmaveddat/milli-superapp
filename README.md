# Milli SuperApp — IA Mockup variations

Gallery shell at `/` with a dropdown to switch designs. Each design is
self-contained in `variations/<name>/index.html` (shared JS behavior kept).

## Brand (applies to ALL variations, current and future)

- **Backgrounds use neutral or near-neutral darks** (`#000000` / `#09090B` / `#0B0C10` / `#101217`)
  in Dark mode, avoiding heavy blue or green color cast.
- **Navy `#021065` is the DOMINANT brand UI color in both Light and Dark mode across all variations.**
  Navy and its vibrant interactive shades (`#1A3DBF`, `#1E44D6`, `#B7C1FF`)
  form the primary buttons, active tabs, main cards, and key interactive highlights on top of the neutral canvas.
- **Gold `#FFB100` is strictly secondary/accent.** It highlights moments of value (gold asset avatar,
  physical gold bank card, active favorite star, subtle chip badges), and **never swaps places with navy**.
- `#FFB100` is a **graphics-first** color: readable as large fills and accents, but
  **never as text on light backgrounds** (white on gold is 1.82:1 — fails WCAG AA).
  Text on gold must use `#021065` (9.13:1) or another verified dark tone.
- Accessible derivatives in use: `#FFE3A6` (light gold tint), `#3D2900` (dark gold container),
  `#C07F00` (muted mid-gold for gradients).
- When adding a variation: always keep Navy dominant — differentiate via surfaces, shapes,
  elevation, and layout rhythm, not by swapping navy with gold.

| Route | Design |
|---|---|
| Route | Design |
|---|---|
| `/variations/v3/` | **Obsidian Editorial (نسخه برتر)** — بر پایه `design-md`: پس‌زمینه خنثی `#0B0C10`، سرمه‌ای غالب `#021065` و کارت‌های مدرن |
| `/variations/v5/` | **Navy Aurora (گرادیان Revolut)** — بر پایه v3: هیرو گرادیانی سرمه‌ای روی صفحه خانه در هر دو تم روشن و تیره |

## Dev

```bash
python3 -m http.server 8000
# open http://127.0.0.1:8000/  (?v=v3 / ?v=v5 deep-links, choice remembered)
```

## Deploy (Vercel)

Static project, no build step. Import the repo/folder in Vercel — `vercel.json` handles clean URLs.
