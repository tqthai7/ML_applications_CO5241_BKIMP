# 📌 Question 6: Model Evaluation – Mean Squared Error & R²

## 🔍 Problem Overview
In this task, we evaluate the performance of our **multiple linear regression model** (from Question 5) by computing:
- **Mean Squared Error (MSE)**: Measures average squared differences between actual and predicted `CreditScore` values.
- **R² Score (Coefficient of Determination)**: Assesses how well the model explains variance in the data.

## 🏗️ Methodology
### 1️⃣ Compute Mean Squared Error (MSE)
The MSE formula is:
\[
MSE = \frac{1}{m} \sum_{i=1}^{m} (y_i - \hat{y}_i)^2
\]
where:
- \( y_i \) is the actual `CreditScore`
- \( \hat{y}_i \) is the predicted `CreditScore`
- \( m \) is the number of training samples

### 2️⃣ Compute R² Score
The R² formula is:
\[
R^2 = 1 - \frac{\sum (y_i - \hat{y}_i)^2}{\sum (y_i - \bar{y})^2}
\]
where:
- \( \bar{y} \) is the mean of `CreditScore`
- The numerator represents **unexplained variance**
- The denominator represents **total variance**

### 3️⃣ Model Suitability Assessment
- **If MSE is low**: Model predictions are close to actual values.
- **If R² is close to 1**: Model explains most of the variance in `CreditScore`.
- **If R² is low**: `Age` and `Education` might not be strong predictors, suggesting a need for additional features or a different model.

## 📊 Expected Outcome
By computing MSE and R², we determine whether linear regression is appropriate for predicting `CreditScore` and gain insights into model accuracy.

