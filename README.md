# Documentation-Driven Feasibility Constraints for Adversarial NIDS Evaluation

This repository contains the code, prompts, LLM request logs,
constraint sets, numerical results, and publication figures associated
with the study:

**From Documentation to Feasibility: LLM-Derived Constraints for
Adversarial Evaluation of Network Intrusion Detection Systems**

## Repository structure

- `code/` — experimental notebook
- `documentation/` — feature documentation used by the methodology
- `prompts/` — exact system prompt and extraction-prompt template
- `constraints/` — extracted and baseline constraint sets
- `llm_logs/` — cached LLM request/response records
- `results/tables/` — numerical results reported in the study
- `results/artifacts/` — selected intermediate reproducibility artifacts
- `figures/` — publication figures
- `metadata/` — experimental and LLM configuration

## LLM models

The study evaluates:

- `deepseek/deepseek-v4-pro-0813`
- `openai/gpt-6-luna`
- `qwen/qwen3.8-27b`

Each model was evaluated over five independent extraction runs.

## Methodological scope

The LLM receives feature documentation and schema information and
proposes candidate hard constraints.

Observed traffic is used only to falsify unsupported candidates and
for vacuity screening; class labels are not used for candidate
generation.

The resulting constraints characterize feature-space feasibility.
They do not demonstrate packet-level realizability.

## Data

The original benchmark datasets are not redistributed in this
repository. See `documentation/README.md` and the paper for dataset
details.

## Reproducibility

The numerical result files and cached LLM logs are included so that
reported analyses can be audited without repeating paid LLM calls.

The full notebook can also be rerun after the required datasets and
API credentials are configured.
