# FunASR Newcomer Guide

Welcome to FunASR! This guide summarizes the repository layout, key components, and next steps to help new contributors ramp up quickly.

## Repository structure at a glance
- **funasr/**: Core Python library with training and inference code.
  - `auto/`: Entry points such as `AutoModel` that simplify loading pretrained models for inference.
  - `datasets/`, `frontends/`, `models/`, `losses/`, `metrics/`, `optimizers/`, `schedulers/`: Building blocks for training pipelines.
  - `utils/` and `train_utils/`: Helper functions, data processing, and trainer support.
  - `bin/`: Command-line tools (e.g., `funasr` CLI) for quick experiments.
- **runtime/**: Service deployment assets and SDK documentation for offline, online, and GPU inference pipelines.
- **examples/**: Task-oriented examples (industrial data pretraining, Whisper/Qwen demos, etc.) showing how to run and fine-tune models.
- **docs/**: Tutorials, model zoo listings, and additional documentation referenced throughout the repo.
- **model_zoo/**: Curated configurations for publicly released models on ModelScope and Hugging Face.
- **fun_text_processing/**: Text normalization and punctuation utilities that complement ASR pipelines.
- **tests/**: Unit and integration tests that cover core APIs.
- **benchmarks/**: Benchmark scripts and results for comparing model performance and runtime.

## Important concepts to know first
- **Installation and quick start**: The root `README.md` documents installation, command-line usage via `funasr`, and Python API examples for running speech recognition models.
- **Model Zoo**: The `model_zoo/` directory and the Model Zoo section in `README.md` list representative pretrained models (Paraformer, SenseVoice, Whisper, Qwen-Audio, etc.) and their capabilities.
- **Deployment paths**: `runtime/readme.md` explains how to stand up offline and online transcription services, including CPU/GPU options and runtime SDKs.
- **Tutorials**: `docs/tutorial/README.md` links to walk-throughs for training, fine-tuning, and extending pipelines.

## Suggested learning path
1. **Skim the root README** to understand available features, supported tasks (ASR, VAD, punctuation, diarization, KWS, emotion recognition), and quick-start commands.
2. **Run a small inference** using the `funasr` CLI or the `AutoModel` Python snippet to validate your environment.
3. **Review examples** relevant to your task (e.g., Whisper demos, Qwen-Audio chat) under `examples/industrial_data_pretraining/` to see end-to-end scripts.
4. **Explore deployment docs** in `runtime/` if you need to package services, including real-time and offline pipelines.
5. **Dive into core modules** inside `funasr/` once you are ready to customize architectures, training loops, or data processing.

## Tips for contributors
- Favor existing utilities in `funasr/utils/` and `fun_text_processing/` before adding new helpers.
- Mirror patterns used in `examples/` and `runtime/` when adding new tasks or deployment modes.
- Add tests under `tests/` for new features to keep coverage consistent.
- Update documentation in `docs/` or the relevant README sections when introducing user-facing changes.
