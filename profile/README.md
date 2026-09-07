# ctrl alt doc

**Documentation, without the baggage.**

A documentation framework built to just work.

Write your docs. Configure what you need. Ship.

---

### 0.9.0 — Packaging & Scaffolding

ctrl alt doc is now structured as an actual framework package rather than a standalone documentation application.

The framework runtime, server-side document system, navigation, search, Markdown processing, icons, components, and framework stylesheet now live in `ctrl-alt-doc`, with the reference application consuming them as a package.

A `create-ctrlaltdoc` scaffolder has also been introduced. It generates a complete SvelteKit documentation project with the ctrl alt doc runtime, configuration, styling, routes, and starter documentation already wired together.

The generated project has been validated from a clean environment and successfully passes type checking and production builds using the packaged `ctrl-alt-doc` tarball.

The intended authoring model is now taking shape:

- `docs/` — your documentation
- `ctrlaltdoc.config.ts` — your configuration
- `custom.css` — your custom styling
- everything else — ctrl alt doc-managed framework infrastructure

The path toward the first stable release is now:

**Package → Scaffold → Validate → Release**

## Roadmap

### 0.8.0 — Working Application
The core documentation experience is working, including navigation, Markdown rendering, search, themes, callouts, cards, downloads, figures, file trees, and other documentation features.

### 0.9.0 — Packaging & Scaffolding
**In progress**

ctrl alt doc is becoming a distributable framework rather than an application template.

- Framework runtime extracted into `ctrl-alt-doc`
- Server runtime packaged and consumed through `ctrl-alt-doc/server`
- Framework components packaged and consumed through `ctrl-alt-doc/components`
- Framework stylesheet exposed as a package asset
- Reference application migrated to consume the framework package
- Local framework implementation removed from the reference application
- `create-ctrlaltdoc` scaffolder introduced
- Generated projects receive the complete SvelteKit application shell
- Project name is applied automatically during scaffolding
- Fresh generated projects validated with install, type-check, and production build
- Packaged `ctrl-alt-doc` artifacts validated outside the workspace
- Release packaging and public distribution still to be completed

### 1.0.0 — First Stable Release
The first stable release will arrive when a new project can be created, configured, documented, built, and deployed without requiring changes to ctrl alt doc's internal framework code.

**North star:**  
> ctrl alt doc manages the application. You manage the documentation.

---

### Projects

- **ctrl alt doc** — the documentation framework
- **Website** — the ctrl alt doc project website

More coming as the project develops.
