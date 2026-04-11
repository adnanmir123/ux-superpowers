---
name: research-intake
description: >
  Use when the user provides raw research data — interview transcripts, survey results,
  support tickets, analytics screenshots, NPS feedback, app reviews, usability test notes,
  customer call recordings (transcribed), forum posts, or any other user signal. Processes
  and synthesizes raw data into structured insights that feed into persona building,
  JTBD, and journey mapping. Accepts data in any format.
version: 1.0.0
---

# Research Intake — Processing Raw User Data

Transform messy real-world data into structured insights.

## Accepted Data Types

This skill processes ANY user data the user provides. Common types:

- Interview transcripts (pasted text, uploaded files)
- Survey results (CSV, pasted responses, summaries)
- Support tickets / bug reports
- App store reviews / NPS verbatims
- Analytics data (pasted numbers, screenshots described)
- Usability test notes
- Sales call notes
- Forum/community posts
- Customer emails or chat logs
- Competitive analysis notes

## Processing Flow

### Step 1: Receive Data

When the user provides data, acknowledge what you received and classify it:

> "I see you've shared [type of data]. Let me analyze this for patterns. 
> Is there anything specific you want me to look for, or should I do an open analysis?"

### Step 2: Extract Signals

For each data source, extract:

```markdown
## Data Source: [type and brief description]

### Key Themes (frequency-ranked)
1. **[Theme]** — mentioned [N] times
   - Supporting evidence: [direct observations, not quotes]
   
### User Pain Points
- [specific, actionable pain points with severity]

### Unmet Needs
- [things users want but don't have]

### Positive Signals
- [things users value about current solutions — preserve these]

### Behavioral Patterns
- [how users actually behave, especially if different from expectations]

### Surprising Findings
- [anything unexpected or counter-intuitive]
```

### Step 3: Cross-Reference

If multiple data sources are provided, identify:

- **Converging signals**: Themes that appear across multiple sources (high confidence)
- **Diverging signals**: Contradictions between sources (needs investigation)
- **Gaps**: Important questions that NO data source answers

### Step 4: Confidence Assessment

```markdown
## Research Confidence Assessment

| Insight | Data Sources | Sample Size | Confidence | Action |
|---------|-------------|-------------|------------|--------|
| [insight] | [which sources] | [how much data] | High/Med/Low | [use as-is / validate further / treat as hypothesis] |
```

### Step 5: Feed Forward

Present the synthesis and ask:

> "Here's what I'm seeing in the data. Should I use these insights to build personas,
> or do you want to adjust anything first?"

Structured insights from this skill feed directly into:
- `persona-builder` — behavioral patterns become persona foundations
- `jobs-to-be-done` — unmet needs become job statements  
- `user-journey` — pain points map to journey phases
- `telemetry-designer` — themes suggest what to measure

## Rules

- **Don't invent data** — if the sample is small, say so. Don't over-generalize from 3 data points.
- **Distinguish observation from interpretation** — "5 users said X" is observation. "Users hate X" is interpretation. Label both.
- **Preserve nuance** — don't flatten contradictions. Surface them.
- **Ask about context** — "When was this data collected? Has anything changed since?"
- **Respect privacy** — if data contains PII, note it and suggest anonymization
