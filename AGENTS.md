# Repository Guidelines

## Project Structure & Module Organization
- `layouts/` holds Hugo templates (`_default/` and `partials/` for shared blocks).
- `static/` contains theme assets such as CSS (`static/css/`).
- `archetypes/` defines default content front matter (`archetypes/default.md`).
- `exampleSite/` is a runnable demo site with content, data, and config.
- `images/` includes theme screenshots and thumbnails.

## Build, Test, and Development Commands
- `hugo server -s exampleSite -D` runs the demo site locally with drafts.
- `hugo -s exampleSite` builds the demo site into `exampleSite/public/`.
- `blogdown::new_site(theme = "yihui/hugo-xmag")` (R) boots a new site using this theme.

## Coding Style & Naming Conventions
- Keep indentation consistent with existing files (2 spaces in YAML and HTML templates).
- CSS lives in `static/css/`; follow existing selector naming and keep rules small.
- Hugo templates should use descriptive partial names (match existing files in `layouts/partials/`).

## Testing Guidelines
- No automated test suite is defined in this repository.
- Validate changes by running `hugo server -s exampleSite -D` and checking rendered pages.

## Commit & Pull Request Guidelines
- Commit messages are short, present tense, and often use a prefix like `fix:` or `add:`.
- PRs should describe the change, list affected templates/assets, and include screenshots for UI changes.

## Configuration Tips
- Theme options are driven by Hugo config (see `exampleSite/config.yaml`).
- Add new content in `exampleSite/content/` to exercise templates during development.
