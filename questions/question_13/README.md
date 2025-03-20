# 📌 Question 13: Precision and Recall for Loan Risk Assessment

## 🔍 Problem Overview
In this task, we evaluate the performance of different classifiers (Perceptron and Naïve Bayes) using **precision** and **recall** metrics. These metrics help determine the effectiveness of our models in identifying `High Risk` cases accurately.

## 🏗️ Methodology
### 1️⃣ Precision and Recall Calculation
Precision and recall are defined as:
- **Precision**: Measures how many predicted `High Risk` cases are actually `High Risk`.
  \[
  Precision = \frac{TP}{TP + FP}
  \]
- **Recall**: Measures how many actual `High Risk` cases were correctly predicted.
  \[
  Recall = \frac{TP}{TP + FN}
  \]

Where:
- **TP** (True Positives): `High Risk` cases correctly predicted.
- **FP** (False Positives): `Low Risk` cases incorrectly classified as `High Risk`.
- **FN** (False Negatives): `High Risk` cases missed by the model.

### 2️⃣ Evaluating Perceptron and Naïve Bayes
- Compute **confusion matrices** for both models.
- Calculate precision and recall for each classifier.
- Compare results to determine which model is better for loan risk assessment.

### 3️⃣ Choosing the More Important Metric
- **When precision matters**: If false positives (misclassifying `Low Risk` as `High Risk`) cause unnecessary loan rejections.
- **When recall matters**: If missing `High Risk` cases (false negatives) leads to financial losses.
- **Recommended Focus**: Higher recall is often preferred in loan risk assessment to minimize default risk.

## 📊 Expected Outcome
- Compute precision and recall for both classifiers.
- Recommend the more critical metric for this domain.
- Justify the decision based on financial implications.