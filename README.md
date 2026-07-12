# Airline Passenger Satisfaction Prediction ✈️

A Machine Learning classification project to predict airline passenger satisfaction based on passenger demographics, travel information, flight experience, and service-related features.

The main objective of this project is to build machine learning models that can classify passengers as **Satisfied** or **Neutral/Dissatisfied** and discover the key factors influencing customer satisfaction.

---

# 📌 Project Overview

Customer satisfaction is a critical factor in the airline industry. By analyzing passenger data and applying machine learning techniques, airlines can better understand customer expectations and improve their services.

This project includes:

* Data exploration
* Data cleaning
* Feature engineering
* Data preprocessing
* Feature scaling
* Machine learning model training
* Model evaluation
* Feature importance analysis
* Business insight visualization

---

# 📂 Dataset

The dataset contains airline passenger survey information, including:

* Passenger demographics
* Flight distance
* Travel type
* Customer loyalty status
* Travel class
* Service ratings
* Delay information
* Satisfaction status

## Target Variable

The target variable is:

```text
satisfaction
```

Encoding:

| Original Value          | Encoded Value |
| ----------------------- | ------------- |
| satisfied               | 1             |
| neutral or dissatisfied | 0             |

---

# 🔄 Project Workflow

## 1. Data Loading

The training and testing datasets were loaded using Pandas.

Initial exploration included:

* Dataset shape
* Column names
* Data types
* Satisfaction distribution

---

# 🧹 Data Cleaning

The following preprocessing steps were performed:

### Handling Missing Values

Rows containing missing values were removed.

### Removing Unnecessary Columns

The following columns were dropped:

* `Unnamed: 0`
* `id`

because they do not contribute useful information for prediction.

---

# 🔢 Feature Engineering

Categorical features were converted into numerical values.

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

## Satisfaction

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

The following features were scaled:

* Age
* Flight Distance
* Departure Delay in Minutes
* Arrival Delay in Minutes

---

# 🤖 Machine Learning Models

Three classification algorithms were trained and compared:

## Logistic Regression

A baseline linear classification algorithm.

---

## Random Forest Classifier

An ensemble learning algorithm based on multiple decision trees.

Parameters:

```python
n_estimators = 100
random_state = 42
```

---

## Gradient Boosting Classifier

A boosting algorithm that improves prediction performance by combining multiple weak learners.

Parameters:

```python
n_estimators = 100
random_state = 42
```

---

# 📈 Model Evaluation

The models were evaluated using:

* Accuracy Score
* Precision
* Recall
* F1-score
* Classification Report

The Random Forest model was selected for further analysis because of its strong performance.

---

# 🌲 Feature Importance Analysis

Feature importance was extracted from the Random Forest model to identify the most influential features affecting passenger satisfaction.

Features with importance values greater than:

```text
0.01
```

were selected.

The performance of:

* Model using all features
* Model using selected features

was compared.

---

# 📊 Results

## Confusion Matrix

The confusion matrix shows the classification performance of the final Random Forest model.

![Confusion Matrix](images/confusion_matrix.png)

---

# 💡 Passenger Satisfaction Insights

Business analysis was performed to understand the relationship between passenger satisfaction and different factors:

* Type of Travel
* Customer Type
* Travel Class
* Online Boarding Score

![Passenger Satisfaction Analysis](images/satisfaction.png)

---

# 📁 Project Structure

```text
airline-passenger-satisfaction-prediction/

│
├── README.md
│
├── notebooks/
│   └── airline-passenger-satisfaction.ipynb
│
├── images/
│   ├── confusion_matrix.png
│   └── satisfaction.png
│
├── data/
│   └── raw/
│       ├── train.csv
│       └── test.csv
│
└── requirements.txt
```

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

Open the notebook:

```text
notebooks/airline-passenger-satisfaction.ipynb
```

Run all cells to reproduce the results.

---

# 🚀 Future Improvements

Future improvements could include:

* Hyperparameter tuning using GridSearchCV
* Cross-validation
* Saving trained models
* Building a prediction API
* Deploying the model using Streamlit

---

# 👤 Author

Your Name

Machine Learning | Data Science Project
