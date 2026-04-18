---
type: topic
status: active
created: 2026-04-18
updated: 2026-04-18
tags:
  - topic
  - speech-processing
  - speech-ml
  - voice-assistants
---

# Speech Processing

## Summary

Speech processing connects human speech structure to machine systems that can detect, transcribe, classify, or generate audio. The source bundle presents it as a stack that starts with phonetic units and acoustic features, then moves into task-specific modules such as keyword spotting, ASR, language identification, speaker recognition, and text-to-speech.

## Key Points

- Linguistic units such as phonemes, phones, allophones, and graphemes explain how speech sounds relate to meaning and writing.
- Feature extraction converts raw waveform audio into more model-friendly representations such as spectrograms, log-Mel filterbanks, and MFCCs.
- Voice-assistant systems are usually pipelined rather than monolithic, with early gating stages used to control power and latency.
- Speech systems must balance accuracy, responsiveness, multilingual handling, and deployment constraints such as on-device compute.
- The source mixes classical speech-recognition structure with newer neural end-to-end modeling approaches.

## Tensions Or Open Questions

- How much of the pipeline should remain modular as end-to-end models get stronger?
- When should this wiki split out dedicated pages for speaker recognition, TTS, and multilingual ASR?
- Which speech concepts here are domain-stable fundamentals versus implementation details likely to change quickly?

## Related Pages

- [speech-features.md](speech-features.md)
- [automatic-speech-recognition.md](automatic-speech-recognition.md)
- [keyword-spotting.md](keyword-spotting.md)
- [../sources/speech-processing-primers.md](../sources/speech-processing-primers.md)

## Sources

- [../sources/speech-processing-primers.md](../sources/speech-processing-primers.md)
