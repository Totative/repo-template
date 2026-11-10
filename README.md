# repo-template

The Totative starting point for a new repository: secret-scanning hooks, Dependabot, CodeQL, dependency review, Scorecard and an attested release workflow.

## After you create a repository from this

1. Run `lefthook install`.
2. Add the repository's languages to the matrix in `.github/workflows/codeql.yml`, and its package ecosystems to `.github/dependabot.yml`.
3. Replace this README.
4. If the repository goes public, an org owner adds the `default-branch` ruleset.
5. Cut the first release with `git tag -s vX.Y.Z && git push origin vX.Y.Z`.
6. Anyone can verify a release with `gh attestation verify <file> --owner Totative`.

The `LICENSE` is Apache-2.0. `SECURITY.md` and `CONTRIBUTING.md` come from the org defaults, so the template has neither.
