---
title: "Aman's AI Journal • Primers • Speech Processing"
source: "https://aman.ai/primers/ai/speech-processing/"
author:
published:
created: 2026-04-18
description: "Aman's AI Journal | Course notes and learning material for Artificial Intelligence and Deep Learning Stanford classes."
tags:
  - "clippings"
---
## Terminology

### Phoneme

- A phoneme is the smallest unit that distinguishes meaning between sounds in a given language.” What does that mean? Let’s look at a word using IPA, a transcription system created by the International Phonetic Association.
- Let’s look at the word puff. We use broad transcription when describing phonemes. When we are using broad transcription we use slashes (`/ /`). So the word puff in broad transcription is:

$$
/pʌf/
$$
$$
/ p ʌ f /
$$

- Here we see that puff has three phonemes `/p/`, `/ʌ/`, and `/f/`. When we store the pronunciation of the word puff in our head, this is how we remember it. What happens if we change one phoneme in the word puff? If we change the phoneme (not the letters) `/f/` to the phoneme `/k/` we get another word. We get the word puck which looks like this in broad transcription:

$$
/pʌk/
$$
$$
/ p ʌ k /
$$

- This is a type of test that we can do to see if `/f/` and `/k/` are different phonemes. If we swap these two phonemes we get a new word so we can say that in English `/f/` and `/k/` are different phonemes. We’re going to discuss phones now, but keep this in the back of your head, because we are going to come back to it.

### Phone

- Now that we’ve covered what a phoneme is, we can discuss phones. Remember that we defined a phoneme as “the smallest unit that distinguishes meaning between sounds in a given language.” However, a phoneme is really the mental representation of a sound, not the sound itself. The phoneme is the part that is stored in your brain. When you actually produce a sound you are producing a phone. To give an example, let’s say you want to say the word for a small four-legged animal that meows, a cat. Your brain searches for the word in your lexicon to see if you know the word. You find the lexical entry. You see that phonemic representation of the word is `/kæt/`. Then you use your vocal tract to produce the sounds `[k]`, `[æ]`, and `[t]` and you get the word `[kæt]`.
- Phones, the actual sound part that you can hear, are marked with brackets (`[]`) and the phonemes, the mental representation of the sound, are marked with slashes (`/ /`).

### Why Do We Need Phonemes and Phones?

- Recap: Phonemes are the mental representation of the how a word sounds and phones are the actual sounds themselves. If we take an example from above, the word puff we can write out the phonemic representation (with phonemes using slashes) and the phonetic representation (with phones using brackets).

$$
/pʌf/[pʌf]
$$
$$
/ p ʌ f / \\ \left[\right. p ʌ f \left]\right.
$$

- What does the above show us? Not a whole lot really. So why do we need two different versions? Recall that the transcription that uses phonemes is called broad transcription while the transcription that uses phones is called narrow transcription. These names can give us a clue about the differences.
- By looking at the broad transcription, `/pʌf/`, we can know how to pronounce the word puff. Not only we (as native English speakers) can pronounce the word, but also a non-native English speaker can pronounce it as well. We should all be able to understand what we are saying. However, what if we wanted more information about how the word actually sounds? Narrow transcription can help us with that.
- Narrow transcription just gives us extra information about how a word sounds. So the word puff can be written like this in narrow transcription:

$$
[pʰʌf]
$$
$$
\left[\right. p ʰ ʌ f \left]\right.
$$

- Well, that’s new. This narrow transcription of the word puff gives us a little more information about how the word sounds. Here, we see that the `[p]` is aspirated. This means that when pronouncing the sound `[p]`, we have an extra puff of air that comes out. We notate this by using the superscript `ʰ`. So you are probably asking yourself, why don’t we just put the `ʰ` in the broad transcription? Remember that broad transcription uses phonemes and by definition, if we change a phoneme in a word, we will get a different word. Look at the following:

$$
/pʌf//pʰʌf/∗
$$
$$
/ p ʌ f / \\ / p ʰ ʌ f / *
$$

- An asterisk denotes that the above is incorrect. But why? Because in English, an aspirated p and an unaspirated p don’t change the meaning of a word. That is, you can pronounce the same sound two different ways, but it wouldn’t change the meaning. And by definition, if we change a phoneme, we change the meaning of a word. That means there’s only one `/p/` phoneme in English. If we were speaking a language where aspiration does change the meaning of a word, then that language could have two phonemes, `/p/` and `/pʰ/`. Since it doesn’t change the meaning in English, we just mark it in narrow transcription.

### Allophones

