# Pending Clarifications

Purpose: track clarification questions Brain Bot has asked but not yet resolved.

Brain Bot should check this file before sending reminders or deciding whether an uncertainty should move to `../inbox/unclear.md`.

## Active Clarifications

No active clarifications.

## Entry format

```md
### YYYY-MM-DD HH:MM — Short title

Status: Waiting for response | Resolved | Moved to inbox
Asked by: Brain Bot
Asked to: Name or chat
Original message:
> Original Telegram message or concise summary.

Uncertainty:
- What Brain Bot does not know yet.

Clarifying question sent:
> The exact question sent to the user.

Reminder count: 0
First asked: YYYY-MM-DD HH:MM
Last reminder: None
Next reminder due: YYYY-MM-DD HH:MM

Do not update yet:
- Files that are intentionally not changed until this is resolved.

Resolution:
- Not resolved yet.
```

## Reminder policy

- Reminder interval: every 12 hours.
- Maximum reminders: 3.
- After 3 unanswered reminders, move the item to `../inbox/unclear.md`.
- Do not push structured brain changes while the clarification is unresolved.
