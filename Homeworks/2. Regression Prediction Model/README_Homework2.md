# 🏗 Homework 2 -- Predicting Concrete Strength for Bridge Construction

## 🔎 Project Overview

This project builds a regression model to predict **concrete compressive
strength** using material composition data.

The scenario is framed as advising a construction team (AABC) that needs
to build a bridge over the Huron River in Ann Arbor. The bridge must
achieve a **minimum strength of 40** to support anticipated traffic
load.

The goal is to develop a predictive model to evaluate different material
combinations and recommend the optimal mixture.

------------------------------------------------------------------------

## 🎯 Objective

-   Train a regression model to predict concrete strength
-   Evaluate model performance
-   Identify the best combination of ingredients to reach a target
    strength of 40
-   Communicate results clearly in a professional report format

------------------------------------------------------------------------

## 🗂 Dataset

Dataset used:

``` r
data <- read.csv("concrete.csv")
```

The dataset includes:

-   Cement
-   Slag
-   Fly Ash
-   Water
-   Superplasticizer
-   Coarse Aggregate
-   Fine Aggregate
-   Age
-   **Strength** (target variable)

This is a **supervised regression problem**.

------------------------------------------------------------------------

## 🧹 Data Preparation

Key steps:

-   Loaded dataset into R
-   Explored summary statistics and structure
-   Checked variable distributions
-   Prepared training and testing datasets
-   Used the `caret` package for model training and validation

------------------------------------------------------------------------

## 🤖 Modeling Approach

-   Applied regression modeling using `caret`
-   Split dataset into training and testing sets
-   Evaluated model performance using appropriate regression metrics
    (e.g., RMSE, R²)
-   Used model predictions to determine material combinations achieving
    strength ≥ 40

------------------------------------------------------------------------

## 📈 Model Evaluation

Performance evaluated using:

-   Root Mean Squared Error (RMSE)
-   R-squared (R²)
-   Predicted vs. Actual comparisons

The final model was used to recommend the optimal concrete mixture to
meet safety requirements.

------------------------------------------------------------------------

## 📁 Project Structure

    ├── concrete.csv
    ├── HW2–BeatrizWahle.Rmd
    ├── HW2–BeatrizWahle.html
    ├── README.md

------------------------------------------------------------------------

## 🚀 How to Reproduce

1.  Install required packages:

``` r
install.packages("caret")
```

2.  Place `concrete.csv` in your working directory.
3.  Open the R Markdown file.
4.  Run all code chunks.
5.  Knit to HTML to generate the final report.

------------------------------------------------------------------------

## 📌 Skills Demonstrated

-   Supervised Machine Learning (Regression)
-   Model training with `caret`
-   Train/test splitting
-   Model evaluation (RMSE, R²)
-   Applied predictive modeling
-   Data-driven decision making
-   Professional R Markdown reporting

------------------------------------------------------------------------

## 👤 Author

Beatriz Wahle\
Homework 2 -- September 2024
