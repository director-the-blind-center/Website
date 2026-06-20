# Repository Guidelines

## Project Structure & Module Organization

This repository is a small static website intended for direct hosting, such as GitHub Pages. The main page lives at `index.html`, and global styling lives in `styles.css`. Keep additional pages at the repository root unless the site grows enough to justify folders. Put reusable assets in an `assets/` directory, using subfolders such as `assets/images/` or `assets/fonts/` when needed.

## Build, Test, and Development Commands

No package manager or build step is currently configured. Open `index.html` directly in a browser for a quick local check.

- `python3 -m http.server 8000`: serves the site locally at `http://localhost:8000` for browser testing.
- `git status --short`: checks which files are changed before committing.
- `git diff`: reviews exact edits before opening a pull request.

If a future toolchain is added, document the new install, build, lint, and test commands here.

## Coding Style & Naming Conventions

Use two-space indentation in HTML and CSS, matching the existing files. Keep HTML semantic and simple: prefer structural elements such as `main`, `section`, `h1`, and `p` before adding extra wrappers. Use lowercase, hyphenated class names such as `site-shell` and `intro-text`. Define shared colors, spacing, and typography through CSS custom properties in `:root` when values are reused.

Keep CSS organized from broad rules to specific components: root variables, resets, page layout, then element or class styles. Avoid introducing frameworks unless the site needs capabilities that plain HTML and CSS cannot reasonably provide.

## Testing Guidelines

There is no automated test suite yet. Before committing, manually verify `index.html` in a browser, including desktop and narrow mobile widths. Confirm that text remains readable, layout does not overflow, and links or assets load with relative paths. If JavaScript or a build pipeline is introduced later, add focused tests and document the command in this guide.

## Commit & Pull Request Guidelines

The current history uses short, descriptive commit messages, for example `Initial static site`. Continue using concise imperative or descriptive subjects, such as `Update homepage copy` or `Add responsive image assets`.

Pull requests should include a brief summary, screenshots for visible design changes, and notes about manual browser checks. Link related issues when available and call out any new dependencies or hosting configuration changes.
