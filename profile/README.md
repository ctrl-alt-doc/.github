# ctrl alt doc

**Documentation, without the baggage.**

A documentation framework built to just work.

Write your docs. Configure what you need. Ship.

---
# Changelog

All notable changes to ctrl alt doc are documented here.

## 1.0.0 --- Documentation, without the baggage.

The first stable release of ctrl alt doc.

ctrl alt doc is now a complete documentation framework with a packaged runtime,
project scaffolder, built-in documentation components, search,
navigation, icon system, and support for user-owned Svelte components
directly inside Markdown.

### Framework

-   Established `ctrl-alt-doc` as the framework/runtime package.
-   Established `create-ctrlaltdoc` as the project scaffolding CLI.
-   Added stable public package entry points for framework
    configuration, server utilities, Svelte components, framework
    styles, and Vite integration.
-   Kept generated projects thin: CAD manages the application while
    users own their documentation, configuration, assets, and custom
    styles.

### Project scaffolding

-   Added `pnpm create ctrlaltdoc` project generation.
-   Added a complete SvelteKit project template.
-   Added generated API routes for search, navigation, suggestions, and
    page metadata.
-   Added required Hugeicons SSR configuration to generated projects.
-   Synchronized bundled documentation between the reference application
    and generated-project template.

### Markdown and documentation

-   Added CAD Markdown extensions including callouts, Steps, Tabs,
    cards, file trees, downloads, details, and syntax-highlighted code
    blocks.
-   Added table of contents generation.
-   Added breadcrumbs and pagination.
-   Added document discovery, metadata, excerpts, navigation, and
    relative-link handling.
-   Preserved ordinary Markdown authoring without requiring CAD-specific
    file extensions.

### Svelte components in Markdown

-   Added the `ctrl-alt-doc/vite` integration.
-   Added support for importing Svelte components directly inside
    ordinary `.md` documentation.
-   Components resolve through the consuming project's normal
    Svelte/Vite dependency graph.
-   Component props and accessibility attributes are preserved.
-   Existing CAD Markdown processing remains intact.
-   Existing documents require no syntax changes.
-   User-owned icon/component packages remain user dependencies rather
    than CAD dependencies.
-   Invalid or missing component imports produce normal build errors.

Example:

``` svelte
<script>
    import AcademicCapIcon from '@iconify-svelte/heroicons/academic-cap';
</script>

<AcademicCapIcon height="1em" />
```

### Icons

-   Added the built-in Hugeicons Stroke Rounded icon system.
-   Added built-in interface, documentation, and social icons.
-   Added native built-in icon reference documentation.
-   Added GitHub, X, Discord, Instagram, YouTube, LinkedIn, Twitch,
    Reddit, and Bluesky brand icons.
-   Preserved `icons?: Record<string, string>` for custom SVG icons used
    by framework-owned icon slots.
-   Kept document-authored Svelte components separate from
    framework-owned icon resolution.

### Search

-   Added server-side documentation search.
-   Search covers document titles, descriptions, and rendered document
    content.
-   Added keyboard access with `/` and `Ctrl/Cmd + K`.
-   Added keyboard result navigation and selection.
-   Added generated-project search API support.

### Navigation and interface

-   Added collapsible documentation navigation.
-   Added independent category collapse state.
-   Collapsed categories remain collapsed when navigating to an active
    document inside them.
-   Added responsive sidebar behaviour.
-   Added theme support and navigation branding/social configuration.
-   Added configurable footer content and links.

### Validation

The `1.0.0` release candidate was validated from its distributable
packages rather than only from the development monorepo.

Validation included:

-   fresh project scaffolding from the packed `1.0.0` CLI
-   installation of the packed `ctrl-alt-doc` package
-   external `@iconify-svelte/heroicons` installation
-   Svelte component imports from Markdown
-   SSR compilation
-   production builds
-   all 22 bundled Markdown routes
-   search API
-   navigation API
-   suggestions API
-   page metadata API
-   TypeScript checks
-   Svelte checks
-   Prettier
-   ESLint
-   package tarball contents
-   CLI tarball installation and scaffolding

The live and scaffold documentation sets are synchronized at 24 files.

### Release status

ctrlaltdoc `1.0.0` marks the feature-freeze boundary for the first stable
release.

Further framework features are deferred to post-1.0 development.

