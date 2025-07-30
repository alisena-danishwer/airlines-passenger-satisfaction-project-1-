


# Airline Passenger Satisfaction - Machine Learning Analysis

This project is an individual assignment submitted for the CCS2213 Machine Learning course at Albukhary International University. The goal is to analyze airline passenger satisfaction using machine learning models, focusing on data preprocessing, model evaluation, and classifier comparison.

## 📊 Dataset Overview

* **Source:** [Kaggle - Airline Passenger Satisfaction Dataset](https://www.kaggle.com/datasets/teejmahal20/airline-passenger-satisfaction)
* **Size:** 103,904 records
* **Target Variable:** `Satisfaction` (`Satisfied` or `Neutral or Dissatisfied`)
* **Features:**

  * **Demographics:** Gender, Age, Customer Type, Type of Travel, Class
  * **Service Ratings:** Wi-Fi, Food, Boarding, Cleanliness, Seat Comfort
  * **Flight Info:** Distance, Delays, Time Convenience

## 📈 Project Workflow

### 1. Exploratory Data Analysis (EDA)

* Visualized patterns, distributions, and outliers
* Used libraries: `pandas`, `matplotlib`, `seaborn`

### 2. Data Preprocessing

* **Missing values:** Imputed with mean/mode
* **Outliers:** Removed using IQR method
* **Encoding:** One-hot encoding for categorical variables
* **Feature scaling:** StandardScaler
* **Feature selection:** Correlation matrix & Recursive Feature Elimination (RFE)

### 3. Class Distribution & Balance

| Label                   | Count  | Percentage |
| ----------------------- | ------ | ---------- |
| Neutral or Dissatisfied | 58,211 | 56.2%      |
| Satisfied               | 45,519 | 43.8%      |

* **Moderate imbalance** observed; handled using:

  * SMOTE / Undersampling
  * Class weights (`class_weight='balanced'`)
  * Evaluation metrics like F1-score, ROC-AUC

## 🧠 Classifiers Used

### 1. K-Nearest Neighbors (KNN)

* Pros: Simple, effective with naturally clustered data
* Cons: Sensitive to feature scaling

### 2. Decision Tree

* Pros: Interpretable, handles categorical and numerical data
* Additional benefit: Feature importance insight

## 🧪 Model Evaluation

* **Cross-validation:** k-Fold CV
* **Metrics:**

  * Accuracy
  * Precision & Recall
  * F1-Score (Primary Metric)
  * ROC-AUC Score
* **Why F1?**: Balances precision & recall, ideal for imbalanced datasets

## ✅ Key Takeaways

* Data preprocessing significantly improves model performance
* F1-score is more insightful than accuracy for imbalanced classes
* Both KNN and Decision Trees have unique strengths in classification
* Insights from this model can help airlines optimize service quality and passenger satisfaction

## 📚 References

1. Ban, H.-J., & Kim, H.-S. (2019). [Sustainability, 11(15), 4066](https://doi.org/10.3390/su11154066)
2. Santos et al. (2019). [Journal of Retailing and Consumer Services, 50](https://doi.org/10.1016/j.jretconser.2019.04.010)
3. Agarwal & Gowda (2021). [Materials Today: Proceedings, 37(2)](https://doi.org/10.1016/j.matpr.2020.06.557)
4. Dataset: [Kaggle - Airline Passenger Satisfaction](https://www.kaggle.com/datasets/teejmahal20/airline-passenger-satisfaction)

Best Regards
Ali Sena Danishwer
