# Loan Risk Prediction Analysis 🚀

## 📌 Project Overview
This repository contains a comprehensive analysis of loan risk prediction using various machine learning techniques. We explore decision trees, regression models, neural networks, SVMs, k-NN, and Hidden Markov Models, with detailed step-by-step explanations and implementations.

## 📂 Repository Structure
- `notebooks/` - Jupyter notebooks implementing solutions for each question
- `cheat_sheets/` - A complete cheat sheet summarizing essential concepts, formulas, and methods
- `reports/` - PDF files containing mathematical derivations and detailed explanations
- `data/` - Training and test datasets for model evaluation

├── data/                  # Contains all datasets  
│   ├── train/             # Training datasets
│   ├── test/              # Testing datasets
│  
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


## 📝 Issues & Solutions
### 🌳 Decision Trees
1. **Is CreditScore = 650 the Best Split?** - Calculating information gain for decision tree classification.
2. **Variance Reduction in Regression Trees** - Analyzing the effect of splitting on Age = 35.

### 🎲 Probabilistic Models
3. **Handling Missing Values in Loan Risk Prediction** - Estimating risk level probability when Education is missing.
4. **Naïve vs. Bayesian Classification for Loan Risk** - Comparing probability-based classification approaches.

### 📈 Regression Models
5. **Batch Gradient Descent for CreditScore Prediction** - Implementing gradient descent from scratch.
6. **Solving Multiple Linear Regression with Normal Equation** - Finding optimal parameters using matrix algebra.
7. **Model Performance: MSE & R² Calculation** - Evaluating regression accuracy.

### 🔍 Classification Models
8. **Optimizing Logistic Regression for Loan Risk** - Training and evaluating logistic regression.
9. **Perceptron for Loan Risk Classification** - Implementing a simple neural network classifier.
10. **Neural Networks: Forward & Backpropagation** - Training a single hidden-layer neural network.

### 💡 SVM and k-NN
11. **Finding the Optimal SVM Margin for Loan Risk** - Identifying support vectors and hyperplanes.
12. **Kernel SVM: Nonlinear Decision Boundaries** - Applying the RBF kernel for classification.
13. **k-NN Loan Risk Classification with Euclidean Distance** - Implementing k-nearest neighbors.
14. **Distance-Weighted k-NN vs. Standard k-NN** - Comparing robustness in loan classification.

### 🔄 Hidden Markov Models
15. **Credit Risk Progression using the Viterbi Algorithm** - Predicting state sequences over time.
16. **Future Credit Score Prediction with Forward Algorithm** - Estimating observation likelihoods.

### 📊 Model Evaluation & Bias Analysis
17. **Bias Detection in Loan Risk Dataset** - Identifying and mitigating potential biases in training data.
18. **Precision & Recall for Loan Risk Models** - Evaluating classification performance metrics.
19. **CreditScore Variance & Entropy Analysis** - Understanding data distribution impact on ML models.

### 🔥 Advanced ML Concepts
20. **Loan Risk Prediction with Nonlinear Decision Boundaries** - Applying kernel SVM and calculating the kernel matrix.

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
