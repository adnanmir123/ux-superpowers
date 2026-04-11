---
name: jobs-to-be-done
description: >
  Use when defining what users are trying to accomplish with a product or feature.
  Applies the Jobs-to-be-Done framework to uncover functional, emotional, and social
  jobs users hire a product to do. Produces structured job statements that drive
  feature prioritization. Works for any software type.
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
