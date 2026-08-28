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

The research paper contains 23 bibliography entries. The collection below organizes the relevant scholarly works into meaningful research categories.

The instruction sheet requires at least 20 verified scholarly papers and recommends categorizing papers according to research subtopics.

---

## Survey and Review Papers

### 1. Holistic Evaluation of Language Models

**Bommasani, R., Liang, P., & Lee, T. (2023)**  
*Holistic evaluation of language models.*  
Annals of the New York Academy of Sciences, 1525(1), 140–146.

[DOI: 10.1111/nyas.15007](https://doi.org/10.1111/nyas.15007)

Provides a concise discussion of holistic evaluation of language models and supports evaluating models across multiple scenarios and metrics rather than relying on a single capability measure.

---

### 2. Benchmarking Large Language Models Under Data Contamination: A Survey from Static to Dynamic Evaluation

**Chen, S., Chen, Y., Li, Z., Jiang, Y., Wan, Z., He, Y., Ran, D., Gu, T., Li, H., Xie, T., & Ray, B. (2025)**  
*Benchmarking large language models under data contamination: A survey from static to dynamic evaluation.*  
EMNLP 2025, 10080–10098.

[DOI: 10.18653/v1/2025.emnlp-main.511](https://doi.org/10.18653/v1/2025.emnlp-main.511)

Reviews benchmark contamination and the transition from static evaluation toward dynamic evaluation.

---

### 3. Quantifying Reproducibility in NLP and ML

**Belz, A. (2021)**  
*Quantifying reproducibility in NLP and ML.*  
arXiv:2109.01211.

[DOI: 10.48550/arXiv.2109.01211](https://doi.org/10.48550/arXiv.2109.01211)

Provides methodological background for evaluating reproducibility in NLP and machine learning experiments.

---

## Foundational Papers

### 4. Scaling Laws for Neural Language Models

**Kaplan, J., McCandlish, S., Henighan, T., Brown, T. B., Chess, B., Child, R., Gray, S., Radford, A., Wu, J., & Amodei, D. (2020)**  
*Scaling laws for neural language models.*

[DOI: 10.48550/arXiv.2001.08361](https://doi.org/10.48550/arXiv.2001.08361)

Studies relationships between model size, training data, compute, and language-model loss.

---

### 5. An Empirical Analysis of Compute-Optimal Large Language Model Training

**Hoffmann, J., Borgeaud, S., Mensch, A., et al. (2022)**  
*An empirical analysis of compute-optimal large language model training.*  
Advances in Neural Information Processing Systems, 35.

[DOI: 10.52202/068431-2176](https://doi.org/10.52202/068431-2176)

Examines the relationship between model parameters, training data, and compute in large language model training.

---

### 6. Measuring Massive Multitask Language Understanding

**Hendrycks, D., Burns, C., Basart, S., Zou, A., Mazeika, M., Song, D., & Steinhardt, J. (2021)**  
*Measuring massive multitask language understanding.*  
ICLR 2021.

[arXiv: 2009.03300](https://arxiv.org/abs/2009.03300)

Introduces MMLU, a broad benchmark covering 57 tasks across subjects including mathematics, history, computer science, law, and other areas.

---

### 7. Training Verifiers to Solve Math Word Problems

**Cobbe, K., Kosaraju, V., Bavarian, M., Chen, M., Jun, H., Kaiser, L., Plappert, M., Tworek, J., Hilton, J., Nakano, R., Hesse, C., & Schulman, J. (2021)**  
*Training verifiers to solve math word problems.*

[DOI: 10.48550/arXiv.2110.14168](https://doi.org/10.48550/arXiv.2110.14168)

Introduces GSM8K and provides a benchmark for evaluating mathematical reasoning.

---

### 8. Are Emergent Abilities of Large Language Models a Mirage?

**Schaeffer, R., Miranda, B., & Koyejo, S. (2023)**  
*Are emergent abilities of large language models a mirage?*

[DOI: 10.48550/arXiv.2304.15004](https://doi.org/10.48550/arXiv.2304.15004)

Examines how evaluation metrics can influence apparent changes in model capabilities.

---

## Recent Research Papers

### 9. How Is ChatGPT's Behavior Changing Over Time?

**Chen, L., Zaharia, M., & Zou, J. (2024)**  
*How is ChatGPT’s behavior changing over time?*  
Harvard Data Science Review, 6(2).

[DOI: 10.1162/99608f92.5317da47](https://doi.org/10.1162/99608f92.5317da47)

Directly studies changes in GPT-3.5 and GPT-4 behavior over time and provides important evidence for longitudinal LLM evaluation.

---

### 10. Mapping and Measuring the Behavioral Evolution of Large Language Models

**Qiao, D., Ding, C., & Fan, J. (2026)**  
*Mapping and measuring the behavioral evolution of large language models.*

[DOI: 10.48550/arXiv.2608.11027](https://doi.org/10.48550/arXiv.2608.11027)

Studies behavioral evolution across model generations and supports analyzing LLM behavior as a temporal trajectory.

---

### 11. MMLU-Pro: A More Robust and Challenging Multi-Task Language Understanding Benchmark

**Wang, Y., Ma, X., Zhang, G., et al. (2024)**  
*MMLU-Pro: A more robust and challenging multi-task language understanding benchmark.*

[DOI: 10.48550/arXiv.2406.01574](https://doi.org/10.48550/arXiv.2406.01574)

Introduces a more challenging version of MMLU designed to provide more discriminative evaluation.

---

### 12. NEO-BENCH: Evaluating Robustness of Large Language Models with Neologisms

**Zheng, J., Ritter, A., & Xu, W. (2024)**  
*NEO-BENCH: Evaluating robustness of large language models with neologisms.*  
ACL 2024, 13885–13906.

[DOI: 10.18653/v1/2024.acl-long.749](https://doi.org/10.18653/v1/2024.acl-long.749)

Investigates temporal language drift and model performance on emerging neologisms.

---

## Methods and Algorithms

### 13. An Empirical Investigation of Statistical Significance in NLP

**Berg-Kirkpatrick, T., Burkett, D., & Klein, D. (2012)**  
*An empirical investigation of statistical significance in NLP.*  
EMNLP-CoNLL 2012, 995–1005.

[ACL Anthology: D12-1091](https://aclanthology.org/D12-1091/)

Provides statistical methodology relevant to determining whether differences between model versions represent meaningful changes.

---

### 14. The Hitchhiker's Guide to Testing Statistical Significance in Natural Language Processing

**Dror, R., Baumer, G., Shlomov, S., & Reichart, R. (2018)**  
*The hitchhiker’s guide to testing statistical significance in natural language processing.*  
ACL 2018.

Provides practical guidance for statistical significance testing in NLP.

---

### 15. Judging LLM-as-a-Judge with MT-Bench and Chatbot Arena

**Zheng, L., Chiang, W.-L., Sheng, Y., Zhuang, S., Wu, Z., Zhuang, Y., Lin, Z., Li, Z., Li, D., Xing, E. P., Zhang, H., Gonzalez, J. E., & Stoica, I. (2023)**  
*Judging LLM-as-a-judge with MT-Bench and Chatbot Arena.*  
NeurIPS 2023, 46595–46623.

[DOI: 10.52202/075280-2020](https://doi.org/10.52202/075280-2020)

Examines LLM-based judging and identifies biases and reliability issues relevant to automated longitudinal evaluation.

---

### 16. Benchmarking LLM-as-a-Judge for Long-Form Output Evaluation

**Chen, J., Dong, Y., Li, H., Su, W., Zhou, Y., Zhang, M., Liu, Y., & Ai, Q. (2026)**  
*Benchmarking LLM-as-a-judge for long-form output evaluation.*

[DOI: 10.48550/arXiv.2606.01629](https://doi.org/10.48550/arXiv.2606.01629)

Examines the reliability of LLM judges for long-form outputs.

---

## Applications

### 17. SWE-bench: Can Language Models Resolve Real-World GitHub Issues?

**Jimenez, C. E., Yang, J., Wettig, A., Yao, S., Pei, K., Press, O., & Narasimhan, K. (2024)**  
*SWE-bench: Can language models resolve real-world GitHub issues?*  
ICLR 2024.

[DOI: 10.48550/arXiv.2310.06770](https://doi.org/10.48550/arXiv.2310.06770)

Evaluates language models on real-world software-engineering issues and demonstrates application-grounded evaluation.

---

### 18. WildBench: Benchmarking LLMs with Challenging Tasks from Real Users in the Wild

**Lin, B. Y., Deng, Y., Chandu, K., Brahman, F., Ravichander, A., Pyatkin, V., Dziri, N., Le Bras, R., & Choi, Y. (2024)**  
*WildBench: Benchmarking LLMs with challenging tasks from real users in the wild.*

[DOI: 10.48550/arXiv.2406.04770](https://doi.org/10.48550/arXiv.2406.04770)

Uses challenging tasks derived from real user interactions to bridge the gap between academic benchmarks and real-world workloads.

---

### 19. Holistic Evaluation of Language Models

**Liang, P., Bommasani, R., Lee, T., et al. (2022)**  
*Holistic evaluation of language models.*

[DOI: 10.48550/arXiv.2211.09110](https://doi.org/10.48550/arXiv.2211.09110)

Introduces HELM, a framework for standardized and multidimensional evaluation of language models.

---

## Evaluation Methods and Benchmarks

### 20. LiveCodeBench: Holistic and Contamination-Free Evaluation of Large Language Models for Code

**Jain, N., Han, K., Gu, A., Li, W.-D., Yan, F., Zhang, T., Wang, S., Solar-Lezama, A., Sen, K., & Stoica, I. (2025)**  
*LiveCodeBench: Holistic and contamination-free evaluation of large language models for code.*  
ICLR 2025.

[DOI: 10.48550/arXiv.2403.07974](https://doi.org/10.48550/arXiv.2403.07974)

Uses newly released coding problems and temporal evaluation to reduce contamination and evaluate coding capabilities.

---

### 21. How Contaminated Is Your Benchmark? Measuring Dataset Leakage in Large Language Models with Kernel Divergence

**Choi, H. K., Khanov, M., Wei, H., & Li, Y. (2025)**  
*How contaminated is your benchmark? Measuring dataset leakage in large language models with Kernel Divergence.*  
ICML 2025, PMLR 267, 10666–10682.

Studies methods for measuring benchmark leakage and contamination.

---

### 22. Investigating Data Contamination in Modern Benchmarks for Large Language Models

**Chen, C., Zhao, Y., Tang, X., Gerstein, M., & Cohan, A. (2024)**  
*Investigating data contamination in modern benchmarks for large language models.*  
NAACL-HLT 2024.

[ACL Anthology](https://aclanthology.org/2024.naacl-long.482/)

Investigates benchmark contamination in modern LLM evaluation.

---

### 23. An Empirical Investigation of Statistical Significance in NLP

**Berg-Kirkpatrick, T., Burkett, D., & Klein, D. (2012)**  
*An empirical investigation of statistical significance in NLP.*  
EMNLP-CoNLL 2012.

[ACL Anthology: D12-1091](https://aclanthology.org/D12-1091/)

Provides statistical methods relevant to comparing model versions.

> **Note:** This paper is already listed under Methods and Algorithms. The duplication here reflects the benchmark/evaluation relevance of the work; the repository's detailed `references/references.md` should contain each paper only once.

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
