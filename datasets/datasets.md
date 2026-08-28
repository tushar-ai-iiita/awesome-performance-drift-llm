# Datasets and Benchmarks

This document contains datasets and benchmarks relevant to tracking performance and behavioral drift in Large Language Models (LLMs) across successive version updates.

These resources represent different dimensions of LLM evaluation, including general knowledge and reasoning, mathematical reasoning, software engineering, and contamination-resistant temporal evaluation.

---

## 1. MMLU

**Full Name:** Measuring Massive Multitask Language Understanding

**Source:** Hendrycks et al. (2021)

**Description:**  
MMLU is a broad benchmark for evaluating language-model knowledge and reasoning across 57 subjects.

**Application:**  
MMLU can be used as a fixed evaluation cohort for comparing the performance of successive LLM versions. Because it covers many subjects, it can help identify whether an update produces improvements or regressions across different capability areas.

**Limitation for Drift Tracking:**  
As a static benchmark, MMLU can become less discriminative over time and may be affected by benchmark contamination.

**Research Paper:**  
[Measuring Massive Multitask Language Understanding](https://arxiv.org/abs/2009.03300)

**Dataset / Code:**  
[GitHub Repository](https://github.com/hendrycks/test)

---

## 2. GSM8K

**Full Name:** Grade School Math 8K

**Source:** Cobbe et al. (2021)

**Description:**  
GSM8K is a benchmark for evaluating mathematical reasoning using grade-school mathematics word problems.

**Application:**  
GSM8K can be used to monitor changes in mathematical reasoning performance between successive model versions.

**Limitation for Drift Tracking:**  
Like other fixed benchmarks, GSM8K can become stale or potentially affected by contamination, so it is better used alongside fresh evaluation data.

**Research Paper:**  
[Training Verifiers to Solve Math Word Problems](https://doi.org/10.48550/arXiv.2110.14168)

**Dataset / Code:**  
[GitHub Repository](https://github.com/openai/grade-school-math)

---

## 3. SWE-bench

**Full Name:** SWE-bench: Can Language Models Resolve Real-World GitHub Issues?

**Source:** Jimenez et al. (2024)

**Description:**  
SWE-bench evaluates language models on real-world software-engineering tasks derived from GitHub issues.

**Application:**  
It provides application-grounded evaluation of coding and software-engineering capabilities. Comparing model versions on the same SWE-bench tasks can help identify changes in practical coding performance.

**Research Paper:**  
[SWE-bench Paper](https://doi.org/10.48550/arXiv.2310.06770)

**Dataset / Code:**  
[SWE-bench GitHub Repository](https://github.com/SWE-bench/SWE-bench)

---

## 4. LiveCodeBench

**Full Name:** LiveCodeBench: Holistic and Contamination-Free Evaluation of Large Language Models for Code

**Source:** Jain et al. (2025)

**Description:**  
LiveCodeBench is a coding benchmark designed around newly released programming problems. Problems are associated with their release dates, allowing evaluation using temporally newer tasks.

**Application:**  
LiveCodeBench is particularly relevant to performance-drift research because it supports temporal and contamination-resistant evaluation. It can be used to compare successive model versions on relatively fresh coding problems.

**Research Paper:**  
[LiveCodeBench Paper](https://doi.org/10.48550/arXiv.2403.07974)

**Dataset / Code:**  
[LiveCodeBench GitHub Repository](https://github.com/LiveCodeBench/LiveCodeBench)

---

## Dataset Selection for Longitudinal Evaluation

Different datasets measure different aspects of LLM performance:

| Dataset / Benchmark | Primary Evaluation Dimension | Role in Drift Tracking |
|---|---|---|
| **MMLU** | Knowledge and reasoning | Fixed regression evaluation |
| **GSM8K** | Mathematical reasoning | Capability-specific evaluation |
| **SWE-bench** | Software engineering | Real-world application evaluation |
| **LiveCodeBench** | Coding | Temporal and contamination-resistant evaluation |

A reliable longitudinal evaluation strategy should not depend on a single benchmark. Fixed benchmarks can provide stable comparisons between releases, while temporally fresh benchmarks can help reduce the effects of benchmark contamination and saturation.

The research paper therefore recommends combining **immutable evaluation cohorts** with **fresh temporal cohorts** when monitoring model-version drift.
