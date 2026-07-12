# Profile Maintenance

This repository is a GitHub profile repository. The main product is the public `README.md` rendered at the top of the `shiguemori` GitHub profile.

## Purpose

The profile should quickly communicate:

- Who Vinicius Shiguemori is professionally.
- The engineering problems he is strongest at solving.
- The technologies and practices he uses most often.
- Clear ways for recruiters, peers, and collaborators to connect.

## Current Structure

```text
.
|-- README.md
|-- docs/
|   |-- improvements.md
|   `-- profile-maintenance.md
|-- .github/
|   `-- workflows/
|       `-- profile-quality.yml
|-- .lychee.toml
|-- .markdownlint-cli2.jsonc
`-- .gitattributes
```

## Maintenance Checklist

Run through this checklist when updating the profile:

- Keep the first screen focused on role, specialty, and value.
- Prefer concise bullets over long biography paragraphs.
- Keep technologies grouped by capability, not by every tool ever used.
- Verify all links after editing badges, social links, or external images.
- Avoid unsupported HTML or Markdown that could render poorly on GitHub.
- Keep contact information current.
- Review the improvement backlog once per quarter.

## Local Validation

Markdown linting can be run locally with:

```bash
npx --yes markdownlint-cli2
```

Link validation is handled in GitHub Actions through Lychee. If you want to run an equivalent local check and have Lychee installed:

```bash
lychee --config .lychee.toml README.md "docs/**/*.md"
```

Some badge, stats, and social-profile hosts are excluded in `.lychee.toml` because they commonly block automated requests or return intermittent status codes even when they render correctly on GitHub.

## GitHub Actions

The workflow at `.github/workflows/profile-quality.yml` runs on:

- Pushes to `main`.
- Pull requests.
- Manual dispatch.
- A weekly scheduled check.

It validates Markdown style and scans links so regressions are caught before the profile degrades silently.

## Content Guidelines

Use the README as a professional signal, not a resume dump. The best updates are specific enough to show seniority but short enough to scan in under a minute.

Good content:

- Names real engineering domains: distributed systems, observability, API performance.
- Explains outcomes: reliability, throughput, maintainability, delivery confidence.
- Uses stable links and badges.

Avoid:

- Encoding-sensitive decorative characters that may render incorrectly.
- Overloaded skill lists with no prioritization.
- Too many dynamic widgets that can slow or break the profile.
- Claims that are hard to verify or maintain.
