# LLM Wiki Schema

This workspace is a personal LLM-maintained wiki. The agent's job is to keep the wiki coherent, current, and easy to navigate.

## Purpose

- Treat `raw/` as the immutable source layer.
- Treat `wiki/` as the maintained knowledge layer.
- Treat this file as the operating schema for ingest, query, and lint workflows.

## Directory Layout

- `llm-wiki.md`: the seed concept document that inspired this wiki.
- `raw/inbox/`: new source files waiting to be processed.
- `raw/processed/`: optional archive for sources that have already been ingested.
- `raw/assets/`: local images and attachments referenced by raw sources.
- `wiki/home.md`: the main landing page for the wiki.
- `wiki/index.md`: the content catalog. Update it whenever pages are added or materially changed.
- `wiki/log.md`: append-only operational log.
- `wiki/sources/`: one page per source or source bundle.
- `wiki/topics/`: concept, theme, workflow, and synthesis pages.
- `wiki/entities/`: people, companies, books, places, tools, or other named things.
- `wiki/analyses/`: answers to important questions that should persist.
- `wiki/dashboards/`: overview pages, trackers, and curated navigation hubs.
- `templates/`: reusable page skeletons.

## Page Conventions

- Use markdown for every wiki page.
- Prefer lowercase kebab-case filenames.
- Keep pages concise, but make them useful enough that future sessions can build on them.
- Add YAML frontmatter to every wiki page with:
  - `type`
  - `status`
  - `created`
  - `updated`
  - `tags`
- End substantial pages with a `## Sources` section.
- Link related wiki pages with relative markdown links.
- When a claim comes from a source, preserve provenance on the relevant page.

## Source Handling Rules

- Never modify the contents of files in `raw/`.
- If a source lives outside `raw/`, you may still ingest it, but document the path in the source page.
- If the user asks you to ingest a source from `raw/inbox/`, do not delete it after processing.
- Treat local source files as the ground truth when the wiki and source disagree.

## Workflow: Ingest

When the user asks to ingest a source:

1. Read the source file carefully.
2. Create or update a page in `wiki/sources/`.
3. Update any relevant pages in `wiki/topics/`, `wiki/entities/`, `wiki/analyses/`, or `wiki/dashboards/`.
4. Update `wiki/index.md`.
5. Append a new entry to `wiki/log.md`.
6. If the wiki structure is missing something important, extend it minimally and document the change in the log.

Each ingest should capture:

- What the source is.
- The key claims or takeaways.
- Important terminology or entities.
- Open questions, contradictions, and follow-up paths.
- Which existing wiki pages were updated because of this source.

## Workflow: Query

When answering a question:

1. Search `wiki/index.md` first.
2. Read only the pages needed to answer well.
3. Prefer answering from the wiki layer instead of re-reading raw sources unless the wiki is clearly insufficient.
4. If the answer produces durable knowledge, save it as a page in `wiki/analyses/` and add it to the index and log.
5. Cite the relevant wiki pages and source pages in the answer.

## Workflow: Lint

When asked to lint or health-check the wiki, look for:

- Orphan pages with weak navigation.
- Missing backlinks or obvious cross-references.
- Claims that are stale, undersourced, or contradicted by newer material.
- Pages that should be split because they mix too many concerns.
- Important concepts or entities that are mentioned repeatedly but lack their own page.
- Index entries that are missing or outdated.

Document the findings in chat. If the user wants changes applied, update the wiki and record the pass in `wiki/log.md`.

## Writing Standard

- Optimize for future reuse, not for a single chat answer.
- Prefer explicitness over cleverness.
- Keep summaries faithful to the source material.
- Separate observations from inference when the distinction matters.
- Avoid filler. The wiki should read like maintained working notes, not marketing copy.
