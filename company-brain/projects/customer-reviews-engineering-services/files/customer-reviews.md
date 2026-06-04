# Purpose of File

Purpose: this file stores structured mock customer reviews for the mock engineering-services project.

# Customer Reviews

## Agent Usage Rules

- Treat all entries as mock data unless Carson explicitly says otherwise.
- Preserve the raw review wording when possible.
- Add structure around the review so future agents can summarize it.
- Do not invent customer names, project names, ratings, or trends.
- If a review is unclear, ask a clarification before writing to this file.
- Do not store real private customer information, secrets, credentials, or private URLs.

## Review Entry Format

Use this format for new entries:

```markdown
### YYYY-MM-DD — Short Review Label

- Rating: <1–5 stars, or Unknown>
- Service Area: <design review / analysis / prototyping / test planning / consulting / Unknown>
- Theme: <clarity / communication / speed / technical quality / cost / scheduling / other>
- Sentiment: <positive / mixed / negative / unclear>
- Raw Feedback: "<preserved wording>"
- Structured Summary: <one-sentence neutral summary>
- Possible Follow-up: <safe next step or question>
- Source: Telegram update from <person, if known>
- Confidence: <High / Medium / Low>
```

## Mock Reviews

No mock reviews logged yet.

## Theme Summary

Only update this section when the logged reviews actually support the pattern.

- No repeated themes yet.

## Possible Follow-Ups

- Add 3–5 fake reviews through Telegram.
- Include at least one unclear review to test the clarification flow.
- Check whether agents can summarize themes without overclaiming.
