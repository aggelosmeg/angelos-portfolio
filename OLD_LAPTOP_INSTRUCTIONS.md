# Instructions for Claude Code on the old laptop

<!--
  FOR ANGELOS – how to use this file
  1. Copy this file to the old laptop (USB, AirDrop, email to yourself…).
  2. Install Claude Code there, open a terminal in the folder containing this file, and run `claude`.
  3. Type: "Read OLD_LAPTOP_INSTRUCTIONS.md and follow it."
  4. Answer its questions. At the end you get one folder called `website-handoff`.
  5. Copy `website-handoff` to the new laptop, into the website folder (keep the name; merge with the existing one if there is one).
-->

You are helping **Angelos Mengoudis** gather material for his personal portfolio
website. The website itself is built on a **different laptop**. Your job on this
laptop is only to **find, read, select and summarize** his project material and
pack it into one small folder that he will copy over. You do **not** build any
web pages here.

Angelos is new to this kind of work. Explain briefly what you are about to do
before running commands, keep messages short, and avoid jargon.

---

## 1. Background you need

Angelos is an MSc Astrophysics student at the University of Geneva (previously
BSc Physics at Aristotle University of Thessaloniki). His website will have
these sections: **Projects**, **Master's Thesis**, **Science Outreach**,
**Visual Work** (videos, timelapses, photos), **About**, **Contact**.

Work already known (from his CV). Use this list to recognise folders. It is not
complete, and the titles may differ from the folder names:

| Working title | Year | Focus |
|---|---|---|
| NIRPS Guiding Camera Characterization | 2025 | Guiding-camera images: PSF analysis, contrast curves, statistics. Supervisor: F. Bouchy. |
| Photometric Calibration Pipeline | 2024 | Bias/dark/flat, plate solving, catalog matching. |
| Exoplanet Transit Analysis (ExoClock) | 2024 | Relative photometry, transit light curves. |
| Convolutional Neural Network from Scratch | 2025 | CNN in Python with custom backpropagation and losses. |
| Time-Series Analysis Project | 2024 | Noisy time series: signal extraction, trends, errors. |
| Two Master's semester projects | ? | Titles unknown – ask Angelos. May match items above. |
| Data-analysis course projects | ? | Several smaller course projects. |
| Other university coding projects | ? | |
| Master's thesis (ongoing) | 2025– | "Probing exoplanets in polarized light: study of a polarimetric mode for the RISTRETTO instrument." |
| Outreach: NOESIS Science Center, Thessaloniki | 2024 | Science communication intern. |
| Outreach: Astro-hiking guide | 2024 | Night astronomy hikes, groups of 20–30. |
| Outreach: university observatory tours | 2023 | |
| Visual: timelapses / hyperlapses / videos | 2022– | Night sky, weather, urban scenes; YouTube videos. |

---

## 2. Rules (read carefully)

1. **Never change the originals.** Do not edit, move, rename or delete anything
   in his existing folders. Only read, and copy into `website-handoff`.
2. **Never invent anything.** Every fact you write must come from a file you read
   or from Angelos. If something is unclear, write `PLACEHOLDER – …` and add a
   question. Do not guess results, numbers, roles or dates.
3. **Keep it small.** Aim for under ~20 MB per project. Never copy raw data,
   FITS files, datasets, virtual environments, `node_modules`, caches, or whole
   code folders. Never copy video files (see section 6).
