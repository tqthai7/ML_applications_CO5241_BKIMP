# 📌 Question 1: Information Gain for CreditScore Split

## 🔍 Problem Overview
In this task, we analyze whether splitting on `CreditScore = 650` is an optimal decision for constructing a decision tree to classify loan risk levels. By calculating the **information gain (IG)**, we will determine if this attribute should be chosen as the root node.

## 🏷️ Methodology
To evaluate the effectiveness of this split, we follow these key steps:

### 1️⃣ Compute Parent Node Entropy
Entropy measures the impurity of a dataset and is calculated using:

![Entropy Formula](https://latex.codecogs.com/png.image?H(S)=-%5Csum_%7Bi=1%7D%5E%7Bc%7D%20p_i%20log_2(p_i))

where \( p_i \) represents the proportion of each class (High Risk or Low Risk).

### 2️⃣ Split Data and Compute Child Node Entropy
- Divide the dataset into two groups:
  - `CreditScore ≤ 650`
  - `CreditScore > 650`
- Compute entropy for each subset using the same formula.

### 3️⃣ Calculate Information Gain (IG)
Information Gain quantifies how much entropy is reduced after the split:

![Information Gain Formula](https://latex.codecogs.com/png.image?IG=H(S)-%5Csum_%7Bi=1%7D%5E%7Bk%7D%20%5Cfrac%7B%7CS_i%7C%7D%7B%7CS%7C%7D%20H(S_i))

where \( S_i \) represents each subset created by the split.

### 4️⃣ Decision Analysis
- **Higher IG** → The split is effective, making `CreditScore` a strong candidate for the root node.
- **Lower IG** → The split is weak, and other attributes (e.g., `Age` or `Education`) should be considered.

## 📊 Expected Outcome
By computing IG, we will determine if `CreditScore=650` provides the best split for the root node. If the gain is insufficient, alternative features should be evaluated.
