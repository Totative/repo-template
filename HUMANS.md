# HUMANS

Checklist after GitHub creates a repository from this template. Replace this file when the new repository has its own runbook.

## Quick start

```sh
lefthook install
```

1. Add the repository's languages to the matrix in `.github/workflows/codeql.yml`, and its package ecosystems to `.github/dependabot.yml`.
2. Replace `README.md`.
3. If the repository goes public, an org owner adds the `default-branch` ruleset.
4. Cut the first release with `git tag -s vX.Y.Z && git push origin vX.Y.Z`.
5. Anyone can verify a release with `gh attestation verify <file> --owner Totative`.

## Verify

`gate` runs gitleaks (skipped in CI) and `bunx --bun markdownlint-cli2 '**/*.md'`.
