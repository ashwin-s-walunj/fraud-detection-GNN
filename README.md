# Explainable Fraud Detection and Alert Prioritization Using Tabular and Graph-Informed Models

This repository contains the implementation pipeline for a master's thesis on fraud detection, graph-informed modeling, alert prioritization, and explainability using the IEEE-CIS Fraud Detection dataset.

## Overview

The project is organized into two layers:

1. core experimental phases that generate frozen raw outputs
2. research-question artifact scripts that generate proposal-facing tables and figures

Core phases:

- `01_data_baselines.py`
- `02_graph_models.py`
- `03_ranking_explainability.py`
- `04_results_reporting.py`

Artifact generators:

- `rq1_artifacts.py`
- `rq2_artifacts.py`
- `rq3_artifacts.py`
- `rq4_artifacts.py`
- `rq5_artifacts.py`
- `rq6_artifacts.py`
- `rq7_artifacts.py`

## Research Scope

The implementation supports:

- temporal fraud detection benchmarking with strong tabular baselines
- graph neural network modeling on heterogeneous transaction graphs
- learnable fraud alert prioritization
- case-level explainability using SHAP, graph evidence, and fusion attribution
- operational evaluation under analyst budget constraints
- complementary-value analysis of graph-informed fusion

## Execution Order

Run the pipeline in this order:

1. `01_data_baselines.py`
2. `02_graph_models.py`
3. `03_ranking_explainability.py`
4. `rq1_artifacts.py` through `rq7_artifacts.py`
5. `04_results_reporting.py`

The core phase files are designed as raw-output producers. The `rq*_artifacts.py` files read the frozen outputs and generate the final proposal-facing tables and figures.

## Dataset

The experiments use the IEEE-CIS Fraud Detection dataset from Kaggle.

This repository does not redistribute:

- raw Kaggle data
- generated model artifacts
- large intermediate outputs

You should place the dataset and frozen outputs in the locations expected by the scripts before execution.

## Environment

Main libraries used in the project include:

- Python 3.10+
- pandas
- numpy
- scikit-learn
- xgboost
- lightgbm
- shap
- matplotlib
- seaborn
- PyTorch
- PyTorch Geometric

The main experiments were developed and executed using Kaggle and local support scripts.

## Reproducibility Notes

The implementation emphasizes:

- temporal train/validation/test splitting
- leakage-safe out-of-fold meta-feature generation
- frozen intermediate outputs
- separate reporting scripts for final artifacts

See the methodology and coverage documents in this repository for more detail on the final thesis-aligned workflow.
