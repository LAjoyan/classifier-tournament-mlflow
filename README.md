# Classification Model Lab

This repository will contain my experiments with classification models in machine learning.

The goal of this project is to practice training different classification models, evaluate their performance, and track experiments using MLflow.

This project will use CSV datasets loaded with Pandas for classification experiments.

## What this repository will include

- CSV datasets
- Data visualization and preparation
- Scikit-learn Pipeline integration for robust preprocessing
- Classification model training and evaluation
- MLflow experiment tracking
- Comparison between different classification models

## Classification models I plan to test

- Logistic Regression
- Ridge Classifier
- KNN Classifier
- SVM Classifier
- Decision Tree Classifier
- Random Forest Classifier
- Gradient Boosting Classifier
- Naive Bayes Classifier

## Planned Methodology

To compare the models fairly and avoid data leakage, I plan to use scikit-learn Pipelines.

Some models, such as Logistic Regression, Ridge Classifier, KNN, and SVM, usually benefit from feature scaling. These models will be tested with a scaler inside the pipeline.

Tree-based models, such as Decision Tree, Random Forest, and Gradient Boosting, usually do not require feature scaling and can be tested on the prepared data directly.

Naive Bayes will also be tested as a simple and fast baseline classifier.

## Evaluation Metrics

I plan to evaluate the models using classification metrics such as:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

## Tools and libraries

- Python
- Pandas
- NumPy
- Scikit-learn
- MLflow
- Matplotlib
- Seaborn

## Tracking Experiments with MLflow

This project will use MLflow to track and compare different classification models.

MLflow will help me save:

- Model parameters
- Evaluation metrics
- Trained model artifacts
- Experiment history

## How to view the MLflow Dashboard

To see the model comparisons, metrics, and parameters, run:

```python
uv run mlflow ui --port 5000
```
If the server instantly crashes on Windows, run:

```python
uv run mlflow ui --port 5000 --workers 1
```

Then open:

```python
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

I will use this repository to improve my understanding of classification models, experiment tracking, preventing data leakage with pipelines, and building better machine learning workflows.