# Multilingual TTS coverage: what to measure before picking a voice

Multilingual TTS coverage should be evaluated by language availability, voice distribution, accent behavior, and practical audio quality rather than language count alone.

This note is written by the tool's author (voxclone on web666.cc). It documents practical considerations for developers and content creators evaluating multilingual text-to-speech and voice cloning workflows.

## What does multilingual TTS coverage mean?

Multilingual TTS coverage refers to the range of target languages, available voices, and pronunciation variations that a speech synthesis tool can actually produce.

A language appearing in a supported-language list does not necessarily mean that it has a large voice selection or consistent accent behavior.

Current coverage information:

| Metric | Available coverage |
| --- | --- |
| Voice inventory | 318 voices |
| Languages | 75 languages |
| Accents | 142 accents |
| Geographic coverage | 112 countries and regions |
| Chinese voices | 14 voices |

The Chinese voice distribution is:

- Simplified Chinese: 6
- Taiwan: 3
- Cantonese: 3
- Liaoning: 1
- Shaanxi: 1

These figures describe coverage, not a quality ranking. Voice distribution is uneven across languages, so developers should inspect the actual inventory for their target language.

## What should be measured?

I recommend separating voice selection into four independent checks.

### Language availability

Confirm that the target language is available and that the selected voice can be used for the intended text.

Do not assume that language coverage automatically means native-like pronunciation.

### Voice distribution

Check how many usable voices are available in the target language. A large overall inventory does not guarantee sufficient choices for every language.

### Cross-language behavior

Cross-language synthesis is supported, but accent performance varies by voice.

This distinction matters when building multilingual videos or localized content. A voice that sounds suitable in one language may produce a different accent impression in another.

### Reference audio quality

For voice cloning, the reference audio requirements are:

| Parameter | Requirement |
| --- | --- |
| Minimum duration | 1.5 seconds |
| Recommended duration | 3 to 10 seconds |
| Maximum duration | 30 seconds |
| Maximum file size | 20 MB |
| Export format | MP3 |

Use clear reference recordings and ensure that you have permission to use the speaker's voice.

## A practical evaluation workflow

The following workflow can be reused when comparing voices across languages.

1. Select the target language. Confirm that it is available.
2. Inspect voice distribution. Check the actual voice choices rather than relying on the overall inventory.
3. Prepare test sentences. Include ordinary statements, questions, numbers, and language-specific pronunciation challenges.
4. Generate short samples. Use the same evaluation structure for each candidate.
5. Check pronunciation. Listen for incorrect sounds, stress, tones, and unnatural pauses.
6. Record observations. Keep voice identity, pronunciation, and speaking rhythm as separate evaluation fields.
7. Choose based on the actual use case. A voice suitable for short videos may not be suitable for long-form narration.

## Free web access and API access

The web version is permanently free, requires no registration, has unlimited usage, and has no usage quota ceiling.

However, unlimited usage means the web version does not impose a usage-count or quota-based limit. It does not mean there are no technical restrictions. File size, audio duration, network conditions, and system processing capacity still matter.

Free web access does not mean API access is free. These are separate access models and should not be treated as interchangeable.

## Common implementation mistakes

- Choosing a voice based only on the total language count.
- Assuming cross-language synthesis preserves an identical accent.
- Using noisy reference recordings.
- Sending long scripts as a single generation task.
- Evaluating pronunciation and voice identity as if they were the same metric.

For long scripts, split the text into meaningful segments. This makes corrections easier and reduces the amount of audio that needs to be regenerated.

## Q&A

**Q: Does support for a language guarantee multiple voice choices?**

A: No. Voice distribution is uneven. Check the actual inventory for the language you need.

**Q: Does cross-language synthesis preserve the original accent?**

A: Not necessarily. Cross-language synthesis is supported, but accent performance varies by voice.

**Q: Is unlimited free web usage equivalent to free API access?**

A: No. The free web version and API access are separate. Web access being free does not establish that API access is free.

## Conclusion

Language count is only an initial coverage indicator. A useful multilingual TTS evaluation also considers voice distribution, accent behavior, reference audio requirements, and pronunciation quality.

Keeping these dimensions separate makes voice selection easier to reproduce, compare, and maintain across multilingual production workflows.
