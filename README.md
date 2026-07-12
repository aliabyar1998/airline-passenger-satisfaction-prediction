# Airline Passenger Satisfaction Prediction ✈️

A Machine Learning classification project to predict airline passenger satisfaction based on passenger demographics, flight information, travel details, and service experience.

The objective of this project is to develop machine learning models that classify passengers into:

* **Satisfied**
* **Neutral or Dissatisfied**

and identify the key factors that influence airline customer satisfaction.

---

## 📌 Project Overview

Customer satisfaction is one of the most important factors in the airline industry. By analyzing passenger data and applying machine learning techniques, airlines can better understand customer behavior and improve service quality.

This project covers the complete machine learning workflow:

* Exploratory Data Analysis (EDA)
* Data Cleaning
* Feature Engineering
* Data Preprocessing
* Feature Scaling
* Machine Learning Model Training
* Model Evaluation
* Feature Importance Analysis
* Business Insight Visualization

---

## 📂 Dataset

The dataset used in this project is the **Airline Passenger Satisfaction Dataset** from Kaggle.

Dataset Link: https://www.kaggle.com/datasets/teejmahal20/airline-passenger-satisfaction

| Property | Value |
|---|---|
| Train Records | 103,594 |
| Test Records | 25,893 |
| Features (original) | 25 |
| Features (after preprocessing) | 23 |
| Missing Values | 310 rows removed |
| Class Balance | 57% Dissatisfied — 43% Satisfied |

---

## 🎯 Target Variable

The prediction target is:

```text
satisfaction
```

| Original Value | Encoded Value |
|---|---|
| satisfied | 1 |
| neutral or dissatisfied | 0 |

---

## 🔄 Project Workflow

```
Train CSV + Test CSV → Remove Nulls → Label Encoding → One-Hot Encoding → Feature Scaling → Model Training → Evaluation
```

---

## 🧹 Data Preprocessing

### Missing Values
310 rows with missing values in `Arrival Delay in Minutes` were removed — only 0.3% of total data.

### Removing Unnecessary Columns
The following columns were removed:

* `Unnamed: 0`
* `id`

because they do not provide useful predictive information.

---

## 🔢 Feature Engineering

### Label Encoding

| Feature | Mapping |
|---|---|
| Gender | Male=1, Female=0 |
| Customer Type | Loyal Customer=1, Disloyal Customer=0 |
| Type of Travel | Business Travel=1, Personal Travel=0 |
| satisfaction | Satisfied=1, Neutral or Dissatisfied=0 |

### One-Hot Encoding

Applied to `Class` (3 categories) with `drop_first=True`:

| Class | Class_Eco | Class_Eco Plus |
|---|---|---|
| Business | 0 | 0 |
| Eco | 1 | 0 |
| Eco Plus | 0 | 1 |

---

## 📊 Feature Scaling

Numerical features were standardized using `StandardScaler`:

* Age
* Flight Distance
* Departure Delay in Minutes
* Arrival Delay in Minutes

---

## 🤖 Machine Learning Models

Three classification algorithms were trained and compared:

### Model Comparison Results

| Model | Accuracy | Precision | Recall | F1-Score |
|---|---|---|---|---|
| Logistic Regression | 0.87 | 0.87 | 0.87 | 0.87 |
| Gradient Boosting | 0.94 | 0.94 | 0.94 | 0.94 |
| **Random Forest** | **0.96** | **0.96** | **0.96** | **0.96** |

The Random Forest model was selected as the best performer.

---

## 🌲 Feature Importance Analysis

Feature importance was extracted from the Random Forest model.

### Top 10 Features

| Rank | Feature | Importance Score |
|---|---|---|
| 1 | Online boarding | 0.181 |
| 2 | Inflight wifi service | 0.143 |
| 3 | Type of Travel | 0.102 |
| 4 | Class_Eco | 0.076 |
| 5 | Inflight entertainment | 0.066 |
| 6 | Flight Distance | 0.038 |
| 7 | Ease of Online booking | 0.038 |
| 8 | Seat comfort | 0.038 |
| 9 | Leg room service | 0.037 |
| 10 | Customer Type | 0.035 |

Features with importance below 0.01 were removed: `Gender`, `Class_Eco Plus`

### Full vs Selected Features

| Model | All 23 Features | 21 Selected Features |
|---|---|---|
| Random Forest | 0.96 | 0.96 |

Removing low-importance features had no negative impact on accuracy.

---

## 📊 Results

### Confusion Matrix

![Confusion Matrix](images/confusion_matrix.png)

| | Predicted Dissatisfied | Predicted Satisfied |
|---|---|---|
| Actual Dissatisfied (14,528) | 14,236 ✓ | 292 ✗ |
| Actual Satisfied (11,365) | 670 ✗ | 10,695 ✓ |

* 98% of dissatisfied passengers correctly identified
* 94% of satisfied passengers correctly identified
* Only 6% miss rate on dissatisfied passengers

---

## 💡 Passenger Satisfaction Insights

![Passenger Satisfaction Analysis](images/satisfaction.png)

### Key Findings

| Factor | Finding | Recommendation |
|---|---|---|
| Type of Travel | Business: 58% satisfied. Personal: only 10% | Improve personal travel experience |
| Customer Type | Loyal: 48% satisfied. Disloyal: only 23% | Implement loyalty rewards program |
| Class | Business: 69%. Eco Plus: 25%. Eco: 19% | Upgrade Eco class amenities |
| Online Boarding | Top feature — satisfied passengers rate it higher | Invest in online boarding UX as top priority |
| Inflight Wifi | Second most important feature | Upgrade wifi quality and reliability |

### High-Risk Passenger Profile

A passenger is at high risk of dissatisfaction if they match 3 or more:

* Traveling for personal reasons
* First-time or disloyal customer
* Flying in Eco class
* Online boarding score below 3 out of 5
* Inflight wifi rating below 3 out of 5

---

## 📁 Project Structure

```text
airline-passenger-satisfaction-prediction/
│
├── README.md
├── requirements.txt
│
├── notebooks/
│   └── airline-passenger-satisfaction.ipynb
│
└── images/
    ├── confusion_matrix.png
    └── satisfaction.png
```

---

## 🛠️ Technologies Used

* Python 3.10
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Jupyter Notebook

---

## ▶️ How to Run

Clone the repository:

```bash
git clone https://github.com/your-username/airline-passenger-satisfaction-prediction.git
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Download the dataset from Kaggle and run the notebook:

```text
notebooks/airline-passenger-satisfaction.ipynb
```

Run all cells to reproduce the results.

---

## 🚀 Future Improvements

* Hyperparameter tuning using GridSearchCV
* Cross-validation
* Saving trained models
* Building a prediction API
* Deploying the model using Streamlit

---

## 👤 Author

Ali Abyar

Machine Learning | Data Science Project
