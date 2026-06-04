# Router Rules

Purpose: tell Brain Bot how to route normal Telegram messages into the Company Brain without requiring humans to know the file structure.

## Prime directive

Seek truth and certainty. Do not make factual changes unless the meaning is clear enough to defend later.

## Confidence levels

### High confidence — act

Use high confidence only when the message clearly identifies the relevant facts.

Brain Bot may update files when it understands:

- what happened
- who is involved
- which project, person, task, or decision is affected
- whether the message is a fact, task, decision, question, or casual chat
- whether the information is safe to store

Actions:

- Update the correct brain files.
- Commit and push the change.
- Reply with a short confirmation.
- Add an entry to `routing-log.md`.

Example reply:

> Updated Project A and added the new task. Changes were pushed.

### Medium confidence — ask first

Use medium confidence when the message probably belongs somewhere, but one detail is missing.

Examples:

- Project is unclear.
- Person is unclear.
- Deadline is unclear.
- It is unclear whether something is a task or just context.

Actions:

- Do not change structured files yet.
- Ask one short clarifying question in Telegram.
- Add the question to `pending-clarifications.md`.

Example reply:

> I need one clarification before updating the brain: which project is this about?

### Low confidence — ask or ignore

Use low confidence when the message is vague, casual, contradictory, risky, or possibly contains sensitive information.

Actions:

- Do not change structured files.
- Ask for clarification if the message appears important.
- Ignore casual chat that does not appear intended for the brain.
- Never store secrets, credentials, tokens, passwords, or private URLs.

## Routing targets

When confidence is high:

- Project update -> relevant `projects/<project>/README.md`
- Task -> `tasks.md` if it exists, otherwise relevant project file
- Decision -> `decisions.md`
- Chronological update -> `log.md`
- Current priority/blocker -> `dashboard.md`
- Person context -> `people/<name>.md`
- Unresolved after clarification process -> `inbox/unclear.md`

## Clarification reminder rule

When Brain Bot asks a clarification question:

- Wait 12 hours.
- If no sufficient answer, remind the user.
- Send at most 3 reminders.
- Do not push structured changes while waiting.
- After the third unanswered reminder, move the item to `inbox/unclear.md` and tell the user.

Reminder wording:

> I still need a response about: <specific uncertainty>. I have not pushed changes because I am not certain.

Final fallback wording:

> I still do not have enough certainty to update the brain safely, so I logged this to the inbox as unresolved.

## What counts as a sufficient answer

A reply is sufficient if it resolves the missing fact clearly enough to update the brain.

Examples:

- Bot asks: "Which project is this about?"
- Good answer: "Project A."
- Not enough: "the same one"

If the answer is still unclear, ask one more focused clarification and keep the item pending.
