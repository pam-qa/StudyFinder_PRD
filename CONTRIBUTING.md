# Contributing to the StudyFinder PRD

This repository is a **living Product Requirements Document** kept as a wiki of linked Markdown pages.
Contributions that sharpen the requirements or improve clarity are welcome.

## How it's organized

- [`README.md`](README.md) — home page and table of contents.
- [`docs/`](docs/) — numbered foundation pages (`01`–`04`) plus the Core Product Areas overview.
- [`docs/areas/`](docs/areas/) — one page per core product area (Study Discovery, Search & Filtering,
  Scouts, Email Sequences, etc.).
- Pages cross-link with relative Markdown links so they render on GitHub.

## Making changes

1. Create a branch (e.g., `docs/clarify-email-sequences`).
2. Edit the relevant page(s). Keep changes focused.
3. Update **cross-links** and the **table of contents** in `README.md` if you add/rename/move a page.
4. Open a pull request describing *what changed and why*.

## Style conventions

- Keep content faithful to the source PRD; flag proposed additions clearly in the PR.
- Preserve prev/next navigation links at the top and bottom of each page.
- Keep the feature-access matrix in [Subscription Tiers](docs/03-subscription-tiers.md) as the single
  source of truth for tier gating; individual area pages should link to it rather than restate limits.

## Adding a new page

1. Create the `.md` file with prev/next nav links at top and bottom.
2. Add it to the table of contents in [`README.md`](README.md).
3. Link to it from related pages.
