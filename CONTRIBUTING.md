# Contributing to ThinkHuman repositories

This is the default for every ThinkHuman repository. A repository with its own `CONTRIBUTING.md`
replaces it; read that one where it exists. By taking part you agree to the
[Code of Conduct](CODE_OF_CONDUCT.md).

## Workflow

1. **Start from an issue.** Bugs and scoped changes are issues, opened from a template. Small fixes
   and docs corrections can go straight to a pull request.
2. **Branch from the default branch** with a plain name: `feat/<slug>`, `fix/<slug>`, `chore/<slug>`,
   `docs/<slug>`, `ci/<slug>`. No personal or tool prefixes.
3. **One change per pull request.** Reference the issue with `Closes #NN` and fill in the template.
4. **CI must be green.** A red check is yours to fix. Never skip, disable or delete a test to get
   green.
5. **Merging.** Pull requests are squash-merged and the branch is deleted on merge. Long-lived
   branches (a release or staging line) are protected and stay.

## Commits and pull request titles

- Repositories that check pull request titles use [Conventional Commits](https://www.conventionalcommits.org):
  `type(scope): subject`. The title becomes the squash commit.
- Elsewhere, write a plain imperative subject in sentence case, with no type prefix.
- Subject in the imperative, no trailing period; the body says why.
- **No trailers of any kind**: no `Co-authored-by`, `Signed-off-by`, tool names or session links.

## Code style

Formatting and linting are [Biome](https://biomejs.dev) on the shared
[`@thinkhuman/biome-config`](https://github.com/ThinkHumanDotDev/biome-config). Run the repository's
`lint` script before pushing; `lint:fix` applies the safe fixes. Do not hand-format against it.

## Dependencies

[Renovate](https://github.com/ThinkHumanDotDev/renovate-config) opens update pull requests on Monday
mornings. A new dependency needs a reason in the pull request description.

## Security

Never report a vulnerability in public. See [SECURITY.md](SECURITY.md).
