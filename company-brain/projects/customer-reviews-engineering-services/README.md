# Customer Reviews: Mock Engineering Services

## Summary

Customer Reviews is a test case inside the larger Company Brain Prototype. It is not a real business project.

The goal of this project is to validate whether agents can receive messy mock customer review updates from Telegram, classify them safely, and preserve them in a consistent project structure without inventing patterns or facts.

This project focuses on fake reviews for mock engineering services, such as design reviews, analysis work, prototyping support, test planning, and technical consulting.

## Status

In progress

## Owner

Carson

## Team

- Carson
- John

## Responsibilities

- Carson: owns the test case and decides whether the customer-review structure is easy to understand.
- John: supports through testing, feedback, and mock customer-review input.
- Future agents: use this project as the source of truth for mock engineering-services customer feedback.

## Current Priorities

- Keep customer reviews clearly labeled as mock data.
- Verify that agents can turn casual Telegram updates into structured review entries.
- Verify that agents can categorize feedback by theme without overclaiming trends.
- Verify that agents ask clarifying questions when the review, rating, customer type, or service area is unclear.
- Preserve raw review wording while adding useful structure around it.

## Open Tasks

- [ ] Carson: send several fake customer reviews through Telegram to test routing.
- [ ] John: send one unclear or incomplete mock review to test the clarification flow.
- [ ] Agent: add clear reviews to `files/customer-reviews.md` using the project directions.
- [ ] Agent: update theme counts only when enough reviews support a pattern.
- [ ] Agent: ask before treating one review as a company-wide trend.

## Deadlines

No deadline currently.

## Important Files

- `files/customer-reviews.md` — structured mock customer-review log for engineering-services feedback.
- `files/project-notes.md` — short working notes and agent directions for this test case.

## Recent Updates

- 2026-06-04 — Customer Reviews project created as a second infrastructure test case for the Company Brain Prototype.

## Decisions

- 2026-06-04 — Use this project to test review intake, theme categorization, clarification behavior, and safe trend detection for mock engineering-services feedback.
- 2026-06-04 — Keep the folder architecture similar to Project A so future agents have a predictable project pattern.

## Open Questions

- Which fake engineering service categories should be tested first?
- Should review ratings use a 1–5 star scale for every mock review?
- How many repeated reviews are enough before the dashboard should mention a possible trend?

## Blockers

- No blockers currently.
- More mock Telegram reviews are needed before agents can test categorization and trend summaries.

## Last Updated

2026-06-04 by Hermes Agent via Carson.

## Confidence / Source

Confirmed by Carson in chat:

- Carson wants a mock customer-review project for engineering services.
- The project should live under `company-brain/projects/`.
- The folder architecture should match the existing project style so future agents are not confused.
- The purpose is infrastructure testing, not real business use.
