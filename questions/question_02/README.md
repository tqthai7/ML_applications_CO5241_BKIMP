# 📌 Question 2: Variance Reduction for Regression Decision Tree

## 🔍 Problem Overview
In this task, we analyze whether splitting on `Age = 35` in a regression decision tree for predicting `CreditScore` leads to a significant **variance reduction**. This will help determine if `Age` is an effective splitting criterion.

## 🏗️ Methodology
To assess the effectiveness of this split, we follow these key steps:

### 1️⃣ Compute the Variance of the Parent Node
Variance measures the spread of values within the dataset and is calculated as:
\[
Var(S) = \frac{1}{n} \sum_{i=1}^{n} (x_i - \bar{x})^2
\]
where \( x_i \) are individual values and \( \bar{x} \) is the mean of `CreditScore`.

### 2️⃣ Split Data and Compute Variance for Each Child Node
- Divide the dataset into two groups:
  - `Age ≤ 35`
  - `Age > 35`
- Compute variance for each subset using the same formula.

### 3️⃣ Calculate Variance Reduction
Variance Reduction (VR) quantifies the effectiveness of a split and is calculated as:
\[
VR = Var(S) - \sum_{i=1}^{k} \frac{|S_i|}{|S|} Var(S_i)
\]
where \( S_i \) represents each subset created by the split.

### 4️⃣ Decision Analysis
- **Higher VR** → The split significantly reduces variance, making `Age` a strong candidate for splitting.
- **Lower VR** → The split does not significantly improve prediction accuracy, and other features should be considered.

### 🔹 Difference Between Variance Reduction & Information Gain
- **Information Gain (IG)** is used in classification tasks and measures entropy reduction.
- **Variance Reduction (VR)** is used in regression tasks and measures the reduction in numerical spread.

## 📊 Expected Outcome
By computing VR, we determine if `Age = 35` is a meaningful split for a regression tree predicting `CreditScore`. If the VR is low, alternative splits should be explored.