- We can pronounce the `/p/` phoneme in at least two different ways: `[p]` and `[pʰ]`. This means that `[p]` and `[pʰ]` are allophones of the phoneme `/p/`. The prefix “-allo” comes from the Greek állos meaning “other,” so you can think of allopones are just “another way to pronounce a phoneme.”
- This really helps us when we talk about different accents. Take the word water for example. I’m American, so the phonemic representation that I have for the word water is:

$$
/wɑtəɹ/
$$
$$
/ w ɑ t ə ɹ /
$$

- But if you’ve ever heard an American pronounce the word water before, you know that many Americans don’t pronounce a `[t]` sound. Instead, most Americans will pronounce that `[t]` similar to a `[d]` sound. It’s not pronounced the same was as a `[d]` sound is pronounced, though. It’s actually a “flap” and written like this:

$$
[ɾ]
$$
$$
\left[\right. ɾ \left]\right.
$$

- So the actual phonetic representation of the word water for many Americans is:

$$
[wɑɾɚ]
$$
$$
\left[\right. w ɑ ɾ ɚ \left]\right.
$$

- So, in the phonemic representation (broad transcription), we have the `/t/` phoneme, but most Americans will produce a `[ɾ]` here. That means we can say that in American English `[ɾ]` is an allophone of the phoneme `/t/`.
- But sometimes the `/t/` phoneme does use a `[t]` sound like in the name Todd:

$$
/tɑd/
$$
$$
/ t ɑ d /
$$

- and in narrow transcription:

$$
[tʰɑd]
$$
$$
\left[\right. t ʰ ɑ d \left]\right.
$$

- With these examples, we can see that the phoneme `/t/` has at least two allophones: `[tʰ]` and `[ɾ]`. We can even look at the word putt and see that the `[t]` can be pronounced as a “regular” `[t]` sound:

$$
[pʌt]
$$
$$
\left[\right. p ʌ t \left]\right.
$$

- Fantastic! So now we know that the phoneme `/t/` has at least three allophones, `[t]`, `[tʰ]`, and `[ɾ]`. But how do we know when to say each one?

#### Environments of Phonemes

- When we talk about the environments of a phoneme we are talking about where the phoneme occurs, usually in relation to other phonemes in a word. We can use this information to predict how a phoneme will be pronounced. Take for example the name Todd:

$$
/tɑd/
$$
$$
/ t ɑ d /
$$

- If this was a word that we had never heard before, how would we know how to pronounce the `/t/` phoneme? Well, we can already narrow it down to `[t]`, `[tʰ]`, or `[ɾ]` because we’ve seen in past examples that we can pronounce these when we have `/t/` phoneme. But how do we know which phone is the correct one?
- If you combed through many many words in English, you would find out that the phoneme `/t/` is often aspirated when it’s at the beginning of a word. By looking at other words that start with `/t/` like tap, take, tack, etc. you’ll find that `/t/` becomes `[tʰ]` when at the beginning of a word and that the narrow transcription of the name Todd would be:

$$
[tʰɑd]
$$
$$
\left[\right. t ʰ ɑ d \left]\right.
$$

- We can use the same process to find out how to pronounce other words in an American accent. If we look at the words eating, little, latter, etc… we can see that in American English all of `/t/` are pronounced as `[ɾ]`. Deciding all of the requirements for realizing `/t/` as `[ɾ]` is beyond the scope of this post, but you can see that in similar environments the `/t/` becomes a `[ɾ]`.

### Graphemes

- In linguistics, a grapheme is the smallest functional unit of a **writing system**.
- The name grapheme is given to the letter or combination of letters that represents a phoneme. For example, the word ‘ghost’ contains five letters and four graphemes (`gh`, `o`, `s`, and `t`), representing four phonemes.

### Mono vs. Stereo Sound

- The difference between monophonic (mono) and stereophonic (stereo) sound is the number of channels used to record and playback audio.
- Mono signals are recorded and played back using a single audio channel, while stereo sounds are recorded and played back using two audio channels.
- As a listener, the most noticeable difference is that stereo sounds are capable of producing the perception of width, whereas mono sounds are not.
- Using Mono instead of Stereo playback is most useful for users with certain types of hearing loss or for safety reasons, for example when you need to listen to your surroundings.

### Key Takeaways

- A phoneme is a mental representation of a sound, not necessarily a letter. Also, when we swap a phoneme we change the word.
- A phone is the phonetic representation of a phoneme (the actual sound).
- Allophones are different ways to pronounce the same phoneme while keeping the same meaning.
- Sometimes allophones are predictable depending on their environment and who is speaking.
- With Mono audio, both left and right audio channels get played back simultaneously via a single channel when playing audio (as opposed to Stereo audio where individual channels retain their presence and are played back separately).