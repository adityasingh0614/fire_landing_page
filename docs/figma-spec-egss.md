# EGSS (fire & electrical) — Figma spec (file lX2mBL9BS6UhPuKXveic5C)

Desktop frame: "EGSS — Visual Precision Landing (Desktop)" — 1280 x 6267.5
Mobile frame:  "EGSS — Engineering Precision Landing (Mobile)"
**Mobile frame is reference only.** Per client: web and mobile carry the SAME
content. The build is one responsive page; nothing is dropped below 1024px.

## Fonts (measured from Figma)
- **Space Grotesk** — headings (h1 700 72/72 ls -1.8px; h2 700 48/48 ls -1.2px)
- **Manrope** — body / UI text (400, 12-18px)
- **JetBrains Mono** — eyebrows, labels, telemetry, codal refs (600 12/16 ls +0.6px, uppercase)

## Colours (measured)
| token | value | use |
|---|---|---|
| orange   | #FF7A29 | primary accent, CTA fill |
| cyan     | #00F0FF | secondary accent, technical labels |
| muted    | #9CA3AF | body copy |
| white    | #FFFFFF | headings |
| bg-a     | #0B0D13 | odd sections |
| bg-b     | #05070A | even sections |
| footer   | #000000 | footer |
| hairline | #FFFFFF @ 5% / 10% | section + card borders |

## Layout
- frame 1280, container **1232** (section horizontal padding 24)
- section vertical padding **96 / 96**; hero **112 / 80**, min-height 800
- section border-top/bottom 1px #FFFFFF 5%
- footer padding 64, border-top 1px #FFFFFF 10%
- hero background: two linear gradients #FFFFFF 3% -> 0% (ambient orbs + overlay/blur)

## Page structure (layer tree, desktop)
1. Header — TOP APP BAR
2. HERO SECTION: heavily visual led with HUD overlays
3. SECTION 2: THE REGULATORY REALITY
4. SECTION 3: WHAT EGSS DOES (4 operating modes)
5. SECTION 4: DIAGNOSTIC TELEMETRY & DIGITAL TWIN
6. SECTION 5: STANDARDS & CODES (codified reference grid, 5x2)
7. SECTION 6: 5-STAGE LIFECYCLE (horizontal stepper)
8. SECTION 7: OBJECTION HANDLING (FAQ accordion)
9. SECTION 8: TECHNICAL SCOPING PORTAL (form)
10. Footer — FOOTER

## Gaps in the source design (decisions taken)
- **FAQ answers are not in the Figma file** — every accordion row is collapsed
  in both frames. Answer copy in `fire.html` was written to match the surrounding
  voice and is marked `<!-- COPY: drafted, client to confirm -->`. Replace freely.
- **Images are not exported.** Three raster slots live in `fireimages/`:
  `hero-tower-thermal.png`, `riser-cross-section-infrared.png`,
  `sensor-node-hydraulic.png`. Until the client supplies them the slots render
  as dark technical panels (CSS fallback), not broken-image icons.
- Select menus show one option each in the design; the remaining options were
  filled in from the section's own vocabulary.
