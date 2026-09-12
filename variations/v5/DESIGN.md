# Design System: Milli SuperApp — Variation 5 "Navy Aurora" (v3-based, Revolut-style hero gradient)
**Project ID:** milli-superapp-local (variation v5, derived from v3 with a navy hero gradient on home)

> **Brand rule (all variations):** Milli primary **#021065** (navy) and secondary **#FFB100** (gold)
> are the anchors. Emerald is a *supporting* tertiary here — this concept differentiates
> via surfaces, shapes, elevation, and layout rhythm, never via a new primary/secondary.
> `#FFB100` is graphics-first: never as text on light backgrounds (white-on-gold is 1.82:1);
> text on gold always uses `#021065` (9.13:1) or another verified dark tone.

## 0. v5 Delta vs v3 (Revolut-inspired home hero gradient)

- The home screen (only) gets a full-bleed navy hero gradient behind the status bar,
  topbar, balance block, and quick actions — like Revolut's saturated top fade.
- Light theme: `#D9DFFF → #E7EBFC → transparent` fading into `#FFFFFF` (620px tall).
- Dark theme: `#2B3ED6 → #1B2B9E → #121B54 → transparent` fading into `#0E1015` (560px tall).
- The gradient sits on `.screen` via `:has(home active)`, stays fixed while the
  asset list scrolls over it, and applies to the home screen only.
- Home topbar is transparent so the gradient shows through; all other screens
  keep the exact v3 look.

## 1. Visual Theme & Atmosphere

Variation 3 embodies an **architectural, obsidian sanctuary for money** — marrying the restrained, disciplined clarity of contemporary Swiss editorial design with high-end fintech precision. 

