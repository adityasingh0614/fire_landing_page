# ErgoTattva — Figma spec (file RKOjVE5iYcO5BVlEs1dv7q)

Desktop frame: node 2:2 — 1280 x 7114.5
Mobile frame:  node 2:667 — 390 x 12048.61

Font: **Plus Jakarta Sans** (all text)

## Page structure (layer tree)
Body
- TOP ANNOUNCEMENT TICKER
- Header - NAVIGATION HEADER
- Main
  - 1. HERO SECTION (50/50 ULTRA VISUAL SPLIT)
  - 2. WHAT IS WORKPLACE ERGONOMICS (LARGE BIOMEC...)
  - 3. CONSULTING & ASSESSMENT SERVICES (INDUSTRIA...)
  - 4. STANDARDIZED METHODOLOGIES & CLINICAL RIGOR
  - 5. DELIVERABLES & ENTERPRISE DASHBOARD (FEATUR...)
  - 6. CLINICAL LEADERSHIP TEAM (DOCTORS & ERGONOM...)
  - 7. STRUCTURED 4-STAGE ENGAGEMENT & INDUSTRIES
  - 8. OBJECTIONS, FAQ & HIGH-CONVERSION INTAKE
- Footer - FOOTER

## Measured nodes

### Section 1 HERO (node 2:22)
flow vertical; width fill 1280; height hug 792
padding 80 / 32 / 80 / 32
border-bottom 1px
bg linear-gradient #FCFAFA -> #FFFFFF -> #FCFAFA
Container: Right Column 52% (visual) / Left Column 48%

### H1 (node 2:31)
Plus Jakarta Sans 800 ExtraBold, 48px / 48px line-height, letter-spacing -1.2px
width 567.61 hug, height 144
span "Biomechanical": same size/weight, Italic, colour dark red

### Container (node 2:79 parent) — THE GRID
display grid; width 1216px; 12 columns; row gap 48px; column gap 48px
=> col width = (1216 - 11*48)/12 = 57.333px
Section 1 padding L/R 32px, so 32 + 1216 + 32 = 1280 exact.

### Hero Right Column (node 2:79) "52% Visual"
grid column start 7, span 6 => width 584px  (6*57.333 + 5*48 = 584) OK
top 74.5px, left 632px, radius 16px, border 1px #EDE5E0, bg #FFFFFF

### Section 2 (node 2:101) WHAT IS WORKPLACE ERGONOMICS
vertical, width fill 1280, height hug 1150
padding top 96, bottom 96 (no horizontal)
border-bottom 1px #EDE5E0
bg #F5F1EE @ 40%

## TYPE SCALE (all Plus Jakarta Sans)
letter-spacing is consistently **-0.025em** on headings, +0.05em on eyebrows.

| role | size/lh | weight | ls | colour |
|---|---|---|---|---|
| H1 hero | 48 / 48 | 800 | -1.2px | #181414-ish near-black; span italic #8A182B |
| H2 section | 36 / 40 | 800 | -0.9px | near-black; span #8A182B |
| body lead | 18 / 28 | 400 | 0 | #4E4645 |
| eyebrow / badge | 12 / 16 | 700 | +0.6px | uppercase, #8A182B |

## COLOURS
brand red      #8A182B
border         #EDE5E0
tint bg        #F5F1EE (often @40%)
off-white      #FCFAFA
white          #FFFFFF
body text      #4E4645
dark           #181414

## LAYOUT
container 1216px, 12-col grid, gap 48px
section horizontal padding 32px  (32 + 1216 + 32 = 1280)
section vertical padding: hero 80, others 96
section border-bottom 1px #EDE5E0

