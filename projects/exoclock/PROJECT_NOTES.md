# Exoplanet Transit Analysis (ExoClock)

**Status:** research and content notes only — no project page has been built.  
**Prepared:** 12 October 2026  
**Project listing context:** 2024 · Relative photometry and analysis of exoplanet transit light curves.

## Short project description — working draft

This was my first hands-on introduction to exoplanets and to the transit method used to detect and study them. Working in a two-student group under the supervision of **Ioannis Gkolias**, we observed a star during a known exoplanet transit. We reduced and analysed the observations with the ExoClock analysis workflow, producing a transit light curve for submission to the ExoClock platform.

The project connected a local observing session with a larger collaborative effort: measurements of when transits occur help keep the predicted schedules of known exoplanets current. That makes future observations more efficient.

> **Before publishing:** confirm the exact name of the analysis software/pipeline, the observing site and equipment, the planet/host star, observation date, the other student’s preferred credit, and whether the submitted result was accepted and publicly listed by ExoClock. Do not imply that the two-student group achieved a particular scientific result until this is checked.

## What ExoClock does, and why it matters

ExoClock is an open project of the ARIEL Ephemerides Working Group that monitors the **ephemerides** of transiting exoplanets — the predictions of when their transits will occur. [ExoClock describes its mission](https://www.exoclock.space/) as supporting ESA’s ARIEL space mission, which is planned to study the composition and thermal structure of roughly 1,000 exoplanets by observing them in visible and infrared light.

For a space observatory to observe a transit efficiently, it needs an accurate predicted transit time and information about variability in the host star. Predictions become less certain over time, so new ground-based transit observations are used to update them. ExoClock coordinates these contributions from small and medium telescopes, combines them with other data, and makes the resulting information available for observing plans and research.

This work supports more than a single observing programme. ExoClock’s publications page describes its database and tools as open resources for scheduling future exoplanet observations, including observations from facilities such as ARIEL, JWST, VLT, ELT and Subaru.

The project’s 2026 peer-reviewed catalogue gives a concrete sense of this value: it combined 30,000 measurements to update the ephemerides of 620 exoplanets. The authors report that 45% of those planets required an update and that the prediction uncertainties improved by about an order of magnitude. This is useful context for explaining why even individual, carefully reviewed transit light curves matter to the network.

## How our observation contributed

The contribution can be described accurately at this level:

1. We recorded a sequence of images of a host star before, during and after a predicted transit.
2. We used relative photometry: measuring the target star against comparison stars in the same images to track its brightness over time.
3. A transit appears as a small, temporary dip in the resulting light curve as the planet passes in front of the star from our viewpoint.
4. We analysed the observation through the ExoClock workflow and submitted the light curve to ExoClock.
5. ExoClock reviews submitted observations before publishing them in its observations database. Accepted measurements can contribute to refined transit-time predictions.

ExoClock’s documented workflow is: register telescope information, receive a personalised schedule, observe a transit, analyse the data (it recommends its HOPS software for homogeneous results), and upload the light curve for review. The HOPS reference should remain a **confirmation point** until it is clear that this was the exact software used in this project.

## Transit method — plain-language explainer

An exoplanet transit occurs only when the geometry is favourable: from Earth, the planet’s orbit carries it across the face of its star. The planet blocks a small fraction of the starlight, so the measured brightness falls and then returns to its normal level. Plotting brightness against time creates a transit light curve.

The timing of the dip is especially important for ExoClock. Comparing the measured mid-transit time with the predicted one shows whether the ephemeris needs updating. Observations outside the transit are also essential because they establish the star’s normal brightness and help distinguish the transit signal from noise or changing observing conditions.

## Suggested page structure when the project is built

1. **Hero / overview** — title, 2024, two-student group, supervised by Ioannis Gkolias.
2. **The question** — how can a small brightness dip reveal a planet crossing its star?
3. **Observation and analysis** — concise account of the real target, telescope/camera, data reduction and relative photometry once confirmed.
4. **Transit method explainer** — a small animation paired with a simple light-curve graphic.
5. **Why the data was useful** — ExoClock’s ephemeris-monitoring role and the link to efficient future observations.
6. **Our submitted light curve** — only if the plot and its public-use permission are available; include a link to the ExoClock database record if one exists.
7. **Credits** — collaborators and supervisor, using their preferred names and roles.

## Animation / visual recommendation

**Recommended starting point:** [NASA Scientific Visualization Studio — *Exoplanet Transit Animations*](https://svs.gsfc.nasa.gov/13022/). Its single-transit animation explicitly pairs the planet crossing a star with the corresponding light curve, which fits this project particularly well. The page offers a 1080p WebM download (4.1 MB) and asks for credit to **NASA’s Jet Propulsion Laboratory**.

For the eventual site, prefer embedding or linking to the original NASA page until we have checked the desired format, page performance and final credit wording. A custom, lightweight CSS/SVG explainer could later be made in the site’s visual style, but it should be schematic — not presented as the group’s data. The strongest project visual would instead be the team’s own calibrated light curve, once its source and sharing permission are confirmed.

Suggested accessible caption for the NASA animation:

> A planet crosses the face of its star as seen by a distant observer. The small blocked fraction of starlight produces the dip in the light curve below. Illustration: NASA/JPL.

## Information to get from the two student contributors

- Which exoplanet and host star did we observe?
- On what date and from which observatory/location?
- What telescope, camera, filter and exposure settings were used?
- Was **HOPS** the software used, or was it another ExoClock-compatible pipeline?
- Do we have the original images, reduced data, final light curve, analysis notebook/report, and submission confirmation?
- Was the submission accepted and is there a public ExoClock observation URL?
- What were each student’s responsibilities, and how does the collaborator want to be credited?
- Is it correct to name Ioannis Gkolias as supervisor, and what affiliation/title should be used?
- Is there a project photo or observing image that both students approve for the portfolio?

## Sources

- [ExoClock — project overview and relationship to ARIEL](https://www.exoclock.space/) (accessed 12 October 2026).
- [ExoClock — how to contribute](https://www.exoclock.space/contribute) (accessed 12 October 2026).
- [ExoClock — publications and data](https://www.exoclock.space/publications) (accessed 12 October 2026). The page reports a catalogue of 620 updated ephemerides built from 30,000 measurements and explains the project’s open-science scope.
- Kokori, A. et al. (2026). [*ExoClock Project. IV. A Homogeneous Catalog of 620 Updated Exoplanet Ephemerides*](https://doi.org/10.3847/1538-4365/ae3238), *The Astrophysical Journal Supplement Series*, 283(1), 5. This is the peer-reviewed version of the key ExoClock Project IV result; it is published under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
- [Ariel Space Mission — official mission overview](https://arielmission.space/) (accessed 12 October 2026).
- [NASA Scientific Visualization Studio — *Exoplanet Transit Animations*](https://svs.gsfc.nasa.gov/13022/) (accessed 12 October 2026). Credit requested on the asset page: NASA’s Jet Propulsion Laboratory.

