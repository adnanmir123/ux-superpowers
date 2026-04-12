# Changelog

All notable changes to this project are documented here. The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## Unreleased

- Rewrote skill descriptions for 7 of 8 skills (persona-builder, jobs-to-be-done,
  user-journey, telemetry-designer, research-intake, insight-synthesizer, ux-validate)
  to use the "pushy trigger" pattern recommended by Anthropic's skill-creator docs.
  New descriptions lead with concrete user phrases, enumerate trigger contexts, and
  add explicit do-not-trigger guards to prevent false positives. Skill bodies are
  unchanged. ux-discover description is unchanged in this revision.

## 1.0.0 (2026-04-11)

### Initial Release

- **ux-discover**: Orchestrator skill — entry point for UX discovery
- **persona-builder**: Evidence-based behavioral personas
- **jobs-to-be-done**: Functional, emotional, social job mapping with opportunity scoring
- **user-journey**: Current-state and desired-state journey maps for any software type
- **telemetry-designer**: North star metrics, telemetry events, qualitative feedback plans
- **research-intake**: Process raw user data (interviews, surveys, tickets, analytics)
- **insight-synthesizer**: Compile UX Discovery Document from all phases
- **ux-validate**: Check implementation alignment during development
- **SessionStart hook**: Gentle nudge to run discovery before coding
- **Superpowers integration**: Designed to hand off to Superpowers brainstorming skill
