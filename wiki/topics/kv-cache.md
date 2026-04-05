---
type: topic
status: active
created: 2026-04-05
updated: 2026-04-05
tags:
  - topic
  - llm-inference
  - kv-cache
---

# KV Cache

## Summary

KV cache stores the key and value tensors for previously processed tokens so the model can reuse them during autoregressive generation instead of recomputing them at every step.

## Why It Matters

- It reduces repeated computation during decoding.
- It makes token-by-token generation much faster.
- It shifts part of the inference bottleneck from compute to memory capacity and memory management.

## Main Tradeoff

The cache improves latency and throughput, but it consumes memory proportional to sequence length and the number of active requests. In multi-user serving, this memory pressure can become a hard limit on concurrency.

## Operational Implication

Any serving system that relies heavily on KV cache needs an efficient strategy for allocating, extending, and reusing cache memory. This is the motivation for techniques such as [paged-attention.md](paged-attention.md).

## Related Pages

- [paged-attention.md](paged-attention.md)
- [inference-memory-sharing.md](inference-memory-sharing.md)
- [../sources/paged-attention-in-llms.md](../sources/paged-attention-in-llms.md)

## Sources

- [../sources/paged-attention-in-llms.md](../sources/paged-attention-in-llms.md)
