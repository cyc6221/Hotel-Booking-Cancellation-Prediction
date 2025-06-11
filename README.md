# Hotel Booking Cancellation Prediction – Final Report

This repository contains the complete source code and report files for the project **"Hotel Booking Cancellation Prediction"**, which aims to predict booking cancellations using machine learning techniques including XGBoost and CatBoost with SHAP and SMOTE.

## Report Structure (`main.Rmd`)

The main report file is `main.Rmd`, which serves as the top-level document. Instead of containing all code and content directly, it includes multiple **child `.Rmd` files** using the `child=` option.

This modular design improves organization and maintainability, as each chapter is kept in a separate file:

```r
# Example structure in main.Rmd

# Problem Statement
{r child="ProblemStatement.Rmd"}

# Dataset Description
{r child="Dataset.Rmd"}

# Exploratory Data Analysis
{r child="Visualization.Rmd"}

# Analysis Process
{r child="ProcessDesign.Rmd"}

# Analysis Results
{r child="Result.Rmd"}
{r child="Result2.Rmd"}
{r child="Result3.Rmd"}

# Conclusion
{r child="Conclusion.Rmd"}
```

## Important Notes

- Do **not** knit `main.Rmd` in isolation if the child `.Rmd` files are missing — doing so will result in errors.
- This structure relies on all chapter-specific `.Rmd` files (e.g., `Dataset.Rmd`, `Visualization.Rmd`, etc.) being present in the same directory.
- All source code and analysis results are split across these child files.

## How to Knit the Full Report

To correctly generate the full report (e.g., as PDF or HTML), please ensure:

1. You have all the following child files in the same folder:
   - `ProblemStatement.Rmd`
   - `Dataset.Rmd`
   - `Visualization.Rmd`
   - `ProcessDesign.Rmd`
   - `Result.Rmd`
   - `Result2.Rmd`
   - `Result3.Rmd`
   - `Conclusion.Rmd`

2. Then, open **`main.Rmd`** in RStudio and click **"Knit"**.

Alternatively, use the following R command:

```r
rmarkdown::render("main.Rmd")
```

## File Structure Overview

```css
├── main.Rmd
├── ProblemStatement.Rmd
├── Dataset.Rmd
├── Visualization.Rmd
├── ProcessDesign.Rmd
├── Result.Rmd
├── Result2.Rmd
├── Result3.Rmd
├── Conclusion.Rmd
├── references.bib
└── output/
    └── [Your final rendered report]
```