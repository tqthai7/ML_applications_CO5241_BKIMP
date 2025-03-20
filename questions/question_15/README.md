# 📌 Question 15: Optimal Margin Hyperplane for Loan Risk Classification

## 🔍 Problem Overview
In this task, we construct an **Optimal Margin Hyperplane (OMH)** using **Support Vector Machines (SVM)** to separate `Low Risk` and `High Risk` classes based on `Age` and `CreditScore`. We also analyze the impact of **soft margin SVM** on the classification boundary.

## 🏗️ Methodology
### 1️⃣ Identifying Support Vectors
- **Support vectors** are the data points that lie closest to the decision boundary.
- The margin is defined as the perpendicular distance between these support vectors and the hyperplane.
- The hyperplane equation:
  \[
  w_1 \cdot \text{Age} + w_2 \cdot \text{CreditScore} + b = 0
  \]

### 2️⃣ Hard Margin SVM
- Assumes that the data is **perfectly separable**.
- Maximizes the margin \( \frac{2}{||w||} \) without misclassifications.

### 3️⃣ Soft Margin SVM (Handling Overlapping Data)
- Introduces **slack variables** \( \xi_i \) to allow some misclassifications.
- The optimization problem becomes:
  \[
  \min \frac{1}{2} ||w||^2 + C \sum \xi_i
  \]
  where \( C \) controls the trade-off between maximizing the margin and minimizing classification errors.

### 4️⃣ Impact of Using Soft Margin
- **Larger C** → Fewer misclassifications, but lower margin.
- **Smaller C** → Wider margin, but allows more misclassified points.
- Practical when data contains noise or slight overlaps.

## 📊 Expected Outcome
- Determine the **support vectors** from the training set.
- Compute the **optimal margin hyperplane** using SVM.
- Compare **hard margin vs. soft margin SVM** and analyze how the margin changes.