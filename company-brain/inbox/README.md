# Inbox

Purpose: capture raw Telegram updates that may belong in the Company Brain before they are organized into project files, logs, decisions, tasks, or dashboards.

## Why this exists

Telegram is the conversation stream. The Company Brain is durable memory.

Not every Telegram message should be saved here. Use the inbox for messages that are intentionally meant to become company memory, especially when the correct destination is not obvious yet.

## When to write to the inbox

Add an inbox entry when a message starts with or clearly means one of these:

- `Log this:`
- `Brain note:`
- `Project update:`
- `Task:`
- `Decision:`
- `Remember for the brain:`

Do not automatically append every Telegram message. Questions, debugging chatter, corrections, secrets, credentials, and casual conversation should stay out of GitHub unless the human explicitly asks to save them.

## Routing guide

After capture, an agent should later process entries into the right durable file:

- Project-specific facts -> `projects/<project>/README.md` or notes files
- Chronological history -> `log.md`
- Durable decisions -> `decisions.md`
- Current priorities or blockers -> `dashboard.md`
- Person-specific context -> `people/<name>.md`
- Tasks -> future `tasks.md` or the relevant project file

## Inbox files

- `carson.md` — raw updates from Carson.
- `john.md` — raw updates from John.

## Entry format

```md
### YYYY-MM-DD — Short title

Source: Telegram
From: Name
Status: Unprocessed | Processed
Type: Raw update | Task | Decision | Project update | Question
Related project: Project name, or `Unknown`

Message:
> Original or lightly cleaned message text.

Agent notes:
- Where this likely belongs.
- Any follow-up questions.

Processed into:
- Not processed yet.
```

## Processing rule

When an entry has been moved into the right durable files, update `Status` to `Processed` and list the destination under `Processed into`.
