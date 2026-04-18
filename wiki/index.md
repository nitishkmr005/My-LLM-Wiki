---
type: index
status: active
created: 2026-04-05
updated: 2026-04-18
tags:
  - index
  - navigation
---

# Index

This file is the main catalog for the wiki. Start here before drilling into individual pages.

## Dashboards

- [home.md](home.md) - Main landing page and operating overview.

## Sources

- [sources/llm-wiki-pattern.md](sources/llm-wiki-pattern.md) - Summary of the seed concept document and how it informs this wiki.
- [sources/paged-attention-in-llms.md](sources/paged-attention-in-llms.md) - Summary of how paged attention reduces KV cache memory waste in LLM serving.
- [sources/speech-processing-primers.md](sources/speech-processing-primers.md) - Summary of bundled speech-processing primer notes covering phonetics, features, ASR, and wake-word systems.

## Topics

- [topics/kv-cache.md](topics/kv-cache.md) - Why KV cache speeds decoding and why it creates memory pressure during serving.
- [topics/paged-attention.md](topics/paged-attention.md) - Block-based KV cache allocation inspired by operating-system paging.
- [topics/inference-memory-sharing.md](topics/inference-memory-sharing.md) - How shared prefixes can reuse KV cache blocks across requests.
- [topics/persistent-wiki.md](topics/persistent-wiki.md) - Why a maintained wiki is different from one-shot retrieval.
- [topics/wiki-operations.md](topics/wiki-operations.md) - The practical ingest, query, and lint workflow for this workspace.
- [topics/speech-processing.md](topics/speech-processing.md) - Overview of the speech-processing stack from linguistic units and features to assistant pipelines.
- [topics/speech-features.md](topics/speech-features.md) - Common speech representations such as waveforms, spectrograms, log-Mel features, and MFCCs.
- [topics/automatic-speech-recognition.md](topics/automatic-speech-recognition.md) - How ASR maps speech features to text across classical and neural architectures.
- [topics/keyword-spotting.md](topics/keyword-spotting.md) - Wake-word detection design patterns, evaluation tradeoffs, and always-on deployment constraints.

## Entities

- [entities/README.md](entities/README.md) - Notes on how entity pages should be used in this wiki.

## Analyses

- [analyses/README.md](analyses/README.md) - Placeholder for durable question-and-answer pages.

## Supporting Notes

- [dashboards/README.md](dashboards/README.md) - Placeholder for future dashboard pages.

## Dashboards To Add Later

- A source tracker once multiple ingests exist.
- A topic map once the wiki spans several domains.

## Sources

- [../llm-wiki.md](../llm-wiki.md)
