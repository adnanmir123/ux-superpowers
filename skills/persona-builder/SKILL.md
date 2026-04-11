---
name: persona-builder
description: >
  Use when creating or refining user personas for a project. Builds evidence-based personas
  from raw data (interviews, analytics, feedback) or guides persona creation from scratch
  through structured questions. Produces actionable personas with behavioral patterns,
  goals, frustrations, and context — not demographic stereotypes. Works for any software type.
version: 1.0.0
---

# Persona Builder

Build personas that drive decisions, not decorate slide decks.

## Principles

- **Behavioral over demographic** — age/gender matter far less than behaviors, motivations, and context
- **Fewer is better** — 1-3 personas max. If you need more, your product scope is too broad.
- **Primary persona first** — one persona whose needs you prioritize above all others
- **Evidence-based** — every claim should trace to data or a stated assumption (clearly labeled)

## When Raw Data Is Available

If the user has provided interview transcripts, survey data, support tickets, analytics,
or feedback:

1. Read and analyze the data
2. Identify behavioral patterns and clusters
3. Propose persona groupings with evidence
4. Ask the user to validate groupings before fleshing out

## When Starting from Scratch

Ask these questions ONE AT A TIME:

1. "Who is the primary user of what you're building? Describe them by their **role and context**, not demographics."
   - Example good answer: "A backend engineer at a mid-size startup debugging production issues at 2am"
   - Example bad answer: "Males aged 25-35" (redirect if this happens)

2. "What does a typical day look like for this person, specifically around the problem you're solving?"

3. "What's their technical sophistication relative to your solution?"
   - Offer: Expert / Intermediate / Beginner / Mixed

4. "Are there other distinct user types who use this differently?"
   - If yes: repeat questions 1-3 for secondary personas (max 2 more)
   - If no: proceed

## Persona Template

For each persona, produce:

```markdown
### Persona: [Name — a memorable shorthand, not a real name]

**Role & Context**: [one sentence — who they are and where they operate]

**Behavioral Pattern**: [how they currently approach the problem space]

**Primary Goal**: [what they're trying to achieve — functional]
**Emotional Goal**: [how they want to feel — confident, in control, relieved, etc.]
**Social Goal**: [how they want to be perceived — competent, innovative, responsible, etc.]

**Frustrations & Pain Points**:
- [specific, observable frustrations — not vague]

**Current Tools & Workarounds**:
- [what they use today and how they hack around gaps]

**Context of Use**:
- **When**: [time pressure, frequency of use]
- **Where**: [environment — desk, mobile, terminal, meeting, etc.]
- **Device/Platform**: [relevant technical context]
- **Constraints**: [bandwidth, permissions, compliance, accessibility, etc.]

**Quote** (real or synthesized from data):
> "[A sentence that captures their mindset]"

**Priority**: [Primary | Secondary | Tertiary]
**Evidence basis**: [Data-backed | Assumption — validated by user | Assumption — needs validation]
```

## Validation

After presenting personas, ask:

> "Do these feel right? Is there anything that doesn't match your understanding of your users?"

Iterate based on feedback. Then confirm:

> "Which persona should we prioritize as the primary user? Their needs will take precedence when we face tradeoffs."

## Anti-Patterns to Avoid

- **The Everything Persona** — a persona that represents "everyone." Push back. Who is the PRIMARY user?
- **Demographic Stereotypes** — avoid assumptions based on age, gender, location unless evidence-based
- **Aspirational Personas** — personas should reflect WHO USERS ARE, not who the team wishes they were
- **Too Many Personas** — more than 3 means the scope needs narrowing, not more personas
