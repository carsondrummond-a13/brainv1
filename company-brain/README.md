# Company Brain POC

This is a simple proof-of-concept Company Brain for Carson and John.

## TL;DR

- Telegram is where Carson and John talk to agents.
- GitHub is where the durable company memory lives.
- Markdown files are the simple database.
- Future skills and cron jobs will do the heavy lifting automatically.

## The basic loop

1. Carson or John sends an update or question through Telegram.
2. An agent reads or updates these Markdown files.
3. GitHub keeps the long-term memory and version history.
4. Cron jobs can send scheduled summaries, reminders, or project updates.

## Simple folder structure

```text
company-brain/
  README.md
  OPERATING_PROTOCOL.md
  dashboard.md
  log.md
  decisions.md
  people/
    carson.md
    john.md
  projects/
    prototype.md
```

## What each file is for

- `dashboard.md`: what is happening right now.
- `log.md`: chronological record of important updates.
- `decisions.md`: decisions the company should not forget.
- `people/`: useful context about Carson and John.
- `projects/`: project-specific details and history.

## Example future questions this should support

- "What projects has John worked on?"
- "What changed this week?"
- "What decisions did we make about the prototype?"
- "What is Carson waiting on?"
- "Send John a project update."

## Prototype principle

Keep this simple until the workflow is proven.

Add new folders only when the current files become painful to use.
