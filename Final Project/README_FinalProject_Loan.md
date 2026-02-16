# 💳 Loans -- Final Group Project

### Data Detectives \| November 2024

## 🔎 Project Overview

This final project develops a comprehensive predictive modeling system
to help financial institutions reduce losses from defaulted loans.

Using historical loan data (2008--2015), we built and compared multiple
machine learning models to predict whether a loan will be repaid or
defaulted. The ultimate goal was to determine whether implementing
predictive analytics could improve profitability and reduce financial
risk.

------------------------------------------------------------------------

## 🎯 Business Objective

Banks face significant losses from loan defaults. Although defaulted
loans represent a small percentage of total loans granted, their
financial impact is disproportionately high.

This project aims to:

-   Predict loan repayment outcomes
-   Reduce exposure to high-risk borrowers
-   Improve profitability
-   Quantify the financial impact of model implementation

------------------------------------------------------------------------

## 🗂 Dataset

-   Source: American financial services company\
-   Time period: April 2008 -- September 2015\
-   Observations: \~870,000 loans\
-   Target variable: `y` (Binary)
    -   1 → Loan Repaid\
    -   0 → Loan Defaulted

### Data Cleaning

-   Removed irrelevant columns (`id`, `prime_id`, `url`)
-   Filtered out loan statuses not aligned with the prediction goal
-   Created binary target variable
-   Encoded categorical variables
-   Scaled data for neural-network-based models

------------------------------------------------------------------------

## 🤖 Models Implemented

Seven predictive models were developed and compared:

1.  Logistic Regression\
2.  K-Nearest Neighbors (KNN)\
3.  Artificial Neural Network (ANN)\
4.  Support Vector Machine (SVM)\
5.  Decision Tree (C5.0)\
6.  Random Forest\
7.  XGBoost

### 🔗 Stacked Model

After training individual models, a **stacked ensemble model** was
created using the predictions of all base models.

The stacked model combined the strengths of each algorithm to improve
overall performance and robustness.

------------------------------------------------------------------------

## 📊 Evaluation Metrics

Models were evaluated using:

-   Accuracy\
-   Sensitivity (Recall)\
-   Specificity\
-   Precision\
-   Balanced Accuracy\
-   Confusion Matrix

Because false positives (predicting repayment when the loan defaults)
are financially costly, **Specificity** was a key metric in model
selection.

------------------------------------------------------------------------

## 🏆 Final Recommendation

The **Final Stacked Model** was selected as the optimal solution.

It provides:

-   Strong Sensitivity (\~95%+)\
-   Improved Specificity (\~77%)\
-   Balanced Accuracy (\~86%)\
-   Robust generalization

This model best aligns with the business objective of minimizing
financial losses while maintaining strong predictive performance.

------------------------------------------------------------------------

## 💰 Financial Impact

### Before Model Implementation:

-   Losses: **10.12%** of revenue\
-   Profitability: **89.88%**

### After Model Implementation:

-   Losses reduced to **7.76%**\
-   Profitability increased to **92.24%**

### 🔥 Key Result:

A **2.36 percentage-point reduction in losses**, representing
approximately:

> **\$3.9+ million increase in profitability**

This demonstrates the real-world financial value of predictive analytics
in credit risk management.

------------------------------------------------------------------------

## 🧠 Key Takeaways

-   Ensemble models outperform individual models in complex financial
    datasets.
-   Aligning model metrics with business objectives is critical.
-   Even simple predictive systems can generate multi-million-dollar
    financial impact.
-   Data quality and preprocessing significantly influence model
    performance.
-   Computational constraints limit model complexity --- future work
    could explore deeper neural networks or stepwise regression.

------------------------------------------------------------------------

## 📁 Project Structure

    ├── FinalProject_Loan.Rmd
    ├── FinalProject_Loan.html
    ├── README.md

------------------------------------------------------------------------

## 🚀 How to Reproduce

1.  Install required R packages:

``` r
install.packages(c(
  "dplyr", "ggplot2", "caret", "class",
  "neuralnet", "kernlab", "C50",
  "randomForest", "xgboost"
))
```

2.  Place the dataset in your working directory.
3.  Open `FinalProject_Loan.Rmd` in RStudio.
4.  Run all code chunks.
5.  Knit to HTML.

------------------------------------------------------------------------

## 📌 Skills Demonstrated

-   End-to-end Machine Learning pipeline\
-   Feature engineering & preprocessing\
-   Model comparison & benchmarking\
-   Ensemble learning (Stacking)\
-   Cost-sensitive modeling\
-   Business-driven model evaluation\
-   Financial impact analysis\
-   Professional R Markdown reporting

------------------------------------------------------------------------

## 👥 Team

**Data Detectives**\
University Predictive Analytics Project -- 2024
