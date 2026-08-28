# Awesome Tracking Performance Drift in Large Language Models

> A curated research repository on tracking, measuring, evaluating, and understanding performance and behavioral drift in Large Language Models across successive version updates.

## Contents

- [Overview](#overview)
- [AI-Assisted Research Paper](#ai-assisted-research-paper)
- [Citation Integrity Audit](#citation-integrity-audit)
- [Curated Research Papers](#curated-research-papers)
  - [Survey and Review Papers](#survey-and-review-papers)
  - [Foundational Papers](#foundational-papers)
  - [Recent Research Papers](#recent-research-papers)
  - [Methods and Algorithms](#methods-and-algorithms)
  - [Applications](#applications)
  - [Evaluation Methods and Benchmarks](#evaluation-methods-and-benchmarks)
- [Datasets](#datasets)
- [Tools and Libraries](#tools-and-libraries)
- [GitHub Implementations](#github-implementations)
- [Tutorials and Learning Resources](#tutorials-and-learning-resources)
- [License](#license)

---

## Overview

Large Language Models (LLMs) are increasingly deployed as continuously updated services rather than static model artifacts. A model identifier may remain unchanged while the underlying parameters, post-training procedures, safety policies, routing mechanisms, system prompts, or inference configurations change. As a result, a deployed LLM can exhibit measurable performance and behavioral changes across successive releases even when users perceive it as the same model.

This repository focuses on the problem of **tracking performance drift in LLMs across successive version updates**. The central objective is to move beyond single-point benchmark comparisons and study how an LLM evolves over time.

Performance drift can occur across multiple dimensions, including:

- Capability
- Reasoning
- Mathematical performance
- Coding performance
- Instruction following
- Safety
- Reliability
- Calibration
- Robustness
- Hallucination behavior
- Output structure
- Interaction behavior
- Efficiency
- Latency
- Token consumption
- Cost

The research paper associated with this repository distinguishes model-version drift from data drift, concept drift, and evaluation drift. It also examines benchmark contamination, benchmark saturation, prompt sensitivity, stochasticity, evaluator instability, and the difficulty of attributing an observed change to a specific cause.

A major conclusion of the research is that longitudinal evaluation should use **multidimensional drift profiles** instead of relying only on scalar benchmark differences. A robust evaluation protocol should preserve immutable evaluation cohorts, maintain temporally fresh cohorts, repeat stochastic tests, report uncertainty and effect sizes, archive prompts and outputs, and distinguish genuine capability changes from evaluation artifacts.

The broader goal is to establish reproducible approaches for monitoring LLM behavior throughout its lifecycle.

---

## AI-Assisted Research Paper

### Tracking Performance Drift in Large Language Models Across Successive Version Updates

The research paper studies how Large Language Models can change across successive version updates and proposes a methodological framework for measuring and monitoring such changes.

The paper covers:

- Static versus longitudinal evaluation
- Model-version drift
- Data drift
- Concept drift
- Evaluation drift
- Multidimensional capability measurement
- Benchmark contamination
- Benchmark saturation
- Prompt sensitivity
- Stochasticity
- Evaluator instability
- Human-preference evaluation
- LLM-as-a-judge evaluation
- Dynamic benchmarks
- Real-world task evaluation
- Application-grounded evaluation
- Statistical uncertainty
- Reproducibility
- Drift attribution
- Longitudinal monitoring
- Research gaps and future directions

The paper specifically argues that an LLM should be evaluated as a changing socio-technical system rather than simply as a static neural-network checkpoint.

The proposed evaluation framework uses four evaluation cohorts:

1. **Immutable regression set**
2. **Fresh temporal set**
3. **Behavioral probe set**
4. **Production-like sample**

The paper also proposes monitoring dimensions such as correctness, reasoning, instruction following, safety, robustness, hallucination, calibration, output format, efficiency, and behavioral distribution.

**Research Paper:**  
[AI-Assisted Research Paper](paper/AI_Assisted_Research_Paper.pdf)

---

## Citation Integrity Audit

The research paper was accompanied by a systematic citation-integrity audit.

The audit was performed to determine whether AI-generated references were genuine, correctly identified, associated with the supplied identifiers, and appropriate for the claims for which they were cited.

### Audit Profile

| Item | Result |
|---|---:|
| AI tool used | ChatGPT |
| Model/version shown | GPT-5.6 Luna |
| Date of paper generation | 21 August 2026 |
| Total references in paper | 23 |
| DOI available | 18 |
| PMID available without DOI | 0 |
| arXiv ID available without DOI/PMID | 0 |
| URL-only references | 2 |
| No persistent identifier | 3 |
| References selected for systematic audit | 10 |

The audit selected references systematically using the required sampling procedure rather than choosing only suspicious-looking citations.

### Audit Results

| Classification | Count |
|---|---:|
| A — Verified | 10 |
| B — Wrong Metadata | 0 |
| C — Frankenstein | 0 |
| D — Fabricated | 0 |
| E — Identifier Mismatch | 0 |
| Total Audited | 10 |

### Scores

- **Authenticity Score:** 100/100
- **Prediction Accuracy:** 100%

All ten audited references were classified as genuine and the supplied bibliographic information and identifiers were found to correspond to the cited publications.

The audit also found that the cited claims in the sampled references were consistent with the scope and findings of the corresponding publications.

> **Important:** The 100/100 result applies to the systematically audited sample of 10 references. It does not mean that every one of the 23 references in the paper was individually audited.

The audit demonstrates why AI-generated citations must be independently checked rather than accepted solely because they contain realistic authors, venues, DOI identifiers, or arXiv identifiers.

**Citation Integrity Audit:**  
[Citation Integrity Audit](citation-audit/Citation_Integrity_Audit.pdf)

---

# Curated Research Papers

# Curated Research Papers

The following papers represent key research relevant to LLM evaluation, benchmark reliability, model behavior, and performance drift.

## 1. How Is ChatGPT's Behavior Changing Over Time?

**Chen, L., Zaharia, M., & Zou, J. (2024)**

Directly investigates changes in ChatGPT behavior over time and is one of the most directly relevant works for longitudinal LLM evaluation.

[DOI](https://doi.org/10.1162/99608f92.5317da47)

---

## 2. Holistic Evaluation of Language Models

**Liang, P., Bommasani, R., Lee, T., et al. (2022)**

Introduces HELM, a framework for evaluating language models across multiple scenarios and metrics.

[DOI](https://doi.org/10.48550/arXiv.2211.09110)

---

## 3. Measuring Massive Multitask Language Understanding

**Hendrycks, D., Burns, C., Basart, S., et al. (2021)**

Introduces MMLU, a widely used benchmark for evaluating knowledge and reasoning across multiple subjects.

[arXiv](https://arxiv.org/abs/2009.03300)

---

## 4. MMLU-Pro

**Wang, Y., Ma, X., Zhang, G., et al. (2024)**

Introduces a more challenging and robust version of MMLU for evaluating modern language models.

[DOI](https://doi.org/10.48550/arXiv.2406.01574)

---

## 5. LiveCodeBench

**Jain, N., Han, K., Gu, A., et al. (2025)**

Presents a contamination-resistant coding benchmark using newly released programming problems.

[DOI](https://doi.org/10.48550/arXiv.2403.07974)

---

## 6. SWE-bench

**Jimenez, C. E., Yang, J., Wettig, A., et al. (2024)**

Evaluates language models on real-world GitHub software-engineering issues.

[DOI](https://doi.org/10.48550/arXiv.2310.06770)

---

## 7. Judging LLM-as-a-Judge with MT-Bench and Chatbot Arena

**Zheng, L., Chiang, W.-L., Sheng, Y., et al. (2023)**

Investigates LLM-based evaluation and identifies important biases and reliability considerations.

[DOI](https://doi.org/10.52202/075280-2020)

---

## 8. Are Emergent Abilities of Large Language Models a Mirage?

**Schaeffer, R., Miranda, B., & Koyejo, S. (2023)**

Examines how evaluation methods and metrics can affect apparent changes in model capabilities.

[DOI](https://doi.org/10.48550/arXiv.2304.15004)

---


# Datasets

The following datasets and benchmarks are directly relevant to the research topic because they provide evaluation tasks that can be used to compare LLM versions.

## 1. MMLU

**Source:** Hendrycks et al.

**Purpose:**  
Measures multitask language understanding across 57 subjects.

**Application to performance drift:**  
Can be used as a fixed evaluation cohort for comparing model versions.

**Limitation:**  
Static benchmarks can become saturated or contaminated over time.

**Official resource:**  
[Hendrycks MMLU repository](https://github.com/hendrycks/test)

---

## 2. GSM8K

**Source:** Cobbe et al.

**Purpose:**  
Evaluates mathematical reasoning using grade-school mathematics word problems.

**Application to performance drift:**  
Can be used to monitor mathematical reasoning changes between model versions.

**Limitation:**  
As a fixed benchmark, it may be affected by benchmark aging or contamination.

**Official resource:**  
[OpenAI GSM8K repository](https://github.com/openai/grade-school-math)

---

## 3. LiveCodeBench

**Source:** Jain et al.

**Purpose:**  
Provides contamination-resistant coding evaluation using newly released programming problems.

**Application to performance drift:**  
Its temporal design makes it particularly suitable for measuring coding performance over successive model versions.

**Official resource:**  
[LiveCodeBench repository](https://github.com/LiveCodeBench/LiveCodeBench)

---

## 4. MMLU-Pro

**Source:** Wang et al.

**Purpose:**  
Provides a more challenging and robust version of MMLU.

**Application to performance drift:**  
Useful for evaluating whether apparent improvements or regressions remain visible on a more difficult benchmark.

---

## 5. WildBench

**Source:** Lin et al.

**Purpose:**  
Uses challenging tasks derived from real user interactions.

**Application to performance drift:**  
Useful for measuring changes that may not appear on conventional academic benchmarks.

---

## 6. LiveBench

**Purpose:**  
Provides a continuously updated benchmark designed to limit test-set contamination.

**Application to performance drift:**  
Its monthly release of new questions makes it relevant to temporal and contamination-resistant evaluation.

**Official resource:**  
[LiveBench repository](https://github.com/LiveBench/LiveBench)

---

# Tools and Libraries

## 1. EleutherAI Language Model Evaluation Harness

A unified framework for evaluating generative language models across a large collection of evaluation tasks.

**Relevant features:**

- Standardized evaluation tasks
- Custom tasks and metrics
- Local model evaluation
- API-based model evaluation
- Reproducible evaluation configurations

**Project:**  
[EleutherAI/lm-evaluation-harness](https://github.com/EleutherAI/lm-evaluation-harness)

---

## 2. Stanford HELM

Holistic Evaluation of Language Models is an open-source framework for holistic, reproducible, and transparent evaluation of foundation models.

**Relevant features:**

- Standardized benchmarks
- Multiple evaluation metrics
- Model comparison
- Prompt and response inspection
- Leaderboards

**Project:**  
[Stanford CRFM HELM](https://github.com/stanford-crfm/helm)

---

## 3. Hugging Face Evaluate

A library for evaluating machine-learning models and datasets using reusable evaluation modules.

**Relevant features:**

- Metrics
- Comparisons
- Measurements
- Reusable evaluation modules
- Metric documentation

**Project:**  
[Hugging Face Evaluate](https://github.com/huggingface/evaluate)

---

## 4. DeepEval

An open-source LLM evaluation framework designed for evaluating LLM systems and applications.

**Relevant features:**

- LLM-as-a-judge metrics
- Hallucination evaluation
- Answer relevancy
- Task completion
- RAG evaluation
- Regression testing

**Project:**  
[Confident AI DeepEval](https://github.com/confident-ai/deepeval)

---

## 5. Promptfoo

A CLI and library for evaluating and red-teaming LLM applications.

**Relevant features:**

- Prompt evaluation
- Model comparison
- Regression testing
- Red teaming
- CI/CD integration
- RAG evaluation

**Project:**  
[Promptfoo](https://github.com/promptfoo/promptfoo)

---

## 6. Ragas

An evaluation framework focused on evaluating LLM and RAG applications.

**Relevant applications:**

- RAG evaluation
- Faithfulness
- Context relevance
- Answer relevance
- Application-level evaluation

**Project:**  
[Ragas](https://github.com/explodinggradients/ragas)

---

# GitHub Implementations

This section collects existing open-source implementations that can be used to perform or support longitudinal LLM evaluation.

## 1. EleutherAI / lm-evaluation-harness

**What it implements:**  
A unified evaluation framework for language models and a large number of standardized tasks.

**Why it is relevant:**  
The same evaluation suite can be executed against different model versions, making it useful for release-to-release comparison.

[GitHub Repository](https://github.com/EleutherAI/lm-evaluation-harness)

---

## 2. Stanford CRFM / HELM

**What it implements:**  
Holistic evaluation infrastructure for foundation models.

**Why it is relevant:**  
Its multidimensional evaluation approach directly supports the research paper's recommendation to move beyond single benchmark scores.

[GitHub Repository](https://github.com/stanford-crfm/helm)

---

## 3. OpenAI / Evals

**What it implements:**  
An evaluation framework for testing model behavior using evaluation examples and custom evaluation implementations.

**Why it is relevant:**  
Custom evaluations can be used to create regression suites for successive model releases.

[GitHub Repository](https://github.com/openai/evals)

---

## 4. LiveCodeBench

**What it implements:**  
A contamination-resistant coding benchmark that continuously collects newly released programming problems.

**Why it is relevant:**  
It demonstrates how temporal evaluation can be incorporated into practical LLM benchmarking.

[GitHub Repository](https://github.com/LiveCodeBench/LiveCodeBench)

---

## 5. LiveBench

**What it implements:**  
A continuously updated benchmark designed around contamination-resistant and objective evaluation.

**Why it is relevant:**  
It provides an example of a benchmark that changes over time rather than remaining completely static.

[GitHub Repository](https://github.com/LiveBench/LiveBench)

---

## 6. MMLU

**What it implements:**  
Evaluation code and data associated with the MMLU benchmark.

**Why it is relevant:**  
Provides a well-established fixed benchmark for longitudinal comparisons.

[GitHub Repository](https://github.com/hendrycks/test)

---

## 7. DeepEval

**What it implements:**  
Testing and evaluation infrastructure for LLM applications.

**Why it is relevant:**  
Supports regression testing and application-level evaluation, which are important components of practical drift monitoring.

[GitHub Repository](https://github.com/confident-ai/deepeval)

---

# Tutorials and Learning Resources

## 1. lm-evaluation-harness Documentation

Provides installation instructions, CLI usage, configuration, Python API information, and task documentation.

**Useful for:**  
Learning how to build and execute standardized LLM evaluation experiments.

[Documentation and Repository](https://github.com/EleutherAI/lm-evaluation-harness)

---

## 2. lm-evaluation-harness New Task Guide

Explains how to create and evaluate custom benchmark tasks.

**Useful for:**  
Building custom evaluation datasets for longitudinal regression testing.

[New Task Guide](https://github.com/EleutherAI/lm-evaluation-harness/blob/main/docs/new_task_guide.md)

---

## 3. Stanford HELM Documentation

Provides instructions for installing and running HELM and using its evaluation infrastructure.

**Useful for:**  
Learning holistic and reproducible LLM evaluation.

[HELM Documentation](https://github.com/stanford-crfm/helm)

---

## 4. Hugging Face Evaluate Documentation

Provides practical instructions for loading metrics, evaluation modules, comparisons, and measurements.

**Useful for:**  
Learning how to construct reusable evaluation pipelines.

[Evaluate Documentation](https://github.com/huggingface/evaluate)

---

## 5. Promptfoo Documentation

Provides guides for testing prompts, agents, RAG applications, and model behavior.

**Useful for:**  
Learning practical regression testing and model comparison workflows.

[Promptfoo Documentation](https://github.com/promptfoo/promptfoo)

---

## 6. LiveCodeBench Documentation

Provides information about the benchmark, data, evaluation setup, and temporal coding evaluation.

**Useful for:**  
Understanding contamination-resistant and time-aware benchmark construction.

[LiveCodeBench Documentation](https://github.com/LiveCodeBench/LiveCodeBench)

---

## 7. LiveBench Documentation

Provides information about the continuously updated benchmark, data, evaluation process, and benchmark releases.

**Useful for:**  
Understanding dynamic benchmark construction and temporal evaluation.

[LiveBench Documentation](https://github.com/LiveBench/LiveBench)

---

# License

The original materials created for this repository, including the repository documentation, are subject to the license specified in the repository's `LICENSE` file.

The research paper and citation-integrity audit uploaded to this repository are the student's own course materials.

Third-party research papers, datasets, software, GitHub repositories, documentation, and other resources remain subject to their respective copyright and license terms.

This repository does **not** redistribute copyrighted research papers belonging to other authors. Where appropriate, it links to publisher pages, DOI records, arXiv records, ACL Anthology pages, or official project repositories.

---
