# 📌 Question 5: Multiple Linear Regression Using Normal Equation

## 🔍 Problem Overview
In this task, we apply **multiple linear regression** to predict `CreditScore` using both `Age` and `Education`. We compute the optimal coefficients using the **normal equation** method:
\[
\theta = (X^T X)^{-1} X^T y
\]
where:
- \( X \) is the matrix of input features (`Age`, `Education`)
- \( y \) is the vector of `CreditScore`
- \( \theta \) contains the model parameters

## 🏗️ Methodology
### 1️⃣ Construct the Feature Matrix
We set up the feature matrix \( X \) including a bias term:
\[
X = \begin{bmatrix} 1 & Age_1 & Education_1 \\ 1 & Age_2 & Education_2 \\ \vdots & \vdots & \vdots \\ 1 & Age_m & Education_m \end{bmatrix}
\]
The output vector is:
\[
y = \begin{bmatrix} CreditScore_1 \\ CreditScore_2 \\ \vdots \\ CreditScore_m \end{bmatrix}
\]

### 2️⃣ Compute the Normal Equation
Using the formula:
\[
\theta = (X^T X)^{-1} X^T y
\]
we calculate the regression coefficients, which represent:
- **Intercept** (\( \theta_0 \)): Baseline prediction
- **Coefficient for Age (\( \theta_1 \))**: Impact of `Age` on `CreditScore`
- **Coefficient for Education (\( \theta_2 \))**: Impact of `Education` on `CreditScore`

### 3️⃣ Interpret the Coefficients
- If \( \theta_1 > 0 \), older individuals tend to have higher credit scores.
- If \( \theta_2 > 0 \), higher education levels correlate with better credit scores.

## 📊 Expected Outcome
By solving the normal equation, we derive a regression model that predicts `CreditScore` using `Age` and `Education` with minimal error.