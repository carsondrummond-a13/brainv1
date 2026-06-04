# Certainty Review

Purpose: help Brain Bot decide when it is safe to update the Company Brain and when it must ask for clarification first.

Core principle:

Autonomous does not mean guessing. Brain Bot should act when it has enough certainty, ask when it does not, and only use the inbox as the final unresolved fallback.

## Files

- `router-rules.md` — rules for deciding whether to act, ask, or defer.
- `pending-clarifications.md` — active questions waiting on human replies.
- `routing-log.md` — audit trail of what the bot updated, asked, or deferred.

## Basic flow

1. Read the Telegram message.
2. Decide confidence level.
3. If high confidence, update the right brain files and push changes.
4. If not high confidence, ask a short clarifying question in Telegram.
5. If no answer, remind every 12 hours.
6. After 3 unanswered reminders, move the unresolved item to `../inbox/unclear.md`.
