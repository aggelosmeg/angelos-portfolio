# Sources – nirps-guiding-camera (not published)

Built 2026-10-12 from `~/Documents/apl_nirps/` (read only, nothing changed there).
Angelos asked for an animation-centred page based on his 1-page summary.

## Decisions from Angelos (conversation, 2026-10-12)
- Public: yes, figures and results may go online. Credit the people he worked with.
- APL = Astrophysics Laboratory: first-year MSc project, one day per week, his first semester at UNIGE.
- Numbers: use what is in his own documents (the 1-page summary / report), not the notebooks.
- Link both the 1-page summary and the full report.
- Featured on the homepage, next to the other projects.
- Pierced-mirror drawing is his own.
- Third-party images (NIRPS optical layout, AO open/closed, La Silla night photo): not used for now.
  La Silla photo: maybe later, once its photographer/credit is found (slide 2 of `APL 1.pptx`, media/image3.jpeg).

## Facts and where they came from
| Fact | Source |
|---|---|
| Title, authors (A. Mengoudis, L. Messamah, F. Bouchy), Observatoire de Genève | `send/NIRPS_Guiding_Camera_Summary.tex` |
| Supervisors "Prof. François Bouchy & Lina Messamah", presentation 15 Dec 2025 | `APL 1.pptx`, slide 1 |
| Year 2025 | CV list in the brief; first semester (autumn 2025) per Angelos |
| NIRPS on ESO 3.6 m at La Silla, radial-velocity method, 0.4″ HA fibre | Full report §1.3.1; slide 2 |
| Pierced mirror: hole → fibre, rest → guiding camera | Full report §1.3.3; slide 4 |
| PSF: two Moffat components, FWHM 0.26″ and 0.44″ | Summary ("PSF characterisation and filtering") |
| Filtering adapted from Wahhaj et al. (2013), five steps | Summary; report §2.3.4 |
| Injection in a spiral (137.5° steps), 19/20 = 95% completeness, pattern rotated | Report §2.3.8; summary |
| Curve close to 5σ; Δm ≈ 9.6–9.8 beyond ~2.5″; limiting magnitude ≈ 13.5 | Summary ("Companion detectability") |
| Contamination method + dashed-line interpretation | Summary ("Contamination") |
| Limitation: q Vel, single night; companion PSF = primary PSF | Summary ("Limitation") |
| Tools: Python, NumPy, SciPy, Astropy, Photutils | imports in `APL NIRPS/helpers_contrast.py` and notebooks |

## Images (copied, never moved)
| Site file | Source |
|---|---|
| `images/binary-fibre-visualisation.jpg` (card cover) | `Characterization of the NIRPS Guiding Camera for Close Visual Binaries/binary_fibre_visualisation.png`, resized to 1200 px, JPG |
| `images/fibre-centred-vs-offset.png` | same folder, `2.png` (= report Fig. 3) |
| `images/filter-step-1…5.png` | the 5 frames of the GIF on slide 10 of `APL 1.pptx` (media/image17.gif), white border cropped |
| `images/injected-companions.png` | `companion_injection_recovery.png` (summary Fig. 2) |
| `images/contrast-curve.png` | `companion_contrast_curve.png` (summary Fig. 3) |
| `images/fibre-contamination.png` | `fibre_contamination.png` (summary Fig. 4) |
| `files/nirps-guiding-camera-summary.pdf` | `send/NIRPS_Guiding_Camera_Summary.pdf` |
| `files/nirps-guiding-camera-report.pdf` | `send/NIRPS_Guiding_Camera_Full_Report.pdf` |

## Animations (drawn in the page, illustrative only)
- "The leak": two Moffat profiles with made-up parameters; labelled "Illustration, not measured data".
- Pierced mirror: redrawn from Angelos's own drawing (slide 4, media/image5.png).
- Filtering stepper: real frames. The step names per frame are my reading of the GIF, matched to the
  step list on the same slide (original → halo removed → smoothed → azimuthal → stripes). To confirm.
- Injection/recovery: illustrative limit curve and random jitter; labelled "Illustration of the method".

## Not used (on purpose)
- Notebook-only numbers flagged in `appendix_review_notes.md` (fibre radius, 2 vs 20 angles, thresholds).
- Slide 7 PSF table (0.24″ / 0.93″), which disagrees with the summary.
- Report abstract's contamination range (10⁻³–10⁻⁵): the review notes question its units.

## Revision 2026-10-12 (Angelos's feedback)
- 20 starting angles confirmed by Angelos (matches report §2.3.8; the saved notebook's 2-angle loop was not the final run).
  New section + animation "Twenty angles: 95% completeness": spiral rotated 20 × 18°, the 20 copies at one
  separation form a ring, faded until fewer than 19 are found. Illustrative limits, labelled as such.
- Injection text now from report §2.3.7–2.3.8: injections made fainter until recovery fails; detection threshold
  = brightest peak in the non-injected image (zero false positives).
- Filtering step names now from report §2.3.4 (broad Gaussian halo model + unsharp masking, narrow Gaussian,
  azimuthal subtraction, vertical stripe correction) and the pre-filtering calibration from §2.3.2–2.3.3.
  GIF frame 2 shows the result of report steps 1+2 together (the halo model itself is not a frame).
- My role: Angelos did essentially all of the work himself (conversation). Page says so; no personal note (his choice).
- Phone number removed from all pages and the template (Angelos's request).

## Open questions
- Code on GitHub?
- La Silla photo credit (later).

## Revision 2026-10-12 (2)
- Leak animation: profiles now core + halo Moffat (β = 3) with the summary's FWHMs (0.26″, 0.44″), scaled so the
  16 px hole = 0.4″ fibre; stretched (asinh-like) brightness scale that falls to zero. Halo strength (5%) illustrative.
  Angelos: the old profile's wings reached much too far.
- Opening image `images/binary-fibre-wide.jpg`: wide crop (1550 × 760, rows 430–1190) of
  `binary_fibre_visualisation.png`, at Angelos's request. Caption from summary Fig. 1.

## Revision 2026-10-12 (3)
- "My role" section removed at Angelos's request.

## Revision 2026-10-12 (4) – clarity pass
- Intro: wider scope from Angelos (many stars are binaries, many expected to host planets; need to know whose light
  we measure) + report §1.1 / abstract (companion light can bias RV measurements).
- Mirror section renamed "Seeing the star and the fibre at once" (Angelos found this interesting; keep the how).
- Filtering: short side section, shorter captions; calibration detail dropped from the page.
- First injection animation no longer rotates (rotation only in the "Twenty angles" section). S/N map moved up.
- Results split into "How faint can a companion be?" and "How much light leaks in?".
  "Changes little beyond ~3″" and "non-detection must be combined with contamination estimate": report abstract.
  "7,000–8,000 times fainter" = 10^(0.4 × 9.6–9.8).
- CNN removed from related projects.

## Revision 2026-10-12 (5)
- "anyway" removed from summary, meta description and both cards.
- Angelos: the old "Planting fake companions" text was wrong (e.g. "no known companion" is not in the report).
  Merged "Planting fake companions" + "Twenty angles" into one section, "Fake companions and 95% completeness",
  following report §2.3.7–2.3.8 (spiral, 20 starting angles 18° apart, fainter step by step, 19/20 = 95%).
  One animation: spiral → 20 rotations → all fade → counter for one separation → 19-of-20 points → contrast curve.
