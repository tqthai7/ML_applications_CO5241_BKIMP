# Loan Risk Prediction Analysis 🚀

## 📌 Project Overview
This repository contains a comprehensive analysis of loan risk prediction using various machine learning techniques. We explore decision trees, regression models, neural networks, SVMs, k-NN, and Hidden Markov Models, with detailed step-by-step explanations and implementations.

## 📂 Repository Structure
A structured **folder architecture** ensures clear feature ownership, predictable module usage, and ease of maintenance.

- `notebooks/` - Jupyter notebooks implementing solutions for each question
- `cheat_sheets/` - A complete cheat sheet summarizing essential concepts, formulas, and methods
- `reports/` - PDF files containing mathematical derivations and detailed explanations
- `data/` - Training and test datasets for model evaluation

```plaintext
repo-root/
│── 📜 README.md               # Project documentation
│── 📜 .gitignore              # Git ignore rules
│── 📜 requirements.txt        # List of dependencies
│
├── 📂 data/                   # Contains all datasets
│   ├── 📂 train/              # Raw, unprocessed training data
│   ├── 📂 test/               # Cleaned and transformed test data
│
├── 📂 questions/              # Jupyter notebooks and reports for each question
│   ├── 📂 question_01/        # Question 1: Decision Trees
│   │   ├── 📂 notebook/       # Jupyter notebook implementation
│   │   │   ├── 📄 decision_tree.ipynb
│   │   ├── 📂 report/         # Detailed explanation and derivation
│   │   │   ├── 📄 decision_tree_report.pdf
│   │   └── 📂 figures
│   │
│   ├── 📂 question_02/        # Question 2: Regression Trees
│   │   ├── 📂 notebook/       
│   │   │   ├── 📄 regression_tree.ipynb
│   │   ├── 📂 report/        
│   │   │   ├── 📄 regression_tree_report.pdf
│   │   └── 📂 figures
│   │
│   ├── 📂 question_03/        # Question 3: Handling Missing Values
│   │   ├── 📂 notebook/       
│   │   │   ├── 📄 missing_values.ipynb
│   │   ├── 📂 report/        
│   │   │   ├── 📄 missing_values_report.pdf
│   │   └── 📂 figures
│   │
│   ├── ...                    # More questions follow the same structure
│   ├── 📂 question_20/        # Question 20: Nonlinear Decision Boundaries
│   │   ├── 📂 notebook/       
│   │   │   ├── 📄 nonlinear_svm.ipynb
│   │   ├── 📂 report/        
│   │   │   ├── 📄 nonlinear_svm_report.pdf
│   │   └── 📂 figures
│   
├── 📂 reports/                # Final reports and documentation
│   ├── 📄 summary_report.pdf   # High-level summary of findings
│   ├── 📄 bias_analysis.pdf    # Bias detection and mitigation report
│   ├── 📄 feature_importance.pdf # Feature analysis report
│
├── 📂 cheat_sheets/           # Quick reference guides for key concepts
│   ├── 📄 decision_trees_cheat_sheet.pdf
│   ├── 📄 regression_cheat_sheet.pdf
│   ├── 📄 neural_networks_cheat_sheet.pdf
│   ├── 📄 svm_knn_cheat_sheet.pdf
│   ├── 📄 hmm_cheat_sheet.pdf
```

## 📝 Issues & Solutions
Each question corresponds to a **specific machine learning topic**, with a Jupyter notebook and an explanation report.

### 🌳 Decision Trees
1. **Is CreditScore = 650 the Best Split?** - Information gain analysis.
2. **Variance Reduction in Regression Trees** - Impact of Age = 35 split.

### 🎲 Probabilistic Models
3. **Handling Missing Values** - Estimating risk probability when Education is missing.
4. **Naïve vs. Bayesian Classification** - Comparing probability-based approaches.

### 📈 Regression Models
5. **Batch Gradient Descent for CreditScore Prediction** - Implementing gradient descent.
6. **Solving Multiple Linear Regression with Normal Equation** - Finding optimal parameters.

### 🔍 Classification Models
8. **Optimizing Logistic Regression** - Training and evaluating logistic regression.
9. **Perceptron for Loan Risk Classification** - Implementing a simple neural network classifier.
10. **Neural Networks: Forward & Backpropagation** - Training a single hidden-layer network.

### 💡 SVM and k-NN
11. **Finding the Optimal SVM Margin** - Identifying support vectors and hyperplanes.
12. **Kernel SVM: Nonlinear Decision Boundaries** - Applying the RBF kernel.
13. **k-NN Classification** - Implementing k-nearest neighbors.
14. **Distance-Weighted k-NN vs. Standard k-NN** - Robustness comparison.

### 🔄 Hidden Markov Models
15. **Credit Risk Progression using Viterbi Algorithm** - Predicting state sequences.
16. **Future Credit Score Prediction with Forward Algorithm** - Estimating likelihoods.

### 📊 Model Evaluation & Bias Analysis
17. **Bias Detection in Loan Risk Dataset** - Identifying biases.
18. **Precision & Recall Analysis** - Evaluating classification performance.
19. **CreditScore Variance & Entropy Analysis** - Understanding data impact.

### 🔥 Advanced ML Concepts
20. **Nonlinear Decision Boundaries** - Kernel SVM and kernel matrix calculations.

## ⚙️ How to Run
1. Clone the repository:
   ```sh
   git clone <repo-link>
   ```
2. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```
3. Run Jupyter notebooks:
   ```sh
   jupyter notebook
   ```

## 🤝 Contribution
Each issue corresponds to a specific question, tracked via GitHub Issues. Contributions, pull requests, and discussions are welcome!

## ✍️ Author
- **Trần Quốc Thái**  
- **ID Student:** 2370759
