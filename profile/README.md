# ctrl alt doc

**Documentation, without the baggage.**

A documentation framework built to just work.

Write your docs. Configure what you need. Ship.

---

# Changelog

## v1.0.4

### Fixed

- Fixed imported Svelte components not rendering inside Markdown table cells.
- Added regression coverage for Svelte component placeholders in tables.
- Preserved normal inline Markdown formatting within table cells.

### Installation

```bash
npm install ctrl-alt-doc@1.0.4
```

## v1.0.3

### Added

- Added GitHub Packages publishing for the framework and project creator packages.
- Added generated-project support for the updated bundled documentation and template presentation.
- Added improved installation guidance and template examples.

### Fixed

- Fixed duplicate heading links in the table of contents.
- Fixed route-level TOCs drifting from the renderer-generated heading IDs.
- Improved development hot-reload handling while Markdown files are being saved.
- Updated the production workflow to use Node.js 22.

### Improved

- Refined the bundled documentation layout and visual presentation.
- Improved Steps documentation and examples.
- Improved generated-project route and document handling.
- Updated package metadata and GitHub repository links.

### Installation

```bash
npm install ctrl-alt-doc@1.0.3
