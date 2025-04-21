# Diabetes Detection and Analysis

## Overview

This project is a preliminary exploratory data analysis (EDA) exercise using the **[Pima Indians Diabetes Dataset](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database)**. The primary goal was to better understand the structure of the data, clean and visualize it using Python, and uncover any significant patterns related to diabetes outcomes. 

The analysis follows a simplified version of the **OSEMN** framework (Obtain, Scrub, Explore, Model, and Interpret), with a focus on data acquisition, cleaning, and exploration. While this version does not include predictive modeling, it sets the foundation for potential machine learning applications in future work.

---

## Aim

- To explore key health metrics that may influence the onset of diabetes.
- To clean and visualize the dataset for clearer insights.
- To extract meaningful observations that can inform further analysis or predictive modeling.

---

## Tools and Technologies

- **Python**  
- **Jupyter Notebook**  
- Libraries used:
  - `pandas` for data manipulation
  - `numpy` for numerical operations
  - `matplotlib` and `seaborn` for data visualization
  - `scipy` for statistical functions

---

## Workflow

### 1. Obtain

The dataset used is the **Pima Indians Diabetes dataset**, which includes medical diagnostic data for 768 female patients. It contains eight independent variables (such as Glucose, Blood Pressure, and BMI) and one dependent variable `Outcome`, indicating whether or not the patient is diabetic (1 for diabetic, 0 for non-diabetic).

### 2. Scrub

- Checked data types and general structure using `.info()` and `.describe()`.
- Identified zero values in features like `Glucose`, `BloodPressure`, `SkinThickness`, `Insulin`, and `BMI`, which are medically improbable and likely represent missing data.
- No null values were present in the dataset, but the zero values indicate the need for further imputation or data cleaning in future work.

### 3. Explore

- Used visualizations such as histograms, boxplots, and a heatmap to understand feature distributions and relationships.
- Separated visualizations based on the `Outcome` variable to analyze differences between diabetic and non-diabetic patients.
- Computed correlation metrics to assess relationships between independent variables and diabetes status.

---

## Observations

Based on the visualizations and summary statistics:

- **Glucose** levels showed the most significant separation between diabetic and non-diabetic groups. Higher glucose levels are closely associated with diabetes.
- A large number of zero values in `Insulin` and `SkinThickness` could significantly affect model accuracy and needed to be handled appropriately.
- **BMI** and **Age** tend to be higher for individuals with diabetes.
- The correlation matrix revealed that **Glucose**, **BMI**, and **Age** have the strongest correlations with the outcome variable, though none are extremely high.
- Boxplots showed noticeable differences in the distributions of several features between the two outcome groups, reaffirming the need for proper feature scaling and data treatment prior to modeling.

---

## Insights

- **Data cleaning** is a critical step before any modeling. Many health metrics have unrealistic zero values that must be addressed through imputation or removal.
- **Glucose** appears to be the most predictive feature based on visual trends and correlation.
- The dataset is imbalanced and may benefit from resampling or weighting techniques in future modeling stages.

---

## Future Work

- Impute or address zero values in relevant features using appropriate statistical or machine learning methods.
- Normalize or scale features where necessary.
- Develop and evaluate classification models (e.g., Logistic Regression, Random Forest, Gradient Boosting).
- Use model evaluation metrics such as confusion matrix, accuracy, precision-recall, and ROC-AUC to assess performance.

---

## Project Structure

```
├── diabetes.csv
├── diabetes_analysis.ipynb
├── README.md
└── images/
    ├── histogram_glucose.png
    ├── boxplot_bmi_vs_outcome.png
    ├── heatmap_correlation.png
    └── ...
```

---

## References

- Pima Indians Diabetes Dataset: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/pima+indians+diabetes)
- General data exploration techniques were inspired by the OSEMN framework commonly used in data science projects.

---

## Author
Rachana Kotha
This analysis was conducted as part of my effort to deepen practical understanding of data preprocessing and EDA techniques. It reflects the early steps in a broader project focused on predicting diabetes using medical datasets. The intention is to iteratively expand this into a more complete machine learning pipeline.
