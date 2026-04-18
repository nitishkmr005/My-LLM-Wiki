---
type: topic
status: active
created: 2026-04-18
updated: 2026-04-18
tags:
  - topic
  - speech-processing
  - speech-features
  - audio-representations
---

# Speech Features

## Summary

Speech features are the intermediate representations that turn raw audio into inputs a model can work with. The source emphasizes time-domain views such as waveforms, time-frequency views such as spectrograms, and auditory-inspired features such as Mel filterbanks and MFCCs, along with longer-span prosodic and idiolectal cues.

## Key Points

- An oscillogram represents amplitude over time, while a spectrum represents frequency content within a slice of audio.
- A spectrogram stacks spectra over time, making phones, formants, and transitions easier to inspect visually.
- Mel filterbanks and MFCCs incorporate an auditory-inspired frequency scale and have long been standard ASR front ends.
- The source notes that deep models often work well with log-Mel features directly, reducing the need for MFCC decorrelation.
- Prosodic and idiolectal features capture slower or speaker-specific patterns that complement shorter-frame acoustic features.
- In neural audio pipelines, "tokens" often correspond to short feature frames or segments rather than words or subwords.

## Tensions Or Open Questions

- When do raw-waveform front ends outperform engineered features in practice?
- When is MFCC still the right choice instead of log-Mel filterbanks?
- Which speech tasks benefit most from prosodic or idiolectal features rather than only acoustic frames?

## Related Pages

- [speech-processing.md](speech-processing.md)
- [automatic-speech-recognition.md](automatic-speech-recognition.md)
- [keyword-spotting.md](keyword-spotting.md)
- [../sources/speech-processing-primers.md](../sources/speech-processing-primers.md)

## Sources

- [../sources/speech-processing-primers.md](../sources/speech-processing-primers.md)
