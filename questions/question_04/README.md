# 📌 Question 4: Batch Gradient Descent for CreditScore Prediction

## 🔍 Problem Overview
In this task, we implement **batch gradient descent** to optimize the weights for predicting CreditScore using Age. The goal is to perform one iteration of gradient descent and interpret how the parameters update.

## 🏗️ Methodology
To find the optimal weights \( \theta_0 \) and \( \theta_1 \), we use the **Mean Squared Error (MSE) cost function**:
\[
J(\theta_0, \theta_1) = \frac{1}{2m} \sum_{i=1}^{m} (y_i - (\theta_0 + \theta_1 x_i))^2
\]
where:
- \( y_i \) is the actual CreditScore
- \( x_i \) is Age
- \( m \) is the number of training samples
- \( \theta_0, \theta_1 \) are model parameters

### 1️⃣ Compute Partial Derivatives
The gradients for the cost function are:
\[
\frac{\partial J}{\partial \theta_0} = -\frac{1}{m} \sum_{i=1}^{m} (y_i - \hat{y}_i)
\]
\[
\frac{\partial J}{\partial \theta_1} = -\frac{1}{m} \sum_{i=1}^{m} (y_i - \hat{y}_i) x_i
\]
where \( \hat{y}_i \) is the predicted CreditScore.

### 2️⃣ Update Parameters
Using **gradient descent**, the parameters are updated as follows:
\[
\theta_0^{(new)} = \theta_0 - \alpha \frac{\partial J}{\partial \theta_0}
\]
\[
\theta_1^{(new)} = \theta_1 - \alpha \frac{\partial J}{\partial \theta_1}
\]
where \( \alpha = 0.01 \) is the learning rate.

### 3️⃣ Interpret the Updates
The direction of parameter updates indicates whether the model is moving towards a better fit. If the gradient is **positive**, the parameter is **decreased**; if it is **negative**, the parameter is **increased**.

## 📊 Expected Outcome
By performing one iteration of gradient descent, we update \( \theta_0 \) and \( \theta_1 \), improving the model's ability to predict CreditScore based on Age.
