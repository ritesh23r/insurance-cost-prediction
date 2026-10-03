# Insurance Cost Prediction

## Overview

This project focuses on predicting **insurance charges** using Machine Learning.

The dataset contains information such as age, sex, BMI, number of children, smoking status, and region. The project follows an end-to-end workflow, starting from exploratory data analysis and preprocessing and ending with a Linear Regression model and evaluation.

## Project Workflow

```text
Raw Data
   ↓
Exploratory Data Analysis
   ↓
Data Cleaning
   ↓
Categorical Encoding
   ↓
Feature Engineering
   ↓
Feature Selection
   ↓
Train/Test Split
   ↓
Linear Regression
   ↓
Model Evaluation
```

## Dataset Features

| Feature    | Description                   |
| ---------- | ----------------------------- |
| `age`      | Age of the individual         |
| `sex`      | Gender                        |
| `bmi`      | Body Mass Index               |
| `children` | Number of children/dependents |
| `smoker`   | Smoking status                |
| `region`   | Residential region            |
| `charges`  | Medical insurance charges     |

## Exploratory Data Analysis

The dataset was explored using:

* Dataset shape and information
* Descriptive statistics
* Missing-value analysis
* Duplicate analysis
* Distribution analysis
* Categorical feature analysis
* Boxplots for outlier analysis
* Correlation heatmap

## Data Cleaning & Preprocessing

The following preprocessing steps were performed:

* Removed duplicate records
* Checked for missing values
* Converted categorical variables into numerical representations
* Applied one-hot encoding to the `region` feature
* Used `drop_first=True` to avoid redundant dummy variables

## Feature Engineering

A new BMI category feature was created using BMI ranges:

```text
Underweight
Normal
Overweight
Obese
```

BMI categories were then converted into numerical features using one-hot encoding.

Numerical features such as:

* Age
* BMI
* Children

were standardized using `StandardScaler`.

## Feature Analysis

Correlation analysis was used to understand relationships between numerical variables and insurance charges.

A **Chi-square test** was also performed on categorical features to investigate their association with insurance charge categories.

The significance level used was:

```text
α = 0.05
```

## Machine Learning Model

### Linear Regression

A Linear Regression model was trained to predict insurance charges.

The dataset was divided into:

```text
80% → Training Data
20% → Testing Data
```

`random_state=42` was used to make the train-test split reproducible.

## Model Evaluation

The model was evaluated using:

### R² Score

R² measures how much of the variation in the target variable is explained by the model.

### Adjusted R²

Adjusted R² accounts for the number of predictors used by the model and provides a more controlled measure of model fit.

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* SciPy
* Jupyter Notebook / Google Colab

## Project Structure

```text
insurance-cost-prediction/
│
├── insurance.csv
├── insurance_cost_prediction.ipynb
├── README.md
└── requirements.txt
```

## Key Learning Outcomes

Through this project, I practiced:

* Exploratory Data Analysis
* Data preprocessing
* Categorical encoding
* Feature engineering
* Feature scaling
* Statistical feature analysis
* Train/Test splitting
* Linear Regression
* R² and Adjusted R²
* Building an end-to-end Machine Learning workflow

## Future Improvements

* Compare Linear Regression with Ridge and Lasso Regression
* Evaluate the model using MAE, MSE, and RMSE
* Perform cross-validation
* Experiment with additional regression models
* Improve feature selection and preprocessing

## Author

**Ritesh Das**

GitHub: `ritesh23r`
