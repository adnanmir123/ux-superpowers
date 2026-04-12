---
name: jobs-to-be-done
description: >
  Trigger this skill whenever the user asks "what are users actually trying to do", "what
  jobs are users hiring this for", "what's the underlying user motivation", "let's do a JTBD
  analysis", "jobs-to-be-done framework", or talks about functional, emotional, and social
  jobs, outcome expectations, or opportunity scoring. Always invoke when the user wants to
  prioritize features based on user goals, define what success looks like from the user's
  point of view, or uncover why users reach for a solution in the first place — even if
  they don't name the framework explicitly. Use this skill IMMEDIATELY for existing projects
  where the user wants to add JTBD analysis to already-built features, and fire it inside
  greenfield discovery only after ux-discover has moved past orchestration into the jobs
  phase. Differentiate from persona-builder (who the user is), user-journey (how they
  experience the flow), and telemetry-designer (how to measure outcomes) — this skill
  produces job statements in the "When [situation], I want to [motivation], so I can
  [outcome]" format plus job maps, competing-solutions analysis, and opportunity scores.
  Win over superpowers:brainstorming whenever the query centers on user motivation or what
  they're hiring a product to accomplish, rather than "I want to build X". Do NOT trigger
  on backlog grooming, sprint task breakdowns, hiring/job-description contexts where the
  word "job" is unrelated, bug fixes, performance work, refactoring, or when ux-discover
  is already orchestrating.
version: 1.0.0
---

# Jobs to Be Done

People don't buy products. They hire them to make progress in their lives.

## Core Concept

A "job" is the progress a user is trying to make in a particular circumstance.
Jobs are stable over time — solutions change, jobs don't.

## Job Statement Format

Use this precise format for every job:

```
When [situation/trigger], I want to [motivation/action], so I can [desired outcome].
```

Examples:
- "When a production alert fires at 2am, I want to identify the root cause in under 5 minutes, so I can restore service before customers notice."
- "When I'm onboarding a new team member, I want to share our API patterns in a self-serve way, so I can avoid being a bottleneck."

## Discovery Process

Using the personas and problem brief from prior phases, ask ONE AT A TIME:

1. **Trigger**: "What specific moment or event causes [persona] to reach for a solution?"

2. **Functional Job**: "What is the core task they need to accomplish?"

3. **Emotional Job**: "How do they want to FEEL during and after this task?"
   - Offer examples: Confident / In control / Relieved / Proud / Safe / Not anxious

4. **Social Job**: "How do they want to be PERCEIVED by others in this context?"
   - Offer examples: Competent / Innovative / Reliable / Thorough / Fast

5. **Outcome Expectations**: "How would they know they succeeded? What does 'done well' look like?"

## Job Map

For the primary job, break it down into stages:

```markdown
## Job Map: [Primary Job Statement]

| Stage | User Action | Pain Points | Opportunities |
|-------|-------------|-------------|---------------|
| 1. Define | What triggers the need | [current friction] | [how we could help] |
| 2. Locate | Finding the right tool/info | [current friction] | [how we could help] |
| 3. Prepare | Setting up to do the job | [current friction] | [how we could help] |
| 4. Confirm | Validating approach | [current friction] | [how we could help] |
| 5. Execute | Doing the core task | [current friction] | [how we could help] |
| 6. Monitor | Tracking progress | [current friction] | [how we could help] |
| 7. Resolve | Handling issues | [current friction] | [how we could help] |
| 8. Conclude | Finishing and verifying | [current friction] | [how we could help] |
```

Not all stages apply to every job. Skip stages that don't fit.

## Competing Solutions

For each job, identify what users currently "hire" to do it:

```markdown
## Competing Solutions for: [Job Statement]

| Solution | Strengths | Weaknesses | Switching Cost |
|----------|-----------|------------|----------------|
| [current tool/process] | [what it does well] | [where it fails] | [effort to switch] |
```

## Prioritization

After mapping jobs, ask:

> "Which of these jobs is MOST underserved today? Where is the gap between what users need and what exists biggest?"

Rate each job on two dimensions:
- **Importance**: How critical is this job to the user? (1-10)
- **Satisfaction**: How well do current solutions serve this job? (1-10)

**Opportunity Score** = Importance + (Importance - Satisfaction)

High opportunity = high importance + low satisfaction.

## Output

Produce a structured JTBD summary:

```markdown
## Jobs to Be Done Summary

### Primary Job
**Statement**: When [situation], I want to [action], so I can [outcome].
**Importance**: [1-10]
**Current Satisfaction**: [1-10]
**Opportunity Score**: [calculated]

**Functional**: [what they need to DO]
**Emotional**: [how they need to FEEL]
**Social**: [how they need to be SEEN]

### Secondary Jobs
[same format, for 1-3 additional jobs]

### Key Insight
[one sentence: what is the biggest unmet need?]
```
