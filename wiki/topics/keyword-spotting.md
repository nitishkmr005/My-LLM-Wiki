---
type: topic
status: active
created: 2026-04-18
updated: 2026-04-18
tags:
  - topic
  - speech-processing
  - keyword-spotting
  - wake-word-detection
---

# Keyword Spotting

## Summary

Keyword spotting is the always-on speech task that decides when a device should wake up and listen more deeply. The source emphasizes that this is a systems problem as much as a modeling problem: the detector has to preserve battery life, keep latency low, avoid false activations, and still avoid missing genuine wake words.

## Key Points

- Keyword spotting often sits behind a lightweight voice-activity detector so more expensive models do not run unnecessarily.
- A common production pattern is a two-stage system: a cheap always-on stage with high recall and a more accurate checker with higher precision.
- Both stages can share the same computed speech features to avoid duplicate front-end work.
- Threshold tuning is an operational tradeoff between missed detections, accidental wakeups, and battery cost.
- The source highlights precision, recall, F1, and DET curves as important evaluation tools for wake-word systems.
- Low-threshold live-data collection plus manual filtering can supply true positives and hard negatives for robustness updates.

## Tensions Or Open Questions

- How much personalization should a wake-word detector support on-device?
- When is a two-stage design still preferable to a single stronger model?
- How should multilingual wake-word detection interact with language identification and downstream ASR routing?

## Related Pages

- [speech-processing.md](speech-processing.md)
- [speech-features.md](speech-features.md)
- [automatic-speech-recognition.md](automatic-speech-recognition.md)
- [../sources/speech-processing-primers.md](../sources/speech-processing-primers.md)

## Sources

- [../sources/speech-processing-primers.md](../sources/speech-processing-primers.md)
