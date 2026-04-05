---
type: topic
status: active
created: 2026-04-05
updated: 2026-04-05
tags:
  - topic
  - persistent-knowledge
  - llm-wiki
---

# Persistent Wiki

## Claim

A maintained wiki is more valuable than repeated one-shot retrieval because the synthesis work is preserved and improved over time.

## Why it matters

In a standard RAG flow, the system repeatedly rediscovers the same information from raw documents. A persistent wiki shifts that work upfront. The LLM extracts, organizes, cross-links, and revises knowledge once, then future questions can build on a richer intermediate layer instead of starting from raw fragments every time.

## Working Principles

- Knowledge should accumulate.
- Cross-references should be explicit.
- Contradictions should be surfaced, not hidden.
- Useful answers should become durable pages.
- The wiki should reflect the current state of understanding, not just a pile of notes.

## Benefits

- Faster future synthesis.
- Better continuity across sessions.
- Easier navigation for a human reader.
- Lower maintenance burden than a hand-maintained wiki.

## Risks

- The wiki can drift from source truth if provenance is weak.
- Poor schema discipline can turn the wiki into an unstructured note dump.
- Over-automation can create noisy pages with low long-term value.

## Design Response In This Workspace

- Raw sources stay separate in `raw/`.
- The agent uses `AGENTS.md` to maintain consistent behavior.
- Every durable page should expose its sources.
- The index and log make the wiki navigable without extra infrastructure.

## Related Pages

- [wiki-operations.md](wiki-operations.md)
- [../sources/llm-wiki-pattern.md](../sources/llm-wiki-pattern.md)
- [../index.md](../index.md)

## Sources

- [../sources/llm-wiki-pattern.md](../sources/llm-wiki-pattern.md)
- [../../llm-wiki.md](../../llm-wiki.md)
