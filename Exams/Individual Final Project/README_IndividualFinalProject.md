# 📊 Individual Final Project

### Beatriz Wahle \| November 2024

## 🔎 Project Overview

This Individual Final Project develops a complete predictive analytics
pipeline to solve a real-world financial risk problem.

The project focuses on building, evaluating, and comparing multiple
machine learning models to predict loan repayment outcomes. The
objective is to apply advanced predictive modeling techniques while
aligning model performance with real business priorities.

------------------------------------------------------------------------

## 🎯 Business Objective

Financial institutions face significant losses due to loan defaults.

The goal of this project is to:

-   Predict whether a loan will be repaid or defaulted\
-   Reduce financial exposure to high-risk borrowers\
-   Improve credit risk decision-making\
-   Quantify the business value of predictive modeling

------------------------------------------------------------------------

## 🗂 Dataset

-   Historical financial loan data\
-   Large-scale dataset (\~800k+ observations)\
-   Target variable transformed into binary format:
    -   `1` → Loan Repaid\
    -   `0` → Loan Defaulted

### Data Preparation

-   Cleaned loan status categories\
-   Removed non-informative columns\
-   Created binary target variable\
-   Encoded categorical variables\
-   Applied scaling where required\
-   Split data into training and testing sets (50/50 split)

------------------------------------------------------------------------

## 🤖 Models Developed

The project includes implementation and evaluation of:

1.  Logistic Regression\
2.  K-Nearest Neighbors (KNN)\
3.  Artificial Neural Network (ANN)\
4.  Support Vector Machine (SVM)\
5.  Decision Tree (C5.0)\
6.  Random Forest\
7.  XGBoost\
8.  Stacked Ensemble Model

Each model was evaluated using consistent train/test splits to ensure
fair comparison.

------------------------------------------------------------------------

## 📊 Evaluation Metrics

Performance metrics included:

-   Accuracy\
-   Sensitivity (Recall)\
-   Specificity\
-   Precision\
-   Balanced Accuracy\
-   Confusion Matrix\
-   Kappa Statistic

Because false positives (predicting repayment when the loan defaults)
are financially costly, **Specificity** was treated as a key metric in
model comparison.

------------------------------------------------------------------------

## 🏆 Final Model

A **Stacked Ensemble Model** was created by combining predictions from
all base models.

The stacked model demonstrated:

-   High overall accuracy\
-   Strong sensitivity\
-   Improved specificity\
-   Balanced predictive performance

This ensemble approach provided a more stable and reliable solution than
any individual model.

------------------------------------------------------------------------

## 💰 Business Impact

Model implementation resulted in:

-   Reduction in financial losses\
-   Increase in overall profitability\
-   Improved risk-adjusted loan approval strategy

The project demonstrates how predictive analytics can generate
measurable financial value in credit risk management.

------------------------------------------------------------------------

## 🧠 Key Learnings

-   Model performance must align with business priorities.
-   Ensemble methods improve robustness and generalization.
-   Data preprocessing significantly affects predictive accuracy.
-   Cost-sensitive modeling helps align predictions with financial
    goals.
-   Computational constraints impact model complexity choices.

------------------------------------------------------------------------

## 📁 Project Structure

    ├── IndividualFinalProject.Rmd
    ├── IndividualFinalProject.html
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
3.  Open `IndividualFinalProject.Rmd` in RStudio.
4.  Run all code chunks.
5.  Knit to HTML.

------------------------------------------------------------------------

## 📌 Skills Demonstrated

-   End-to-end Machine Learning workflow\
-   Feature engineering & preprocessing\
-   Model benchmarking & comparison\
-   Ensemble learning (Stacking)\
-   Cost-sensitive classification\
-   Business-oriented model evaluation\
-   Financial impact analysis\
-   Professional analytical reporting

------------------------------------------------------------------------

## 👤 Author

**Beatriz Wahle**\
Predictive Analytics Course -- 2024
