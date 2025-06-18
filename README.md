# Diabetes Progression Prediction - Machine Learning Lab 2

This project analyzes and models the progression of diabetes using various supervised learning techniques. It is part of the **Foundations of Machine Learning Frameworks (CSCN8010)** course, and aims to compare the performance of different regression models.

## Author

- **Name:** Kumari Nikitha Singh  
- **Student ID:** 9053016  
- **College:** Conestoga College  
- **Course:** CSCN8010 – Foundations of Machine Learning Frameworks  
- **Lab:** Practical Lab 2

---

##  Problem Statement

We aim to predict **disease progression one year after baseline** using patient health data from the **Scikit-Learn Diabetes Dataset**. The problem is treated as a **supervised regression** task.

---

##  Dataset Description

- **Source:** `sklearn.datasets.load_diabetes()`
- **Samples:** 442
- **Features:** 10 standardized medical attributes (e.g., age, BMI, blood pressure)
- **Target:** Quantitative measure of disease progression

---

##  Models Implemented

### Part 1: Univariate Polynomial Regression (on BMI)
- Polynomial degrees: 0 to 5
- Metrics: R², MAE, MAPE
- Selected best model using validation metrics
- Tested final model on unseen test set

### Part 2: Multivariate Polynomial Regression
- Features: `bmi`, `bp`, `s3`, `s5`
- Polynomial degrees: 2 and 3

### Part 3: Model Comparisons
- **Decision Trees**: max_depth = 2, 5
- **k-Nearest Neighbors**: k = 3, 7
- All evaluated on: R², MAE, MAPE

---

##  Evaluation Metrics

| Metric | Meaning |
|--------|---------|
| R²     | Coefficient of Determination (model fit) |
| MAE    | Mean Absolute Error (average magnitude of error) |
| MAPE   | Mean Absolute Percentage Error (relative error %) |

---

##  Results Summary

| Model               | R² (Test) | MAE     | MAPE   |
|--------------------|-----------|---------|--------|
| **Poly Deg 2**      | **0.47**  | 43.15   | 0.278  |
| Poly Deg 3         | 0.43      | 45.25   | 0.295  |
| Decision Tree (d=2)| 0.39      | 45.80   | 0.290  |
| kNN (k=7)          | 0.38      | 44.90   | 0.280  |

**Best Model:** Polynomial Regression (Degree 2) — best balance of generalization and performance.

---

##  Project Structure

```bash
Lab-2/
│
├── Diabetes_Prediction_Lab2.ipynb   # Main Jupyter Notebook
├── requirements.txt                 # Python dependencies
├── .gitignore                       # Files to ignore in version control
└── README.md                        # Project overview
```

---

##  Installation

1. Clone the repo:
```bash
git clone https://github.com/nikitha2002-bot/Lab-2.git
cd Lab-2
```

2. Create a virtual environment (optional but recommended):
```bash
python -m venv venv
source venv/bin/activate   # or venv\Scripts\activate on Windows
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

---

##  Requirements

See `requirements.txt` for full list. Key libraries:
- scikit-learn
- pandas
- matplotlib
- seaborn
- numpy

---


