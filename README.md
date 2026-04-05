# Personal LLM Wiki

This workspace is now set up as a local, markdown-first LLM wiki. The idea is simple:

- you collect raw material in `raw/`
- the LLM maintains structured notes in `wiki/`
- `AGENTS.md` tells the LLM how to ingest, update, and answer from the wiki

The scaffold is seeded from [`llm-wiki.md`](llm-wiki.md), which has already been turned into initial wiki pages.

## Structure

- `AGENTS.md` - operating rules for Codex or another agent
- `raw/inbox/` - drop new sources here
- `raw/processed/` - optional archive area
- `raw/assets/` - images and attachments
- `wiki/home.md` - starting page
- `wiki/index.md` - catalog of pages
- `wiki/log.md` - chronological history
- `wiki/sources/` - source summaries
- `wiki/topics/` - themes and concepts
- `wiki/entities/` - named things
- `wiki/analyses/` - durable answers
- `templates/` - reusable page skeletons

## How To Use It

### 1. Open the folder in your tools

- In Obsidian: open this folder as a vault.
- In Codex: open this folder as your workspace.

If you want version history, initialize git:

```bash
git init
```

## 2. Add a source

Put a new markdown, PDF, note, or transcript into `raw/inbox/`.

Then ask the agent something like:

```text
Ingest raw/inbox/<filename> into the wiki. Update relevant topic pages, update index.md, and append to log.md.
```

## 3. Ask questions against the wiki

Example prompts:

```text
Answer this using the wiki only: what are the main themes across my recent sources?
```

```text
Compare the pages related to <topic> and save the result as a new analysis page.
```

```text
What is missing from this wiki if I want to understand <subject> deeply?
```

## 4. Run maintenance

Example prompt:

```text
Lint the wiki for stale claims, missing cross-links, orphan pages, and concepts that should have their own page.
```

## 5. Keep useful answers

If a chat answer is worth preserving, ask:

```text
File this answer into the wiki as an analysis page and update the index and log.
```

## Suggested Workflow

1. Ingest one source at a time.
2. Read the generated source summary.
3. Check which topic pages changed.
4. Ask follow-up questions.
5. Save the important answers back into `wiki/analyses/`.
6. Run a lint pass every so often.

## Current Seed Content

The wiki currently contains:

- a home page
- an index and log
- a source summary derived from `llm-wiki.md`
- topic pages for the persistent wiki pattern and the ingest/query/lint workflow

Start at [`wiki/home.md`](wiki/home.md).
