# Portfolio audit

Branch: portfolio-mambo-ui
Base: current main at setup time

Purpose: preparation before MAMBO visual adaptation. No redesign. No public main branch update.

Findings:

- The current page is centered on index.html.
- Markup, styling, and scripting are currently kept in the same file.
- The page has clear content columns: hero, research, introduction, theory, case studies, model, ontology, summary.
- The main layout uses page, matrix, column, panel, card, and group-box classes.
- Section opening and closing is controlled by section-toggle buttons and matching panel IDs.
- Several links are still placeholders with hash targets. These should be checked before publishing.
- The contact anchor exists, but there is no visible contact content yet.
- Local asset structure is not yet separated. Fonts and the PhD gif are external resources.
- Responsive breakpoints exist, but long Hungarian titles should be checked on narrow screens.

Recommended next structural step:

- Create assets/css/portfolio.css.
- Create assets/js/portfolio-status.js.
- Move styling and scripting out of index.html without changing content.
- Add comments around the main HTML sections.
- Keep temporary overrides clearly marked.

Do not start the MAMBO visual layer until the separated structure has been previewed.