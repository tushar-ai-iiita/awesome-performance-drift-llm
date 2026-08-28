# Tools and Libraries

This document contains tools and libraries useful for evaluating Large Language Models (LLMs), running benchmarks, comparing model versions, and monitoring performance and behavioral changes over time.

---

## 1. EleutherAI LM Evaluation Harness

**Purpose:**  
A unified framework for evaluating language models across a large collection of standardized benchmarks and evaluation tasks.

**Use in Performance Drift Tracking:**  
Can be used to run the same evaluation tasks across multiple model versions and compare their results.

**Link:**  
https://github.com/EleutherAI/lm-evaluation-harness

---

## 2. Stanford HELM

**Full Name:** Holistic Evaluation of Language Models

**Purpose:**  
A framework for standardized and holistic evaluation of language models across multiple scenarios and metrics.

**Use in Performance Drift Tracking:**  
Its multi-metric evaluation approach can reveal regressions that may not be visible through a single benchmark score.

**Link:**  
https://github.com/stanford-crfm/helm

---

## 3. Hugging Face Evaluate

**Purpose:**  
A library providing reusable evaluation metrics and evaluation modules for machine-learning models and datasets.

**Use in Performance Drift Tracking:**  
Can be used to calculate consistent evaluation metrics across different model versions.

**Link:**  
https://github.com/huggingface/evaluate

---

## 4. OpenAI Evals

**Purpose:**  
An open-source framework for evaluating LLMs and AI systems using customizable evaluation criteria.

**Use in Performance Drift Tracking:**  
Custom evaluations can be created to test specific behaviors or application requirements across model releases.

**Link:**  
https://github.com/openai/evals

---

## 5. Promptfoo

**Purpose:**  
A framework for evaluating prompts, models, and LLM applications.

**Use in Performance Drift Tracking:**  
Supports model comparison and regression testing, making it useful for detecting changes in application behavior after model updates.

**Link:**  
https://github.com/promptfoo/promptfoo

---

## 6. DeepEval

**Purpose:**  
An evaluation framework for testing and evaluating LLM applications.

**Use in Performance Drift Tracking:**  
Can be used to create evaluation tests and monitor changes in LLM application performance.

**Link:**  
https://github.com/confident-ai/deepeval

---

## Tool Selection Summary

| Tool | Primary Use | Relevance to Drift Tracking |
|---|---|---|
| **LM Evaluation Harness** | Standardized benchmarks | Version-to-version comparison |
| **Stanford HELM** | Holistic evaluation | Multi-dimensional drift |
| **Hugging Face Evaluate** | Evaluation metrics | Consistent metric calculation |
| **OpenAI Evals** | Custom evaluations | Application-specific regression testing |
| **Promptfoo** | Model and prompt testing | Regression and comparison |
| **DeepEval** | LLM application evaluation | Continuous evaluation |

---

## Recommended Use

For longitudinal LLM evaluation, these tools can be combined rather than relying on a single framework:

1. Use **LM Evaluation Harness** or **HELM** for standardized benchmark evaluation.
2. Use **Hugging Face Evaluate** for consistent metric computation.
3. Use **OpenAI Evals**, **Promptfoo**, or **DeepEval** for application-specific and behavioral regression tests.
4. Preserve model version, evaluation configuration, prompts, outputs, and scores so that changes can be analyzed across releases.
