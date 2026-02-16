# 📊 Homework 3 -- Predictive Models for Telemarketing Dataset

## 🔎 Project Overview

This project develops and compares three supervised classification
models on a telemarketing dataset (`tele.csv`).

The objective is to predict whether a client subscribes to a term
deposit (`y`) using:

-   Logistic Regression
-   K-Nearest Neighbors (KNN)
-   Artificial Neural Network (ANN)

After evaluating each model individually, their predictions are combined
into an ensemble model using weighted voting.

------------------------------------------------------------------------

## 🎯 Problem Statement

Given structured marketing campaign data, build predictive models to
classify whether a customer subscribes to a term deposit.

This is a **binary classification problem** with notable class
imbalance.

Target variable: - `y ∈ {0,1}` - 0 → No subscription - 1 → Subscription

------------------------------------------------------------------------

## 🗂 Dataset

-   File: `tele.csv`
-   Observations: \~41,000
-   Mixed numerical and categorical variables
-   Includes demographic, economic, and campaign-related features

Important considerations: - `duration` is a post-call variable and
introduces data leakage. - `pdays` uses `999` to indicate customers
never contacted. - Many categorical variables require encoding.

------------------------------------------------------------------------

## 🧹 Data Preprocessing Pipeline

### 1️⃣ Data Cleaning

-   Removed index column `X`
-   Converted character variables to factors
-   Transformed `pdays`:
    -   `999` → 0 (never contacted)
    -   `<999` → 1 (previously contacted)
-   Converted target `y` into binary (0/1)

------------------------------------------------------------------------

### 2️⃣ Feature Scaling

Min-Max normalization applied to numerical variables:

x' = (x - min(x)) / (max(x) - min(x))

Scaling was required because: - KNN is distance-based - Neural Networks
are sensitive to feature magnitude

------------------------------------------------------------------------

### 3️⃣ Encoding

Categorical variables were converted to dummy variables using:

``` r
model.matrix(~ . - 1, data = scaled_data)
```

This ensures compatibility across all models.

------------------------------------------------------------------------

### 4️⃣ Class Imbalance Handling

SMOTE (Synthetic Minority Oversampling Technique) was applied using:

``` r
library(smotefamily)
SMOTE(...)
```

Purpose: - Improve recall of minority class - Reduce bias toward
majority class - Improve ANN and KNN stability

------------------------------------------------------------------------

### 5️⃣ Train/Test Split

-   75% Training
-   25% Testing
-   `set.seed(666)` for reproducibility

------------------------------------------------------------------------

## 🤖 Models Implemented

### 🔹 Logistic Regression

-   Built using `glm(..., family = binomial)`
-   Stepwise feature selection applied
-   Probability threshold adjusted (0.25)

------------------------------------------------------------------------

### 🔹 K-Nearest Neighbors (KNN)

-   Distance-based classifier
-   Requires scaled features
-   Tuned with chosen K value

------------------------------------------------------------------------

### 🔹 Artificial Neural Network (ANN)

-   Single hidden-layer neural network
-   Trained on balanced dataset
-   Sensitive to scaling and class imbalance

------------------------------------------------------------------------

## 📈 Model Evaluation

Each model was evaluated using:

-   Confusion Matrix
-   Accuracy
-   Sensitivity (Recall)
-   Specificity
-   Balanced Accuracy

------------------------------------------------------------------------

## 🧠 Ensemble Model

Predictions from all three models were combined using weighted voting.

Example: - Neural Network assigned higher weight due to better
sensitivity.

Final combined model achieved approximately:

-   Accuracy ≈ 0.86
-   Sensitivity ≈ 0.93

This demonstrates that simple models, when combined, can produce strong
predictive performance.

------------------------------------------------------------------------

## 📁 Project Structure

    ├── tele.csv
    ├── Homework3.R / Homework3.Rmd
    ├── README.md

------------------------------------------------------------------------

## 🚀 How to Reproduce

1.  Place `tele.csv` in working directory.
2.  Install required packages:

``` r
install.packages(c("caret", "class", "neuralnet", "smotefamily"))
```

3.  Run the script sequentially.

------------------------------------------------------------------------

## 📌 Skills Demonstrated

-   Data preprocessing & cleaning
-   Feature engineering
-   Scaling & encoding techniques
-   Handling imbalanced datasets (SMOTE)
-   Logistic Regression modeling
-   KNN implementation
-   Neural Network training
-   Model evaluation & confusion matrices
-   Ensemble modeling (weighted voting)
-   Reproducible experimentation in R

------------------------------------------------------------------------

## 👤 Author

Beatriz Wahle\
October 2024
