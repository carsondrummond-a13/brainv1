# Customer Reviews Notes

Purpose: short working notes and agent directions for the Customer Reviews mock engineering-services test case.

## Notes

- This project is a test case inside the larger Company Brain Prototype.
- All reviews in this project are mock data unless Carson explicitly says otherwise.
- The current test artifact is `customer-reviews.md`.
- The test checks whether agents can convert messy Telegram review updates into structured Markdown entries.
- The test also checks whether agents can categorize feedback by theme without inventing unsupported trends.

## Agent Directions

When a Telegram message contains a mock customer review for engineering services:

1. Decide whether the review is clear enough to route.
2. If clear, add it to `files/customer-reviews.md`.
3. Preserve the original wording as closely as possible.
4. Add light structure: rating, service area, theme, sentiment, possible follow-up, source, and date.
5. Do not claim a trend from one review.
6. If the service area, rating, or meaning is unclear, ask one short clarification before updating structured files.
7. Never store secrets, credentials, private URLs, or real customer personal information.

## Example Clear Update

Telegram message:

> Another person reviewed our mock engineering service three stars and said the analysis was useful but the final report was hard to understand.

Good project entry:

- Rating: 3 stars
- Service Area: Engineering analysis / reporting
- Theme: Report clarity
- Sentiment: Mixed
- Raw Feedback: "The analysis was useful but the final report was hard to understand."
- Possible Follow-up: Review report formatting and executive-summary clarity.

## Example Unclear Update

Telegram message:

> Another customer complained about the same issue again.

Agent response:

> I need one clarification before updating the customer-review project: what issue did the customer complain about?
