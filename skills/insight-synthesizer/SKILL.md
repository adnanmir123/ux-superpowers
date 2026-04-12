---
name: insight-synthesizer
description: >
  Trigger whenever the user says "compile the discovery doc", "synthesize everything into
  one document", "write the UX discovery document", "produce the final discovery artifact",
  "consolidate personas jobs journeys and metrics", "extract design principles from our
  discovery", "surface assumptions and risks", "create the requirements anchor", "wrap up
  discovery", or any phrase signaling they are ready to assemble prior discovery outputs
  into a single anchoring document. Always invoke when the user has existing persona, JTBD,
  journey, telemetry, or research-intake artifacts and wants them fused into one cohesive
  UX Discovery Document saved to docs/ux-discovery/ with design principles, validated and
  unvalidated assumptions, risks, technical and business constraints, scope boundaries, and
  next steps. This is the LAST step in the ux-superpowers discovery pipeline and the
  canonical handoff point to superpowers:brainstorming — fire it when the user asks "we're
  done with discovery, what's next", "ready to move to technical brainstorming", or
  otherwise signals the discovery phase is closing. Do NOT fire for building any single
  artifact (the dedicated sub-skill owns that), while ux-discover is still orchestrating
  earlier phases, when the user has no prior discovery artifacts to synthesize, or for
  general document writing, engineering RFCs, or status reports unrelated to UX discovery.
version: 1.0.0
---

# Insight Synthesizer

Distill everything into a single document that keeps the team honest.

## Process

### Step 1: Gather All Artifacts

Collect outputs from all prior skills:
- Problem Brief (from ux-discover)
- Personas (from persona-builder)
- Jobs to Be Done (from jobs-to-be-done)
- Journey Maps (from user-journey)
- Telemetry Plan (from telemetry-designer)
- Research Insights (from research-intake, if used)

### Step 2: Extract Design Principles

From all the data, derive 3-5 design principles that should guide every technical decision:

```markdown
## Design Principles

1. **[Principle Name]**: [One sentence explaining the principle]
   - *Because*: [evidence from discovery that supports this]
   - *This means*: [concrete implication for what we build]
   - *This means NOT*: [what this principle rules out]
```

Examples:
- "Speed over completeness — users need answers in seconds, not comprehensive reports"
- "Progressive complexity — simple by default, powerful when needed"
- "Offline-first — users are often in environments with unreliable connectivity"

### Step 3: Assumptions & Risks

```markdown
## Assumptions & Risks

### Validated Assumptions (evidence-based)
- [assumption] — Supported by: [evidence]

### Unvalidated Assumptions (hypotheses)
- [assumption] — How to validate: [suggested method]
- Risk if wrong: [impact]

### Known Risks
| Risk | Likelihood | Impact | Mitigation |
|------|-----------|--------|------------|
| [risk] | High/Med/Low | High/Med/Low | [what to do] |
```

### Step 4: Constraints & Boundaries

```markdown
## Constraints

### Technical Constraints
- [platform, language, infrastructure limitations]

### User Constraints
- [accessibility needs, device limitations, skill levels]

### Business Constraints
- [timeline, budget, compliance, regulatory]

### Scope Boundaries
- **In scope**: [what we're building]
- **Out of scope**: [what we're explicitly NOT building — and why]
- **Future consideration**: [things we might build later]
```

### Step 5: Compile UX Discovery Document

Assemble the final document with this structure:

```markdown
# UX Discovery Document: [Project Name]
**Date**: [YYYY-MM-DD]
**Author**: [user + UX Superpowers]
**Status**: [Draft | Reviewed | Approved]

## 1. Problem Brief
[from ux-discover phase]

## 2. Personas
[from persona-builder — include all personas with priority levels]

## 3. Jobs to Be Done
[from jobs-to-be-done — primary and secondary jobs]

## 4. User Journey Maps
[from user-journey — current state and desired state]

## 5. Success Metrics & Telemetry
[from telemetry-designer — north star, health metrics, telemetry plan]

## 6. Design Principles
[from this synthesis]

## 7. Assumptions & Risks
[from this synthesis]

## 8. Constraints & Boundaries
[from this synthesis]

## 9. Research Summary
[from research-intake, if raw data was provided]

## 10. Recommended Next Steps
- [ ] [specific next action]
- [ ] [specific next action]
- [ ] [specific next action]
```

Save to: `docs/ux-discovery/YYYY-MM-DD-<project-name>-discovery.md`

### Step 6: User Review

Present the document in digestible sections (not all at once).
Ask the user to review and approve each major section.

After approval, suggest next steps:
- If Superpowers is installed: "Ready to move to technical brainstorming? I'll pass this discovery doc as context to the brainstorming skill."
- If not: "This discovery doc should anchor your technical design. Reference it when making tradeoff decisions."
