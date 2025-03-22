Here’s the corrected version of your question with properly formatted equations:  

---

# 📌 Question 5: Multiple Linear Regression Using Normal Equation  

## 🔍 Problem Overview  
In this task, we apply **multiple linear regression** to predict `CreditScore` using both `Age` and `Education`. We compute the optimal coefficients using the **normal equation** method:  

<div align="center">  
    <img src="https://latex.codecogs.com/svg.latex?\theta%20=%20(X^T%20X)^{-1}%20X^T%20y" alt="Normal Equation">  
</div>  

where:  
- \( X \) is the matrix of input features (`Age`, `Education`)  
- \( y \) is the vector of `CreditScore`  
- \( \theta \) contains the model parameters  

## 🏗️ Methodology  

### 1️⃣ Construct the Feature Matrix  
We set up the feature matrix \( X \) including a bias term:  

<div align="center">  
    <img src="https://latex.codecogs.com/svg.latex?X%20=%20\begin{bmatrix}%201%20&%20Age_1%20&%20Education_1%20\\%201%20&%20Age_2%20&%20Education_2%20\\%20\vdots%20&%20\vdots%20&%20\vdots%20\\%201%20&%20Age_m%20&%20Education_m%20\end{bmatrix}" alt="Feature Matrix X">  
</div>  

The output vector is:  

<div align="center">  
    <img src="https://latex.codecogs.com/svg.latex?y%20=%20\begin{bmatrix}%20CreditScore_1%20\\%20CreditScore_2%20\\%20\vdots%20\\%20CreditScore_m%20\end{bmatrix}" alt="Output Vector y">  
</div>  

### 2️⃣ Compute the Normal Equation  
Using the formula:  

<div align="center">  
    <img src="https://latex.codecogs.com/svg.latex?\theta%20=%20(X^T%20X)^{-1}%20X^T%20y" alt="Normal Equation">  
</div>  

we calculate the regression coefficients, which represent:  
- **Intercept** (\( \theta_0 \)): Baseline prediction  
- **Coefficient for Age** (\( \theta_1 \)): Impact of `Age` on `CreditScore`  
- **Coefficient for Education** (\( \theta_2 \)): Impact of `Education` on `CreditScore`  

### 3️⃣ Interpret the Coefficients  
- If \( \theta_1 > 0 \), older individuals tend to have higher credit scores.  
- If \( \theta_2 > 0 \), higher education levels correlate with better credit scores.  

## 📊 Expected Outcome  
By solving the normal equation, we derive a regression model that predicts `CreditScore` using `Age` and `Education` with minimal error.  
