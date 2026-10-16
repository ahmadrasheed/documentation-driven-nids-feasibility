# LLM request logs

This directory contains cached request/response records used in the
experiments.

Filename components encode:

- dataset/schema
- model
- repetition
- constraint category

Examples of categories:

- definition
- protocol
- count_semantics
- math

The logs are retained to support auditing of the LLM-generated
constraint candidates and experimental reproducibility.
