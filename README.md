# repo-template

The Totative starting point for a new repository: secret-scanning hooks, Dependabot, CodeQL, dependency review, Scorecard and an attested release workflow.

## After you create a repository from this

1. Run `lefthook install`.
2. Add the repository's languages to the matrix in `.github/workflows/codeql.yml`.
3. Add a `LICENSE`. An org owner picks it.
4. Replace this README.
5. If the repository goes public, an org owner adds the `default-branch` ruleset.
6. Cut the first release with `git tag -s vX.Y.Z && git push origin vX.Y.Z`.
7. Anyone can verify a release with `gh attestation verify <file> --owner Totative`.

`SECURITY.md` and `CONTRIBUTING.md` come from the org defaults, so the template has neither.
