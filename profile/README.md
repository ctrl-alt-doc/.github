# ctrl alt doc

**Documentation, without the baggage.**

A documentation framework built to just work.

Write your docs. Configure what you need. Ship.

---

# Changelog

## v1.0.2

This release improves navigation, documentation cards, external links, serverless deployment,
development asset handling, and package update visibility.

### Added

- Added `New`, `Updated`, and `Beta` badges.
- Page badges now appear in sidebar navigation.
- Page badges now appear on generated documentation cards.
- Category badges can be configured through `_category.yml`.
- Added automatic package update notifications during `npm run dev`.
- Update notifications detect npm, pnpm, Yarn, and Bun.
- Added `ExternalLinkIcon` to external Markdown links, cards, and footer links.
- Added documentation covering badges, external links, documentation cards, and update notifications.
- Added build-time documentation bundling for serverless and edge deployments.

### Fixes in place

- Fixed `:::doc-cards` rendering an empty container on the homepage.
- Direct child directories containing an `index.md` document now appear as homepage documentation cards.
- Fixed homepage slug normalization in the Svelte-aware Vite transform.
- Fixed access to project-root assets such as `custom.css` during local development.
- Fixed Cloudflare Workers deployments requiring the source `docs/` directory at runtime.
- Fixed transient missing-file errors during replace-style Markdown saves in Vite development.
- Preserved existing documentation-card styling and Markdown behavior.
- External web links now open in a new tab.
- External links now include `rel="noopener noreferrer"`.
- Internal links and heading links continue to open in the current tab.

### Update notifications

When a newer version is available, running the development server now displays an update notice:

```text
┌  ctrl alt doc update available
│
│  1.0.1 → 1.0.2
│
│  Run: npm update ctrl-alt-doc
└
```

The update check:

- runs only during local development
- runs at most once every 24 hours
- does not delay development-server startup
- fails silently when the npm registry is unavailable
- is disabled automatically in CI
- never runs during production builds

Disable it manually with:

```bash
CTRL_ALT_DOC_DISABLE_UPDATE_CHECK=1 npm run dev
```

### Package versions

This release is distributed through:

- `ctrl-alt-doc@1.0.2`
- `create-ctrlaltdoc@1.0.3`

The intermediate `create-ctrlaltdoc@1.0.2` release was deprecated because npm removed its executable metadata during publication. Use `1.0.3` or newer.

### Updating an existing project

With npm:

```bash
npm install ctrl-alt-doc@latest
```

With pnpm:

```bash
pnpm update ctrl-alt-doc@latest
```

Restart the development server after updating.

You do not need to update `create-ctrlaltdoc` in an existing project. The scaffolder is only used when creating a new project.

---

## v1.0.1

### Repaired

- Allowed generated projects to serve project-root assets during development.
- Fixed Vite filesystem allow-list errors affecting `custom.css`.
- Confirmed the issue only affected the development server and HMR.
- Production builds and deployed output were unaffected.
