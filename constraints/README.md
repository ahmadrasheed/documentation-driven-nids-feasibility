# Constraint Sets

This directory contains the constraint sets and baseline artifacts used
in the experiments.

## NetFlow-v3 template-mined constraints

`nf_template_miner_hard.json`

Final hard constraints produced by the NetFlow-v3 template-mining
baseline after empirical filtering.

## UNSW-NB15 experimental constraint sets

`unsw_constraint_sets.json`

Original experimental artifact used in the UNSW-NB15 adaptive
adversarial evaluation. It contains the LLM-derived, template-mined,
and reference constraint sets used by the notebook.

## Documentation-and-literature reference set

`unsw_documentation_literature_reference_set.json`

A separately exported copy of the reference set from
`unsw_constraint_sets.json`.

The original artifact label is retained internally for reproducibility.
In the paper, this set is referred to as the
**documentation-and-literature reference set**, because it is derived
primarily from explicit UNSW-NB15 feature documentation and
supplemented by selected published or protocol-level relations.

This reference set is a comparison baseline and is not treated as
semantic ground truth.

## NetFlow-v3 LLM outputs

The repository also includes all cached raw LLM responses under:

`../llm_logs/`

The notebook reconstructs candidate constraints from those responses
and applies falsification and vacuity filtering before evaluation.

The currently released raw logs, notebook, prompts, documentation, and
numerical result tables are sufficient to audit the extraction process.
A separate per-run export of the final post-filtered NetFlow-v3 LLM
sets is not included in this lightweight repository enrichment step
because those sets were held in runtime memory as `LLM_HARD`.

## Scope

These constraints characterize feature-space feasibility only.
Constraint satisfaction does not establish packet-level or
problem-space realizability.
