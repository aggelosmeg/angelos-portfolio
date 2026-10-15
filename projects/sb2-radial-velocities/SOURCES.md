# Sources – sb2-radial-velocities (not published)

Built 2026-10-11 from the old-laptop hand-off `website-handoff/sb2-radial-velocities/`
(original folder: `C:\Users\Aggelos\Desktop\1st Semester\Astrophysics & Data Science\Angelos Mengoudis Data Science Projects\A2-RV_SB2`).
The full hand-off notes are copied below; they map every fact and image to its source file.

## Used on the page
- Images: ccf-initial-model-epoch-1/2/3 (epoch 1 is the card cover). These show the INITIAL model, not the final MCMC fit – captions say so.
- No numerical results published: the hand-off flagged inconsistencies in the notebook (interval labels, parameter counts) needing review first.
- Category shown as Data Analysis + University Coursework.

## Still placeholders / open questions
- Year and exact course credit.
- Individual work? (My role text is a draft from the notebook.)
- Data credit, and may the plots be public?
- Code: publish on GitHub? Link.
- Featured on homepage?

---

---
title: "Radial Velocities of a Double-Lined Spectroscopic Binary"
slug: "sb2-radial-velocities"
kind: project
year: null
status: completed
category: "University Coursework"
tags: [Python, Spectroscopy, Bayesian inference, MCMC]
summary: "I analysed observations of the binary star HD 195521 to estimate both stars' radial velocities. I compared individual and joint fits to study how overlapping signals affect the measurements."
featured: false
cover_image: images/cover.png
source_folder: "C:\\Users\\Aggelos\\Desktop\\1st Semester\\Astrophysics & Data Science\\Angelos Mengoudis Data Science Projects\\A2-RV_SB2"
---

## Overview
I studied how to measure the velocities of two stars whose light is recorded together. I modelled their cross-correlation functions (CCFs) with two Gaussians and compared fits to individual observations with a joint fit.

## Context
Data-analysis assignment A2: "Optimal determination of the radial velocities of the double-lined spectroscopic binary (SB2)". The supplied statement identifies HD 195521 and three observations from 20, 24 and 28 July 2016. These are observation dates, not the project year.
PLACEHOLDER - confirm course title, supervisor and project year.

## My role
Draft based on the user-selected notebook: I implemented initial velocity estimates, the two-Gaussian model, a likelihood with an additional noise term, and single- and multi-epoch analysis.
The assignment supplied scaffolding, the prior function, plotting helpers and the SAM sampler. PLACEHOLDER - confirm personal contribution and any collaborators before publishing this first-person text.

## Methods and tools
Python, NumPy, SciPy curve fitting, Matplotlib, the SAM/Scaled Adaptive Metropolis sampler, corner and Seaborn. The input comprises three CCFs with quoted uncertainties. The joint model shares four depth/width parameters across epochs and fits separate velocities and jitter for each observation: 13 parameters total.

## Process
I estimated the two signals, compared an initial model with the data, sampled the posterior, discarded burn-in and inspected uncertainties and correlations. I then fitted the three observations together using shared line shapes.

## Results and visuals
The first and third observations show two distinct dips; the middle observation blends them together. The saved posterior statistics show much larger single-epoch velocity uncertainties for the blended observation and smaller uncertainties in the joint fit.

The selected images are direct exports from the requested notebook, with white backgrounds and the original axes and legends. They show INITIAL fits from Question 2, not the final MCMC solution. Their native size is 576 x 453 pixels; they were not enlarged. The cover repeats the third plot so it can be used directly on a project card.

- `images/cover.png` - Third observation, with two clearly separated stellar signals. Alt text: "Two absorption-like dips in the observed cross-correlation function, overlaid with an initial two-Gaussian model."
- `images/ccf-initial-model-epoch-1.png` - First observation: two distinct stellar signals. Alt text: "Observed CCF with two separated dips and a green initial SB2 model, labelled Epoch 1."
- `images/ccf-initial-model-epoch-2.png` - Second observation: overlapping stellar signals. Alt text: "Observed CCF and initial model forming a blended central dip, labelled Epoch 2."
- `images/ccf-initial-model-epoch-3.png` - Third observation: separated signals at different velocities. Alt text: "Observed CCF with two separated dips and a green initial model, labelled Epoch 3."

