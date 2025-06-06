# 🎯 Machine Learning Project

## 📋 Problem Statement

This project aims to predict depression based on various factors including demographic information, professional status, academic/work metrics, and lifestyle factors. The target variable is binary (Depression: 0 or 1), making this a binary classification problem.

## 📊 Dataset Overview

- **Size**: 140,700 records with 20 features
- **Target Distribution**:
  - Non-depressed (0): 81.8%
  - Depressed (1): 18.2%
- **Features**: Demographic, professional, academic, lifestyle, and mental health indicators

## 🤖 Model Implementations

### 1. Support Vector Machine (SVM)

- **Kernels Tested**: Linear, RBF, Polynomial, Sigmoid
- **Hyperparameter Tuning**: GridSearchCV
- **Key Features**:
  - Probability estimates enabled
  - Bias-variance analysis performed
  - Kernel-specific performance evaluation
- **Implementation**: `SVC(kernel='rbf', probability=True, random_state=42)`

### 2. Random Forest Classifier

- **Configuration**:
  - Class weight balancing
  - Feature importance analysis
- **Implementation**: `RandomForestClassifier(class_weight='balanced', random_state=42)`

### 3. Logistic Regression

- **Configuration**:
  - Maximum iterations: 1000
  - Random state: 42
- **Implementation**: `LogisticRegression(max_iter=1000, random_state=42)`

### 4. Adaboost
- **Configuration**:
  - Base estimator: Decision Tree
  - Number of estimators: 100
  - Learning rate: 0.1
- **Key Features**:
  - Boosting weak learners
  - Adaptive weight adjustment
  - Robust to overfitting
- **Implementation**: `AdaBoostClassifier(n_estimators=100, learning_rate=0.1, random_state=42)`



## 📈 Model Evaluation

All models were evaluated using:

- Classification Report (Precision, Recall, F1-score)
- Accuracy Score
- Confusion Matrix

- all models gives around 94% accuracy

## 🛠️ Technical Implementation

- **Data Processing**: Feature scaling and encoding
- **Model Selection**: Multiple algorithms with hyperparameter tuning
- **Evaluation**: Cross-validation and performance metrics
- **Tools**: scikit-learn, pandas, numpy, matplotlib

## 📁 Project Structure

```
.
├── dataset/
│   ├── train.csv
│   ├── test.csv
│   └── sample_submission.csv
├── notebooks/
│   ├── data_analysis.ipynb
│   ├── feature-engineering.ipynb
│   └── model.ipynb
└── 
```

## 🚀 Usage

1. Clone the repository
2. Install dependencies: `pip install -r requirements.txt`
3. Run notebooks in sequence:
   - `data_analysis.ipynb`: Initial data exploration
   - `feature-engineering.ipynb`: Feature preprocessing
   - `model.ipynb`: Model training and evaluation

