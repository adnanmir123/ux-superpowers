# Contributing to UX Superpowers

Thanks for your interest in contributing! This project exists to make user-centered development the default, not the exception.

## How to Contribute

### Adding a New Skill

1. Create a directory under `skills/` with a kebab-case name
2. Add a `SKILL.md` with frontmatter (`name`, `description`, `version`)
3. Include clear instructions, examples, and anti-patterns
4. Test locally with `claude --plugin-dir ./ux-superpowers`
5. Submit a PR

### Improving Existing Skills

The best improvements come from using the skills on real projects and noticing where they fall short. If a skill asks the wrong questions, misses a common scenario, or produces output that doesn't help — that's a contribution opportunity.

### Skill Quality Bar

- **One question at a time** — skills should guide conversationally, not dump forms
- **Software-type agnostic** — skills must work for CLI, API, web, mobile, infra, etc.
- **Evidence-based** — instructions should distinguish facts from assumptions
- **Token-light** — skills should be concise. Claude reads these into context.
- **Opinionated** — skills should recommend, not just ask. Have a point of view.

### Reporting Issues

File issues on GitHub. Include:
- What you were trying to do
- What the skill did vs. what you expected
- The type of software you were building (helps us test edge cases)

## Release Process

UX Superpowers follows [semantic versioning](https://semver.org/):

- **MAJOR** — breaking changes to skill invocation, discovery document schema, or expected I/O
- **MINOR** — new skills, new fields in the discovery document, backward-compatible enhancements
- **PATCH** — prompt tweaks, bug fixes, doc improvements

### Cutting a release

1. Land all changes on `main` via PR
2. Bump `version` in `.claude-plugin/plugin.json`
3. Add a dated section to `CHANGELOG.md` at the top
4. Commit: `chore: release vX.Y.Z`
5. Tag: `git tag vX.Y.Z && git push origin vX.Y.Z`
6. The `Release` workflow creates a GitHub Release automatically from the tag + changelog section
7. Users pick up the new version on next `/plugin marketplace update`

> **Important**: Claude Code caches plugins by version. If you change code without bumping `version`, existing users will not see the change. Always bump.

## Agile Workflow

This project is small but aims to stay sustainable. Practices:

- **Trunk-based**: `main` is always releasable; feature work in short-lived branches
- **PRs over direct pushes**: even solo maintainer commits should flow through PR for CI to run
- **Small slices**: one skill change per PR where possible — easier to review, revert, and bisect
- **Issue-first for non-trivial work**: open an issue, agree on approach, then PR
- **Dogfood**: run discovery on your own plugin changes before shipping them

## Repository Transfer

The repo currently lives at `github.com/adnanmir123/ux-superpowers`. If the project grows to multiple maintainers, it may transfer to a `ux-superpowers` GitHub organization. GitHub preserves stars, issues, PRs, and auto-redirects old URLs, so the transfer is non-breaking for installed plugins.

## Code of Conduct

Be kind. Be constructive. Remember that this project exists to help people build better software for their users.
