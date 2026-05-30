# Decisions

Purpose: record decisions the company should not forget.

## Decision format

```md
### YYYY-MM-DD — Decision title

Decision:

Reason:

Impact:
```

## Decisions

### 2026-05-30 — Use a simpler Company Brain for the POC

Decision:
Use a small Markdown structure instead of the larger full operating-system structure.

Reason:
The proof of concept should be easy for Carson and John to understand and use.

Impact:
The first version focuses on dashboard, log, decisions, people, and projects. More folders can be added later if the workflow proves useful.

### 2026-05-30 — GitHub is durable memory, Telegram is communication

Decision:
Use Telegram for fast interaction with agents and GitHub Markdown files for long-term memory.

Reason:
Telegram is easy for humans to use, while GitHub gives version history and a durable source of truth.

Impact:
Future skills and cron jobs should read from and write to this brain when answering questions or sending updates.
