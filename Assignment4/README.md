# Support Vector Machine Model Comparison

This project compares support vector machine classifier performance across kernel techniques and hyperparameter combinations. It is linked from the portfolio card “Machine Learning Modeling, Evaluation, and Feature Engineering.”

## Project signal

This project demonstrates systematic model comparison: controlled hyperparameter sweeps, reproducible training calls, stored results, parsed summaries, and interpretation of which modeling choices worked best for a specific dataset.

It supports the portfolio signal that I can compare models and evaluate whether performance comes from a method that is actually appropriate to the data rather than assuming a more complex model is always better.

## What the project does

The workflow uses a synthetic binary-classification dataset generated with scikit-learn. The data was designed to resemble high-variance numeric features similar to those that can come from scientific instrumentation. The project trains SVC models under different kernel, C, and gamma settings, stores results, parses results into interpretable summaries, and identifies the strongest model configuration.

The report concluded that RBF-kernel models performed best overall for this dataset, especially when omitting extreme gamma values. The best-performing configuration was described as an RBF kernel with `C=10` and `Gamma=0.1` / `scale`, while also noting that simply increasing hyperparameter values does not necessarily improve results.

## Repository navigation

Core files:

- `TrainSVC.py` — trains SVC models with argument-driven hyperparameter settings and stores results.
- `generate_models.sh` — runs the training script across the selected hyperparameter combinations.
- `parse_results.py` — parses accumulated results into an interpretable comparison.
- `ML_Assignment4Report_JBennett.pdf` — written report explaining objective, data, approach, results, and conclusion.
- `UHart_25Fall_MachineLearning_HW4_SVM.pdf` — assignment prompt / project requirements.

Existing README:

- `README.md` — original code explanation. This version expands it with project overview, navigation, and portfolio signal language.

## How to review

Recommended review path:

1. Read `ML_Assignment4Report_JBennett.pdf` for the experiment design and conclusions.
2. Inspect `generate_models.sh` to see how the controlled model sweep is executed.
3. Review `TrainSVC.py` to understand how model arguments are passed and results are captured.
4. Review `parse_results.py` to see how the accumulated results are converted into a comparison.

## Reproduction notes

From the `Assignment4` directory, the original workflow is:

```bash
bash generate_models.sh
```

The shell script calls the model-training script across hyperparameter combinations and then calls the parsing script to summarize results.

A fresh environment may require numpy, pandas, scikit-learn, matplotlib, and related scientific Python dependencies.

