# Random Forest Evaluation Project

This project trains and evaluates a random forest classifier for mobile-phone price-range prediction. It is linked from the portfolio card “Machine Learning Modeling, Evaluation, and Feature Engineering.”

## Project signal

This project demonstrates supervised classification workflow development, practical model evaluation, and communication of performance through standard metrics and visuals.

It supports the portfolio signal that I can train a model, evaluate it with multiple metrics, inspect where it succeeds or fails, and explain why those metrics matter for the use case.

## What the project does

The project uses a real-world mobile-phone attribute dataset to classify phones into price-range categories. The workflow evaluates and cleans the data, prepares train/test splits, trains a random forest classifier, and assesses performance using accuracy, precision, recall, F1-score, confusion matrix, and ROC/AUC curves.

The report concludes that the fitted model performed well overall, while identifying realistic next steps such as improving hyperparameter search ranges, increasing dataset size, and considering class balance.

## Repository navigation

Core files:

- `Assinment1_JBennett.py` — main training/evaluation script for the random forest classifier.
- `load_csv.py` — helper for loading CSV data.
- `data/mobile_price.csv` — source dataset.
- `data/best_model.csv` — stored output describing the best model/result.
- `model_dict.pkl` — serialized model/result dictionary.
- `confusion_matrix.png` — confusion-matrix visualization.
- `AUC_ROC.png` — ROC/AUC visualization.
- `ML-F25_Assignment1-JB.md` — rendered assignment writeup in Markdown form.
- `J_Bennett_ML_assignment1/ML_Assignment1_JBennett.pdf` — written report.
- `UHart_25Fall_MachineLearning_HW1.pdf` — assignment prompt / project requirements.

## How to review

Recommended review path:

1. Read the report or Markdown writeup to understand the objective and results.
2. Inspect `Assinment1_JBennett.py` for the model-training and evaluation workflow.
3. Review `confusion_matrix.png` and `AUC_ROC.png` for the visual model-performance summary.
4. Inspect `data/best_model.csv` and `model_dict.pkl` if reviewing stored outputs.

## Reproduction notes

From the `Assignment1` directory, the main workflow is:

```bash
python3 Assinment1_JBennett.py
```

A fresh environment may require pandas, scikit-learn, matplotlib, seaborn, and related scientific Python dependencies.

