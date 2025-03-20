# 📌 Question 7: Logistic Regression for Loan Risk Classification

## 🔍 Problem Overview
In this task, we formulate a **logistic regression model** to predict `RiskLevel` (Low or High) based on `Age` and `CreditScore`. We then compute the initial prediction for test case **T1** using given weights.

## 🏗️ Methodology
### 1️⃣ Logistic Regression Model
Logistic regression predicts the probability of `RiskLevel` using the **sigmoid function**:
\[
P(\text{Low Risk} | \text{Age}, \text{CreditScore}) = \sigma(w_0 + w_1 \cdot \text{Age} + w_2 \cdot \text{CreditScore})
\]
where:
- \( \sigma(z) = \frac{1}{1 + e^{-z}} \) is the sigmoid function
- \( w_0, w_1, w_2 \) are model weights

### 2️⃣ Compute Initial Prediction for T1
Given:
- **Test case T1**: Age = 37, CreditScore = 705
- **Weights**: \( w_0 = 0.5, w_1 = -0.02, w_2 = 0.01 \)

We compute:
\[
z = w_0 + w_1 \cdot 37 + w_2 \cdot 705
\]
Then apply the sigmoid function to obtain the probability.

### 3️⃣ Compute Cost Function
The logistic regression cost function is:
\[
J(\theta) = -\frac{1}{m} \sum_{i=1}^{m} \Big[ y_i \log(\hat{y}_i) + (1 - y_i) \log(1 - \hat{y}_i) \Big]
\]
where:
- \( \hat{y}_i \) is the predicted probability
- \( y_i \) is the actual label (Low = 1, High = 0)
- \( m \) is the number of training samples

## 📊 Expected Outcome
- Compute the probability of `T1` being `Low Risk`
- Evaluate the model's initial performance with the cost function

