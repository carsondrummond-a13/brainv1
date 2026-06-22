# Future Architecture

This file captures ideas inspired by mature brain systems such as GBrain, without requiring Brain v1 to become complex too early.

## What Brain v1 does now

Brain v1 is a simple, inspectable company-brain proof of concept.

Current strengths:

- Uses Markdown files as the durable company memory.
- Uses GitHub for version history and reviewability.
- Treats Telegram as the communication and intake surface.
- Gives agents clear routing rules through `OPERATING_PROTOCOL.md` and `certainty-review/router-rules.md`.
- Separates clear updates from uncertain updates.
- Sends unresolved or unclear information to the inbox instead of guessing.
- Keeps the system easy for humans to read, debug, and trust.

The current goal is not to be a fully automated company brain. The goal is to prove the workflow:

```text
message or update
→ agent interprets it
→ agent routes it safely
→ Markdown files are updated
→ GitHub preserves history
→ humans can inspect what happened
```

## What GBrain-like features might be added later

GBrain shows what a more mature brain system can grow into. These are possible future directions, not immediate requirements.

Potential future features:

- Search across all brain files instead of manually opening Markdown pages.
- Synthesized answers with citations back to source files.
- Gap analysis that says what the brain does not know yet.
- Contradiction detection between old and new information.
- Source attribution for every important claim.
- Multiple data sources, such as Telegram, email, meeting notes, Drive folders, GitHub issues, and docs.
- User or team permissions so different people can only access the right information.
- Scheduled agents that summarize progress, detect stale projects, and surface unresolved questions.
- A retrieval layer, such as GBrain, that indexes the Markdown repo and helps agents answer questions more intelligently.
- A migration workflow for importing messy historical company data into structured brain files.

A likely future architecture could be:

```text
Markdown/GitHub brain
→ indexed by retrieval system
→ queried by agents
→ answers include citations, uncertainty, and gaps
→ safe updates return to Markdown through reviewed agent workflows
```

In that model, Brain v1 remains the human-readable source of truth, while a tool like GBrain becomes the search and reasoning layer on top.

## What not to add yet

Do not add complexity before the simple workflow is proven.

Avoid adding too early:

- Large database systems before Markdown becomes painful.
- Complex permission systems before there are real users with different access needs.
- Fully autonomous agents that update important records without review.
- Broad data ingestion from many sources before one or two sources work reliably.
- Fancy dashboards before the underlying files are consistently maintained.
- Automated deletion, restructuring, or overwriting of brain content.
- Claims that Telegram messages are saved permanently unless the agent confirms a file update and commit.

The guiding rule:

Build the smallest reliable workflow first. Add infrastructure only when a real failure mode appears.

## Open questions about permissions, search, and ingestion

These questions should be answered before Brain v1 becomes a real company system.

### Permissions

- Who is allowed to read each part of the brain?
- Who is allowed to write updates?
- Which files should require human approval before changes become official?
- Should mock projects and real projects live in separate folders?
- How should sensitive information be excluded from the brain entirely?

### Search and retrieval

- Is basic file search enough for now?
- When does the brain need semantic search or embeddings?
- Should answers cite exact files and lines?
- How should the system handle stale, conflicting, or low-confidence information?
- Should GBrain or a similar tool index this repo later?

### Ingestion

- Which input sources matter first: Telegram, GitHub, meeting notes, email, Drive, or something else?
- Should raw imports be kept separate from trusted brain files?
- What confidence level is required before an agent updates a structured project or person file?
- What should happen when imported history contains contradictions?
- Who reviews uncertain historical facts before they become company memory?

## Near-term recommendation

Keep Brain v1 simple for now.

The next useful improvements are:

1. Maintain the current Markdown structure consistently.
2. Make every agent update traceable through Git commits.
3. Require citations or source notes for important claims.
4. Keep uncertainty handling strict: ask, defer, or use the inbox instead of guessing.
5. Treat GBrain as a reference architecture until Brain v1 needs stronger search, retrieval, or multi-user permissions.
