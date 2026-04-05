---
type: topic
status: active
created: 2026-04-05
updated: 2026-04-05
tags:
  - topic
  - llm-inference
  - paged-attention
  - memory-management
---

# Paged Attention

## Summary

Paged attention is a KV cache memory-management technique for LLM serving. It breaks cache storage into fixed-size blocks that can live in non-contiguous memory and uses a block table to map logical token order to those physical blocks.

## Problem It Solves

Traditional KV cache allocation often reserves one large contiguous chunk per request before the final output length is known. This causes:

- Internal waste: reserved capacity that the request never uses.
- External waste: free memory exists, but not as a large enough contiguous region for a new request.

## Core Mechanism

- Split KV cache memory into fixed-size blocks.
- Allocate blocks only when needed as generation grows.
- Track block locations through a block table.
- Read prior-token keys and values through the block table instead of assuming contiguous storage.

## Why It Helps

- Only the final partially filled block is likely to be wasted.
- Fragmented free memory becomes usable because blocks do not need contiguous placement.
- The same hardware can serve more simultaneous requests.

## Limits And Open Questions

- The source explains the high-level idea, not the implementation costs.
- Real systems still need efficient block lookup, scheduling, and memory reclamation.
- Performance tradeoffs likely depend on block size, workload shape, and serving stack design.

## Related Pages

- [kv-cache.md](kv-cache.md)
- [inference-memory-sharing.md](inference-memory-sharing.md)
- [../sources/paged-attention-in-llms.md](../sources/paged-attention-in-llms.md)

## Sources

- [../sources/paged-attention-in-llms.md](../sources/paged-attention-in-llms.md)
