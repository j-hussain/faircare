# FAIRcare - Fairness and AI Interpretability for Responsible medical care

**FAIRcare** is an independent research project that explores algorithmic fairness and model explainability in healthcare-related machine learning systems. It integrates state-of-the-art tools including SHAP, Fairlearn, and IBM’s AI Fairness 360 to audit, interpret, and mitigate potential biases in predictive models. The project applies these tools to clinical datasets with the goal of improving transparency and trust in ML-driven diagnostic systems—particularly in addressing racial and demographic disparities in outcomes.

---

## Project Motivation

With the advent of commercial machine learning, healthtech companies are increasingly using ML models for clinical decision-making. Medical datasets are often imbalanced or biased, resulting in unfair or opaque model behavior, especially for underrepresented groups.

This project aims to:
- Quantify the extent of bias across demographic subgroups
- Improve model interpretability for both developers and clinicians
- Explore mitigation strategies that reduce disparities without compromising model validity

---

## Repository Overview

| Folder | Description |
|--------|-------------|
| `data/` | Preprocessed and synthetic datasets for experimentation |
| `notebooks/` | Executable Marimo notebooks implementing the full analysis pipeline |
| `models/` | Baseline classifiers (e.g., logistic regression, XGBoost) used for evaluation |
| `explainability/` | SHAP-based global and local feature attribution visualizations |
| `fairness/` | Metrics and mitigation implementations using Fairlearn and AIF360 |
| `report/` | Research report to serve as a discussion of results |

---

## Tools and Libraries

- [SHAP](https://github.com/slundberg/shap) – Model interpretability and attribution
- [Fairlearn](https://fairlearn.org/) – Fairness metrics and bias mitigation techniques
- [AI Fairness 360](https://aif360.mybluemix.net/) – Fairness auditing toolkit and clinical datasets
- [Marimo](https://github.com/marimo-team/marimo) – Interactive notebook interface for code + documentation

---

## Key Features

- Evaluation of model performance across demographic groups
- Comparison of fairness metrics (e.g., demographic parity, equalized odds)
- Application of post-processing and reweighting mitigation algorithms
- SHAP-based feature attribution analysis to assess transparency
- Integration of interpretability with fairness metrics for cross-validation

# FAIRCARE: Project Development Checklist

This checklist outlines the development workflow for the FAIRCARE project, which explores fairness and interpretability in clinical AI systems. The structure follows a research-oriented methodology and emphasizes reproducibility, scientific rigor, and clarity of presentation.

---

# Development Plan

## Phase 1: Project Setup

- [ ] Define the scope of the research problem
  - [ ] Focus: diagnostic bias in healthcare AI (e.g., diabetes classification)
  - [ ] Use case justification: disparities in BAME patient outcomes
- [ ] Select datasets
  - [ ] Acquire and preprocess **MIMIC-III Light** and/or **PhysioNet** datasets
  - [ ] Ensure compliance with license/data usage agreements
- [ ] Set up development environment
  - [ ] Create virtual environment
  - [ ] Install dependencies (`shap`, `fairlearn`, `aif360`, and install relevant data science dependencies)
  - [ ] Configure Marimo for interactive notebooks
- [ ] Initialize GitHub repository and `README.md`

---

## Phase 2: Baseline Modeling

- [ ] Clean and preprocess dataset
- [ ] Train baseline classifiers
- [ ] Evaluate baseline performance
- [ ] Document model selection rationale

---

## Phase 3: Explainability Analysis

- [ ] Integrate SHAP into the pipeline
  - [ ] Compute global feature importances
  - [ ] Compute local explanations for individual predictions
  - [ ] Compare SHAP results across demographic subgroups (e.g., race, age, gender)
- [ ] Generate interpretability visualizations
  - [ ] Summary plots
  - [ ] Dependence plots
  - [ ] Waterfall/force plots for selected samples
- [ ] Document SHAP findings and interpretability insights

---

## Phase 4: Fairness Auditing and Mitigation

- [ ] Integrate Fairlearn into the pipeline
  - [ ] Compute fairness metrics (e.g., demographic parity difference, equalized odds)
  - [ ] Visualize group-level disparities in outcomes
- [ ] Integrate AI Fairness 360
  - [ ] Cross-validate fairness metrics using AIF360
  - [ ] Explore additional mitigation techniques
- [ ] Apply mitigation techniques and retrain models
- [ ] Compare pre- and post-mitigation performance and fairness
- [ ] Document trade-offs between fairness and accuracy
