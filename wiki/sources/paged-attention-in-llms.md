---
type: source
status: active
created: 2026-04-05
updated: 2026-04-05
tags:
  - source
  - llm-inference
  - kv-cache
  - paged-attention
---

# Paged Attention in LLMs

## Source

- File: [../../raw/inbox/Paged Attention in LLMs.md](Paged%20Attention%20in%20LLMs.md)
- Nature: explanatory blog post / technical note

## Summary

The source explains how paged attention improves LLM serving efficiency by changing how KV cache memory is allocated. Instead of reserving one large contiguous memory region for each request, the cache is divided into fixed-size blocks that are allocated on demand. This sharply reduces wasted memory and allows more concurrent requests to fit in the same hardware budget.

## Key Takeaways

- KV cache speeds generation by reusing previously computed keys and values for earlier tokens.
- Traditional contiguous KV cache allocation wastes memory because systems do not know the final output length in advance.
- The waste has two forms: internal waste from unused reserved space and external waste from fragmentation caused by the need for large contiguous blocks.
- Paged attention borrows the operating-system idea of paging: fixed-size blocks plus a table that maps logical order to physical memory locations.
- With paged attention, only the final partially filled block is typically wasted, so memory efficiency improves materially.
- Better memory efficiency increases serving capacity because more requests can run at the same time.
- The block-based layout also enables memory sharing across requests with identical prefixes, which is especially useful for parallel sampling and beam search.

## Important Concepts

- [../topics/kv-cache.md](../topics/kv-cache.md)
- [../topics/paged-attention.md](../topics/paged-attention.md)
- [../topics/inference-memory-sharing.md](../topics/inference-memory-sharing.md)

## Open Questions

- What block size tradeoffs matter most in real systems?
- What implementation overhead does block-table lookup introduce relative to contiguous storage?
- Which production serving stacks use paged attention or related techniques?

## Related Pages

- [../home.md](../home.md)
- [../index.md](../index.md)
- [../topics/kv-cache.md](../topics/kv-cache.md)
- [../topics/paged-attention.md](../topics/paged-attention.md)
- [../topics/inference-memory-sharing.md](../topics/inference-memory-sharing.md)

## Sources

- [../../raw/inbox/Paged Attention in LLMs.md](Paged%20Attention%20in%20LLMs.md)
