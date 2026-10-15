# Sources – optical-design (not published)

Built 2026-10-12 from `projects/optical design/` (source folder, read only, not changed):
- `Optics_Project_presentation.pdf`: 18-slide deck "Optics Project", author Angelos Mengoudis, PDF created 2026-09-25.
- `Project.pptx`: the same 18 slides (file dated 2026-04-30). Used only to get the original, full-resolution images.

Angelos (2026-10-12): the designs were made for exercises in the Optics and Detectors course.

## Project record
| Field | Value | Source |
|---|---|---|
| title | Optical Design Exercises | Confirmed by Angelos, 2026-10-12 |
| slug | optical-design | |
| year | 2026 | Confirmed by Angelos, 2026-10-12 |
| status | completed | |
| category | University Coursework | Angelos, 2026-10-12 |
| tags | Python, Ray tracing, Optics | Python code on slides 12–13 |
| featured | no | Not asked for |

## Images
| File | From | Idea it shows |
|---|---|---|
| `ao-layout.png` | pptx `image1.png` (slides 1 and 9) | Final AO bench layout |
| `card.png` | Crop of `ao-layout.png` (bench part) | Project card |
| `pupil-relay.png` | Slide 2 diagram, rendered from the PDF at 220 dpi and cropped | L1 collimates and puts the pupil on the DM |
| `prism-ray-sketch.jpg` | pptx `image36.jpg` (slide 14) | Angelos's hand-drawn ray trace through the double prism |
| `adc-result.png` | pptx `image44.png` (slide 18) | Dispersion, ADC correction and residual vs. the ±50 mas target |

Slide 2 was used rather than slide 3 because its diagram label (3990 mm) matches the equations. Slide 3's diagram says 3390 mm.

## Text sources
- AO part: slides 1–9 (L1 conjugation and 330 → 5.4 mm, L2 with 4 pixels across the Airy disc, L2/L3 relay M = −f3/f2, dichroic placement, pyramid as prism, 12-pixel sub-pupils 50 pixels apart).
- ADC part: slides 10–18 (air refractive index model, z = 80°, ray tracing in both directions, flipping prisms, N-BK7 + N-SF11, direct vision at 700 nm, least-squares optimisation).
- The short explanations of what an AO system, a pyramid WFS and an ADC do are general background, written by Claude.
- Following the "no metrics" rule, the computed focal lengths, prism angles and the 37.384 mas residual are **not** in the text. They are only visible inside the result plot (the ±50 mas band).

## Deliberately left out
- Pyramid/L3 geometry diagram (slide 6): removed 2026-10-12 when the page was simplified (see below).
- The ADC prism drawing (slides 10 and 17): looks like it is taken from a lecture or paper, not Angelos's own.
- The refractive-index plots (slide 15): screenshots from RefractiveIndex.INFO.
- The equations and code listings: kept off the page to keep it idea-first.
- The deck itself is not linked.

## Placeholders
- None.

## Answered by Angelos (2026-10-12)
- Year: 2026. Title: "Optical Design Exercises".
- He did both parts alone. As with Fourier Optics, the page does not say so explicitly.
- The hand-drawn prism sketch may be shown.
- 3990 mm vs 3390 mm: he doesn't know. The page keeps the slide 2 diagram (3990 mm), which matches the equations on the slides. The page text gives neither number.
- Numbers aren't important for this project: keep the focal lengths, angles and residual out.
- No code to link.

## Simplified (2026-10-12)
Angelos: explain either more or less, whichever suits visitors. Chose **less**: plain language, one line per component saying what it is for, with no derivations and no jargon (conjugation, magnification formulas). Explanations of AO, the pyramid WFS and the ADC are general background in plain words.

## Questions for Angelos
- None open.
