# Sources – photometric-calibration (not published)

Built 2026-10-12 from (read only, not changed):
- `projects/photometric calibration/photometric_calibration.ipynb`: notebook "Photometric calibration", 45 cells.
- `projects/photometric-calibration/IMAGES.md`: image guide. It says the six PNGs in `images/` are direct exports of the notebook figures, unedited.

## Project record
| Field | Value | Source |
|---|---|---|
| title | Photometric Calibration Pipeline | Brief §4 (notebook title: "Photometric calibration") |
| slug | photometric-calibration | Folder already existed |
| year | 2024 | Brief §4 |
| status | completed | |
| category | Data Analysis | Brief §4 |
| tags | Python, Photometry, Plate solving | Notebook imports and steps |
| featured | yes (was already a homepage card) | `index.html` |
| context | Undergraduate project, one of his first substantial coding projects | `IMAGES.md` |

## Text sources (notebook cells)
- Six-step plan: cell 1.
- Median sky subtraction: cell 4. Stretch: cell 5 (auto_stretch).
- DAOStarFinder + circular aperture photometry: cell 7.
- Plate solving with twirl (`find_peaks`, `gaia_radecs`, `compute_wcs`): cells 10–15.
- Wrong header info, field entered by hand: cells 12–13 and 26–27 (red notes). Left off the page, per Angelos.
- Pan-STARRS DR2 query via the MAST API, `rMeanPSFMag`: cells 24–28.
- Position matching and removal of duplicate matches: cells 35–36.
- Magnitude → flux (3631 Jy zero point) and log-log fit, "only for visualitation": cells 37, 40–41.
- The opening "idea" paragraph (what photometric calibration is) is general background, written by Claude.

## Images
| File | Notebook cell | Used |
|---|---|---|
| `detected-stars.png` | 11 | Page figure |
| `card.png` | Crop of `detected-stars.png` (axes removed, 4:3) | Card image (projects page and homepage) |
| `wcs-prediction.png` | 18 | Page figure |
| `catalog-match.png` | 34 | Page figure |
| `counts-to-flux-fit.png` | 41 | Page figure |
| `stretched-source-image.png` | 5 | Not used (same view as `detected-stars.png`) |
| `aperture-count-distribution.png` | 21 | Not used (adds little to the story) |

Images were already under 1600 px, so they were not resized.

## Deliberately left out
- **Bias/dark/flat corrections:** the brief and the old cards listed these, but the notebook does none of them (flat-field code is commented out). Removed from both cards; the page doesn't mention them.
- **All numbers:** fit slope, R² (cell 42), thresholds, aperture radius, number of matched stars. Per the "no metrics" rule.
- **Writing the fit into the FITS header** (cells 43–44): has no output, so it's unclear whether it was run.
- **Target name:** the FITS file name contains "wasp-21", but the page doesn't name the target.
- **The notebook itself:** not linked (`IMAGES.md`: wait until Angelos confirms that image, data and code may be shared).

## Placeholders
- None.

## Answered by Angelos (2026-10-12)
1. Title "Photometric Calibration Pipeline": yes.
2. Not for a course or ExoClock: "it was just a project". Context stays "Undergraduate project".
3. Mention of the wrong header / field entered by hand: no. Sentence removed from the page.
4. The images were taken by the Aristotle University of Thessaloniki. Not credited on the page, per Angelos. The target (WASP-21) is not named.
5. Bias/dark before this notebook: he doesn't know. The page says nothing about it.
6. Credit for the MAST helper functions: no.
7. Link to the notebook or code: no.
8. Year 2024: confirmed.
9. Image credit: don't credit.

## Questions for Angelos
- None open.
