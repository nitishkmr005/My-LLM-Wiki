---
type: source
status: active
created: 2026-04-18
updated: 2026-04-18
tags:
  - source
  - speech-processing
  - asr
  - keyword-spotting
  - speech-features
---

# Speech Processing Primers

## Source

- Files: [Aman's AI Journal • Primers • Speech Processing.md](<../../raw/Speech Processing/Aman's AI Journal • Primers • Speech Processing.md>) and [Aman's AI Journal • Primers • Speech Processing 1.md](<../../raw/Speech Processing/Aman's AI Journal • Primers • Speech Processing 1.md>)
- Original URL: <https://aman.ai/primers/ai/speech-processing/>
- Nature: bundled local clippings from the same speech-processing primer

## Summary

This source bundle combines introductory phonetics, signal representations, and applied speech ML. It starts with linguistic units such as phonemes, phones, allophones, and graphemes, then moves into audio representations such as waveforms, spectrograms, Mel filterbanks, and MFCCs. The later sections outline speech-system pipelines for assistants, covering keyword spotting, ASR, language identification, speaker recognition, data augmentation, and a short survey of model families and evaluation metrics.

## Key Takeaways

- Speech processing spans both linguistic structure and numerical signal processing.
- Feature representations such as spectrograms, log-Mel filterbanks, and MFCCs are core interfaces between raw waveform audio and downstream models.
- Digital assistant pipelines are usually modular: VAD or wake-word detection first, then ASR, language-specific downstream understanding, and TTS.
- Classical ASR decomposes the problem into acoustic modeling, language modeling, and decoding, often with phones and lexicons as intermediate structure.
- The source frames the architectural shift from GMM-HMM systems to DNN-HMM hybrids, CTC-trained models, and end-to-end encoder-decoder systems.
- Always-on keyword spotting is an optimization problem as much as a modeling problem because battery, latency, and false activations all matter.
- Robust speech systems depend on multilingual handling, augmentation, and task-appropriate metrics such as WER, CER, DET, EER, or MOS.

## Notable Systems And Terms

- Phoneme, phone, allophone, grapheme
- Spectrogram, log-Mel filterbanks, MFCCs, PLP
- Keyword spotting (KWS), automatic speech recognition (ASR), language identification (LID), text-to-speech (TTS)
- GMM-HMM, DNN-HMM, CTC, Listen Attend Spell (LAS)
- Distil-Whisper, Parakeet, Canary

## Open Questions

- Which parts of the source should become durable topic pages next: speaker recognition, TTS, multilingual ASR, or speech evaluation?
- When is raw-waveform modeling preferable to engineered front-end features such as log-Mel filterbanks?
- Which model examples in the source are durable architectural references versus time-bound snapshots of the speech-model landscape?

## Related Pages

- [../topics/speech-processing.md](../topics/speech-processing.md)
- [../topics/speech-features.md](../topics/speech-features.md)
- [../topics/automatic-speech-recognition.md](../topics/automatic-speech-recognition.md)
- [../topics/keyword-spotting.md](../topics/keyword-spotting.md)
- [../index.md](../index.md)

## Sources

- [Aman's AI Journal • Primers • Speech Processing.md](<../../raw/Speech Processing/Aman's AI Journal • Primers • Speech Processing.md>)
- [Aman's AI Journal • Primers • Speech Processing 1.md](<../../raw/Speech Processing/Aman's AI Journal • Primers • Speech Processing 1.md>)
- <https://aman.ai/primers/ai/speech-processing/>
