# Classification Model Lab

This repository contains my experiments with classification models in machine learning.

The goal of this project is to practice training different classification models, evaluate their performance, and track experiments using MLflow.

This project uses the built-in Wine dataset from Scikit-learn, converted to a Pandas DataFrame for classification experiments.

## What this repository includes

- Built-in datasets loaded from Scikit-learn (Wine dataset)
- Data visualization and preparation
- Careful Train/Test splitting and scaling to avoid data leakage
- Classification model training and evaluation
- MLflow experiment tracking
- Comparison between different classification models

## Classification models I plan to test

- Logistic Regression
- Ridge Classifier
- KNN Classifier
- SVM Classifier
- Decision Tree Classifier
- Random Forest Classifier 🏆
- Gradient Boosting Classifier
- Naive Bayes Classifier 🏆

## Planned Methodology

Some models, such as Logistic Regression, Ridge Classifier, KNN, and SVM, usually benefit from feature scaling. For these models, a `StandardScaler` is fitted only on the training data and then used to transform both the training and test sets.

Tree-based models, such as Decision Tree, Random Forest, and Gradient Boosting, usually do not require feature scaling and can be tested on the prepared data directly.

Gaussian Naive Bayes will also be tested as a simple and fast baseline classifier.

The experiments are split into two separate Jupyter Notebooks:
- `classification_model_comparison_with_scaling.ipynb`: Tests models that require feature scaling (Logistic Regression, Ridge, KNN, SVC).
- `classification_model_comparison_without_scaling.ipynb`: Tests tree-based and probabilistic models that do not require scaling (Decision Tree, Random Forest, Gradient Boosting, Naive Bayes).

## Evaluation Metrics

I evaluate the models using classification metrics such as:

- Accuracy
- Precision
- Recall
- F1-score

## Tools and libraries

- Python
- Pandas
- NumPy
- Scikit-learn
- MLflow
- Matplotlib
- Seaborn

## Tracking Experiments with MLflow

This project uses MLflow to track and compare different classification models.

MLflow helped me save:

- Model parameters
- Evaluation metrics
- Trained model artifacts
- Experiment history

## How to view the MLflow Dashboard

To see the model comparisons, metrics, and parameters, run:

```bash
uv run mlflow ui --port 5000
```
If the server instantly crashes on Windows, run:

```bash
uv run mlflow ui --port 5000 --workers 1
```

Then open:

```bash
http://127.0.0.1:5000
```
## Important Git Note

The following MLflow tracking files should not be pushed to GitHub:

```
mlflow.db
mlruns/
```

They should be added to .gitignore.

## Purpose

This project is part of my learning journey toward becoming an MLOps engineer.

I will use this repository to improve my understanding of classification models, experiment tracking, preventing data leakage during preprocessing, and building better machine learning workflows.