# Brain v1 Agent Instructions

This repo contains Carson's Brain v1 company-brain proof of concept.

## Primary source of truth

- Work inside `company-brain/` unless the user explicitly asks for repo-level changes.
- Read `company-brain/OPERATING_PROTOCOL.md` before changing brain files.
- For Telegram or natural-language intake, read `company-brain/certainty-review/router-rules.md` before routing updates.

## Safety rules

- Do not invent facts.
- Do not store secrets, passwords, tokens, credentials, private URLs, or sensitive personal data.
- If a message is unclear, ask for clarification or save it to the appropriate inbox instead of guessing.
- Ask before deleting information, restructuring folders, or changing the operating model.

## Git workflow

1. Run `git pull --ff-only` before editing.
2. Make small, focused Markdown changes.
3. Check `git diff` and `git diff --check` before committing.
4. Commit with a clear message when the user wants durable updates.
5. Push after committing unless the user asks for local-only changes.

## Brain profile expectation

Brain v1 should be operated through the dedicated Hermes `brain` profile, not the default Hermes profile. If gateway behavior is relevant, verify that only the brain-profile gateway is connected for this brain workflow.
