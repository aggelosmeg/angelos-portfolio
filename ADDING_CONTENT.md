# Adding content: from a project folder to a website page

This file explains how a project folder on Angelos's laptop becomes a page on
this website. Claude follows these steps every time; Angelos can read it to know
what to give Claude and what to check afterwards.

The same process is used for projects, the thesis, outreach and visual work.
Only the template changes (see "Other kinds of content" at the end).

---

## For Angelos: how to hand over a folder

1. Tell Claude the path to the folder, for example
   `~/Documents/Uni/NIRPS`, or run `/add-dir <path>` in Claude Code
   so Claude can read it.
2. Add a few words if you can (all optional, but it saves questions):
   - What the project was and what **you** personally did.
   - Which files are the "real" ones (final report, final plots).
   - Anything that must **not** go online (unpublished data, a collaborator's figures, private notes).
   - Whether it should be **featured** on the homepage.
3. Claude builds the page, then sends you a short summary and a list of
   questions. Open the page in Live Server, answer the questions, and Claude
   fixes it.

One folder = one project. Claude never changes, moves or deletes anything in
your source folders: it only reads them and copies what it needs.

### Material from the old laptop

Most project folders are on Angelos's old laptop. There, Claude Code follows
`OLD_LAPTOP_INSTRUCTIONS.md` and packs each project into a small hand-off folder
(resized images, small PDFs, and a `project.md` with the record, draft text,
source map and questions). Angelos copies it into this folder as `website-handoff/`.

When `website-handoff/` exists, start from it: read `website-handoff/HANDOFF_INDEX.md`, then
each `website-handoff/<slug>/project.md`. Steps 1–4 below are already done, so check
them quickly and continue from step 5. Use `project.md` as the basis for
`SOURCES.md`. Keep `website-handoff/` out of the published site.

---

## For Claude: the steps

### 1. Look at everything first
- List every file in the folder (including subfolders).
- Read reports, slides, READMEs, notebooks and the main code files.
- Look at every image and plot.
- Do not write anything to the website until this is done.

### 2. Pull out the facts
Fill in the project record (the fields in section 12 of the brief):

| Field | Notes |
|---|---|
| title | From the report/slides title. Shorten only if very long. |
| slug | Lowercase words joined by hyphens, e.g. `nirps-guiding-camera`. Never changes once set. |
| year | When the work was done. |
| status | `completed` or `ongoing`. |
| category | One of: Research & Instrumentation / Data Analysis / Programming & Computational Methods / University Coursework. |
| tags | 2–5 short tags: tools and topics (Python, PSF analysis…). |
| summary | 1–2 sentences for the project card. |
| featured | Only if Angelos says so. |

Then gather what is available for the page sections (any can be left out):
Overview, Context (course, group, supervisor, dates), My role, Methods & tools,
Process, Results & visuals, Files & links, Related projects.

**Every fact must come from a file in the folder or from Angelos.** If it isn't
there, it doesn't go on the page.

### 3. Mark what is unclear, never guess
- Missing or unclear → a visible placeholder (`PLACEHOLDER – …`) and a question
  in the open-questions list.
- Always ask about these if the folder doesn't make them clear:
  - What Angelos did himself vs. what the team or supervisor did.
  - Whether figures, the report and the code may be published.
  - How the supervisor or group should be credited.
- Never publish: unpublished thesis results, restricted data, other people's
  figures or photos of people without permission, or personal details.

### 4. Choose and prepare images
- Pick the 2–6 figures that best explain the work (plus one for the card cover).
- **Copy** them to `projects/<slug>/images/`, never move them.
- Resize to a maximum width of 1600 px, as JPG (photos) or PNG (plots), using
  macOS's built-in `sips`, e.g.
  `sips -Z 1600 input.png --out projects/<slug>/images/figure-1.png`
- Give files clear names: `cover.jpg`, `psf-profile.png`, …
- Write alt text and a caption for each, based on the source caption or report.

### 5. Build the page
- Copy `templates/project.html` to `projects/<slug>/index.html` and fill it in.
- Write in first person, plain and concise. Explain *why* before *how*. Keep
  Angelos's technical terms; don't overstate results.
- Larger projects get all sections; small assignments can be short.

### 6. Link it from the rest of the site
- Add a card to `projects.html` (with the right category for the filters).
- If featured, add or swap a card on the homepage (`index.html`).
- Add "Related projects" links where it makes sense.

### 7. Record the sources
Create `projects/<slug>/SOURCES.md` with:
- The source folder path and date.
- Which files were used, and which fact or image came from which file.
- What is still a placeholder.
- Open questions for Angelos.

This file is not linked from the website. It makes later updates easy and shows
where everything came from.

### 8. Report back
Tell Angelos, in a few lines: what was added, the questions, and which page to
open in Live Server. Then apply his answers and update `SOURCES.md`.

---

## Website folder layout

```
website/
├── index.html                 Homepage
├── projects.html              All projects, with filters
├── projects/
│   └── <slug>/
│       ├── index.html         The project page
│       ├── images/            Copied, resized images
│       └── SOURCES.md         Where everything came from (not published)
├── thesis/index.html
├── outreach/<slug>/…          Same pattern as projects
├── visual/…                   Same pattern as projects
├── templates/                 Blank page templates to copy from
├── css/base.css               Layout
├── css/theme.css              Colours and fonts
└── images/                    Images used by several pages
```

---

## Other kinds of content

| Kind | Template | Differences |
|---|---|---|
| Project | `templates/project.html` | As above. |
| Master's thesis | `thesis/index.html` (single page) | Updated gradually. Labelled **Ongoing**. Only share material Angelos marks as public. |
| Outreach | `templates/outreach.html` | Focus on the audience, what people experienced and what Angelos did. Photos of visitors and participants need permission. |
| Visual work | `templates/visual.html` | Videos are embedded from YouTube/Vimeo, never copied into the site. Each item: title, date, short description. |

Templates are created the first time each kind of page is needed.
