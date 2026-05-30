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
10. If something belongs in long-term memory, write it here instead of leaving it only in chat.

## Where agents should write things

- Current status or priorities: `dashboard.md`
- Chronological updates: `log.md`
- Durable decisions: `decisions.md`
- Context about Carson: `people/carson.md`
- Context about John: `people/john.md`
- Project-specific details: a file inside `projects/`

## Future agent behavior

Future skills can use this brain to:

- answer questions about company history
- summarize weekly progress
- send scheduled cron updates
- route project updates to Carson or John over Telegram
- identify what each person has worked on
- keep project records organized without humans manually maintaining every file

## Human review rule

For now, agents should make small, understandable changes. If a change deletes information, restructures the brain, or changes the operating model, ask for human approval first.
