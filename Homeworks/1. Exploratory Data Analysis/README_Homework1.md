# 📊 Homework 1 -- Exploratory Data Analysis of NYC Flights

## 🔎 Project Overview

This project performs exploratory data analysis (EDA) on the
`nycflights13` dataset using R.

The assignment emphasizes: - Clear communication of analytical
findings - Clean, well-commented R code - Professional HTML report
formatting - Accurate and interpretable results

The analysis focuses on understanding airline performance and arrival
delays using real-world flight data.

------------------------------------------------------------------------

## 🎯 Objective

Analyze NYC flight data to:

-   Explore dataset structure and variables
-   Perform data cleaning and transformation
-   Investigate arrival delays
-   Compare airline performance
-   Compute and interpret "air gain"
-   Communicate insights clearly for non-technical audiences

------------------------------------------------------------------------

## 🗂 Dataset

Dataset used:

``` r
library(nycflights13)
nyc <- nycflights13::flights
```

-   Source: `nycflights13` R package
-   Observations: \~336,000 flights
-   Variables include:
    -   Departure delay
    -   Arrival delay
    -   Airline carrier
    -   Flight time
    -   Distance
    -   Date and time information

------------------------------------------------------------------------

## 🧹 Data Preparation

Key preprocessing steps:

-   Loaded dataset into an object `nyc`
-   Used `dplyr` for manipulation and summarization
-   Handled missing values (e.g., delays)
-   Grouped data by airline to compare performance
-   Calculated summary statistics (mean, median)

------------------------------------------------------------------------

## 📈 Analyses Performed

### 1️⃣ Data Exploration

-   Inspected dataset structure
-   Examined key delay variables
-   Generated descriptive summaries

### 2️⃣ Arrival Delay Analysis

-   Investigated which airlines experience the highest and lowest
    arrival delays
-   Compared mean vs. median delay values
-   Identified outlier behavior

### 3️⃣ Airline Performance

-   Compared airlines based on arrival performance
-   Evaluated consistency using central tendency measures

### 4️⃣ Air Gain

-   Calculated "air gain" (difference between arrival delay and
    departure delay)
-   Interpreted whether airlines recover time in the air
-   Identified best and worst performing carriers

------------------------------------------------------------------------

## 📁 Project Structure

    ├── HW1.Rmd
    ├── HW1-BeatrizWahle.html
    ├── README.md

------------------------------------------------------------------------

## 🚀 How to Reproduce

1.  Install required packages:

``` r
install.packages(c("nycflights13", "dplyr"))
```

2.  Open `HW1.Rmd` in RStudio.
3.  Run all code chunks.
4.  Click **Knit HTML** to generate the final report.

------------------------------------------------------------------------

## 📌 Skills Demonstrated

-   Exploratory Data Analysis (EDA)
-   Data wrangling with `dplyr`
-   Grouping and summarization
-   Statistical interpretation (mean vs. median)
-   Professional R Markdown reporting
-   Clear communication of data insights

------------------------------------------------------------------------

## 👤 Author

Beatriz Wahle\
Homework Assignment 1
