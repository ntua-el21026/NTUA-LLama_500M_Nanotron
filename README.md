# NTUA-LLaMA-500M (Nanotron)

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

- `config/`: canonical training and SFT configurations used in reported runs
  - `config_stage1.yaml`
  - `config_stage2.yaml`
  - `config_stage3.yaml`
  - `sft_stage3_smoltalk.yaml`
- `docs/`: report-related material
- `model/`: model release artifacts (when available)

## Reproducibility Note

Large checkpoints, cached datasets, and full evaluation outputs are produced on Leonardo HPC storage and are not versioned in this repository.

## License

MIT (see `LICENSE`).
