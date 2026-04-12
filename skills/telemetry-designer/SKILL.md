---
name: telemetry-designer
description: >
  Use when the user asks how to measure product or feature success, define success metrics,
  pick a north star metric, track KPIs, design analytics events, build an instrumentation
  plan, decide what telemetry to fire, or figure out "how will we know if this is working
  for users" — trigger whenever users say things like "how will we measure success", "what
  KPIs should we track", "design the analytics events for X", "we need a telemetry plan",
  "what events should we fire", "metrics for the launch of X", or "how do we validate this
  worked". Always invoke when defining leading indicators, guard-rail health metrics,
  activation/retention, qualitative feedback plans (NPS, CSAT, in-app surveys), or a
  decision framework tying metrics to actions; this skill produces an implementable
  user-outcome measurement plan with event specs, properties, baselines, targets, and
  response plans. This is strictly for USER-OUTCOME and product analytics — measuring
  whether users are succeeding with the product. Do NOT trigger for engineering or
  operational observability such as p95 latency, error-rate dashboards, SLO/SLI definition
  for infra, APM, log aggregation, Datadog/Prometheus setup, database query tuning,
  performance optimization, generic "add logging" requests, or bug triage — those are
  SRE/observability concerns, not product telemetry. Skip when ux-discover is already
  orchestrating. When a request mixes product metrics and ops metrics, trigger on the
  product-metric portion only.
version: 1.0.0
---

# Telemetry & Success Metrics Designer

If you can't measure it, you can't know if you helped the user.

## Principles

- **Outcome over output** — measure user success, not feature usage
- **Leading indicators** — find signals that predict success before lagging metrics confirm it
- **Privacy-first** — only track what's necessary. No dark patterns. Be explicit about what's tracked.
- **Actionable** — every metric should have a clear "if X, then we do Y" response

## Process

### Step 1: Define Success

Using all prior discovery artifacts, ask:

> "If this project is wildly successful 6 months from now, how would you KNOW? 
> What would be different for users?"

Then ask:

> "What's the ONE metric that, if it moved in the right direction, would prove 
> this was worth building?"

This becomes the **North Star Metric**.

### Step 2: Metric Framework

Build a layered metric structure:

```markdown
## Success Metrics

### North Star Metric
- **Metric**: [what you're measuring]
- **Current baseline**: [today's value, or "unknown — need to establish"]
- **Target**: [6-month goal]
- **Why this metric**: [how it connects to user success]

### Health Metrics (guard rails)
| Metric | Purpose | Target | Alert Threshold |
|--------|---------|--------|-----------------|
| [metric] | [what it guards against] | [target] | [when to worry] |

### Input Metrics (leading indicators)
| Metric | Predicts | Measurement Method |
|--------|----------|-------------------|
| [metric] | [what outcome it predicts] | [how to measure] |
```

### Step 3: Telemetry Events

For each key moment in the user journey, define what to track:

```markdown
## Telemetry Plan

### Event: [event_name]
- **Trigger**: When [user action or system event]
- **Properties**: 
  - [property_name]: [type] — [why we need this]
- **Purpose**: Answers the question: [what question does this data answer?]
- **Privacy**: [PII: yes/no] [Consent required: yes/no]
```

### Step 4: Qualitative Signals

Not everything is quantitative. Define qualitative feedback channels:

```markdown
## Qualitative Feedback Plan

| Signal Type | Collection Method | Frequency | Owner |
|-------------|-------------------|-----------|-------|
| User satisfaction | [NPS, CSAT, in-app survey, etc.] | [cadence] | [who reviews] |
| Feature feedback | [feedback widget, support tickets, etc.] | [ongoing] | [who reviews] |
| Usability issues | [session replay, user testing, etc.] | [cadence] | [who reviews] |
```

### Step 5: Decision Framework

For each key metric, define what actions you'd take:

```markdown
## Metric Response Plan

| Metric | If improving | If flat | If declining |
|--------|-------------|---------|-------------|
| [metric] | [action: scale, invest more] | [action: investigate, iterate] | [action: pivot, diagnose] |
```

## Output

Produce a Telemetry & Metrics section for the UX Discovery Document containing:
1. North Star Metric with baseline and target
2. Health metrics (guard rails)
3. Input metrics (leading indicators)
4. Telemetry event specifications
5. Qualitative feedback plan
6. Decision framework

## Adaptation by Software Type

- **CLI/DevTool**: Focus on task completion time, error rates, adoption curves, time-to-first-success
- **API/SDK**: Focus on integration success rate, time-to-first-call, error rates by endpoint, SDK adoption
- **Web/Mobile App**: Focus on activation, engagement, retention, task success rates
- **Infrastructure**: Focus on reliability, MTTR, deployment frequency, change failure rate
- **Internal Tool**: Focus on adoption, time saved, error reduction, user satisfaction scores
