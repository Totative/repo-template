# AGENTS.md

The starting point for a new Totative repository: gitleaks hooks, Dependabot, CodeQL, dependency review, Scorecard and an attested release workflow. It is a GitHub template repo, so everything here is copied into each new repo.

## Layout

- `.github/workflows/release.yml`: on a `v*` tag, calls `Totative/.github/.github/workflows/release-source.yml` by commit SHA, so the SLSA Build L3 provenance names that file as the signer.
- `.github/workflows/codeql.yml`, `dependency-review.yml`, `scorecard.yml`, `.github/dependabot.yml`, `.github/CODEOWNERS`.
- `lefthook.yml`, `.gitleaks.toml`, `.gate.toml`, `.markdownlint-cli2.jsonc`, `LICENSE` (Apache-2.0), `README.md`.

## Gate

`gate` runs gitleaks (skipped in CI). `bunx --bun markdownlint-cli2 '**/*.md'` for Markdown.

## Invariants

- The `README.md` is the checklist for a new repo and is replaced there; keep it as a short list of steps.
- This `AGENTS.md` describes the template, so a repo made from it rewrites this file for itself.
- No `SECURITY.md` or `CONTRIBUTING.md`: the org defaults in `Totative/.github` apply.
- When `release-source.yml` changes in `Totative/.github`, bump the SHA pin in `release.yml` here.
- Workflow actions are pinned to a full commit SHA.
