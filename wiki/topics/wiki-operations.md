---
type: topic
status: active
created: 2026-04-05
updated: 2026-04-05
tags:
  - topic
  - workflow
  - ingest
  - query
  - lint
---

# Wiki Operations

## Ingest

The ingest workflow takes a raw source and turns it into maintained wiki knowledge.

### Minimum actions

1. Read the source.
2. Create or update a source page in `wiki/sources/`.
3. Update any relevant topic, entity, dashboard, or analysis pages.
4. Update [../index.md](../index.md).
5. Append an entry to [../log.md](../log.md).

### Expected output

- A source summary page with provenance.
- Cross-links to affected topic pages.
- New pages only when they improve long-term organization.

## Query

The query workflow should search the wiki first. The goal is to answer from the maintained knowledge layer whenever possible.

### Rule of thumb

- Read [../index.md](../index.md) first.
- Open only the pages required for the question.
- Cite the pages that support the answer.
- If the answer will likely matter later, save it to `wiki/analyses/`.

## Lint

The lint workflow checks the health of the wiki.

### Things to look for

- Orphan pages.
- Missing backlinks and weak navigation.
- Repeated mentions of concepts without dedicated pages.
- Claims that newer sources weaken or overturn.
- Gaps where another source would materially improve understanding.

## Workflow Philosophy

The point is not to create the most pages. The point is to keep the wiki useful, navigable, and cumulative. Every update should improve retrieval, synthesis, or future thinking.

## Related Pages

- [persistent-wiki.md](persistent-wiki.md)
- [../sources/llm-wiki-pattern.md](../sources/llm-wiki-pattern.md)
- [../home.md](../home.md)

## Sources

- [../sources/llm-wiki-pattern.md](../sources/llm-wiki-pattern.md)
- [../../llm-wiki.md](../../llm-wiki.md)
