# 📌 Question 7: Logistic Regression for Loan Risk Classification

## 🔍 Problem Overview
In this task, we formulate a **logistic regression model** to predict `RiskLevel` (Low or High) based on `Age` and `CreditScore`. We then compute the initial prediction for test case **T1** using given weights.

## 🏗️ Methodology

### 1️⃣ Logistic Regression Model
Logistic regression predicts the probability of `RiskLevel` using the **sigmoid function**:

![P(\text{Low Risk} | \text{Age}, \text{CreditScore}) = \sigma(w_0 + w_1 \cdot \text{Age} + w_2 \cdot \text{CreditScore})](https://latex.codecogs.com/svg.latex?P(\text{Low%20Risk}%20|%20\text{Age},%20\text{CreditScore})%20=%20\sigma(w_0%20+%20w_1%20\cdot%20\text{Age}%20+%20w_2%20\cdot%20\text{CreditScore}))

where:
- ![\sigma(z) = \frac{1}{1 + e^{-z}}](https://latex.codecogs.com/svg.latex?\sigma(z)%20=%20\frac{1}{1%20+%20e^{-z}}) is the sigmoid function
- ![w_0, w_1, w_2](https://latex.codecogs.com/svg.latex?w_0,%20w_1,%20w_2) are model weights

### 2️⃣ Compute Initial Prediction for T1
Given:
- **Test case T1**: Age = 37, CreditScore = 705
- **Weights**: ![w_0 = 0.5, w_1 = -0.02, w_2 = 0.01](https://latex.codecogs.com/svg.latex?w_0%20=%200.5,%20w_1%20=%20-0.02,%20w_2%20=%200.01)

We compute:

![z = w_0 + w_1 \cdot 37 + w_2 \cdot 705](https://latex.codecogs.com/svg.latex?z%20=%20w_0%20+%20w_1%20\cdot%2037%20+%20w_2%20\cdot%20705)

Then apply the sigmoid function to obtain the probability:

![P(\text{Low Risk}) = \frac{1}{1 + e^{-z}}](https://latex.codecogs.com/svg.latex?P(\text{Low%20Risk})%20=%20\frac{1}{1%20+%20e^{-z}})

### 3️⃣ Compute Cost Function
The logistic regression cost function is:

![J(\theta) = -\frac{1}{m} \sum_{i=1}^{m} \Big[ y_i \log(\hat{y}_i) + (1 - y_i) \log(1 - \hat{y}_i) \Big]](https://latex.codecogs.com/svg.latex?J(\theta)%20=%20-\frac{1}{m}%20\sum_{i=1}^{m}%20\Big[%20y_i%20\log(\hat{y}_i)%20+%20(1%20-%20y_i)%20\log(1%20-%20\hat{y}_i)%20\Big])

where:
- ![\hat{y}_i](https://latex.codecogs.com/svg.latex?\hat{y}_i) is the predicted probability
- ![y_i](https://latex.codecogs.com/svg.latex?y_i) is the actual label (`Low = 1`, `High = 0`)
- ![m](https://latex.codecogs.com/svg.latex?m) is the number of training samples

## 📊 Expected Outcome
- Compute the probability of `T1` being `Low Risk`
- Evaluate the model's initial performance with the cost function
