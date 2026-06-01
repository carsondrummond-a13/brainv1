# BrainV1 Agent Onboarding

Last updated: 2026-06-01

## Purpose

BrainV1 is a proof-of-concept company brain. It is designed to test whether people can use Telegram to communicate with AI agents while GitHub Markdown files preserve useful company memory over time.

The goal is not to build a complex system yet. The goal is to prove this simple loop:

```text
Telegram message → agent reads/writes Markdown → GitHub preserves memory → future agents can answer, summarize, and route updates
```

## Core Mental Model

```text
Telegram = fast human communication
Hermes / agents = workers that read, update, summarize, and route information
GitHub = durable source of truth and version history
Markdown = simple human-readable database
```

## Where to Start

When an agent is pointed at this repo, start here:

1. Read this file: `BrainV1.md`
2. Read the operating protocol: `company-brain/OPERATING_PROTOCOL.md`
3. Read the current dashboard: `company-brain/dashboard.md`
4. Read the relevant person or project file before answering or editing
5. Pull latest changes before editing locally
6. Make small, clear Markdown updates
7. Do not invent facts
8. Do not store secrets

## Repository Structure

```text
brainv1/
  BrainV1.md
  company-brain/
    README.md
    OPERATING_PROTOCOL.md
    dashboard.md
    log.md
    decisions.md
    people/
      carson.md
      john.md
    projects/
      prototype.md
      project-a/
        README.md
        files/
          project-notes.md
          example-reference.md
```

## What Each Area Is For

- `BrainV1.md`: onboarding document for AI agents and humans new to the repo.
- `company-brain/README.md`: plain-English overview of the company brain proof of concept.
- `company-brain/OPERATING_PROTOCOL.md`: rules for how agents should navigate, read, and edit this brain.
- `company-brain/dashboard.md`: current state, priorities, blockers, waiting items, and open questions.
- `company-brain/log.md`: chronological history of meaningful updates.
- `company-brain/decisions.md`: durable decisions and why they were made.
- `company-brain/people/`: context about people, their roles, work, and responsibilities.
- `company-brain/projects/`: project-specific memory, status, tasks, files, updates, and questions.

## Agent Rules

Follow these rules when working in this repo:

1. Treat GitHub + Markdown as the source of truth.
2. Pull latest changes before editing if working locally.
3. Read before writing.
4. Keep updates small and understandable.
5. Do not delete, rewrite, or restructure major content without human approval.
6. Do not invent facts, roles, decisions, deadlines, or project history.
7. Clearly mark examples or mock data as `[Example]` when adding any.
8. Never store secrets, passwords, API keys, tokens, private URLs, or credentials.
9. Keep dashboards current; keep logs chronological.
10. Record durable decisions in `company-brain/decisions.md`, not only in chat.
11. When uncertain, state uncertainty and ask a clarifying question.
12. Prefer simple Markdown over complex systems until the proof of concept is proven.

## How to Update Information

### If someone gives a general company update

Update:

1. `company-brain/log.md` with a dated chronological entry
2. `company-brain/dashboard.md` if the current state changed
3. Relevant people or project files if the update affects them

### If someone gives a project update

Update:

1. The relevant project file under `company-brain/projects/`
2. `company-brain/dashboard.md` if priorities, blockers, or active projects changed
3. `company-brain/log.md` with a short dated entry
4. `company-brain/decisions.md` if the update includes a durable decision

### If someone asks a question

Before answering:

1. Read this file and the operating protocol if needed
2. Read the relevant dashboard, people, project, log, or decision files
3. Answer from repo evidence
4. Mention which files informed the answer when useful
5. If the repo does not contain enough information, say so clearly

### If someone makes a decision

Update:

1. `company-brain/decisions.md`
2. Any related project file
3. `company-brain/log.md`

Decision entries should include:

```text
Date:
Decision:
Context:
Reason:
Impact:
Source:
```

### If someone creates a new project

Create a new folder or file under `company-brain/projects/`.

For a project folder, prefer:

```text
company-brain/projects/project-name/
  README.md
  files/
```

A project `README.md` should include:

- Summary
- Status
- Owner
- Team
- Responsibilities
- Current priorities
- Open tasks
- Deadlines, or `No deadline currently.`
- Important files
- Recent updates
- Decisions
- Open questions
- Blockers
- Last updated
- Confidence / source

## Current Known Prototype Context

- This repo is a mock setup of a company brain.
- Carson and John are the initial people in the proof of concept.
- Project A is the first example project for setting up and testing the brain.
- The system is intentionally simple for now.
- Telegram is the intended communication layer.
- GitHub Markdown is the intended durable memory layer.
- Future skills and cron jobs may automate summaries, routing, and project updates.

## How to Think About Skills

Skills are not company memory. Skills are repeatable procedures agents can follow.

Company facts belong in:

```text
company-brain/dashboard.md
company-brain/log.md
company-brain/decisions.md
company-brain/people/
company-brain/projects/
```

Agent procedures belong in skills, such as:

```text
answer-from-brain
update-project-status
record-decision
route-telegram-update
summarize-daily-log
prepare-weekly-brief
```

A good skill answers:

```text
When this kind of task appears, what repeatable process should the agent follow?
```

## Suggested Agent Workflow

Use this workflow for most tasks:

1. Identify the request type: question, update, decision, project change, or routing task.
2. Read the relevant source files.
3. Make the smallest useful change.
4. Preserve historical context instead of overwriting it.
5. Update dashboard/log/decisions when relevant.
6. Run a quick check before finishing.
7. Summarize what changed and what still needs human input.

## Verification Checklist Before Finishing

Before reporting success, verify:

- The relevant Markdown file exists.
- The update went into the right place.
- No secrets were added.
- No important old context was deleted.
- Markdown is readable.
- `git diff --check` passes if working locally.
- The final summary names the files changed.

Useful local commands:

```bash
git status --short --branch
git diff --check
git diff -- BrainV1.md company-brain/
```

## Human Approval Required For

Ask before doing any of these:

- Deleting files or major sections
- Restructuring the repo
- Renaming people, projects, or folders
- Changing the operating model
- Adding sensitive company data
- Committing or pushing if the human did not ask for it

## Good Answer Style for Agents

When answering from this brain, prefer:

```text
Short answer:
What I checked:
What it means:
Files changed, if any:
Open questions / next step:
```

Keep answers concise and practical.

## Current Design Principle

Keep BrainV1 boring, readable, and useful.

Do not overbuild the system before the core workflow is proven.