4. **Privacy and permission.** Flag (don't copy) anything that looks private or
   not his to publish: unpublished thesis results, collaborators' figures,
   restricted data, photos of identifiable people (museum visitors, hikers),
   personal documents, IDs, grades, passwords or keys.
5. **Stay local.** Don't upload anything anywhere.
6. **One project at a time.** Finish one, show Angelos a short summary, then move on.

---

## 3. Step 1 – Find the folders

0. Create the output folder `website-handoff/` in the same folder as this file.
1. Ask Angelos where his project folders are. If he isn't sure, look (read-only)
   in the usual places, such as Documents, Desktop and Downloads, plus any
   university or "Projects" folders, and **list candidate folders** with a
   one-line guess of what each is and its size.
2. Ask him to confirm the list, and for each one ask (all optional):
   - What it is and what **he** personally did.
   - Whether anything in it must **not** go online.
   - Whether it should be **featured** on the homepage.
3. Write the confirmed list into `website-handoff/HANDOFF_INDEX.md` (format in section 5).

---

## 4. Step 2 – For each project

1. **Look at everything.** List all files. Read reports, slides, READMEs,
   notebooks (including their outputs) and the main code files. Look at every
   image and plot. Note the final versions (latest dates, names like "final").
2. **Pick images.** Choose the 2–6 figures or photos that best explain the
   work, plus one good "cover" image for the project card. Prefer finished,
   labelled plots over debug output.
3. **Copy and resize images** into `website-handoff/<slug>/images/`:
   - Max 1600 px on the longest side. Plots → PNG, photos → JPG.
   - Use whatever is available: `sips -Z 1600` on macOS, Python with Pillow,
     or ImageMagick. If nothing works, copy the original and note it.
   - Clear names: `cover.jpg`, `psf-profile.png`, `light-curve.png`…
   - Figures inside a PDF report: export them only if easy; otherwise note the
     page number in `project.md` instead.
4. **Copy documents** into `website-handoff/<slug>/files/` only if they are his
   own and small (< 15 MB): the final report or slides as PDF. Whether they may
   be published is always a question for Angelos.
5. **Write `website-handoff/<slug>/project.md`** using the template below.

`<slug>` = short lowercase name with hyphens, e.g. `nirps-guiding-camera`.

### `project.md` template

```markdown
---
title: ""
slug: ""
kind: project          # project | thesis | outreach | visual
year:
status: completed      # completed | ongoing
category: ""           # Research & Instrumentation | Data Analysis | Programming & Computational Methods | University Coursework
tags: []               # 2–5 short tags, e.g. Python, PSF analysis
summary: ""            # 1–2 sentences for the project card
featured: false        # true only if Angelos said so
cover_image: images/cover.jpg
source_folder: ""      # full path on the old laptop
---

## Overview
What the project was and its goal. (first person, plain language)

## Context
Course / group / supervisor / dates – only if found in the files.

## My role
What Angelos did himself. If unclear: PLACEHOLDER + question.

## Methods and tools
Data, instruments, software, techniques.

## Process
Key steps, challenges, decisions (short).

## Results and visuals
Key findings in plain words – only what the files state.
- `images/xxx.png` – caption. Alt text: "…"

## Files and links
- `files/report.pdf` – may it be published? (question)
- Code: describe where it is and whether it could go on GitHub; don't copy it.

## Source map
| Fact or image | Came from (file path) |
|---|---|

## Placeholders
- …

## Questions for Angelos
- …
```

Writing style for the draft text: first person ("I measured…"), concise, explain
*why* before *how*, keep his technical terms, never overstate results. Small
assignments can have very short sections; leave a section empty rather than pad it.

---

## 5. `HANDOFF_INDEX.md` format

```markdown
# Website hand-off – <date>

| Slug | Title | Kind | Year | Status | Source folder | Done? | Open questions |
|---|---|---|---|---|---|---|---|
```

Update this table after each project.

---

## 6. Special cases

- **Master's thesis** (`kind: thesis`): extra care. Only summarize the general
  topic, background and methods unless Angelos explicitly says results or
  figures can be public. Mark everything else as a question.
- **Outreach** (`kind: outreach`): focus on the audience, what people
  experienced and what Angelos did. Photos showing identifiable people are
  listed, **not copied**, until he confirms permission.
- **Visual work** (`kind: visual`): do **not** copy video files. For each
  video, record title, date, length, file path and file size, and ask whether
  it's on YouTube/Vimeo (and the link). If `ffmpeg` is available, you may save
  one still frame per video as a JPG thumbnail. Photos: suggest a selection and
  copy resized versions only after he approves it.
- **Group projects:** clearly separate his contribution from the team's.

---

## 7. Finish

When Angelos says he's done for now:
1. Check that `website-handoff` contains only the expected files and report its total size.
2. Give him a short summary: projects packed, projects skipped, and the main open questions.
3. Remind him to copy `website-handoff` to the new laptop, into the website
   folder (keep the name; merge with the existing one).

It's fine to do this over several sessions. Next time, read `HANDOFF_INDEX.md`
first and continue where you left off.
