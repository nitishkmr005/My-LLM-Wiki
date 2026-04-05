---
type: dashboard
status: active
created: 2026-04-05
updated: 2026-04-05
tags:
  - dashboard
  - overview
  - llm-wiki
---

# Home

This is the landing page for the personal LLM wiki. The system is designed to accumulate knowledge over time instead of rediscovering it from scratch on every question.

## What this wiki is for

- Store raw material separately from synthesized knowledge.
- Let an LLM maintain summaries, topic pages, and durable analyses.
- Build a compounding knowledge base that improves with every ingest and every saved answer.

## Start here

- Read the catalog: [index.md](index.md)
- Review the activity history: [log.md](log.md)
- Read the seed source summary: [sources/llm-wiki-pattern.md](sources/llm-wiki-pattern.md)
- Read the core concept page: [topics/persistent-wiki.md](topics/persistent-wiki.md)
- Read the workflow page: [topics/wiki-operations.md](topics/wiki-operations.md)

## Operating model

- `raw/` holds source files.
- `wiki/` holds maintained markdown pages.
- `AGENTS.md` defines how the agent should work in this workspace.

## Immediate next steps

1. Add your first real source to `raw/inbox/`.
2. Ask the agent to ingest it into the wiki.
3. Review the updated topic pages and source summary.
4. Ask a question and save the answer as an analysis if it is worth keeping.

## Sources

- [../llm-wiki.md](../llm-wiki.md)
- [sources/llm-wiki-pattern.md](sources/llm-wiki-pattern.md)
