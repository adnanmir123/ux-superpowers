---
name: ux-validate
description: >
  Use during or after implementation to validate that code, features, and technical
  decisions align with the UX Discovery Document. Checks for persona alignment,
  JTBD coverage, journey gap closure, and metric instrumentation. Use whenever
  reviewing code, PRs, or feature completeness. This is the "throughout" companion
  to the upfront discovery phase.
version: 1.0.0
---

# UX Validation

Check that what you're building still serves the user you researched.

## When to Use

- Before marking a feature complete
- During code review
- When making tradeoff decisions
- When scope changes are proposed
- When the team says "let's just ship it"

## Validation Checklist

Read the project's UX Discovery Document from `docs/ux-discovery/` and evaluate:

### 1. Persona Alignment
- [ ] Does this serve the PRIMARY persona's needs?
- [ ] Does it avoid harming secondary personas?
- [ ] Does it match the persona's technical sophistication level?
- [ ] Does it fit the persona's context of use (device, environment, time pressure)?

### 2. JTBD Coverage
- [ ] Does this help users accomplish the PRIMARY job?
- [ ] Does it address the functional need?
- [ ] Does it support the emotional goal (how they want to feel)?
- [ ] Does it consider the social goal (how they want to be perceived)?

### 3. Journey Gap Closure
- [ ] Does this address identified pain points from the journey map?
- [ ] Does it preserve existing moments of delight?
- [ ] Does it move the experience toward the desired state?
- [ ] Does it handle the error/edge case journey, not just the happy path?

### 4. Design Principle Adherence
- [ ] Does this align with each stated design principle?
- [ ] If it violates a principle, is there an explicit, documented reason?

### 5. Metric Instrumentation
- [ ] Are the specified telemetry events implemented?
- [ ] Can we measure the North Star Metric with what's built?
- [ ] Are guard-rail health metrics in place?
- [ ] Is there a way to collect qualitative feedback?

### 6. Assumption Check
- [ ] Have any unvalidated assumptions been proven wrong during development?
- [ ] If so, does the implementation need to change?

## Output

```markdown
## UX Validation Report

**Feature/PR**: [name]
**Date**: [YYYY-MM-DD]
**Discovery Doc**: [path to discovery doc]

### Alignment Score: [Strong | Partial | Weak | Misaligned]

### Findings
| Area | Status | Notes |
|------|--------|-------|
| Persona alignment | ✅/⚠️/❌ | [detail] |
| JTBD coverage | ✅/⚠️/❌ | [detail] |
| Journey gaps addressed | ✅/⚠️/❌ | [detail] |
| Design principles | ✅/⚠️/❌ | [detail] |
| Telemetry implemented | ✅/⚠️/❌ | [detail] |
| Assumptions valid | ✅/⚠️/❌ | [detail] |

### Recommendations
- [specific, actionable recommendations]

### Risks if Shipped As-Is
- [what could go wrong for users]
```

## Integration with Superpowers

If Superpowers' code-reviewer agent is active, the UX validation report should be
included alongside the code quality review. Technical quality AND user alignment
both matter.
