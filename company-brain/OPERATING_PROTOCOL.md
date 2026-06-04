# Operating Protocol

This file tells agents how to use the Company Brain.

## Core rules

1. Telegram is for communication.
2. GitHub is for durable memory.
3. Markdown files are the company operating system.
4. Do not invent facts.
5. Do not store secrets, passwords, tokens, or private credentials.
6. Pull latest changes before editing locally.
7. Commit changes with clear messages.
8. Ask before deleting major information or restructuring the brain.
9. Prefer simple updates over complicated systems.
10. If something belongs in long-term memory and is clear, write it here instead of leaving it only in chat.
11. Use `certainty-review/router-rules.md` before routing Telegram updates.

## Truth-first routing rule

Brain Bot should be autonomous, but not reckless.

- If the message is clear, update the correct files, commit, push, and confirm.
- If the message is unclear, ask a short clarifying question in Telegram.
- If there is no sufficient answer, remind every 12 hours.
- After 3 unanswered reminders, move the unresolved item to `inbox/unclear.md`.
- Do not push structured brain changes while the meaning is uncertain.

## Where agents should write things

- Routing rules and pending questions: `certainty-review/`
- Current status or priorities: `dashboard.md`
- Chronological updates: `log.md`
- Durable decisions: `decisions.md`
- Context about Carson: `people/carson.md`
- Context about John: `people/john.md`
- Project-specific details: a file inside `projects/`
- Unresolved items after clarification attempts: `inbox/unclear.md`
- Raw person-specific notes, when explicitly requested: `inbox/carson.md` or `inbox/john.md`

## Future agent behavior

Future skills can use this brain to:

- answer questions about company history
- summarize weekly progress
- send scheduled cron updates
- ask clarification when uncertain
- remind users about unresolved clarifications
- identify what each person has worked on
- keep project records organized without humans manually maintaining every file

## Human review rule

Agents may make small, clear, factual updates. If a change deletes information, restructures the brain, changes the operating model, or relies on uncertain facts, ask for human approval first.
