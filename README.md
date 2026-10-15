# README for agents: Angelos Mengoudis portfolio website

Read this first when you join the project. It explains what the site is, what
has been built so far, the rules you must follow, and where to find the details.

Last updated: 2026-10-12 (Science Outreach section added).

---

## 1. What this is

A personal portfolio website for **Angelos Mengoudis**, an MSc Astrophysics
student at the University of Geneva. It shows his projects, his ongoing
master's thesis, science outreach and visual work, and links to his CV.

The person you work with has **never built a website before**. Explain each
command before you run it, keep messages short, and avoid jargon.

## 2. Read these files, in this order

| File | What it is | When to read |
|---|---|---|
| `README.md` | This overview | Always, first |
| `CLAUDE.md` | Project rules and decisions already made | Always |
| `angelos_portfolio_website_brief.md` | The full content plan, and the **source of truth** for sections, navigation and content | Always (skim at least sections 2–4, 12 and 15) |
| `ADDING_CONTENT.md` | Step-by-step process for turning a project folder into a page | Every time Angelos hands over a project |
| `OLD_LAPTOP_INSTRUCTIONS.md` | Instructions for a *separate* Claude session on Angelos's old laptop, which packs project material into `website-handoff/` | Only to understand where `website-handoff/` comes from. Don't follow it here |
| `website-handoff/HANDOFF_INDEX.md` | List of projects packed on the old laptop | When adding content |
| `projects/<slug>/SOURCES.md` | Where every fact and image on a page came from, plus open questions | Before editing that project's page |
| `science-communication-plan.md` | Plan and safeguards for the Science Outreach section | Before editing anything in `outreach/` |
| `outreach/<slug>/SOURCES.md` | Same as above, for outreach pages | Before editing that outreach page |

> **Note:** the "FIRST TASK" section at the bottom of `CLAUDE.md` (set up
> Astro, build 3 style variants) is **out of date**. Those steps were replaced
> by later decisions: plain HTML/CSS, no Astro, and the night-sky style was
> chosen. Follow the "Decisions already made" section instead.

## 3. Decisions already made (don't reopen these)

- **Plain HTML + CSS, no framework, no build step.** A little inline JavaScript
  is fine where needed (project filters, animations).
- **Preview:** Angelos opens pages with the VS Code **Live Server** extension.
  There is no dev server to start.
- **Look:** dark night sky, violet accent, IBM Plex Sans and IBM Plex Mono (from Google Fonts).
- **Online:** public GitHub repo `aggelosmeg/angelos-portfolio`, published with
  GitHub Pages at https://aggelosmeg.github.io/angelos-portfolio/. No custom
  domain or analytics. To update the live site: commit, then `git push`.
- **Kept off GitHub** (see `.gitignore`): the CVs and all raw source folders.

## 4. Content rules (most important)

1. **Never invent anything:** no project details, results, numbers, dates,
   roles, figures, photos, links or testimonials. Every fact must come from a
   source file or from Angelos.
2. **Missing or unclear → visible placeholder** (`PLACEHOLDER – …`) plus a
   question for Angelos. Never guess.
3. **Privacy:** never publish date of birth, phone number or home address. The
   CV PDFs in this folder contain these, so they need web versions before they
   can be linked.
4. **Permissions:** no unpublished thesis results, restricted data, other
   people's figures, or photos of identifiable people without Angelos's OK.
   Separate his own work from the team's.
5. **Never change source folders.** Only read them, and copy what you need into the site.
6. **Tone of project pages:** simple and idea-first. A visitor should quickly
   see what the project was and the idea behind it. Leave out metrics unless
   Angelos asks for them on that project. Write plainly and factually, without
   hype or emotional phrasing. Use his real figures, not generic icon graphics.
   Add a "What I learned" section only if he asks for one. Prefer wording from
   his own reports.

## 5. Folder layout

```
website/
├── README.md                  This file
├── CLAUDE.md                  Rules for Claude
├── angelos_portfolio_website_brief.md   Content plan (source of truth)
├── ADDING_CONTENT.md          How to add a project
├── OLD_LAPTOP_INSTRUCTIONS.md For the old-laptop session only
├── index.html                 Homepage
├── projects.html              All projects, with category filter buttons
├── outreach/
│   ├── index.html             Science Outreach landing page
│   └── noesis/                index.html, images/, SOURCES.md
├── projects/
│   ├── nirps-guiding-camera/  index.html, images/, SOURCES.md
│   ├── cnn-from-scratch/      index.html, images/, SOURCES.md
│   ├── sb2-radial-velocities/ index.html, images/, SOURCES.md
│   ├── fourier-optics/        index.html, images/, SOURCES.md
│   ├── optical-design/        index.html, images/, SOURCES.md
│   ├── optical design/        Raw source for optical-design/ (page built)
│   ├── photometric-calibration/  index.html, images/, IMAGES.md, SOURCES.md
│   ├── photometric calibration/  Raw source (notebook) for photometric-calibration/
│   ├── spectroscopy/          Raw source material only (no page yet)
│   ├── NOESIS/                Raw source (internship report PDF) for outreach/noesis/
│   └── fourier optics/        Raw source for fourier-optics/ (page built)
├── templates/project.html     Blank project page to copy from
├── templates/outreach.html    Blank outreach page to copy from
├── css/base.css               Layout (shared by all pages)
├── css/theme.css              Colours and fonts (CSS variables in :root)
├── images/                    Shared images (empty for now)
├── website-handoff/           Material packed on the old laptop (NOT part of the site)
└── CV_*.pdf                   Current CVs (contain private details, see §4)
```

