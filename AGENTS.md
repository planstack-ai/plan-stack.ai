# Repository Guidelines

## Project Structure & Module Organization
- `index.html` is the single-page landing site, containing HTML, CSS, and inline assets.
- `docs/plans/` holds Plan Stack implementation plans (name format: `YYYYMMDD_feature_name.md`).
- `articles/` stores long-form content drafts (e.g., `plan-commit-ai-documentation.md`).
- `README.md` provides a short project overview.

## Build, Test, and Development Commands
- No build pipeline or package manager is configured; edits are made directly in `index.html`.
- Local preview options:
  - `python3 -m http.server 8000` (serve the folder and open `http://localhost:8000`).
  - Or open `index.html` directly in a browser for a quick check.

## Coding Style & Naming Conventions
- Indentation: 4 spaces in HTML/CSS (match existing formatting in `index.html`).
- Keep CSS variables in the `:root` block and reuse them for colors/spacing.
- Prefer semantic class names that map to sections (e.g., `.hero`, `.nav-links`).

## Testing Guidelines
- No automated tests or test framework are configured.
- Manually verify visual/layout changes at desktop and mobile widths after edits.

## Commit & Pull Request Guidelines
- Recent commits use short, imperative summaries (e.g., “Add Why section…”, “Improve hero…”).
- Draft work sometimes uses a `WIP:` prefix; follow this pattern if the change is not final.
- PRs should link to the related plan in `docs/plans/` and summarize the visual or copy changes.

## Planning Workflow (Plan Stack)
- Before changes, review `docs/plans/` for prior context.
- Create a new plan file for significant updates, then implement and verify against it.
