# Claude Code configuration

`settings.json` registers the [Claude SEO](https://github.com/AgriciDaniel/claude-seo)
plugin (MIT, by AgriciDaniel) for this repository:

- `extraKnownMarketplaces` points at the `AgriciDaniel/claude-seo` GitHub marketplace.
- `enabledPlugins` turns on `claude-seo@agricidaniel-claude-seo`.

Claude Code reads these on session start, so the plugin loads automatically
instead of having to be reinstalled by hand. The first session after cloning may
ask you to trust the marketplace before it loads.

## One-time runtime setup

The plugin ships Python scripts that need an isolated environment. After the
plugin loads, run:

```
/seo setup
```

This creates a virtualenv and installs Playwright Chromium under Claude's plugin
data directory. Nothing is installed globally and no PATH shims are created.
Check it at any time with `/seo doctor`.

## Usage

```
/seo audit <url>     # full-site audit
/seo page <url>      # single-page deep dive
/seo schema <url>    # schema markup validation
/seo geo <url>       # AI-search / GEO analysis
```

These files only affect Claude Code. They are not part of the profile README
that GitHub renders.
