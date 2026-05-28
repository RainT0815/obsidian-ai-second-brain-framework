# CLAUDE

This vault uses Obsidian as the local knowledge base and an AI coding assistant as the analysis and execution layer.

## Vault Map

- `00-Meta`: identity, system prompts, operating rules.
- `01-Inbox`: unprocessed captures.
- `02-Daily`: daily notes, todo notes, weekly learnings.
- `03-Projects`: active projects with clear outcomes.
- `04-Areas`: long-running life/work domains.
- `05-Resources`: evergreen summaries, concepts, references.
- `06-Templates`: reusable Obsidian templates.
- `07-Archives`: inactive or completed material.
- `08-temp`: temporary drafts and generated artifacts.

## Operating Rules

1. Before making decisions, read `00-Meta/System/context-prompt.md`.
2. For personal operations, use `01-Inbox`, `02-Daily`, `03-Projects`, `04-Areas`, and `05-Resources`.
3. For Karpathy-style wiki work, treat `raw/` as read-only source truth and maintain `wiki/` as the compiled knowledge layer.
4. Put processed summaries into `05-Resources/summary` or `wiki/来源`, depending on whether the user wants a casual note or a maintained wiki source page.
5. Put reusable concepts into `05-Resources/concepts` or `wiki/概念`.
6. Put tasks into `02-Daily/Todo` or the relevant project note.
7. Prefer links over duplicated explanations.
8. When unsure where something belongs, leave it in `01-Inbox` with a short triage note.

## Karpathy Wiki Rules

Read `00-Meta/System/karpathy-wiki-schema.md` before ingesting new sources into `wiki/`.

Key rules:

- `raw/` is user-owned and should not be modified except when explicitly adding new raw sources.
- `wiki/` is AI-maintained and should stay interlinked.
- Every source gets a page in `wiki/来源`.
- Entity/concept/comparison pages should normally be created only after appearing in at least two sources.
- Update `wiki/index.md` and append to `wiki/log.md` after every ingest/query/lint operation.

## Commands

- `/context`: load personal and project context.
- `/todo`: generate or refine today tasks.
- `/weekly-learning`: create a weekly learning report.
- `/summary`: summarize source material into evergreen notes.
- `/lint`: inspect vault health.
- `/ingest`: process one raw source into the maintained wiki.
- `/query-wiki`: answer from the compiled wiki and optionally save the answer.