## Hero right column
584px wide (cols 7-12), radius 16, border 1px #EDE5E0, bg #FFF
image 582x480 + dark gradient overlay (#181414 75% -> 0%, #000 10%)
floating micro-badge top-right "Zero Product Bias"
floating micro-card bottom "Clinical Workstation Evaluation"

## COMPONENTS (measured)

### Card "Background+Border+Shadow"  (node 2:115)
display flex row; radius 12px; border 1px #EDE5E0; padding 16px; gap 12px
bg #FFFFFF; box-shadow 0 1px 2px 0 rgba(0,0,0,0.05)   (= tailwind shadow-sm)
4-up row: width 292px each, gap 16px  (4*292 + 3*16 = 1216 exact)

### Label / kicker  (node 2:121)
12px / 16px, weight 700, ls +0.6px, uppercase
colour: #181414 on cards, #8A182B for section eyebrows

### Card body (node 2:123)
12px / 19.5px, weight 400, #4E4645

### Section sub-lead (node 2:109)
16px / 24px, weight 400, ls 0, centered, #4E4645

### Header - NAVIGATION HEADER (node 2:633)
width fixed 1280; height hug 81px; top 33.5px (ticker height)
bg #FFFFFF @90%; backdrop-blur 12px; border-bottom 1px #EDE5E0
shadow 0 1px 2px rgba(0,0,0,.05)   -> sticky header
nav link colour #4E4645

### Top announcement ticker
height 33.5px, dark (#181414), tiny uppercase text, red dot separators

## FINAL TYPE SCALE (Plus Jakarta Sans)
| token | size/lh | wt | ls | colour |
|---|---|---|---|---|
| h1        | 48/48   | 800 | -1.2px  | #181414 (span italic #8A182B) |
| h2        | 36/40   | 800 | -0.9px  | #181414 (span #8A182B) |
| stat-num  | 20/28   | 800 | 0       | varies |
| lead      | 18/28   | 400 | 0       | #4E4645 |
| sub       | 16/24   | 400 | 0       | #4E4645 |
| item      | 14/20   | 600 | 0       | #181414 |
| btn       | 14/20   | 700 | 0       | #fff |
| nav       | 13/19.5 | 600 | -0.32px | #4E4645 |
| label     | 12/16   | 700 | +0.6px  | uppercase |
| card-body | 12/19.5 | 400 | 0       | #4E4645 |

## COLOURS (confirmed in Figma)
--red #8A182B   --amber #E07A2C  --ink #181414
--body #4E4645  --line #EDE5E0   --tint #F5F1EE  --off #FCFAFA

## BUTTON primary (node 2:71)
height 48px, radius 8px, padding 14px 20px, gap 8px
shadow: 0 4px 6px -1px rgba(0,0,0,.1), 0 2px 4px -2px rgba(0,0,0,.1)  (tailwind shadow-md)

## SECTION HEIGHT MAP (desktop 1280) — sums to 7114.5
ticker 33.5 | header 81 | 1.hero 792 | 2.biomechanics 1150 | 3.services 781
4.frameworks 873 | 5.dashboard 709 | 6.leadership 823 | 7.process 768
8.faq 718 | footer 386.5

## PER-SECTION GRID GAPS DIFFER
hero container      : 12col, gap 48
section containers  : vertical stack, gap 40, max-w 1280, px 32
s2 header block     : max-w 768, vertical gap 8, h 164
s3 header           : flex space-between, h 64
s3 "50/50 Split"    : 12col, gap 32  -> span6 = 592, h 476
s2 infographic frame: 1216x612 (1px border + 24 pad + inner 1166x562 r12)
4-up card row       : gap 16 -> card 292

## MORE TOKENS
icon chip      36x36, r8, amber tint #FDF6ED
muted text     #786E6D  (s3 header note: 14/20 w600)

---
## BUILD NOTES

Files: `index.html` + `styles.css`. No build step, no dependencies, no JS.
Preview: `python -m http.server 8099` then http://localhost:8099/

Accuracy vs Figma desktop frame (measured in-browser at 1280 content width):
total page 7136 vs 7114.5 (+0.3%); worst single section +15px.

### Swapping in real images
Every image is a `<div class="ph" data-label="...">` placeholder.
Replace each with `<img src="..." alt="..." width= height= loading="lazy">`
(the hero image should be `loading="eager" fetchpriority="high"` for LCP).
The `.ph` aspect-ratios encode the Figma image box, so keep them:
  hero            582 x 480
  s2 infographic 1166 x 562
  s3 feature      (fills 592 x 476 card)
  s4 methodology  646 x 366
  s5 dashboard   690.67 x 385.78
  s6 team photo   590 x 440
Logo: `.brand__mark` is a text stub — swap for the real ErgoTattva mark.

### Native platform features used instead of JS
FAQ accordion  -> <details>/<summary>
Form validation-> required / type=email / type=tel
Smooth nav     -> scroll-behavior + scroll-padding-top
Sticky header  -> position:sticky + backdrop-filter
