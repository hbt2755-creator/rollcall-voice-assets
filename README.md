# Rollcall Voice Assets

Optional voice engines for the [Rollcall](https://genflow.work/rollcall/) macOS app (Apple Silicon only).
The app downloads these files itself when a user taps **Download** in Settings → Notifications & Voice. You do not need to download them manually.

| File | What it is | Size |
|---|---|---|
| `supertonic-helper-arm64` | Small synthesis helper (ONNX Runtime) for the "Better voice" tier. Based on the MIT-licensed example code of [supertone-inc/supertonic](https://github.com/supertone-inc/supertonic). | ~32 MB |
| `tone-converter.onnx` | Tone-color converter exported to ONNX from [OpenVoice v2](https://github.com/myshell-ai/OpenVoice) (MIT). Gives the "Better voice" tier its 22 Korean voices. | ~128 MB |
| `rollcall-voice-runtime-arm64.tgz` | Self-contained Python runtime ([python-build-standalone](https://github.com/astral-sh/python-build-standalone)) + MLX + a local-only voice bridge (`127.0.0.1`) for the "High-quality voice" tier, plus 22 Korean sample voices. | ~150 MB |

Model weights (Supertonic 3, Qwen3-TTS) are **not** hosted here. The app downloads them directly from Hugging Face.

- Supertonic 3 weights: BigScience OpenRAIL-M (use restrictions apply — no impersonation without consent, disclose AI-generated speech).
- Qwen3-TTS: Apache-2.0.

See `THIRD_PARTY_LICENSES.md`. Voices created from a user-supplied recording stay on the user's Mac.
