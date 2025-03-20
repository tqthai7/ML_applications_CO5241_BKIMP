# Loan Risk Prediction Analysis 🚀

## 📌 Project Overview
This repository contains a comprehensive analysis of loan risk prediction using various machine learning techniques. We explore decision trees, regression models, neural networks, SVMs, k-NN, and Hidden Markov Models, with detailed step-by-step explanations and implementations.

## 📂 Repository Structure
- `notebooks/` - Jupyter notebooks implementing solutions for each question
- `cheat_sheets/` - A complete cheat sheet summarizing essential concepts, formulas, and methods
- `reports/` - PDF files containing mathematical derivations and detailed explanations
- `data/` - Training and test datasets for model evaluation
├── 📂 data/                   # Contains all datasets
│   ├── 📂 train/              # Raw, unprocessed training data
│   ├── 📂 test/               # Cleaned and transformed test data
├── questions/             # Jupyter notebooks and reports for each question  
│   ├── question_1/  
│   │   ├── notebook/      # Jupyter notebook for analysis  
│   │   ├── report/        # PDF report with explanations & derivations  
│   │   ├── models/        # Python implementation of the models  
│   │   └── figures/       # Visualization plots, graphs, and outputs  
│   ├── question_2/  
│   │   ├── notebook/  
│   │   ├── report/  
│   │   ├── models/  
│   │   └── figures/  
│   ├── ...  
│   ├── question_20/  
│   │   ├── notebook/  
│   │   ├── report/  
│   │   ├── models/  
│   │   └── figures/  
│  
├── cheat_sheets/          # Quick reference guides for ML concepts  
│   ├── decision_trees.pdf  
│   ├── regression.pdf  
│   ├── neural_networks.pdf  
│   ├── svm_knn.pdf  
│   ├── hmm.pdf  
│  
├── requirements.txt       # List of dependencies  
├── README.md              # Project documentation  
└── .gitignore             # Ignore unnecessary files  


# Loan Risk Prediction Analysis 🚀

## 📌 Project Overview
This repository contains a comprehensive analysis of **loan risk prediction** using various machine learning techniques. We explore **decision trees, regression models, neural networks, SVMs, k-NN, and Hidden Markov Models**, with step-by-step explanations, implementations, and performance evaluation.

## 📂 Repository Structure
A structured **folder architecture** ensures clear feature ownership, predictable module usage, and ease of maintenance.

```plaintext
repo-root/
│── 📜 README.md               # Project documentation
│── 📜 .gitignore              # Git ignore rules
│── 📜 requirements.txt        # List of dependencies
│
├── 📂 data/                   # Contains all datasets
│   ├── 📂 train/              # Raw, unprocessed training data
│   ├── 📂 test/               # Cleaned and transformed test data
│   ├── 📂 external/           # Additional external datasets
│   ├── 📄 sample.csv          # Example dataset file
│
├── 📂 questions/              # Jupyter notebooks and reports for each question
│   ├── 📂 question_01/        # Question 1: Decision Trees
│   │   ├── 📂 notebook/       # Jupyter notebook implementation
│   │   │   ├── 📄 decision_tree.ipynb
│   │   ├── 📂 report/         # Detailed explanation and derivation
│   │   │   ├── 📄 decision_tree_report.pdf
│   │
│   ├── 📂 question_02/        # Question 2: Regression Trees
│   │   ├── 📂 notebook/       
│   │   │   ├── 📄 regression_tree.ipynb
│   │   ├── 📂 report/        
│   │   │   ├── 📄 regression_tree_report.pdf
│   │
│   ├── 📂 question_03/        # Question 3: Handling Missing Values
│   │   ├── 📂 notebook/       
│   │   │   ├── 📄 missing_values.ipynb
│   │   ├── 📂 report/        
│   │   │   ├── 📄 missing_values_report.pdf
│   │
│   ├── ...                    # More questions follow the same structure
│   ├── 📂 question_20/        # Question 20: Nonlinear Decision Boundaries
│   │   ├── 📂 notebook/       
│   │   │   ├── 📄 nonlinear_svm.ipynb
│   │   ├── 📂 report/        
│   │   │   ├── 📄 nonlinear_svm_report.pdf
│
├── 📂 src/                    # Source code for ML models
│   ├── 📂 models/             # Implementation of different ML models
│   │   ├── 📄 decision_tree.py
│   │   ├── 📄 linear_regression.py
│   │   ├── 📄 neural_network.py
│   │   ├── 📄 svm_knn.py
│   │   ├── 📄 hmm.py
│   │   ├── 📄 evaluation.py
│   │
│   ├── 📂 utils/              # Utility functions (data processing, feature engineering)
│   │   ├── 📄 data_loader.py
│   │   ├── 📄 preprocessing.py
│   │   ├── 📄 feature_engineering.py
│   │   ├── 📄 visualization.py
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
│
├── 📂 tests/                  # Unit tests for all models and utilities
│   ├── 📄 test_decision_tree.py
│   ├── 📄 test_linear_regression.py
│   ├── 📄 test_neural_network.py
│   ├── 📄 test_svm_knn.py
│   ├── 📄 test_hmm.py
│   ├── 📄 test_evaluation.py
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
Each issue corresponds to a specific question, tracked with GitHub Issues. Contributions, pull requests, and discussions are welcome!

## ✍️ Author
Full name: **Trần Quốc Thái**.
ID student: **2370759**.
