# Predict medical insurance costs with machine learning and ANN

## Summary

The objective is to predict the health insurance cost incurred by individuals based on their age, gender, Body Mass Index (BMI), number of children, smoking habits, and geo-location.

## Dataset

The dataset used in this project is `insurance.csv`, which contains the following features:
- `age`: Age of the individual
- `sex`: Gender of the individual (male/female)
- `bmi`: Body Mass Index
- `children`: Number of children/dependents
- `smoker`: Smoking status (yes/no)
- `region`: Residential area (northeast, northwest, southeast, southwest)
- `charges`: Medical insurance cost

## Project Steps

1. **Data Loading and Exploration**:
   - Load the dataset and display its basic information.
   - Check for missing values and get a statistical summary of the data.

2. **Data Preprocessing**:
   - Encode categorical variables (`sex`, `smoker`, and `region`) into numerical values.
   - Visualize the data distribution and relationships between features.

3. **Correlation Analysis**:
   - Calculate and visualize the correlation matrix to understand relationships between variables.

4. **Feature Scaling**:
   - Standardize the feature matrix and target vector to improve model performance.

5. **Model Training and Evaluation**:
   - Split the data into training and testing sets.
   - Train a Linear Regression model and evaluate its performance using various metrics (RSME, MSE, MAE, R2).

6. **Building and Training an ANN**:
   - Build an Artificial Neural Network (ANN) model using TensorFlow and Keras.
   - Train the ANN model and evaluate its performance.

## Libraries Used

- pandas
- numpy
- seaborn
- matplotlib
- scikit-learn
- tensorflow
- keras

## Evaluation Metrics

The performance of the models is evaluated using the following metrics

	- Root Mean Squared Error (RMSE):
	• Measures the average magnitude of the errors between predicted and actual values.
	- Mean Squared Error (MSE):
	• Measures the average of the squares of the errors between predicted and actual values.
	- Mean Absolute Error (MAE):
	• Measures the average magnitude of the errors between predicted and actual values.
	- R-squared (R2 Score):
	• Indicates the proportion of the variance in the dependent variable that is predictable from the independent variables.


 ## Conclusion

The project predicted medical insurance costs using Machine Learning and deep learning models. Both linear regression and artificial neural network models provide insights into the factors influencing insurance costs, with evaluation metrics indicating the performance of each model.