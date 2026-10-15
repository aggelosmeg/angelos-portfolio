# Sources – fourier-optics (not published)

Built 2026-10-12 from `projects/fourier optics/` (source folder, read only, not changed):
- `FourierOptics_report.pdf`: "Fourier Optics Exercises Report", author Angelos Mengoudis, 20 pages, PDF created 2026-04-28.
- `FourierOptics_Exercises.ipynb`: the notebook behind the report. It has **no saved outputs**, so all figures were taken from the PDF.

## Project record
| Field | Value | Source |
|---|---|---|
| title | Fourier Optics Exercises | Report title |
| slug | fourier-optics | |
| year | 2026 | Confirmed by Angelos, 2026-10-12 |
| status | completed | |
| category | University Coursework | Exercises for the Optics and Detectors course (Angelos, 2026-10-12) |
| tags | Python, HCIPy, Optics | Notebook imports: numpy, matplotlib, hcipy |
| featured | no | Angelos, 2026-10-12: not for the homepage |

## Images (all extracted with `pdfimages`, so Angelos's margin notes are NOT in them)
Chosen 2026-10-12 so that each figure shows a different idea (Angelos asked for the figures that best show the work and understanding).
| File | Report figure | Idea it shows |
|---|---|---|
| `clear-vs-obstructed-psf.png` | Fig. 3 (p. 3) | Aperture shape sets the PSF; obstruction moves energy into rings |
| `two-telescopes-finite-apertures.png` | Fig. 12 (p. 10) | PSF = single-aperture envelope × fringes. Cropped to the pupil and PSF columns (the MTF column was almost empty at this scale) |
| `polychromatic-fringe-smearing.png` | Fig. 11 (p. 10) | Bandwidth smearing |
| `filled-vs-sparse-aperture.png` | Fig. 18 (p. 15) | Same resolution as a 12D mirror, but sparse Fourier coverage → sidelobes |
| `piston-fringe-shift.png` | Fig. 19 (p. 16) | Piston difference shifts the fringes |
| `seeing-long-exposure-cuts.png` | Fig. 24 (p. 19) | Long exposure broadens from diffraction size to seeing size |
| `card.png` | Fig. 18, top-right panel | Cropped (seven-telescope PSF), used on the project card |

Dropped on 2026-10-12: Fig. 13 (seven-telescope array, repeated in Fig. 18) and Fig. 23 (25-panel seeing grid, too dense).

## Text sources
All page text paraphrases the report: section 1 (PSF/OTF, obstruction), 2 (Moon), 3 (two-telescope fringes, bandwidth smearing), 4 (seven telescopes, rotation/aperture synthesis, filled-aperture comparison), 5 (seeing, pistons, D/r0 cell model, frozen flow), and the Conclusion.
Numerical results (telescope sizes, laser power, transmission) were left out, following the "no metrics unless asked" rule.

## Deliberately left out
The report PDF contains Angelos's own review notes in the margins (e.g. "add more calculations", "why?"). Some flag doubts about specific figures, so those figures were not used:
- Fig. 16 (average PSF/MTF over rotations): note "DO I even want that? I think this is wrong".
- Fig. 21 (long-exposure two-telescope PSF): note "I should have not normalised the PSF".
- Fig. 14 and 22 have open "why?" notes; not used.
The report is **not linked** (Angelos, 2026-10-12: no report link for this project).

## Placeholders
- None.

## Answered by Angelos (2026-10-12)
- Year: 2026. All the work is his; no need to say so on the page (the "I wrote the calculations and plots" line was removed).
- No report link. No Files and links section.
- Not featured on the homepage.
- Course: Optics and Detectors (exercises).

## Questions for Angelos
- None open.
