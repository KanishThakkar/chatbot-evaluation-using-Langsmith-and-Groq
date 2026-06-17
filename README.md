# LLM Evaluation with LangSmith and Groq

A practical LLM evaluation project that benchmarks multiple Groq-hosted language models using LangSmith. The project evaluates chatbot responses using custom evaluators for **Correctness** and **Concision**, enabling systematic comparison of model quality and response efficiency.

<img width="1890" height="852" alt="image" src="https://github.com/user-attachments/assets/75eacee5-0960-42ad-8b32-784274ca9605" />

## Overview

Evaluating LLMs is essential before deploying them in production systems. This project demonstrates how to:

* Create evaluation datasets in LangSmith
* Run experiments across multiple LLMs
* Build custom evaluators
* Compare model performance using objective metrics
* Track latency and evaluation scores through LangSmith dashboards

## Models Evaluated

* GPT-OSS-20B
* GPT-OSS-120B
* Llama-based Groq Model

## Evaluation Metrics

### Correctness

Uses an LLM-as-a-Judge approach to compare generated responses against reference answers.

The evaluator:

* Receives the question
* Receives the reference answer
* Receives the model-generated response
* Grades the response as CORRECT or INCORRECT

### Concision

Measures whether the generated response remains concise relative to the reference answer.

Formula:

Concision = Response Length < 2 × Reference Answer Length

## Tech Stack

* Python
* Groq API
* LangSmith
* Custom Evaluators
* GPT-OSS Models
* Llama Models

## Project Workflow

Dataset Creation
↓
User Questions
↓
LLM Response Generation
↓
Correctness Evaluation
↓
Concision Evaluation
↓
LangSmith Experiment Tracking
↓
Model Comparison Dashboard

## Example Dataset

| Question           | Reference Answer                                         |
| ------------------ | -------------------------------------------------------- |
| What is Google?    | A technology company known for search                    |
| What is LangSmith? | A platform for observing and evaluating LLM applications |
| What is LangChain? | A framework for building LLM applications                |

## Experimental Results

| Model        | Correctness | Concision |
| ------------ | ----------- | --------- |
| GPT-OSS-20B  | 0.60        | 0.40      |
| GPT-OSS-120B | 0.80        | 0.20      |
| Llama Model  | 0.60        | 0.20      |

### Observations

* GPT-OSS-120B achieved the highest correctness score.
* GPT-OSS-20B produced more concise responses.
* Larger models generally improved answer quality but tended to generate longer outputs.
* LangSmith made it easy to compare experiments and visualize evaluation metrics.

## Key Learnings

* Building custom evaluators for LLM assessment
* Using LangSmith datasets and experiments
* Performing model benchmarking
* Comparing response quality across multiple LLMs
* Understanding trade-offs between accuracy and conciseness

