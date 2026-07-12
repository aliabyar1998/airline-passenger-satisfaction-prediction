# Airline Passenger Satisfaction Prediction ✈️

A Machine Learning classification project to predict airline passenger satisfaction based on passenger demographics, flight details, travel information, and service experience.

The objective of this project is to build machine learning models that classify passengers into:

* **Satisfied**
* **Neutral or Dissatisfied**

and identify the main factors that influence airline customer satisfaction.

---

# 📌 Project Overview

Customer satisfaction is one of the most important factors in the airline industry. Understanding passenger behavior and service experience can help airlines improve their customer experience and make data-driven decisions.

This project covers the complete machine learning workflow:

* Data exploration
* Data cleaning
* Feature engineering
* Data preprocessing
* Feature scaling
* Model training
* Model evaluation
* Feature importance analysis
* Business insight visualization

---

# 📂 Dataset

The dataset used in this project is the **Airline Passenger Satisfaction Dataset** from Kaggle.

Dataset source:

🔗 https://www.kaggle.com/datasets/teejmahal20/airline-passenger-satisfaction

After downloading the dataset, place the files in:

```text
data/raw/
```

Required files:

```text
train.csv
test.csv
```

---

# 🗂️ Project Structure

```text
airline-passenger-satisfaction-prediction/

│
├── README.md
│
├── requirements.txt
│
├── notebooks/
│   └── airline-passenger-satisfaction.ipynb
│
├── images/
│   ├── confusion_matrix.png
│   └── satisfaction.png
│
└── data/
    └── raw/
        ├── train.csv
        └── test.csv
```

---

# 🔄 Machine Learning Workflow

## 1. Data Loading

The dataset was loaded using Pandas.

Initial exploration included:

* Dataset dimensions
* Feature names
* Data types
* Target distribution

---

# 🧹 Data Preprocessing

## Handling Missing Values

Rows containing missing values were removed.

## Removing Unnecessary Features

The following columns were removed:

* `Unnamed: 0`
* `id`

because they do not provide useful predictive information.

---

# 🔢 Feature Engineering

Categorical variables were transformed into numerical values.

## Gender

```text
Male → 1
Female → 0
```

## Customer Type

```text
Loyal Customer → 1
Disloyal Customer → 0
```

## Type of Travel

```text
Business Travel → 1
Personal Travel → 0
```

## Target Encoding

```text
Satisfied → 1
Neutral/Dissatisfied → 0
```

One-hot encoding was applied to:

* Class

---

# 📊 Feature Scaling

Numerical features were standardized using:

`StandardScaler`

Scaled features:

* Age
* Flight Distance
* Departure Delay in Minutes
* Arrival Delay in Minutes

---

# 🤖 Machine Learning Models

Three classification models were trained:

## Logistic Regression

A baseline linear classification algorithm.

---

## Random Forest Classifier

An ensemble model based on multiple decision trees.

Parameters:

```python
n_estimators = 100
random_state = 42
```

---

## Gradient Boosting Classifier

A boosting algorithm that combines multiple weak learners to improve prediction accuracy.

Parameters:

```python
n_estimators = 100
random_state = 42
```

---

# 📈 Model Evaluation

Models were evaluated using:

* Accuracy Score
* Precision
* Recall
* F1-score
* Classification Report

The Random Forest model was selected for additional analysis because of its strong performance.

---

# 🌲 Feature Importance Analysis

Feature importance was extracted from the Random Forest model to identify the most influential features affecting passenger satisfaction.

Features with importance values:

```text
>= 0.01
```

were selected for a reduced-feature model.

The performance of:

* Full feature model
* Selected feature model

was compared.

---

# 📊 Results

## Confusion Matrix

The confusion matrix shows the performance of the final Random Forest classifier.

![Confusion Matrix](images/confusion_matrix.png)

---

# 💡 Business Insights

Additional analysis was performed to understand the relationship between passenger satisfaction and different factors.

The following insights were analyzed:

* Satisfaction rate by travel type
* Satisfaction rate by customer type
* Satisfaction rate by travel class
* Online boarding score relationship with satisfaction

![Passenger Satisfaction Analysis](images/satisfaction.png)

---

# 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Jupyter Notebook

---

# ▶️ How to Run

Clone the repository:

```bash
git clone https://github.com/your-username/airline-passenger-satisfaction-prediction.git
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Download the dataset from Kaggle and place:

```text
train.csv
test.csv
```

inside:

```text
data/raw/
```

Open the notebook:

```text
notebooks/airline-passenger-satisfaction.ipynb
```

Run all cells to reproduce the results.

---

# 🚀 Future Improvements

Possible improvements:

* Hyperparameter tuning using GridSearchCV
* Cross-validation
* Model deployment using Streamlit
* Saving trained models
* Creating an automated prediction pipeline

---

# 👤 Author

Your Name

Machine Learning | Data Science Project
