---
type: topic
status: active
created: 2026-04-18
updated: 2026-04-18
tags:
  - topic
  - speech-processing
  - asr
  - speech-recognition
---

# Automatic Speech Recognition

## Summary

Automatic speech recognition maps speech signals to text. In the source bundle, ASR is presented both as a classical pipeline with acoustic models, language models, lexicons, and decoders, and as an area that has shifted toward neural end-to-end systems trained with methods such as CTC or sequence-to-sequence attention.

## Key Points

- ASR begins with speech features derived from waveform audio, often after normalization steps such as mono conversion and resampling.
- Classical ASR decomposes the task into acoustic modeling, language modeling, and decoding, with phones and word pronunciations providing structure.
- HMM-based systems model phones, words, and sentence transitions hierarchically and use algorithms such as Viterbi decoding.
- The source describes an architectural progression from GMM-HMM systems to DNN-HMM hybrids and then to CTC and end-to-end encoder-decoder models such as LAS.
- Language identification can run alongside ASR so multilingual assistants can route recognition output to the right downstream components.
- WER and CER are operational metrics for transcription quality, while deployment decisions also depend on latency and hardware budget.

## Tensions Or Open Questions

- When do explicit pronunciation and language-model components still outperform simpler end-to-end setups?
- How much multilingual handling should live inside one joint model versus a routed collection of monolingual systems?
- Which newer model families deserve durable pages once more speech sources are ingested?

## Related Pages

- [speech-processing.md](speech-processing.md)
- [speech-features.md](speech-features.md)
- [keyword-spotting.md](keyword-spotting.md)
- [../sources/speech-processing-primers.md](../sources/speech-processing-primers.md)

## Sources

- [../sources/speech-processing-primers.md](../sources/speech-processing-primers.md)
