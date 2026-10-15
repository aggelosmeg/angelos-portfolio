# Science Communication Website Plan

## Purpose

Create a dedicated **Science Outreach** area within Angelos Mengoudis's portfolio. It should show how he communicates science through real public-facing work, beginning with the NOESIS internship, while leaving room for astro-hiking and future outreach activities.

The section should feel like an experience-led portfolio: clear, visual and grounded in what audiences did and what Angelos contributed. It should not read as a CV or reproduce the internship report in full.

## Recommended structure

### 1. Science Outreach landing page

**URL:** `outreach/index.html`

**Navigation label:** Science Outreach

**Page role:** an introduction and a small, growing index of outreach experiences.

Suggested order:

1. Page heading: `Science Outreach`
2. Short introduction connecting astronomy, scientific ideas and public engagement.
3. Featured experience card: **NOESIS — Science Center and Museum of Technology**.
4. Second card: **Astro-Hiking Guide** — keep as a visible `PLACEHOLDER – material and permission to publish needed` until source material is supplied.
5. Space for future workshops, observatory tours, talks and science-media work.
6. Contact invitation.

### 2. NOESIS detail page

**URL:** `outreach/noesis/index.html`

**Working title:** `NOESIS: Science Communication Internship`

**Status:** Completed

**Time period:** April-May 2024

**Location:** Thessaloniki, Greece

**Organisation:** NOESIS — Science Center and Museum of Technology

Recommended sections:

1. **Overview** — a concise explanation of the internship and its public-facing setting.
2. **Learning through participation** — the educational programmes Angelos supported.
3. **Museum interpretation** — visitor orientation, interactive exhibits and guided explanations.
4. **From preparation to presentation** — development and delivery of a short Antikythera mechanism tour.
5. **Planetarium and science storytelling** — observation of interactive sessions and support with visitor seating and flow.
6. **Skills developed** — public explanation, adapting to age groups, facilitation, preparation and collaboration. Keep this specific and evidence-based.
7. **Gallery / media** — only approved images, with captions and alt text.
8. **Related outreach** — later link to astro-hiking.

## Verified NOESIS content

The following points are supported by the supplied internship report and are suitable as the basis for edited web copy. They should still be reviewed by Angelos for accuracy and tone before publication.

| Topic | Supported content for the page |
| --- | --- |
| Internship | Angelos completed a two-month placement at NOESIS during April-May 2024. |
| Educational programmes | He spent substantial time supporting school-group activities and explained tasks to small groups of pupils. |
| Topics and formats | The report documents work with a Mars-colonisation activity, an environmental programme, a physics/mathematics escape room and tinkering activities. |
| Facilitation | His role included helping groups understand tasks, offering hints when needed and allowing participants to carry out the activities themselves. |
| Museum work | He welcomed and informed visitors, checked museum entry, and gave interactive explanations of Technopark exhibits to families and children. |
| Guided tour | He researched, wrote, rehearsed and delivered a short guided explanation of the Antikythera mechanism. |
| Planetarium | He observed interactive presentations, including constellation mythology, and supported audience seating and visitor flow. |
| Media production | The report records camera operation and set support for a video about the Explora summer programme. |
| Communication practice | The report describes learning to adapt explanations for different ages, prepare tours and communicate science in an engaging way. |

## Draft content direction

Use short, idea-first paragraphs in first person. The following is a **draft direction**, not final website copy:

> At NOESIS, I supported science-learning activities for school groups and museum visitors. The work moved between hands-on experiments, interactive exhibits, guided explanation and visitor support — always with the goal of helping people take part in the science themselves.

> I helped facilitate activities on topics including Mars exploration, environmental science, physics puzzles and creative engineering. I also prepared and delivered a short presentation about the Antikythera mechanism, turning research into an accessible story for visiting groups.

Keep individual programme descriptions compact. One short example can show the approach better than a catalogue of every activity.

## Visual direction

Use the existing night-sky portfolio system, but let the outreach pages feel warmer and more participatory than technical project pages:

- Use one large, approved cover image for NOESIS, ideally an activity or exhibit rather than a posed portrait.
- Add 2-4 approved images only when rights and consent are clear.
- Pair each image with a factual caption explaining the activity, not an unverified outcome.
- If no usable images are approved, use a clearly labelled placeholder rather than extracting photos from the report.
- Avoid generic stock imagery and generic science icons.

## Publication safeguards

The supplied report is a source document, not automatically a public web asset.

- Do not publish the report PDF without Angelos's and, where needed, NOESIS's permission.
- Do not reuse its embedded photographs until ownership and consent are confirmed. Some show people and may require permission.
- Do not publish the report's student number, named colleagues/supervisors, daily diary, personal wellbeing reflections or internal criticism of activities.
- Do not state numbers, outcomes or institutional claims beyond what Angelos confirms for public use.
- Credit NOESIS in the form Angelos and the organisation prefer.

## Content still needed

Before building the public pages, confirm:

1. Does Angelos approve the title, summary and specific responsibilities above?
2. Which NOESIS photos, if any, may be used online, and do they have the required permissions?
3. May NOESIS be linked, and what wording/credit should be used?
4. Should the Antikythera mechanism tour be a highlighted story or a brief mention?
5. Which astro-hiking material is ready to publish (images, dates, descriptions and permissions)?
6. Does Angelos want the NOESIS report publicly downloadable? The default should be no.

## Build sequence

1. Get the permissions and missing answers above.
2. Create `templates/outreach.html` from the existing shared header/footer pattern.
3. Build the outreach landing page with the NOESIS card and an honest astro-hiking placeholder.
4. Create the NOESIS detail page from approved copy and media.
5. Add source records in `outreach/noesis/SOURCES.md`, including exact source files, permissions and unresolved questions.
6. Update every repeated navigation header and footer so `Science Outreach` points to the new landing page.
7. Preview in Live Server on desktop and mobile, checking readable type, keyboard navigation, image alt text and the visible placeholders.

## Source record

- Primary source reviewed: `projects/NOESIS/ΑΓΓΕΛΟΣ ΜΕΓΓΟΥΔΗΣ ΠΡΑΚΤΙΚΗ.pdf`
- Source language: Greek
- Report content used here: internship period, documented roles, activities and communication practice.
- This plan intentionally excludes personal identifiers and non-public personal reflections from the proposed site content.
