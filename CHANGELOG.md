# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added

### Changed

### Deprecated

### Removed

### Fixed

### Security

## [1.0.0] - 2026-11-16

First release.

### Added

- A mail-style header on every single page: `From`, `Date`, `Subject`
  (carrying the page's `<h1>`), `Tags`, `Series`, an optional
  `X-Read-Time`, and `X-Plain-Text` linking the page's text twin.
- A plain-text twin of every page through a `txt` output format: the same
  header, then the page's raw Markdown, at the page URL with `.txt` on the
  end, advertised with `<link rel="alternate" type="text/plain">`.
- Content styled like its Markdown source: `#` markers on headings, `*` on
  bullets, `>` on quotes, a `--` signature line in the footer. Decorative
  markers carry empty alternative text so screen readers skip them.
- Light and dark from the system preference through CSS `light-dark()`.
  No JavaScript, no web fonts; JetBrains Mono when installed, otherwise the
  system monospace stack.
- Code highlighting in GitHub's light and dark palettes, generated from
  Hugo's Chroma styles into `light-dark()` pairs by `mise run gen:chroma`.
- An image render hook that serves page and global resources as WebP with
  width and height, resizes anything wider than the column, lazy-loads all
  but the first image, and turns a captioned standalone image into a
  `<figure>`.
- A table render hook that wraps tables in a scrolling container so they
  keep their semantics, with column alignment as classes.
- Lists that read like a log, with an optional one-line summary; a home
  page listing of configurable sections; an archive page grouped by month
  with an "Undated" group; tags and series taxonomies; RSS, sitemap,
  Open Graph tags with image alt text, and a meta description from the
  first paragraphs.
- Hooks for sites to extend without overriding templates: `head-start`,
  `head-end`, `single-after-content`, `footer-start`, `body-end`; and an
  `assets/css/custom.css` appended to the stylesheet.
- Params: `authorName`, `description`, `images`, `imageAlt`,
  `homeIntroContent`, `homeCollection`, `homeCollectionTitle`, `homeCount`,
  `listSummaries`, `listDateFormat`, `readTime`, `showTags`,
  `footerContent`, `inlineCSS`, and `social` signature links.
- A favicon set in `static/` and an archetype that derives title and slug
  from a date-prefixed filename.
- An example site that doubles as the test fixture, mise tasks for every
  check, GitHub Actions for CI and releases, release archives that unpack
  to `themes/mimeo`, and a demo deployed to GitHub Pages on each release.

[Unreleased]: https://github.com/haydenk/mimeo/compare/v1.0.0...HEAD
[1.0.0]: https://github.com/haydenk/mimeo/releases/tag/v1.0.0
