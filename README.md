# UX Superpowers 🔬

**User-centered design methodology for coding agents.**

Ground every line of code in real user needs — not assumptions.

## What Is This?

UX Superpowers is a Claude Code plugin that adds a **UX discovery phase** to your development workflow. Before you brainstorm solutions, before you write code, this plugin ensures you understand:

- **Who** you're building for (Personas)
- **What** they're trying to accomplish (Jobs to Be Done)
- **How** they experience the problem today (User Journey Maps)
- **How** you'll know if you succeeded (Telemetry & Metrics)

It accepts real user data (interviews, feedback, analytics) or guides you through discovery from scratch.

## How It Works With Superpowers

UX Superpowers is designed to **complement** [Superpowers](https://github.com/obra/superpowers), not replace it.

```
┌─────────────────────────┐     ┌──────────────────────────┐
│   UX SUPERPOWERS        │     │   SUPERPOWERS            │
│                         │     │                          │
│  Problem Definition     │     │  Technical Brainstorming │
│  Personas               │────▶│  Implementation Planning │
│  Jobs to Be Done        │     │  TDD & Code Review       │
│  User Journeys          │     │  Subagent Development    │
│  Telemetry Planning     │     │                          │
│                         │     │                          │
│  "WHAT and WHY"         │     │  "HOW"                   │
└─────────────────────────┘     └──────────────────────────┘
```

**UX Superpowers** owns the "what" and "why." **Superpowers** owns the "how."

You can use UX Superpowers standalone or alongside Superpowers. When both are installed, UX discovery runs first, then hands off to Superpowers' brainstorming skill with full context.

## Installation

### From Claude Code Marketplace

```bash
/plugin marketplace add adnanmir123/ux-superpowers
/plugin install ux-superpowers@ux-superpowers
```

### Local Development

```bash
git clone https://github.com/adnanmir123/ux-superpowers.git
claude --plugin-dir ./ux-superpowers
```

## Skills

| Skill | Trigger | What It Does |
|-------|---------|-------------|
| `ux-discover` | "Let's build X", "I want to create Y" | Orchestrates the full discovery flow |
| `persona-builder` | "Who are the users?", "Build personas" | Creates evidence-based user personas |
| `jobs-to-be-done` | "What are users trying to do?" | Maps functional, emotional, social jobs |
| `user-journey` | "Map the user experience" | Current-state and desired-state journey maps |
| `telemetry-designer` | "How do we measure success?" | Defines metrics, events, and feedback loops |
| `research-intake` | User provides raw data (interviews, feedback, etc.) | Synthesizes raw research into structured insights |
| `insight-synthesizer` | After all discovery phases complete | Produces the final UX Discovery Document |
| `ux-validate` | During code review, before shipping | Checks implementation against discovery artifacts |

## Quick Start

Just start building something. UX Superpowers will nudge you to run discovery first:

```
You: "I want to build a CLI tool for managing database migrations"

Claude: "Before we design the solution, let's understand the problem and users.
         Do you have any existing user research or feedback I should review first?"
```

Or invoke directly:

```
/ux-superpowers:ux-discover
```

## Output

UX Superpowers produces a **UX Discovery Document** saved to `docs/ux-discovery/` containing:

1. Problem Brief
2. Personas (1-3, prioritized)
3. Jobs to Be Done (with opportunity scores)
4. User Journey Maps (current + desired state)
5. Success Metrics & Telemetry Plan
6. Design Principles
7. Assumptions & Risks
8. Constraints & Boundaries

This document becomes the **requirements anchor** for all subsequent development.

## Works for ALL Software

Not just web apps. UX Superpowers adapts to:

- Web & Mobile Apps
- CLI Tools & DevTools
- APIs & SDKs
- Infrastructure & Platform
- Internal Tools
- Data Pipelines
- Games
- Hardware Interfaces

## Philosophy

1. **One question at a time** — don't overwhelm the developer
2. **Evidence over opinion** — every decision traces to user data or labeled assumptions
3. **YAGNI applies to research** — get enough signal, then build
4. **Respect expertise** — if you know your users, skip ahead
5. **Progressive disclosure** — nudge, don't gate

## Contributing

We welcome contributions! See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

Skills live in `skills/`. Each skill is a directory with a `SKILL.md` file.

## License

MIT — see [LICENSE](LICENSE)

## Affiliation

UX Superpowers is an independent community project inspired by and designed to complement [Superpowers](https://github.com/obra/superpowers) by Jesse Vincent. It is **not affiliated with, endorsed by, or maintained by** the Superpowers project or its authors. The name reflects the complementary positioning in the workflow (UX discovery → technical brainstorming), not a shared origin.
