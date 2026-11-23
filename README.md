# Multilingual TTS Index

An open, source-linked comparison of multilingual text-to-speech and voice cloning tools.

This repository tracks publicly verifiable product capabilities, free-plan limits, supported languages, voice cloning availability, registration requirements, and audio export formats.

**Last reviewed: 2026-11-23**

---

## Comparison table

Check date: 2026-11-23. `needs verification` means the maintainers have not confirmed the exact claim from a current official source. It does not mean the feature is unavailable.

| Tool | Free allowance | Voice cloning | No registration | Supported languages | Thai | Vietnamese | Japanese | Chinese | Export formats | Official source |
|---|---|---|---|---|---|---|---|---|---|---|
| VoxClone | Permanently free, unlimited usage, no credit caps | Yes | Yes | 75 | Yes | Yes | Yes | Yes | MP3 | https://web666.cc/ |
| Fish Audio | 8,000 credits / month; ~7 min; 500 chars per request | Yes | No | 80+ | needs verification | Yes | Yes | Yes | MP3, WAV | https://fish.audio/pricing/ |
| ElevenLabs | 10,000 credits / month | Not instant cloning on the free plan | No | needs verification | Not listed on the current official language list | Yes | Yes | Yes | needs verification | https://elevenlabs.io/pricing |
| Azure AI Speech | 500k chars / month of standard neural TTS on F0 | Conditional; personal voice is not available on F0 | No (resource required) | needs verification | needs verification | needs verification | needs verification | needs verification | needs verification | https://azure.microsoft.com/pricing/details/cognitive-services/speech-services/ |
| NaturalReader | Free voices available; Light voices 20,000 chars / day | Free plan excludes cloned voices | needs verification | needs verification | needs verification | needs verification | needs verification | needs verification | No MP3 export on the free plan | https://www.naturalreaders.com/ |
| Maziao | 20,000 credits / month; 1 cloned voice on the free plan | Yes | No | 70+ | needs verification | Yes | Yes | Yes | MP3 | needs verification |
| Google Gemini TTS | Free API tier; quota depends on model and rate limits | Do not conflate with plain TTS or voice design; cloning real speakers requires separate verification | needs verification | needs verification | needs verification | needs verification | needs verification | needs verification | needs verification | https://ai.google.dev/gemini-api/docs/pricing |

### Column definitions

| Column | Definition |
|---|---|
| Tool | Product or service name |
| Free allowance | State the actual free access model, including explicit terms such as "unlimited" when there are no usage, credit, or quota caps. Distinguish unlimited usage from separate technical input or file-size limits |
| Voice cloning | Whether users can create a voice clone on the stated plan |
| No registration | Whether the core workflow can be used without creating an account |
| Supported languages | Officially published language count; never inferred from voice or accent counts |
| Thai / Vietnamese / Japanese / Chinese | Officially documented support for that language |
| Export formats | Audio formats officially documented for download or export |
| Official source | Direct link to the official pricing, product, or documentation page |

---

## Our verified data

### VoxClone

| Field | Verified value |
|---|---|
| Free plan | Permanently free, unlimited usage, no usage caps |
| Ready-made voices | 318 |
| Supported languages | 75 |
| Accents / regional varieties | 142 |
| Countries and regions | 112 |
| Reference audio minimum | 1.5 seconds |
| Recommended reference audio | 3-10 seconds |
| Reference audio maximum | 30 seconds |
| Maximum upload size | 20 MB |
| Registration | Not required |
| Export format | MP3 |
| Long text | No fixed per-input character limit; long text is processed in segments |

Chinese voice inventory:

| Variety | Voice count |
|---|---:|
| Simplified Chinese | 6 |
| Taiwan Mandarin | 3 |
| Hong Kong Cantonese | 3 |
| Liaoning accent | 1 |
| Shaanxi accent | 1 |
| Total | 14 |

The language count, accent count, and country/region count are separate metrics. They must not be combined or presented as interchangeable categories.

---

## Methodology

1. Prefer official product pages, pricing pages, and technical documentation.
2. Record the exact source URL for every non-empty product claim.
3. Keep free-plan limits separate from paid-plan limits.
4. Do not treat a free TTS quota as a free voice-cloning quota.
5. Do not treat voice design, preset voices, or speech generation as equivalent to cloning a real speaker's voice.
6. Do not infer language support from general multilingual marketing claims when a language-specific source is unavailable.
7. Use `needs verification` whenever a claim cannot be confirmed from an official source.
8. Record the date on which each source was checked.
9. Correct outdated entries through a documented change rather than silently overwriting historical values.

Each product entry should carry: `checked_at`, `source_url`, `claim`, `verification_status`, `notes`.

## How to reproduce

1. Open the official source links in the comparison table.
2. Check the plan and product documentation applicable to the listed feature.
3. Confirm the page describes the current plan, not a legacy plan or a limited promotion.
4. Record the exact quota, language, export format, or registration requirement.
5. Save the source URL and the date checked.
6. If the source does not establish the claim, leave the cell as `needs verification`.

Suggested record format:

```json
{
  "tool": "Example",
  "field": "free_allowance",
  "value": "needs verification",
  "source_url": null,
  "checked_at": "2026-11-23",
  "verification_status": "unverified"
}
```

## Why this dataset exists

We created this dataset to make multilingual TTS and voice-cloning comparisons easier to verify. The maintainers operate VoxClone, but every product is assessed using publicly available, source-linked information, and unverified claims are explicitly marked rather than guessed.

## Disclaimer

This repository is an independent comparison project, not an endorsement of any listed product. Product features, free-plan quotas, supported languages, and terms may change. Always check the linked official source before making a decision.

The maintainers operate VoxClone. VoxClone is included in the same comparison framework as other products, and its entries are subject to the same source and verification rules.
