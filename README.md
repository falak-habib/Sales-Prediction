# Sales Prediction Using Linear Regression

## Project Overview

This project analyzes the relationship between **advertising expenditure and sales** and uses **Linear Regression** to predict sales based on advertising spending.

The project demonstrates an end-to-end machine learning workflow, including:

* Exploratory Data Analysis (EDA)
* Data visualization
* Understanding relationships between variables
* Train-test splitting
* Linear Regression model development
* Sales prediction
* Model evaluation
* Residual analysis
* Interpretation of model coefficients
* Business-oriented insights

---

## Objective

The main objective of this project is to understand how **advertising expenditure is associated with sales** and develop a Linear Regression model that can estimate expected sales for a given advertising budget.

> **Note:** The relationship identified by the model represents an association within the dataset and does not establish that advertising expenditure alone causes changes in sales.

---

## Dataset

The dataset contains information about:

| Variable    | Description               |
| ----------- | ------------------------- |
| Advertising | Advertising expenditure   |
| Sales       | Corresponding sales value |

The project uses **Advertising expenditure as the independent variable (feature)** and **Sales as the dependent variable (target)**.

---

## Exploratory Data Analysis

Before building the machine learning model, the relationship between advertising expenditure and sales was explored using data visualization.

### Key Question

**Does increased advertising expenditure correspond to increased sales?**

### Observation

The scatter plot shows a **strong positive relationship** between advertising expenditure and sales.

Generally, higher advertising expenditure is associated with higher sales values.

However, correlation or association alone does not prove causation, as other factors may influence sales.

---

## Model Preparation

### Feature and Target

* **Feature (X):** Advertising expenditure
* **Target (y):** Sales

The dataset was divided into:

* **80% Training Data**
* **20% Testing Data**

A `random_state` of **42** was used to ensure that the train-test split is reproducible.

---

## Machine Learning Model

### Linear Regression

Linear Regression was selected because the exploratory analysis showed a strong approximately linear relationship between advertising expenditure and sales.

The model follows the equation:

**Sales = β₀ + β₁ × Advertising**

Where:

* **β₀** = Intercept
* **β₁** = Advertising coefficient

### Model Coefficients

The trained model produced approximately:

* **Intercept:** 14
* **Advertising coefficient:** 1.176

The coefficient indicates that a **one-unit increase in advertising expenditure is associated with an estimated 1.176-unit increase in sales**, according to the fitted model.

This coefficient should be interpreted as an association within the dataset rather than evidence that advertising expenditure alone causes the increase.

---

## Sales Prediction

Once trained, the Linear Regression model can be used to estimate sales for a given advertising expenditure.

### Example

For an advertising expenditure of **40 units**, the trained model can be used to estimate the corresponding expected sales.

The prediction is generated using the learned relationship between advertising expenditure and sales.

---

## Model Evaluation

The model was evaluated using several regression metrics.

| Metric   |  Score |
| -------- | -----: |
| MAE      |  0.357 |
| MSE      |  0.209 |
| RMSE     |  0.457 |
| R² Score | 0.9994 |

### Mean Absolute Error (MAE)

**MAE = 0.357**

MAE represents the average absolute difference between the actual and predicted sales values.

A lower MAE indicates smaller prediction errors.

### Mean Squared Error (MSE)

**MSE = 0.209**

MSE calculates the average squared difference between actual and predicted values. Because the errors are squared, larger errors have a greater influence on the metric.

### Root Mean Squared Error (RMSE)

**RMSE = 0.457**

RMSE is the square root of MSE and is expressed in the same units as the target variable.

### R² Score

**R² = 0.9994**

The R² score indicates that the model explains approximately **99.94% of the variation in sales in the test set**.

The exceptionally high score suggests that advertising expenditure has a very strong linear relationship with sales in this particular dataset.

---

## Fitted Regression Line

The fitted regression line visualizes the linear relationship learned by the model.

The upward slope indicates that higher advertising expenditure corresponds to higher predicted sales.

The actual observations can be compared with the regression line to visually assess how closely the Linear Regression model fits the data.

---

## Residual Analysis

Residuals represent the difference between the actual sales values and the sales predicted by the model.

A residual plot was used to examine whether the prediction errors showed any systematic pattern.

### What to Look For

Ideally:

* Residuals should be randomly distributed around zero.
* There should be no obvious curve or systematic pattern.
* The spread of residuals should remain reasonably consistent.

A systematic pattern could indicate that a simple linear model is not adequately capturing the underlying relationship.

### Interpretation

The residual analysis, together with the high R² score, indicates that the Linear Regression model represents the relationship between advertising expenditure and sales very closely for this dataset.

The MAE of approximately **0.357** also indicates that the average absolute prediction error is relatively small compared with the scale of the target values.

---

## Business Insights

The analysis provides several useful business-oriented observations:

1. **Advertising expenditure is strongly associated with sales** in the dataset.
2. Higher advertising spending generally corresponds to higher predicted sales.
3. Linear Regression provides an effective and interpretable model for this dataset.
4. The model can be used to estimate expected sales for a given advertising budget.
5. The model coefficient provides an interpretable estimate of the expected change in sales associated with a change in advertising expenditure.
6. The model's high R² score indicates an extremely strong fit to the observed data.

However, real-world business decisions should consider other factors such as:

* Product pricing
* Discounts and promotions
* Seasonality
* Competitor activity
* Customer demand
* Market conditions
* Distribution and availability

Therefore, the model should be treated as a **predictive/analytical tool rather than proof of advertising causality**.

---

## Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Scikit-learn**
* **Jupyter Notebook**

---

## How to Run the Project

### 1. Clone the repository

```bash
git clone <your-github-repository-url>
```

### 2. Navigate to the project directory

```bash
cd Sales-Prediction-Linear-Regression
```

### 3. Install the required libraries

```bash
pip install -r requirements.txt
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

### 5. Open the notebook

Open:

```text
Sales_Prediction.ipynb
```

Run the notebook cells sequentially to reproduce the analysis and model results.

---

## Key Results

The Linear Regression model achieved:

* **MAE:** 0.357
* **MSE:** 0.209
* **RMSE:** 0.457
* **R²:** 0.9994

These results indicate that the model fits the relationship between advertising expenditure and sales extremely well in the given dataset.

---

## Limitations

Despite the strong model performance, several limitations should be considered:

* The model uses only **one predictor variable**.
* The dataset may not represent real-world sales conditions.
* A high R² does not establish causation.
* Important variables such as pricing, seasonality, competition, and promotions are not included.
* Model performance may differ on new datasets or real-world data.

Future improvements could include adding multiple relevant business variables and comparing Linear Regression with other regression algorithms.

---

## Future Improvements

Possible extensions of this project include:

* Multiple Linear Regression using additional features
* Feature engineering
* Cross-validation
* Outlier analysis
* Comparison with Ridge and Lasso Regression
* Comparison with tree-based regression models
* Hyperparameter tuning
* Deployment using Flask or FastAPI
* Creating an interactive prediction interface

---

## Author

**Falak Habib**

Computer Science Undergraduate | AIML | Data Science | Data Analysis

---

## Conclusion

This project demonstrates how **Linear Regression** can be used to analyze the relationship between advertising expenditure and sales and make sales predictions.

The model achieved an **R² score of approximately 0.9994**, along with low MAE and RMSE values, showing a very close fit to the relationship observed in the dataset.

The project also demonstrates the importance of combining **data visualization, model evaluation, residual analysis, and business interpretation** when developing a machine learning solution.
