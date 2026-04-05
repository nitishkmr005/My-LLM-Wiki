---
type: source
status: active
created: 2026-04-05
updated: 2026-04-05
tags:
  - source
  - llm-wiki
  - knowledge-management
---

# LLM Wiki Pattern

## Source

- File: [../../llm-wiki.md](../../llm-wiki.md)
- Nature: concept note / design brief

## Summary

The source proposes a pattern for personal or team knowledge systems in which an LLM maintains a persistent wiki instead of relying on one-shot retrieval from raw documents. Raw material remains the source of truth, but the main working layer becomes an interlinked markdown wiki that the LLM continuously updates as new sources arrive and as useful answers are generated.

## Key Ideas

- The wiki should be a persistent artifact that compounds over time.
- New sources should be integrated into existing pages instead of only being indexed for later retrieval.
- Questions answered from the wiki can themselves become durable wiki pages.
- A schema file is required so the LLM behaves like a disciplined maintainer rather than a generic chatbot.
- `index.md` and `log.md` are lightweight but important navigation tools.

## Architecture

- Raw sources: immutable source-of-truth documents.
- Wiki: maintained markdown pages written and updated by the LLM.
- Schema: an instruction file that defines structure and workflow.

## Operational Guidance

- Ingest sources intentionally and update multiple pages in one pass.
- Query the wiki first and only fall back to raw sources when necessary.
- Run periodic lint passes to find contradictions, stale claims, orphan pages, and missing cross-links.

## Implications For This Workspace

- `AGENTS.md` is the schema layer.
- `wiki/index.md` is the catalog layer.
- `wiki/log.md` is the chronological operational record.
- The initial wiki should stay simple until real source volume justifies extra tooling.

## Open Questions

- What subject areas will dominate this wiki first?
- How much metadata should be kept in frontmatter as the wiki grows?
- When will lightweight text search stop being enough?

## Related Pages

- [../topics/persistent-wiki.md](../topics/persistent-wiki.md)
- [../topics/wiki-operations.md](../topics/wiki-operations.md)
- [../home.md](../home.md)

## Sources

- [../../llm-wiki.md](../../llm-wiki.md)
