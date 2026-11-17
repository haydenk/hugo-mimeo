# Contributing to Mimeo

Thanks for considering it. Mimeo is a small theme with a narrow idea, a page
that reads like a text file, and the best contributions keep it that way.

## Before you start

- **Bugs:** open an issue with the bug form. A minimal page or config that
  shows the problem is worth more than a long description.
- **Features:** open an issue first, or a discussion if you are unsure. Say
  what it makes possible and whether a hook or `custom.css` could already do
  it. The answer to "can the theme have X" is sometimes "yes, in your site".
- **Small fixes** (typos, a broken link, an obvious one-liner) can go
  straight to a pull request.

## Setting up

Tool versions are pinned in `.mise.toml`; [mise](https://mise.jdx.dev) is
the only thing you install yourself.

```sh
mise run setup      # install the pinned tools
mise run serve      # the example site on http://localhost:1313
mise run ci         # everything CI runs: format, lint, build, test
```

`mise tasks` lists the rest. The example site under `exampleSite/` is both
the demo and the test fixture: if a change is visible, it should be visible
there.

## Making a change

- Branch from `master`, open a pull request against `master`. The template
  asks for the why; the diff shows the what.
- Run `mise run ci` before pushing. CI runs the same command.
- **Templates** live in `layouts/`. Prefer a hook (`layouts/_partials/hooks/`)
  over a new template when a site could reasonably want to opt out.
- **Styles** live in `assets/css/mimeo.css`. `assets/css/chroma.css` is
  generated; do not edit it by hand, run `mise run gen:chroma`.
- **A new param** needs four things: the template change, a line in the
  README's Configure section, an entry in the example site's `hugo.toml`
  where that helps the demo, and a test assertion in `.mise/tasks/test`
  when its effect is visible in built HTML.
- **Anything a site may depend on** (a param name, a hook name, a template
  a site might override, the `.txt` format) is a breaking change if it
  changes. Say so in the pull request; it decides the next version number.
- Keep the shipped page free of JavaScript and web fonts. That is the
  theme's promise, and the test task fails on a `<script>` element.

## Style

- Templates: Hugo's contextual escaping over `safeHTML`. If you need
  `safeHTML`, explain why in a comment.
- CSS: `light-dark()` pairs for every colour, `ch` units for horizontal
  measure, 4.5:1 contrast or better for text.
- Shell: every task is `bash`, `set -euo pipefail`, passes shellcheck.
- Prose and comments: explain the non-obvious; do not narrate the code.
- Formatting is enforced by `mise run format:check`; `mise run format:run`
  fixes it.

## Releases

Maintainers cut releases by renaming `[Unreleased]` in `CHANGELOG.md` on a
`release/MAJOR.MINOR.PATCH` branch and merging its pull request; the merge
to `master` tags and publishes. See the README's Develop section.
Contributors do not touch versions or tags, but do add a line under
`[Unreleased]` in `CHANGELOG.md` for anything a site would notice. That
section becomes the release notes, followed by the generated list of
merged pull requests grouped by label, so a clear PR title helps too.

## Licence

By contributing you agree that your contribution is licensed under the
project's licence, the GNU Affero General Public License v3.0, the same as
the rest of the theme.
