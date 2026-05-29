# Company Brain

Company Brain is a shared company memory and lightweight operating system for a two-person company.

The purpose is simple:

- GitHub is the durable source of truth.
- Telegram is the communication layer.
- Markdown files are the structured memory format.
- Hermes agents help route messages, update dashboards, preserve decisions, and keep history organized.

This is an initial mockup for Carson and `partner`. Replace `partner` with the real partner name when known.

## Folder Structure

| Folder | Purpose |
| --- | --- |
| `dashboards/` | Current state, priorities, blockers, and decisions needed. |
| `people/` | Stable context about each person, their role, preferences, and responsibilities. |
| `projects/` | Project-specific memory using a reusable template. |
| `tasks/` | Cross-company active, backlog, and completed tasks. |
| `decisions/` | Durable decision history. |
| `meetings/` | Meeting notes and summaries. |
| `updates/` | Routed updates between people or to the whole company. |
| `inbox/` | Items needing a specific person's attention. |
| `outbox/` | Drafted or prepared messages to send to a person. |
| `logs/` | Chronological daily and weekly records. |
| `archive/` | Old, inactive, or superseded material. |

## How Hermes Agents Should Use This

1. Pull the latest repo state before writing.
2. Read the relevant dashboard, person file, project files, and inbox before acting.
3. Do not invent facts. If something is uncertain, label it clearly as unknown or ask for clarification.
4. Write durable company memory to Markdown files, not only to chat.
5. Update dashboards when priorities, blockers, tasks, or decisions change.
6. Record durable decisions in `decisions/decision-log.md`.
7. Route messages through the right `updates/`, `inbox/`, or `outbox/` folder.
8. Commit changes with clear messages.

## How Humans Should Use This

- Use dashboards to quickly see what matters right now.
- Use inbox folders for things needing attention.
- Use outbox folders for messages prepared by agents before they are sent through Telegram.
- Use project folders for detailed project memory.
- Use logs for history, not current priorities.
- Use the decision log when the company makes choices that should not be lost.

## What Counts as Loggable Information

Good things to log:

- A meaningful task was completed.
- A blocker appeared or was resolved.
- A customer, vendor, or teammate gave important feedback.
- A project changed phase.
- A decision was made.
- A recurring process changed.
- A Telegram update contains information that should be preserved.

Do not log:

- Secrets, passwords, API keys, tokens, private credentials, or sensitive personal data.
- Random chatter with no future value.
- Guesses stated as facts.

## Routing Between Carson and Partner

Use these routes:

- Carson to Partner: `updates/carson-to-partner/`
- Partner to Carson: `updates/partner-to-carson/`
- Company-wide: `updates/company-wide/`
- Needs Carson attention: `inbox/carson/`
- Needs Partner attention: `inbox/partner/`
- Prepared message for Carson: `outbox/carson/`
- Prepared message for Partner: `outbox/partner/`

Example: if Carson asks an agent to brief Partner about a blocker, the agent should draft the message in `outbox/partner/`, optionally record the routed update in `updates/carson-to-partner/`, and update relevant dashboards.

## Example Content

This mockup includes light example content such as:

- Example project: Website Launch
- Example task: Review Stripe integration
- Example decision: Use GitHub as durable company memory
- Example routed update from Carson to Partner

Example content is clearly labeled and should be replaced as the real company system develops.
