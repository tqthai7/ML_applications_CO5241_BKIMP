# 📌 Question 3: Probability Estimation and Handling Missing Values

## 🔍 Problem Overview
In this task, we estimate the probability that test sample `T2` belongs to the `High Risk` category, given that its `Education` value is missing. Additionally, we propose a robust method to handle missing values in future cases.

## 🏗️ Methodology
To compute the probability of `T2` being `High Risk`, we use the following approach:

### 1️⃣ Compute Conditional Probabilities
Using the training dataset, we estimate:

<div align="center">
    <img src="https://latex.codecogs.com/png.image?\dpi{110}P(\text{High%20Risk}%20|%20\text{Age},%20\text{CreditScore})" alt="Conditional Probability">
</div>

![Conditional Probability](https://latex.codecogs.com/png.image?\dpi{110}P(\text{High%20Risk}%20|%20\text{Age},%20\text{CreditScore}))

by considering the patterns of `CreditScore` and `Age` in the existing `High Risk` and `Low Risk` samples.

### 2️⃣ Apply Bayesian Probability
Since `Education` is missing, we marginalize over the possible values based on observed distributions:

![Bayes Formula](https://latex.codecogs.com/png.image?\dpi{110}P(\text{High%20Risk}%20|%20\text{Age},%20\text{CreditScore})=%20\frac{P(\text{Age},%20\text{CreditScore}%20|%20\text{High%20Risk})%20P(\text{High%20Risk})}{P(\text{Age},%20\text{CreditScore})})

We estimate probabilities from the training set by computing frequency-based likelihoods.

### 3️⃣ Handling Missing Values
For future cases where `Education` is missing, we consider:
- **Mean/Median Imputation:** Replacing missing values with the mean or median of `Education` in the training set.
- **Predictive Imputation:** Using regression models to estimate the missing value based on correlated features (`Age`, `CreditScore`).
- **Multiple Imputation:** Assigning multiple possible values and averaging results.
- **Using a Special Category:** Treating `missing` as a unique category and incorporating it into the model.

## 📊 Expected Outcome
By computing conditional probabilities, we classify `T2` into `High Risk` or `Low Risk`. Additionally, we identify a robust imputation strategy to handle missing values effectively in future data processing.
