# 📌 Question 2: Variance Reduction for Regression Decision Tree

## 🔍 Problem Overview
In this task, we analyze whether splitting on `Age = 35` in a regression decision tree for predicting `CreditScore` leads to a significant **variance reduction**. This will help determine if `Age` is an effective splitting criterion.

## 🏗️ Methodology
To assess the effectiveness of this split, we follow these key steps:

### 1️⃣ Compute the Variance of the Parent Node
Variance measures the spread of values within the dataset and is calculated as:

![Variance Formula](https://latex.codecogs.com/png.image?\dpi{110}Var(S)=\frac{1}{n}\sum_{i=1}^{n}(x_i-\bar{x})^2)

where  
- ![x_i](https://latex.codecogs.com/png.image?\dpi{110}x_i) are individual values of `CreditScore`,  
- ![\bar{x}](https://latex.codecogs.com/png.image?\dpi{110}\bar{x}) is the mean of `CreditScore`,  
- ![n](https://latex.codecogs.com/png.image?\dpi{110}n) is the number of samples.

### 2️⃣ Split Data and Compute Variance for Each Child Node
- Divide the dataset into two groups:  
  - `Age ≤ 35`
  - `Age > 35`
- Compute variance for each subset using the same formula:

![Subset Variance Formula](https://latex.codecogs.com/png.image?\dpi{110}Var(S_i)=\frac{1}{|S_i|}\sum_{j=1}^{|S_i|}(x_j-\bar{x_i})^2)

where  
- ![S_i](https://latex.codecogs.com/png.image?\dpi{110}S_i) represents each subset created by the split,  
- ![x_j](https://latex.codecogs.com/png.image?\dpi{110}x_j) are individual values in subset \( S_i \),  
- ![\bar{x_i}](https://latex.codecogs.com/png.image?\dpi{110}\bar{x_i}) is the mean of `CreditScore` in subset \( S_i \),  
- ![|S_i|](https://latex.codecogs.com/png.image?\dpi{110}|S_i|) is the number of samples in subset \( S_i \).

### 3️⃣ Calculate Variance Reduction
Variance Reduction (VR) quantifies the effectiveness of a split and is calculated as:

![Variance Reduction Formula](https://latex.codecogs.com/png.image?\dpi{110}VR=Var(S)-\sum_{i=1}^{k}\frac{|S_i|}{|S|}Var(S_i))

where  
- ![Var(S)](https://latex.codecogs.com/png.image?\dpi{110}Var(S)) is the variance of the parent node,  
- ![Var(S_i)](https://latex.codecogs.com/png.image?\dpi{110}Var(S_i)) is the variance of subset \( S_i \),  
- ![|S_i|](https://latex.codecogs.com/png.image?\dpi{110}|S_i|) represents the number of samples in subset \( S_i \),  
- ![|S|](https://latex.codecogs.com/png.image?\dpi{110}|S|) is the total number of samples before the split.

### 4️⃣ Decision Analysis
- **Higher VR** → The split significantly reduces variance, making `Age` a strong candidate for splitting.
- **Lower VR** → The split does not significantly improve prediction accuracy, and other features should be considered.

### 🔹 Difference Between Variance Reduction & Information Gain
- **Information Gain (IG)** is used in classification tasks and measures entropy reduction.
- **Variance Reduction (VR)** is used in regression tasks and measures the reduction in numerical spread.

## 📊 Expected Outcome
By computing VR, we determine if `Age = 35` is a meaningful split for a regression tree predicting `CreditScore`. If the VR is low, alternative splits should be explored.
