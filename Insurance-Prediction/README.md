# Predict Medical Insurance Costs with Machine Learning and Artificial Neural Networks

## Overview

This project focuses on predicting individual medical insurance charges using both traditional machine learning and deep learning techniques. The objective is to estimate healthcare costs based on demographic and lifestyle factors such as age, gender, BMI, number of children, smoking status, and geographic location.

The aim is twofold:
- To explore the statistical relationships between features influencing insurance costs.
- To compare the performance of a Linear Regression model and an Artificial Neural Network (ANN) model for prediction accuracy.

---

## Dataset Description

The dataset used is `insurance.csv`, which contains 1,338 records of insurance data. Each row represents an individual and includes the following features:

| Feature     | Description                                                              |
|-------------|--------------------------------------------------------------------------|
| `age`       | Age of the individual                                                    |
| `sex`       | Gender of the individual (`male` / `female`)                             |
| `bmi`       | Body Mass Index                                                          |
| `children`  | Number of children or dependents                                         |
| `smoker`    | Smoking status of the individual (`yes` / `no`)                          |
| `region`    | Residential area (`northeast`, `southeast`, `southwest`, `northwest`)    |
| `charges`   | Annual medical insurance charges (target variable)                       |

---

## Workflow and Methodology

### 1. Data Loading and Initial Exploration

- Loaded the dataset using `pandas`.
- Verified data integrity and checked for missing values.
- Reviewed summary statistics and data types.

### 2. Data Preprocessing

- Encoded categorical features (`sex`, `smoker`, `region`) into numerical format.
- Performed exploratory data analysis with visualizations to understand patterns and distributions.

### 3. Correlation Analysis

- Built a correlation matrix to examine relationships between input features and the target (`charges`).
- Identified key variables that heavily influence insurance costs such as `smoker`, `age`, and `bmi`.

### 4. Feature Scaling

- Standardized the feature set using `StandardScaler` to improve model convergence and performance.

### 5. Model Training and Evaluation

#### Linear Regression

- Split data into training and test sets (80/20).
- Trained a Linear Regression model using `scikit-learn`.
- Evaluated the model using common regression metrics.

#### Artificial Neural Network (ANN)

- Built a feedforward neural network using TensorFlow and Keras.
- Network architecture:
  - Input layer with 6 features
  - Two hidden layers with ReLU activation
  - Output layer for continuous prediction
- Trained the model and validated its performance.

---

## Key Visualizations

### Charges vs. Smoking Status

![Charges vs Smoker](images/charges_vs_smoker.png)

### BMI Distribution by Smoking Status

![BMI vs Smoker](images/bmi_vs_smoker.png)

### Correlation Heatmap

![Correlation Heatmap](images/correlation_heatmap.png)

These visualizations demonstrate that smoking status is a major factor influencing insurance charges, followed by BMI and age.

---

## Libraries and Tools Used

- `pandas`
- `numpy`
- `seaborn`
- `matplotlib`
- `scikit-learn`
- `tensorflow`
- `keras`

---

## Evaluation Metrics

| Metric       | Description                                                                 |
|--------------|-----------------------------------------------------------------------------|
| MAE          | Mean Absolute Error: average of absolute errors between predicted and true values |
| MSE          | Mean Squared Error: average of squared errors between predicted and actual values |
| RMSE         | Root Mean Squared Error: square root of MSE, gives error in original units |
| R² Score     | R-squared: proportion of variance in target explained by input features     |

---

## Conclusion

This project demonstrates how both statistical learning and deep learning techniques can be used to predict healthcare costs. The Linear Regression model provides a simple and interpretable baseline, while the ANN captures more complex nonlinear relationships in the data.

Key takeaways:
- Smoking is the most influential factor on insurance charges.
- BMI and age are also strong predictors.
- The ANN slightly outperforms Linear Regression in predictive accuracy, showing its capability to model deeper patterns in the data.


## Author
Rachana Kotha
This project work provides a foundation for cost forecasting models in the health insurance domain.