The plot titles count observations as 1, 2, 3; the analysis and parameter tables index the same observations as 0, 1, 2. The dense chain, corner and correlation plots were omitted from this simple selection.

## Files and links
- `image-sources.json` - exact notebook cell/output locations for the exported figures (indices start at zero).
- Code: the original notebook remains in its source folder. It includes hard-coded local paths; a public repository would need a separate preparation pass and confirmation of data and starter-code permissions.
- No report was identified as the user's own final report. The assignment PDFs/HTML, `HD 195521 .pdf`, supplied code, raw data and MCMC arrays were not copied. Ownership/publication permission for supporting material is unconfirmed.

## Source map
| Fact or image | Came from (file path) |
|---|---|
| Three selected figures and cover | `C:\Users\Aggelos\Desktop\1st Semester\Astrophysics & Data Science\Angelos Mengoudis Data Science Projects\A2-RV_SB2\A2_Radial_velocity_of_spectroscopic_binaries.ipynb`, cell 13, outputs 0-2 |
| Model, likelihood, individual and joint fits | Same notebook, cells 7, 11, 19, 21, 23, 28, 52-59 |
| Blended signals and uncertainty comparison | Same notebook, cells 33, 47-49, 59, 69 |
| Target, observation dates, assignment and supplied scaffolding | `C:\Users\Aggelos\Desktop\1st Semester\Astrophysics & Data Science\A2) Optimal determination of the radial velocities of double-lined spectroscopic binaries (SB2)\projectSB2Orbit_statement (1).html` |
| Supplied plotting and table utilities | `C:\Users\Aggelos\Desktop\1st Semester\Astrophysics & Data Science\A2) Optimal determination of the radial velocities of double-lined spectroscopic binaries (SB2)\SB2\plotAndList.py` |

## Placeholders
- Project year, exact course/supervisor, personal contribution, publication permissions and homepage feature preference.
- Editorial check before publishing numerical claims: the notebook calls 5th-95th percentile ranges "95%" intervals (they contain 90%); its prose inconsistently states 12 versus 13 joint parameters and different iteration counts. The final mass-ratio/systemic-velocity estimates need scientific review and are not included as portfolio results.

## Questions for Angelos
- What year/course was this, and did you complete it individually?
- May the selected plots and description be public, and what credit is required for the supplied data and code?
- Should this project be featured on the homepage?
- Is there a final report or a public code repository to link?

---

## Revision 2026-10-11 (simpler page, Angelos's story)
Source re-checked directly: `website-handoff/semester 1/A2-RV_SB2/A2_Radial_velocity_of_spectroscopic_binaries.ipynb`.
- Angelos's angle (conversation): the project has a real physical meaning (two stars); the fitting was standard, the useful part was learning the statistics (likelihood, log-likelihood, MCMC) on a real project.
- Method confirmed as MCMC with the SAM sampler (`samsam`): cells 28, 55. Log-likelihood with jitter: cells 17, 19. Priors/posterior: cells 21–23. Burn-in: cells 30, 57.
- New figures extracted from notebook outputs (unchanged pixels; first one resized to 1600 px):
  - `ccf-three-observations.png` – cell 8 output (plot drawn by the supplied `plotAndList.displaySeries` helper with Angelos's initial estimates).
  - `mcmc-chains-observation-2.png` – cell 29 output, epochId = 1 (the blended observation).
  - `corner-plot-observation-2.png` – cell 40 output, epochId = 1.
- "Almost every parameter correlated" for the blended observation: cell 41 ("Everything is correlated except jitter"). Reduced in the joint fit: cell 69.
- Removed epoch-2/3 initial-model images; kept epoch-1 as the model example.
- Still no numerical results on the page (hand-off flagged interval-label and parameter-count inconsistencies).
- Year 2025: confirmed by Angelos in conversation, 2026-10-11.
- Card image replaced by images/card.svg: an illustrative diagram (still frame of the page animation), not data. Animation range widened to 20–380 px with max dip shift 115 px so Gaussian tails are no longer cut at the edges.
