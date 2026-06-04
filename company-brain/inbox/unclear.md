# Unclear Inbox

Purpose: store unresolved items only after Brain Bot has asked for clarification, sent up to 3 reminders, and still does not have enough certainty to update structured brain files safely.

This is not the first stop for uncertainty. Brain Bot should ask in Telegram first.

## Unresolved Items

No unresolved items yet.

## Entry format

```md
### YYYY-MM-DD — Short title

Status: Needs clarification
Source: Telegram
From: Name or chat
Original message:
> Original Telegram message or concise summary.

Uncertainty:
- What was unclear.

Clarifying question asked:
> Exact question Brain Bot asked.

Reminder history:
- First asked: YYYY-MM-DD HH:MM
- Reminder 1: YYYY-MM-DD HH:MM
- Reminder 2: YYYY-MM-DD HH:MM
- Reminder 3: YYYY-MM-DD HH:MM

Reason not pushed:
- Brain Bot did not have enough certainty to make factual changes safely.

Suggested next action:
- Human should answer the clarification question, then Brain Bot can update the correct files.
```

## End-of-day review

A future EOD cron job should scan this file and summarize the day's unresolved uncertainties.
