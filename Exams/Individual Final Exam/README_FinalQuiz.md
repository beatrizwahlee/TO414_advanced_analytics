# 📊 Final Quiz -- Telco Customer Churn Prediction

### Beatriz Wahle \| November 2024

## 🔎 Project Overview

This Final Quiz project focuses on predicting **customer churn** using
the Telco Customer Churn dataset.

The objective is to apply classification techniques to identify
customers likely to leave a telecommunications company, while
demonstrating strong data preprocessing, model evaluation, and business
interpretation skills.

📄 Based on the submitted report: *Final Quiz* fileciteturn11file0

------------------------------------------------------------------------

## 🎯 Business Objective

Customer churn represents a major revenue risk for telecom companies.

This project aims to:

-   Predict whether a customer will churn\
-   Identify high-risk customer segments\
-   Support retention strategy development\
-   Align model performance with business impact

Target Variable: - `Churn` - Yes → Customer leaves\
- No → Customer stays

------------------------------------------------------------------------

## 🗂 Dataset

Dataset: `TelcoChurn.csv`

The dataset includes:

-   Customer demographics\
-   Account information\
-   Services subscribed\
-   Billing details\
-   Contract type\
-   Tenure\
-   Monthly & total charges

------------------------------------------------------------------------

## 🧹 Data Preparation

Key preprocessing steps:

-   Converted categorical variables to factors\
-   Handled missing or blank values\
-   Encoded categorical variables\
-   Scaled numeric features (where required)\
-   Split data into training and testing sets

------------------------------------------------------------------------

## 🤖 Models Implemented

Classification models applied:

-   Logistic Regression\
-   K-Nearest Neighbors (KNN)\
-   Decision Tree\
-   (Additional models depending on quiz structure)

Each model was evaluated using consistent metrics to ensure fair
comparison.

------------------------------------------------------------------------

## 📊 Evaluation Metrics

Performance assessed using:

-   Accuracy\
-   Sensitivity (Recall for churn class)\
-   Specificity\
-   Precision\
-   Confusion Matrix\
-   Balanced Accuracy

Because missing a churned customer can be costly, **Sensitivity** was
considered especially important.

------------------------------------------------------------------------

## 🧠 Key Insights

-   Contract type and tenure strongly influence churn likelihood.\
-   Month-to-month contracts show higher churn rates.\
-   Customers with higher monthly charges tend to have increased churn
    probability.\
-   Predictive models can meaningfully support proactive retention
    strategies.

------------------------------------------------------------------------

## 📁 Project Structure

    ├── FinalQuiz_BeatrizWahle.Rmd
    ├── FinalQuiz_BeatrizWahle.html
    ├── TelcoChurn.csv
    ├── README.md

------------------------------------------------------------------------

## 🚀 How to Reproduce

1.  Install required R packages:

``` r
install.packages(c(
  "dplyr",
  "ggplot2",
  "caret",
  "class",
  "C50"
))
```

2.  Place `TelcoChurn.csv` in your working directory.
3.  Open `FinalQuiz_BeatrizWahle.Rmd` in RStudio.
4.  Run all code chunks.
5.  Knit to HTML.

------------------------------------------------------------------------

## 📌 Skills Demonstrated

-   Supervised Machine Learning (Classification)\
-   Feature Engineering\
-   Data Cleaning & Encoding\
-   Model Evaluation & Comparison\
-   Business-Oriented Interpretation\
-   Professional R Markdown Reporting

------------------------------------------------------------------------

## 👤 Author

**Beatriz Wahle**\
Predictive Analytics Course -- Final Quiz (2024)
