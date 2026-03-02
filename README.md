# ❤️ Heart Disease Prediction using Machine Learning

This project builds a **machine learning model to predict heart disease** using clinical patient data.
The goal is to determine whether a person has heart disease based on medical attributes such as age, cholesterol, chest pain type, heart rate, and more.

---

## 📌 Problem Statement

> **Given clinical parameters about a patient, can we predict whether or not they have heart disease?**

This is a **binary classification problem** where:

* `1` → Patient has heart disease
* `0` → Patient does not have heart disease

---

## 📊 Dataset

* Original dataset: Cleveland Heart Disease dataset (UCI Machine Learning Repository)
* Alternate source: Kaggle Heart Disease Classification Dataset
* Total records: **303**
* Total features: **13**
* Target variable: **`target`**

No missing values are present in the dataset.

---

## 🧾 Feature Overview

Some important features include:

* `age` – Age in years
* `sex` – 1 = male, 0 = female
* `cp` – Chest pain type
* `trestbps` – Resting blood pressure
* `chol` – Serum cholesterol
* `thalach` – Maximum heart rate achieved
* `exang` – Exercise induced angina
* `oldpeak` – ST depression induced by exercise
* `ca` – Number of major vessels colored by fluoroscopy
* `thal` – Thalium stress test result
* `target` – Heart disease presence (label)

---

## 🔍 Exploratory Data Analysis (EDA)

* Class distribution analysis
* Feature distributions and correlations
* Relationship between age, heart rate, chest pain, and heart disease
* Correlation heatmap for feature importance insights

---

## 🧠 Models Used

Three machine learning models were trained and evaluated:

* **Logistic Regression**
* **K-Nearest Neighbors (KNN)**
* **Random Forest Classifier**

### Baseline Accuracy Results:

| Model               | Accuracy |
| ------------------- | -------- |
| Logistic Regression | ~88.5%   |
| Random Forest       | ~83.6%   |
| KNN                 | ~68.8%   |

---

## ⚙️ Hyperparameter Tuning

* **KNN**: Tuned `n_neighbors`
* **Logistic Regression**: Tuned using `RandomizedSearchCV` and `GridSearchCV`
* **Random Forest**: Tuned using `RandomizedSearchCV`

The **best performing model** was **Logistic Regression** after tuning.

---

## 📈 Model Evaluation

Evaluation metrics used:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix
* ROC Curve & AUC
* Cross-validated metrics (5-fold CV)

### Final Model Performance (Logistic Regression)

* **Accuracy:** ~89%
* **Precision:** ~88%
* **Recall:** ~91%
* **F1-score:** ~89%

---

## 🔁 Cross-Validation Results (Mean)

| Metric    | Score  |
| --------- | ------ |
| Accuracy  | ~84.5% |
| Precision | ~82.1% |
| Recall    | ~92.1% |
| F1 Score  | ~86.7% |

---

## ⭐ Feature Importance

Using Logistic Regression coefficients, the most influential features include:

* Chest pain type (`cp`)
* Maximum heart rate (`thalach`)
* Exercise induced angina (`exang`)
* ST depression (`oldpeak`)
* Number of vessels (`ca`)
* Thalium stress test (`thal`)

---

## 🚀 Future Improvements

* Collect more data for better generalization
* Try advanced models like **XGBoost / CatBoost**
* Perform feature scaling and pipeline optimization
* Export the trained model for deployment (API / web app)

---

## 🛠️ Tech Stack

* Python
* NumPy, Pandas
* Matplotlib, Seaborn
* Scikit-Learn
* Jupyter Notebook

---

## 📂 Project Structure

```
├── data/heart-disease.csv
├── heart_disease_prediction.ipynb
├── README.md
```

---

## 📌 Conclusion

This project demonstrates a **complete machine learning workflow** — from data exploration and modeling to evaluation and interpretation — for predicting heart disease using real clinical data.
