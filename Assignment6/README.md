# PyTorch MLP Evaluation Workflow

This project trains and evaluates a PyTorch multi-layer perceptron (MLP) for wine-quality prediction. It is part of the CS569 Machine Learning coursework repository and is linked from the portfolio card “Applied AI / Neural-Network Fine-Tuning and Evaluation.”

## Project signal

This project demonstrates hands-on neural-network workflow implementation: dataset construction, train/test handling, model definition, hyperparameter tuning, loss tracking, model selection, and evaluation visualization.

It supports the portfolio signal that I can connect model setup, training behavior, and output assessment rather than treating a model as a black box.

## What the project does

The workflow uses a wine-quality dataset with physicochemical attributes such as acidity, sugar, chlorides, sulfur dioxide, density, pH, sulphates, alcohol, and quality rating. The project prepares the data for PyTorch, trains MLP models, tunes hyperparameters, evaluates model behavior, and produces artifacts for comparing results.

The report emphasizes that the training process improved model performance under a fixed architecture and identifies next steps such as testing architecture changes and alternative activation functions.

## Repository navigation

Core files:

- `NN_dataset.py` — defines the PyTorch Dataset objects used for train/test data handling.
- `NN_MLP.py` — defines the MLP architecture as a reusable class.
- `NN_train.py` — trains MLP models and supports hyperparameter experimentation.
- `NN_test.py` — evaluates trained models.
- `tune_hyperParams.sh` — runs iterative model training/testing over hyperparameter combinations.
- `analyze_results.py` — analyzes results and generates visuals for the report.
- `test_train_results.csv` — stores model comparison outputs.
- `results.json` — stores structured model/training results.
- `WineQT.csv` — source dataset used for training/evaluation.
- `ML_Assignment6_Report.pdf` — written report describing the objective, data, approach, results, and conclusion.

Generated/output folders referenced by the workflow:

- `models/` — trained MLP model outputs.
- `plots/` — AUC and confusion-matrix visuals used for evaluation.

## How to review

Start with the report for the high-level objective and conclusions, then inspect the scripts in this order:

1. `NN_dataset.py`
2. `NN_MLP.py`
3. `NN_train.py`
4. `NN_test.py`
5. `tune_hyperParams.sh`
6. `analyze_results.py`

This order shows the full workflow from data representation to model definition, training, evaluation, and result analysis.

## Reproduction notes

From the `Assignment6` directory, the original workflow is:

```bash
bash tune_hyperParams.sh
python3 analyze_results.py
```

Depending on local environment and available dependencies, a fresh setup may require installing the Python ML stack used by the assignment, including PyTorch, pandas, scikit-learn, matplotlib/seaborn, and supporting scientific Python packages.

