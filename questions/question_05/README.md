# 📌 Multiple Linear Regression Using Normal Equation

## 🔍 Problem Overview
In this task, we apply **multiple linear regression** to predict `CreditScore` using both `Age` and `Education`. We compute the optimal coefficients using the **normal equation** method:

![\theta = (X^T X)^{-1} X^T y](https://latex.codecogs.com/svg.latex?\theta%20=%20(X^T%20X)^{-1}%20X^T%20y)

where:
- ![X](https://latex.codecogs.com/svg.latex?X) is the matrix of input features (`Age`, `Education`)  
- ![y](https://latex.codecogs.com/svg.latex?y) is the vector of `CreditScore`  
- ![\theta](https://latex.codecogs.com/svg.latex?\theta) contains the model parameters

## 🏗️ Methodology

### 1️⃣ Construct the Feature Matrix
We set up the feature matrix \( X \) including a bias term:

![X = \begin{bmatrix} 1 & Age_1 & Education_1 \\ 1 & Age_2 & Education_2 \\ \vdots & \vdots & \vdots \\ 1 & Age_m & Education_m \end{bmatrix}](https://latex.codecogs.com/svg.latex?X%20=%20\begin{bmatrix}%201%20&%20Age_1%20&%20Education_1%20\\%201%20&%20Age_2%20&%20Education_2%20\\%20\vdots%20&%20\vdots%20&%20\vdots%20\\%201%20&%20Age_m%20&%20Education_m%20\end{bmatrix})

The output vector is:

![y = \begin{bmatrix} CreditScore_1 \\ CreditScore_2 \\ \vdots \\ CreditScore_m \end{bmatrix}](https://latex.codecogs.com/svg.latex?y%20=%20\begin{bmatrix}%20CreditScore_1%20\\%20CreditScore_2%20\\%20\vdots%20\\%20CreditScore_m%20\end{bmatrix})

### 2️⃣ Compute the Normal Equation
Using the formula:

![\theta = (X^T X)^{-1} X^T y](https://latex.codecogs.com/svg.latex?\theta%20=%20(X^T%20X)^{-1}%20X^T%20y)

we calculate the regression coefficients, which represent:
- **Intercept** (![\theta_0](https://latex.codecogs.com/svg.latex?\theta_0)): Baseline prediction  
- **Coefficient for Age** (![\theta_1](https://latex.codecogs.com/svg.latex?\theta_1)): Impact of `Age` on `CreditScore`  
- **Coefficient for Education** (![\theta_2](https://latex.codecogs.com/svg.latex?\theta_2)): Impact of `Education` on `CreditScore` 

### 3️⃣ Interpret the Coefficients
- If ![\theta_1 > 0](https://latex.codecogs.com/svg.latex?\theta_1%20%3E%200), older individuals tend to have higher credit scores.  
- If ![\theta_2 > 0](https://latex.codecogs.com/svg.latex?\theta_2%20%3E%200), higher education levels correlate with better credit scores.

## 📊 Expected Outcome
By solving the normal equation, we derive a regression model that predicts `CreditScore` using `Age` and `Education` with minimal error.
