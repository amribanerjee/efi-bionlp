# Evidence Fragmentation Index (EFI)

## Status
Planning

---

# Project Overview

Evidence Fragmentation Index (EFI) is a document-level evaluation metric for BioNLP.

Instead of treating all clinical documents as equally difficult, EFI quantifies how fragmented clinically relevant evidence is within a document. The central hypothesis is that evidence fragmentation represents an overlooked dimension of benchmark difficulty and explains language model failures beyond conventional statistics such as document length or readability.

EFI is model-agnostic, deterministic, and computed directly from the source document without requiring language model inference.

---

# Research Question

Can evidence fragmentation explain medical LLM failures better than traditional document-level statistics?

---

# Core Hypothesis

Clinical reasoning difficulty depends not only on how much evidence exists, but on how dispersed that evidence is throughout a document.

---

# Definition of Evidence

Evidence refers to clinically meaningful concepts including:

- Symptoms
- Diagnoses
- Medications
- Laboratory findings
- Procedures
- Imaging findings
- Clinical observations

---

# Definition of Fragmentation

Evidence fragmentation measures how widely clinically related evidence is distributed throughout a document.

High EFI:

- related evidence scattered
- long-distance dependencies
- interrupted reasoning chains

Low EFI:

- supporting evidence appears together
- short reasoning paths
- localized clinical context

---

# Design Principles

- Model agnostic
- CPU only
- Fully reproducible
- Open-source datasets only
- No API usage
- No GPU requirement

---

# Candidate Datasets

Primary:
- PMC-Patients

Secondary:
- MedQA
- AMQA

---

# Pipeline

Notebook 01
Dataset download and preprocessing

Notebook 02
Clinical evidence extraction

Notebook 03
Document graph construction

Notebook 04
EFI computation

Notebook 05
Baseline document statistics

Notebook 06
Prediction alignment

Notebook 07
Statistical analysis

Notebook 08
Robustness analysis

Notebook 09
Visualizations

Notebook 10
Artifact generation

---

# Baseline Comparisons

Compare EFI against:

- Token count
- Sentence count
- Readability
- Entity count
- Lexical diversity

---

# Statistical Evaluation

Primary outcome:

Does EFI predict model failure?

Analyses:

- Correlation
- Logistic regression
- Mixed-effects models (if appropriate)
- SHAP analysis
- Ablation studies

---

# Success Criteria

EFI should:

- outperform document length
- outperform readability
- remain significant after controlling for confounders
- identify a new benchmark difficulty dimension

---

# Expected Deliverables

- EFI Python package
- Complete reproducible pipeline
- Open-source code
- Figures
- Tables
- CSV outputs
- Documentation

---

# Stretch Goals

- EFI leaderboard stratification
- Benchmark characterization toolkit
- Hugging Face integration
- PyPI package
