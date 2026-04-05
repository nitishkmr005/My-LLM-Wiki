---
type: topic
status: active
created: 2026-04-05
updated: 2026-04-05
tags:
  - topic
  - llm-inference
  - memory-sharing
  - serving
---

# Inference Memory Sharing

## Summary

Block-based KV cache management can allow multiple requests to share memory for identical input prefixes instead of storing duplicate cache entries for each request.

## Why It Matters

When several requests start from the same prompt, the key and value tensors for those shared input tokens are identical. Reusing the same memory blocks reduces total memory usage and improves serving efficiency.

## Scenarios Mentioned In Source

- Parallel sampling, where multiple candidate completions are generated from the same prompt.
- Beam search, where several partial continuations are explored in parallel.

## Implication

Paged attention is not only about reducing fragmentation and over-allocation. It also creates a block abstraction that makes shared-prefix reuse practical.

## Caveat

The source presents the concept at a high level. It does not cover reference counting, copy-on-write behavior, or implementation details needed to make sharing safe in production systems.

## Related Pages

- [kv-cache.md](kv-cache.md)
- [paged-attention.md](paged-attention.md)
- [../sources/paged-attention-in-llms.md](../sources/paged-attention-in-llms.md)

## Sources

- [../sources/paged-attention-in-llms.md](../sources/paged-attention-in-llms.md)
