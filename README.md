# Premiere Editing Agent — runtime packs

Runtime files that the Premiere Editing Agent installer downloads during setup. They are not useful on their own.
The files are on the [`packs` release](../../releases/tag/packs); packs over 2 GB are split into `.001` / `.002` parts that
the installer joins again.

| Pack | Contents |
|---|---|
| `core-N.zip` | Python 3.12 runtime, speech libraries (faster-whisper, CTranslate2 and their dependencies), FFmpeg |
| `gpu-N.zip` | NVIDIA cuBLAS / cuDNN runtime libraries for GPU transcription |
| `model-th-N.zip` | Thai speech model (Thonburian Whisper, converted for CTranslate2) |
| `model-en-N.zip` | Whisper large-v3 (CTranslate2 conversion by SYSTRAN) |

## Third-party licenses

- Python: PSF License
- faster-whisper, CTranslate2: MIT License
- FFmpeg: GPL build from gyan.dev; the license text is inside `core-N.zip` (`ffmpeg/LICENSE`), source code at https://ffmpeg.org
- NVIDIA cuBLAS, cuDNN: redistributed as application runtime files under NVIDIA's license terms
- Whisper large-v3 (OpenAI): MIT License; CTranslate2 conversion `Systran/faster-whisper-large-v3`
- Thonburian Whisper (`biodatlab/whisper-th-large-v3-combined`): Apache License 2.0
