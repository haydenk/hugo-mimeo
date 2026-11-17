# Security policy

## What this project is

Mimeo is a Hugo theme: templates and a stylesheet that run at build time on
the site author's machine or CI and produce static HTML. There is no server
component, no JavaScript in the shipped pages, no network calls at runtime,
and no handling of visitor data. The attack surface is correspondingly
small, but not zero.

## What counts as a vulnerability here

- Rendered output that lets content or configuration break out of its
  context: an attribute, URL or element that is emitted without the escaping
  Hugo would otherwise apply, in a way that could inject markup or script
  into a built page.
- A template or render hook that reads or writes files outside the site
  being built.
- A mise task or workflow in this repository that executes untrusted input,
  leaks a token, or pulls an unpinned dependency.

Hugo itself, Chroma, and the pinned tools are upstream projects; report
issues in them upstream. A site author's own content is trusted by design,
as it is in every Hugo theme.

## Reporting

Please do not open a public issue for a security problem.

Use GitHub's private vulnerability reporting for this repository, under
**Security > Report a vulnerability**. If that is not available, contact the
maintainer through the address on their GitHub profile.

Include the affected template or file, the content or configuration that
triggers it, and the output you saw. A minimal reproduction in a copy of
`exampleSite/` is ideal.

## What to expect

The maintainer aims to acknowledge a report within a week and to publish a
fix as a patch release once one exists. Advisories are published through
GitHub's security advisories for the repository, and the release notes name
the fix. Credit is given to reporters who want it.

## Supported versions

The latest release receives fixes. Older releases do not; upgrading is a
Hugo module bump or a new archive in `themes/mimeo`.
