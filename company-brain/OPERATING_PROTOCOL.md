# Company Brain Operating Protocol

These are the rules for humans and Hermes agents using the Company Brain.

## Core Model

- Telegram is for communication.
- GitHub is for memory.
- Markdown files are the operating system.
- Dashboards are for current state.
- Logs are for history.

## Agent Rules

1. Pull before writing if using git locally.
2. Read relevant context before changing files.
3. Do not invent facts.
4. Do not store secrets, passwords, tokens, private keys, or credentials.
5. Commit changes with clear messages.
6. Ask before deleting, restructuring, renaming major folders, or making major company decisions.
7. Route updates to the right inbox, outbox, or updates folder.
8. Update dashboards when priorities, blockers, tasks, ownership, or decisions change.
9. Record durable decisions in `decisions/decision-log.md`.
10. Prefer small, reviewable changes over large rewrites.

## Communication Rules

- Telegram messages are useful for fast coordination, but important information should be preserved in GitHub.
- If a Telegram conversation creates a task, record it in `tasks/active.md` or `tasks/backlog.md`.
- If a Telegram conversation creates a decision, record it in `decisions/decision-log.md`.
- If a Telegram conversation changes project state, update the relevant project file and dashboard.

## Memory Rules

- Current state belongs in dashboards.
- Historical records belong in logs.
- Project-specific details belong in projects.
- Person-specific stable context belongs in people.
- Decisions belong in the decision log.
- Inbox items should be actionable.
- Outbox items should be ready to review or send.

## Safety Rules

- Never commit secrets.
- Never guess a person's preference or decision. Mark unknowns as `Unknown`.
- Ask before deleting information.
- Ask before archiving active material.
- Clearly label examples, assumptions, and draft content.

## Git Workflow

When working locally:

1. Run `git pull --ff-only` before changes.
2. Make the smallest useful update.
3. Review changed files.
4. Commit with a clear message.
5. Push when the user asks or when the workflow expects GitHub to be updated.

## Example Agent Flow

A human says in Telegram: "Tell Partner the Stripe review is blocking Website Launch."

The agent should:

1. Add or update the task in `tasks/active.md`.
2. Add a routed update in `updates/carson-to-partner/` or draft a message in `outbox/partner/`.
3. Update `dashboards/company.md` and any relevant personal dashboard.
4. If this becomes a durable decision, add it to `decisions/decision-log.md`.
5. Commit the changes.
