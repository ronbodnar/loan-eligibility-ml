<h1 align="center">Loan Eligibility Intelligence</h1>

<p align="center">
  An end-to-end Machine Learning pipeline for binary classification and predictive risk assessment.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.9+-3776AB" />
  <img src="https://img.shields.io/badge/Scikit--Learn-F7931E" />
  <img src="https://img.shields.io/badge/Model-Random_Forest-green" />
  <img src="https://img.shields.io/badge/Optimization-GridSearchCV-blue" />
</p>

**Loan Eligibility Prediction** is a comprehensive data science project designed to automate the credit risk assessment process. By leveraging ensemble learning methods and rigorous hyperparameter tuning, the system predicts loan approval outcomes with high precision. The project features a complete lifecycle from exploratory data analysis (EDA) to a real-time interactive prediction interface.

<br />

## 📊 Data Pipeline & Feature Engineering

To ensure model stability, the raw dataset underwent a rigorous preprocessing pipeline:
- **Feature Normalization**: Handling skewed distributions to improve convergence in linear models.
- **Class Balancing (SMOTE/Oversampling)**: Addressing the inherent bias in loan approval data by synthesizing minority class samples to prevent model overfitting toward "Approved" outcomes.
- **Correlation Analysis**: Utilizing Heatmaps to identify multi-collinearity and prune features that do not contribute to predictive power.

<br />

## 🤖 Model Architecture

The project evaluates multiple classification strategies to identify the most robust predictor:

| Algorithm | Intent | Baseline Accuracy |
| :--- | :--- | :--- |
| **Logistic Regression** | Establishing a linear baseline | ~84% |
| **Support Vector Classifier** | High-dimensional margin maximization | ~81% |
| **Random Forest** | Ensemble bagging for variance reduction | **~88%** |

### Hyperparameter Optimization
Using **GridSearchCV**, the Random Forest model was tuned across 500+ permutations.
- **Best Params**: `{'criterion': 'gini', 'max_depth': 10, 'max_features': 'sqrt', 'n_estimators': 500}`
- **Result**: Significant reduction in False Positives, critical for financial risk mitigation.

<br />

## 📈 Performance Evaluation

Beyond simple accuracy, the models were scored on **Precision** and **Recall** to ensure a balance between risk (not approving a good loan) and safety (approving a bad loan).

- **Best Model**: Random Forest (Optimized)
- **Precision**: 89% (High confidence in "Approved" predictions)
- **Recall**: 88% (Effectively capturing the majority of eligible applicants)

<br />

## 💻 Interactive Simulation

The project includes an integrated UI within the Jupyter environment, allowing stakeholders to input custom parameters (Credit Score, Income, Debt Ratio) and receive an instant eligibility prediction with the underlying model confidence.

<br />

## 🚦 Getting Started

1. **Clone the repository**
```bash
git clone https://github.com/ronbodnar/loan-eligibility-prediction.git
cd loan-eligibility-prediction
```

2. **Install Dependencies**
```bash
pip install pandas scikit-learn matplotlib seaborn ipywidgets
```

3. **Launch the Engine**
```bash
jupyter notebook main.ipynb
```

<br />

## 📫 Connect
**Ronald Bodnar**
- Student ID: 011194327
- LinkedIn: [linkedin.com/in/ronbodnar](https://linkedin.com/in/ronbodnar)
- Portfolio: [ronbodnar.com](https://ronbodnar.com)

<br />

## ⚖️ License
MIT License. Created for WGU C964.