The folders with spaces in their names (`optical design`, `spectroscopy`,
`fourier optics`) hold PDFs, slides and notebooks Angelos dropped in. They are
inputs, not pages. When one becomes a page, give it a proper hyphenated slug.

## 6. How the code is organised

- **Every page repeats the same header and footer**, because there is no
  templating. If you change the nav, the CV menu or the footer, change it in
  **all** HTML files: `index.html`, `projects.html`, both files in
  `templates/`, `outreach/index.html`, and each `projects/<slug>/index.html`
  and `outreach/<slug>/index.html`.
- **Relative paths:** top-level pages use `css/...`; `outreach/index.html` uses
  `../css/...`; project and outreach detail pages are two folders deep and use
  `../../css/...`.
- **Outreach pages** use `<body class="outreach">`, which gives a warmer
  (amber) glow and badge colour, set in `theme.css`. Their layout classes
  (`feature-card`, `photo-row`, `photo-split`, `excerpt`) are at the end of
  `base.css`.
- **CV menu:** a `<details>` dropdown that works without JavaScript.
- **Project filters** (`projects.html`): each card has
  `data-categories="research data programming coursework"` (any subset). A
  small script at the bottom of the page hides the cards that don't match.
  Cards for known projects with no material yet have class `upcoming` and read
  "Coming soon".
- **CSS:** `base.css` handles layout: header, cards, project page, figures,
  explainer graphics and the NIRPS animations. `theme.css` handles colours,
  fonts and the night-sky background. To change the overall look, edit the
  variables in `:root` in `theme.css`.
- **Figure classes on project pages:** `figure`, plus `plot` for plots with a
  white background, `wide` for full width, and `pixels` for tiny pixel images.
- Keep code clean and lightly commented. Angelos reviews it in VS Code.

## 7. Current status (2026-10-12)

**Built**
- Homepage: hero, featured work (4 cards), master's thesis highlight, explore
  section, contact footer.
- Projects page with filters.
- Project pages:
  - **NIRPS Guiding Camera** (most complete; includes animated explainers;
    figures approved for publication; featured).
  - **CNN from Scratch** (featured on the homepage; several questions still open).
  - **SB2 Radial Velocities** (draft; numerical results deliberately left out
    until the notebook is checked).
  - **Fourier Optics Exercises** (2026-10-12; Optics and Detectors course;
    no report link, by Angelos's choice).
  - **Optical Design Exercises** (2026-10-12; Optics and Detectors course;
    AO system with pyramid WFS + atmospheric dispersion compensator;
    no numbers, no code link, by Angelos's choice).
  - **Photometric Calibration Pipeline** (2026-10-12; undergraduate notebook;
    featured; no numbers, notebook not linked; questions open in SOURCES.md).

- Science Outreach (2026-10-12): landing page `outreach/index.html` with
  the NOESIS card and an astro-hiking placeholder, plus the detail page
  `outreach/noesis/index.html`. Photos are extracted from the internship
  report. Their permission and credit are still **unconfirmed** (see
  `outreach/noesis/SOURCES.md`). Fine for local preview; confirm before going online.

**Not built yet:** Master's Thesis, Visual Work, About and Contact pages. Nav
links to these point to `#` for now. The visual template is created the first
time it's needed.

**Homepage placeholders:** hero image, thesis diagram, and the ExoClock
card (no material yet). GitHub URL is unknown.

**Known issues to raise with Angelos before fixing**
- The CV menu currently links **directly to the real CV PDFs**
  (`CV_Science 1.pdf` etc.), which breaks rule §4.3. It should use placeholder
  links until web versions exist.
- Open questions for each project (year, course credit, permissions, code on
  GitHub) are listed in each `SOURCES.md`.

## 8. Adding a new project (short version)

Full steps are in `ADDING_CONTENT.md`. In short:

1. Read everything in the source folder (or `website-handoff/<slug>/project.md`) before writing anything.
2. Fill in the project record: title, slug, year, status, category, tags, summary.
3. Copy 2–6 key images to `projects/<slug>/images/` and resize them with
   `sips -Z 1600`. Write alt text and captions.
4. Copy `templates/project.html` to `projects/<slug>/index.html` and fill it in.
5. Add a card to `projects.html` (and to `index.html` only if Angelos wants it featured).
6. Write `projects/<slug>/SOURCES.md` (sources, placeholders, open questions).
7. Report back briefly: what you added, your questions, and which page to open in Live Server.
