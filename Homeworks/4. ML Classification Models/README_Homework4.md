# 📊 Classification Model Benchmarking -- Telecom Marketing Dataset

## 🔎 Project Summary

This project benchmarks multiple supervised classification algorithms on
a telecom marketing dataset (`tele.csv`) to predict client subscription
outcomes.

The workflow includes rigorous preprocessing, feature engineering, class
imbalance handling, and comparative model evaluation.

The objective is to evaluate how different algorithms perform under
identical preprocessing and train/test conditions.

------------------------------------------------------------------------

## 🎯 Problem Statement

Given structured customer and campaign data, predict whether a client
will subscribe to a term deposit (`y ∈ {0,1}`).

This is a binary classification problem with significant class
imbalance.

------------------------------------------------------------------------

## 🗂 Dataset

-   Source: `tele.csv`
-   Observations: \~41,000+
-   Target variable: `y`
-   Type: Structured, mixed categorical and numerical features
-   Imbalance: Strong skew toward negative class

------------------------------------------------------------------------

## 🧹 Data Engineering Pipeline

### 1️⃣ Feature Cleaning

-   Removed:
    -   `duration` (data leakage risk)
    -   `X` (index column)
-   Re-encoded `pdays`:
    -   `999` → 0 (never contacted)
    -   `<999` → 1 (previously contacted)

------------------------------------------------------------------------

### 2️⃣ Encoding

Categorical variables were transformed using:

``` r
model.matrix(~ . - 1, tele_data)
```

-   One-hot encoding
-   No intercept
-   Explicit removal of redundant dummy column (`jobunknown`)
-   Binary target reconstructed as `y`

------------------------------------------------------------------------

### 3️⃣ Feature Scaling

Min-Max normalization applied:

x' = (x - min(x)) / (max(x) - min(x))

Scaling was required for: - KNN - Neural Networks - SVM

Tree-based models were trained on unscaled encoded data.

------------------------------------------------------------------------

### 4️⃣ Train/Test Split

-   50/50 split
-   `set.seed(666)` for reproducibility
-   Same split used across all models for fair comparison

------------------------------------------------------------------------

## ⚖ Class Imbalance Handling

SMOTE (Synthetic Minority Oversampling Technique) was applied using:

``` r
library(smotefamily)
```

Rationale: - Improve recall for minority class - Reduce bias toward
majority prediction - Stabilize neural network and KNN performance

------------------------------------------------------------------------

## 🤖 Models Implemented

  Model                    Package         Notes
  ------------------------ --------------- -----------------------------
  Decision Tree            `C50`           C5.0 algorithm
  Support Vector Machine   `kernlab`       Kernel-based classification
  K-Nearest Neighbors      `class`         Distance-based classifier
  Neural Network           `neuralnet`     Feed-forward architecture
  Logistic Regression      (if included)   Baseline linear model

------------------------------------------------------------------------

## 📈 Evaluation Metrics

Performance assessed using:

-   Confusion Matrix
-   Accuracy
-   Precision
-   Recall
-   F1-score

Primary focus: - Compare generalization performance - Assess sensitivity
to imbalance - Identify trade-offs between interpretability and
predictive power

------------------------------------------------------------------------

## 📁 Project Structure

    ├── tele.csv
    ├── Homework4.R / Homework4.Rmd
    ├── README.md

------------------------------------------------------------------------

## 🚀 How to Reproduce

1.  Place `tele.csv` in working directory.

2.  Install required packages:

    ``` r
    install.packages(c("C50", "caret", "neuralnet", "class", "kernlab", "smotefamily"))
    ```

3.  Run the script sequentially.

------------------------------------------------------------------------

## 📌 Skills Demonstrated

-   Supervised learning (classification)
-   Feature engineering
-   Encoding and scaling techniques
-   Class imbalance mitigation (SMOTE)
-   Model benchmarking
-   Reproducible experimentation
-   Applied ML in R

------------------------------------------------------------------------

## 👤 Author

Beatriz Wahle\
November 2024
