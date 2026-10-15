# Photometric Calibration — Image Guide

This undergraduate project was one of Angelos's first substantial coding projects. The notebook develops a prototype Python workflow for measuring stars in an astronomical image, locating them on the sky, matching them with a catalogue, and comparing image counts with catalogue fluxes.

The PNGs in `images/` are direct exports of figures already embedded in `photometric_calibration.ipynb`. They were not regenerated or edited.

## Images

### `stretched-source-image.png`

A stretched, greyscale view of the source image after the notebook subtracts its median sky level. The stretch makes fainter structure easier to see.

### `detected-stars.png`

The same image with red circular apertures centred on bright peaks selected for the plate-solving step. It shows the stars used to connect image positions with sky coordinates.

### `wcs-prediction.png`

A zoomed region of the image with red circles showing positions predicted by the solved World Coordinate System (WCS). This is the notebook's visual check of the astrometric solution.

### `aperture-count-distribution.png`

A histogram of the logarithm of the aperture counts measured for detected stars. It provides a quick view of the brightness range in the measured sample.

### `catalog-match.png`

A two-panel comparison between star positions measured in the image and positions returned by the Pan-STARRS DR2 catalogue. The right panel zooms in on a smaller region so the alignment is easier to inspect.

### `counts-to-flux-fit.png`

A log-log plot comparing the measured aperture counts with fluxes derived from matched Pan-STARRS magnitudes. The black line is the notebook's linear fit in logarithmic space.

## Notes for the eventual project page

- The notebook performs sky subtraction, star detection, aperture photometry, plate solving, Pan-STARRS DR2 querying, catalogue matching, and a count-to-flux fit.
- Flat-field correction appears in the notebook as commented-out code, so it must not be described as a completed step.
- The notebook notes that the image header information was incomplete and field information was entered manually for plate solving. This can be mentioned as a practical part of the prototype, subject to Angelos's approval.
- Do not present the plots as a final scientific result or link the original notebook publicly until Angelos confirms that the source image, data, and code may be shared.

## Source map

| Exported image | Notebook cell |
| --- | --- |
| `stretched-source-image.png` | 5 |
| `detected-stars.png` | 11 |
| `wcs-prediction.png` | 18 |
| `aperture-count-distribution.png` | 21 |
| `catalog-match.png` | 34 |
| `counts-to-flux-fit.png` | 41 |
