# Angelos Mengoudis - Personal Portfolio Website

## Context

This is a personal portfolio website for Angelos Mengoudis, an MSc Astrophysics student at the University of Geneva. The full content and structure plan is in `angelos_portfolio_website_brief.md` in this folder. Treat it as the source of truth for purpose, sections, navigation and content rules.

The person working with you has never built a website before. Explain any command before running it, keep explanations short, and avoid unnecessary jargon. The code is reviewed in VS Code, so keep it clean, well organized and lightly commented.

## Decisions already made

- **No framework:** plain HTML + CSS, written by Claude. No Astro and no build step (decided by Angelos, 2026-10-11). Angelos previews pages with VS Code Live Server.
- **Look chosen:** night sky with a violet accent and IBM Plex fonts. Layout is in `css/base.css`, colours and fonts in `css/theme.css`.
- **Hosting:** GitHub Pages from the public repo `aggelosmeg/angelos-portfolio` (2026-10-15), live at https://aggelosmeg.github.io/angelos-portfolio/. No custom domain or analytics yet. Commits are authored as Angelos; CVs and raw sources stay local via `.gitignore`.
- **Styling:** plain CSS with CSS variables (colors, fonts, spacing) defined in one place, so that the whole look can be changed easily. No heavy UI frameworks.
- **Main sections** (from the brief): Home, Projects, Master's Thesis, Science Outreach, Visual Work, About, Contact, plus a "View / Download CV" button in the header on every page.

## Content rules (important)

- Never invent project details, results, figures, photos, testimonials, links or achievements.
- Use clearly marked placeholders (for example, a grey box labelled "PLACEHOLDER - project figure") wherever real content is missing.
- Do not publish date of birth, phone number or home address anywhere on the site. Note that the CV PDFs currently contain these, so they will need web versions later. Do not link the current CVs yet, and use placeholder links instead.
- Real, safe-to-use text is limited to: his name, the draft hero text in section 3 of the brief, the UNIGE email, the LinkedIn URL, and the project titles and one-line descriptions listed in section 4.

## Adding content

Follow `ADDING_CONTENT.md` every time Angelos hands over a project folder. It describes the steps from source folder to finished page. Anything unclear gets a placeholder plus a note, never a guess.

---

## FIRST TASK: settle the look

The only goal right now is to find a visual style we like. Keep it simple and do not build every page yet.

1. Set up a minimal Astro project in this folder, and explain each step as you go.
2. Build just enough to judge the look:
   - **Homepage:** hero (name plus draft tagline), short intro, a "Featured work" grid of 3 to 4 project cards, a "Master's thesis - Ongoing" highlight, and a footer with contact links.
   - **Projects page:** a card grid with category filter buttons (All / Research & Instrumentation / Data Analysis / Programming / Coursework), using the candidate projects from section 4 of the brief as sample entries.
   - **One sample project page,** built from the reusable template and filled with placeholders.
   - The header navigation and CV button on every page. Other nav links can lead to simple "Coming soon" pages.
3. Make **3 distinct visual directions** for the homepage that we can switch between easily, for example with a style switcher or with separate routes like `/style-1`, `/style-2` and `/style-3`. Suggested directions:
   - **Clean & light:** white space, strong typography, so that the plots and photos carry the visuals.
   - **Dark night-sky:** a deep dark background with subtle accents, kept tasteful and not cliché.
   - **Editorial / scientific:** a magazine-like layout with a serif and sans-serif pairing and a grid feel.
4. The site must work on both mobile and desktop, use accessible contrast, and use only light, restrained animation.
5. When done, start the dev server, tell me the local URL, and briefly describe each style so we can compare and pick one (or mix elements).

Do not over-polish. Speed of iteration matters more than perfection at this stage.
