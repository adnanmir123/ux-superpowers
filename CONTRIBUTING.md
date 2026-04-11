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

## Code of Conduct

Be kind. Be constructive. Remember that this project exists to help people build better software for their users.
