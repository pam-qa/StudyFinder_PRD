# Contributing to the StudyFinder PRD

This repository is a **living Product Requirements Document** kept as a wiki of linked Markdown pages.
Contributions that sharpen the requirements, resolve open questions, or improve clarity are welcome.

## How it's organized

- [`README.md`](README.md) — home page and table of contents.
- [`docs/`](docs/) — one numbered Markdown page per PRD section (`01-…` through `14-…`).
- Pages cross-link with relative Markdown links so they render on GitHub.

## Making changes

1. Create a branch (e.g., `docs/clarify-eligibility-snapshot`).
2. Edit the relevant page(s) in `docs/`. Keep changes focused.
3. Update **cross-links** and the **table of contents** in `README.md` if you add/rename/move a page.
4. Open a pull request describing *what changed and why*.

## Style conventions

- Use `MUST / SHOULD / MAY` for requirements ([RFC 2119](https://www.rfc-editor.org/rfc/rfc2119)).
- Keep IDs stable: functional requirements `FR-#`, non-functional `NFR-#`, stories `A1`, `B2`, etc.
- Prefer plain language; define domain terms in the [Glossary](docs/14-glossary.md).
- Diagrams use [Mermaid](https://mermaid.js.org/) so they render natively on GitHub.
- When you resolve an open item, move it to the **Decisions log** in
  [Open Questions](docs/13-open-questions.md) with a date and rationale.

## Adding a new page

1. Create `docs/NN-title.md` with prev/next nav links at top and bottom.
2. Add it to the table of contents in [`README.md`](README.md).
3. Link to it from related pages.

## Review

PRD changes should be reviewed by the page area's owner (see
[Open Questions](docs/13-open-questions.md) for owners) before merge.
