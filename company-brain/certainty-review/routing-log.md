# Routing Log

Purpose: provide an audit trail of Brain Bot's routing decisions.

Use this file to record what the bot did with important Telegram messages, especially when it changed files, asked for clarification, or deferred an item.

## Entries

No routing entries yet.

## Entry format

```md
### YYYY-MM-DD HH:MM — Short title

Source: Telegram
From: Name or chat
Confidence: High | Medium | Low
Action: Updated files | Asked clarification | Ignored casual chat | Moved to inbox

Original message:
> Original Telegram message or concise summary.

Reasoning:
- Why Brain Bot chose this action.

Files changed:
- None, or list changed files.

Clarification asked:
- None, or exact question.

Commit:
- None, or commit hash.
```

## Logging rules

- Log every pushed change.
- Log every clarification question.
- Log every item moved to `../inbox/unclear.md`.
- Do not log casual messages that are clearly not meant for the brain.
- Never store secrets or credentials here.
