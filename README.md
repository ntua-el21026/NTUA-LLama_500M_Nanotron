# NTUA-Llama-500M (Nanotron)

Official repository for Team 12 project in the NTUA ECE course "Pattern Recognition" (Winter 2025-2026).

## Project Scope

This project trains and evaluates a 500M-parameter LLaMA-style model with a staged curriculum:

- Stage 1: base pretraining
- Stage 2: high-quality code/math continuation
- Stage 3: reasoning-oriented continuation
- Stage 4: supervised fine-tuning (SFT)

Evaluation follows a tiered protocol:

- Tier 1: training health analytics
- Tier 2: perplexity slices
- Tier 3: conditional-likelihood multiple-choice QA
- Tier 4 (Stage 4): SFT-native prompt behavior checks

## Repository Contents

- `config/`: canonical training and SFT configurations for the reported pipeline:
  `config_stage1.yaml`, `config_stage2.yaml`, `config_stage3.yaml`, `sft_stage3_smoltalk.yaml`.
- `docs/`: paper sources and compiled report (`main.tex`, `Report.pdf`).
- `weights/`: selected model-only checkpoint exports for reproducibility and comparison baselines:
  `stage3_12000_modelonly`, `sft_stage3_smoltalk_run1_5000_modelonly`.

## Reproducibility Note

Full training checkpoints, dataset caches, and complete evaluation outputs are produced on Leonardo HPC storage and are not fully versioned in this repository. This repository keeps the canonical configs, report artifacts, and selected release-ready weights.

## License

MIT (see `LICENSE`).
