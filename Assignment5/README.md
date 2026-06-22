# K-means Clustering Implementation

This project implements K-means clustering and compares the custom implementation against scikit-learn’s implementation on the same synthetic dataset. It is linked from the portfolio card “Machine Learning Modeling, Evaluation, and Feature Engineering.”

## Project signal

This project demonstrates algorithm implementation, clustering validation, and comparison against a known library implementation.

It supports the portfolio signal that I can move beyond simply calling a package function: I can implement a core algorithm, inspect its behavior, validate its output, and compare it against a standard implementation.

## What the project does

The project uses a synthetic two-feature dataset containing 5,000 data objects. The workflow implements K-means clustering, evaluates cluster quality using sum-of-squared-errors distortion, uses the elbow method to select an appropriate number of clusters, and compares the custom implementation to scikit-learn.

The report found that the best K value for the dataset was 5. The custom implementation and the scikit-learn implementation produced matching clustering behavior. The adjusted Rand index was 1.0, indicating perfect alignment between the two label sets, and the total SSE was 40158.49 for both models.

## Repository navigation

Core files:

- `ML_Assignment5.py` — custom K-means implementation, clustering workflow, comparison logic, and plotting/output generation.
- `data_2D.txt` — synthetic two-dimensional dataset used for clustering.
- `ML_Assignment_5_JBennett.pdf` — written report explaining the objective, approach, results, and conclusion.
- `UHart_25Fall_MachineLearning_HW5.pdf` — assignment prompt / project requirements.

## How to review

Recommended review path:

1. Read the report for the objective, method, and validation results.
2. Open `ML_Assignment5.py` and locate the custom K-means implementation.
3. Review how SSE is calculated and used for the elbow method.
4. Compare the custom implementation results against the scikit-learn comparison in the script/report.

## Reproduction notes

From the `Assignment5` directory, the main workflow is contained in:

```bash
python3 ML_Assignment5.py
```

A fresh environment may require numpy, pandas, scikit-learn, matplotlib, and related scientific Python dependencies.