The background is strictly **neutral charcoal-obsidian** (#0B0C10 / #101217) in dark mode, and **crisp light-slate** (#F3F5FA / #FFFFFF) in light mode. By keeping the canvases completely neutral rather than heavily saturated, the interface eliminates visual fatigue and creates an authoritative stage where **Milli Navy (#021065)** functions as the bold, commanding brand anchor on cards, CTAs, and active navigation indicators, while **Milli Gold (#FFB100)** is reserved for moments of value.

**Key Characteristics:**
- Completely neutral or near-neutral dark background (#0B0C10) eliminating chromatic color cast
- Pure Brand Navy (#021065) and Electric Navy (#1E44D6) as the dominant interactive signals
- Milli Gold (#FFB100) strictly as secondary accent (gold asset avatar, gold card, active star)
- Pill-shaped geometry (generous 20–32px radii) providing tactile, human warmth
- Whisper-soft neutral elevation shadows with delicate hairline borders (#232732)
- High-legibility editorial hierarchy with Persian digits in tabular isolation

## 2. Color Palette & Roles

### Neutral Background & Canvas (Per User Mandate)
- **Neutral Obsidian Black** (#0B0C10) – Primary dark-theme background canvas. A deep, neutral dark gray without color cast, providing maximum legibility and zero chromatic fatigue.
- **Matte Charcoal Surface** (#101217) – Neutral surface for the phone screen and content cards in dark mode.
- **Elevated Neutral Slate** (#181B22) – Surface tier for secondary containers, keypads, and input wells (#1A1E27).
- **Hairline Neutral Outline** (#232732) – 1px structural separators providing crisp definition without harshness.

### Brand Dominant Core (Navy #021065)
- **Milli Navy** (#021065) – Brand primary and central identity anchor. Forms the core of the primary bank card gradient, active bottom nav indicator, and key brand surfaces.
- **Electric Navy CTA** (#1E44D6) – High-contrast vibrant navy for primary interactive buttons (`.btn-filled`), focus rings, and active selection chips in dark mode.
- **Periwinkle Navy Container** (#021065 / #DDE1FF) – Used for primary action containers and tonal badges.

### Brand Secondary (Milli Gold #FFB100 - Accent Only)
- **Milli Gold** (#FFB100) – Secondary accent reserved strictly for value indicators. Highlights the physical gold bank card (`.card-visual.gold`), the digital gold asset avatar (with navy glyph, 9.13:1 contrast), active favorite stars, and value badges.
- **Champagne Tint** (#FFE3A6) – Soft gold highlight for card text and banners, always paired with dark navy text (#021065).

### Supporting & Functional
- **Sky Metric Blue** (#38BDF8) – Tertiary information, chart trends, and neutral statistics.
- **Signal Red** (#FFB4AB / #BA1A1A) – Reserved strictly for destructive alerts, debits, and debts.

## 3. Typography Rules

**Primary Font Family:** Yekan Bakh (Variable, local `assets/fonts/YekanBakh-VF.ttf`, weight axis 100–950)
**Secondary Font Family:** IBM Plex Sans (Latin characters and numerals — tabular, trustworthy figures)

### Hierarchy & Weights
- **Hero Balance Figure:** Bold weight (700), large display size. The single most important number on screen — always Persian digits, always tabular.
- **Section Headers:** Medium weight (500), clear size step above body. Never confused with body text.
- **Body Text:** Regular weight (400), relaxed line-height (1.7+) for effortless Persian reading.
- **Labels & Captions:** Semi-bold (600–700) at small sizes for metadata, percentages, and tab labels.
- **Letter-Spacing:** Slightly tight for Latin card numbers (0.12em tracking kept for the bank-card feel); natural spacing for Persian.

## 4. Component Stylings

### Buttons
- **Shape:** Fully pill-shaped (generously rounded) primary and tonal buttons — friendly and thumbable.
- **Primary CTA:** Milli Navy (#021065) background with white text in light contexts; Milli Gold (#FFB100) with navy text in dark contexts; soft tinted shadow beneath.
- **Tonal Button:** Pale Emerald Mist background with emerald text for secondary actions.
- **Segmented Theme Control:** Pill container in container-high with sliding emerald active state.
- **Behavior:** Gentle state-layer press feedback within 80–150ms; never layout-shifting.

### Cards & Containers
- **Bank Cards:** Two cards — (1) Milli Navy gradient (#021065 → deep navy) with gold brand text; (2) Milli Gold gradient (champagne → #FFB100) with navy text. An emerald-gradient treatment may preview on one card as the concept's tertiary signature, always keeping a navy or gold card beside it. Generously rounded (32px), soft shadow with a faint tinted rim.
- **Asset Rows:** Flat white rows separated by feather-light fern dividers; circular Milli Gold avatar (navy glyph) reserved for the gold asset.
- **Banners:** Emerald-tinted and champagne-gold-tinted gradient banners with hairline tonal borders — calm, never loud.
- **Corner Style:** Generous radii throughout (16–32px); pills for chips, buttons, and selectors.

### Navigation
- **Bottom Tab Bar:** Five tabs with a soft emerald pill indicator behind the active icon; active label in Milli Navy (#021065), semibold.
- **Touch Targets:** Minimum 40–44px for all interactive elements; comfortable Persian thumb reach.

### Inputs & Forms
- **Fields:** Pale Emerald Mist fills with fern borders; pill or largely-rounded shapes.
- **Keypad:** Mist-tinted keys with large, confident numerals.

## 5. Layout Principles

### Grid & Structure
- **Phone Canvas:** 378×812 stage centered on the mint background; content max-width 1180px for the gallery page.
- **Vertical Rhythm:** 16/24/32 spacing tiers; hero balance block gets the most air (26px+ padding).
- **Sections:** One idea per band — balance, quick actions, assets, debts, banners — each separated by calm whitespace, not boxes.

### Whitespace Strategy
- **Base Unit:** 8px rhythm; component padding 12–22px; section gaps 22–32px.
- **Hero Breathing Room:** The balance figure floats in open space; nothing competes within one viewport of it.
- **Edge Padding:** Consistent 20px horizontal inset inside the phone across all screens.

### Alignment & Reading Flow
- **RTL-First:** Right-to-left flow with right-aligned Persian text; numerals and card numbers in LTR isolation.
- **Reading Flow:** Balance → actions → assets → context (debts/banners); most liquid first, slowest last.
- **Responsive:** Phone stage fixed at concept size; gallery page wraps gracefully below 760px.

## 6. Design System Notes for Generation

When creating new screens for this concept, reference these specific instructions:

### Language to Use
- **Atmosphere:** "Morning light on deep green marble — fresh editorial fintech sanctuary"
- **Button Shapes:** "Fully pill-shaped, thumbable" (not "rounded-md")
- **Shadows:** "Whisper-soft green-tinted shadows" (not "shadow-lg")
- **Spacing:** "Generous breathing room; hero numbers float in open space"

### Color References
Always use the descriptive names with hex codes:
- Brand anchors: "Milli Navy (#021065)" and "Milli Gold (#FFB100)" — every variation
- Primary actions: "Milli Navy (#021065)" light / "Milli Gold (#FFB100)" dark
- Backgrounds: "Fresh Mint White (#F6FAF7)" and "Pure Card White (#FFFFFF)"
- Gold moments: "Milli Gold (#FFB100)" on "Champagne Tint (#FFE3A6)", text in navy
- Supporting tertiary: "Deep Forest Emerald (#0C5B40)" — surfaces and accents only
- Dark theme: "Midnight Navy (#010826)" background with core "Milli Navy (#021065)" surfaces and "Milli Gold (#FFB100)" CTAs

### Component Prompts
- "Create an asset row with flat white background, feather-light fern divider, and a circular Milli Gold avatar with navy glyph only for the gold asset"
- "Design a primary call-to-action button in Milli Navy (#021065), fully pill-shaped, with a whisper-soft green shadow"
- "Render one bank card as a Milli Navy gradient with gold brand text and one as a Milli Gold gradient with navy text, both with generously rounded 32px corners"

### Incremental Iteration
When refining:
1. Focus on ONE component at a time (e.g., "Update the quick-action tiles")
2. Be specific about what changes (e.g., "Soften the banner gradients toward champagne")
3. Reference this design system language consistently; emerald stays tertiary — never promote it to primary/secondary over the brand anchors
