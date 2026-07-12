# Airline Passenger Satisfaction Prediction ✈️

A Machine Learning classification project to predict airline passenger satisfaction based on passenger demographics, flight information, travel details, and service experience.

The goal of this project is to develop machine learning models that classify passengers into:

* **Satisfied**
* **Neutral or Dissatisfied**

and analyze the key factors that influence airline customer satisfaction.

---

# 📌 Project Overview

Customer satisfaction is a critical factor in the airline industry. By applying machine learning techniques to passenger data, airlines can better understand customer behavior and improve service quality.

This project includes:

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

# 📂 Dataset

The dataset used in this project is the **Airline Passenger Satisfaction Dataset** available on Kaggle.

Dataset Link:

https://www.kaggle.com/datasets/teejmahal20/airline-passenger-satisfaction

The dataset contains information about:

* Passenger demographics
* Flight details
* Travel type
* Customer loyalty status
* Seat class
* Service ratings
* Delay information
* Passenger satisfaction

---

# 🎯 Target Variable

The prediction target is:

`satisfaction`

Encoding:

| Original Value          | Encoded Value |
| ----------------------- | ------------- |
| satisfied               | 1             |
| neutral or dissatisfied | 0             |

---

# 🔄 Project Workflow

## 1. Data Loading

The dataset was loaded using Pandas.

Initial analysis included:

* Dataset dimensions
* Feature names
* Data types
* Satisfaction distribution

---

# 🧹 Data Preprocessing

## Missing Values

Rows containing missing values were removed.

## Removing Unnecessary Columns

The following columns were removed:

* `Unnamed: 0`
* `id`

---

# 🔢 Feature Engineering

Categorical features were converted into numerical values.

### Gender

```
Male → 1
Female → 0
```

### Customer Type

```
Loyal Customer → 1
Disloyal Customer → 0
```

### Type of Travel

```
Business Travel → 1
Personal Travel → 0
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

The following classification models were trained:

## Logistic Regression

Baseline linear classification model.

## Random Forest Classifier

Ensemble learning algorithm using multiple decision trees.

Parameters:

```
n_estimators = 100
random_state = 42
```

## Gradient Boosting Classifier

Boosting algorithm for improving classification performance.

Parameters:

```
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

The Random Forest model was selected for further feature analysis.

---

# 🌲 Feature Importance Analysis

Feature importance was extracted from the Random Forest model to identify the most important factors affecting passenger satisfaction.

Features with importance values greater than:

```
0.01
```

were selected for a reduced-feature model.

---

# 📊 Results

## Confusion Matrix

The confusion matrix shows the performance of the final Random Forest classifier.

![Confusion Matrix](images/confusion_matrix.png)

---

# 💡 Passenger Satisfaction Insights

Business analysis was performed to understand how different factors affect passenger satisfaction:

* Type of Travel
* Customer Type
* Travel Class
* Online Boarding Score

![Passenger Satisfaction Analysis](images/satisfaction.png)

---

# 📁 Project Structure

```
airline-passenger-satisfaction-prediction/

│
├── README.md
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
    └── README.md
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

1. Clone the repository:

```bash
git clone https://github.com/your-username/airline-passenger-satisfaction-prediction.git
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Download the dataset from Kaggle.

4. Run the Jupyter Notebook:

```
notebooks/airline-passenger-satisfaction.ipynb
```

---

# 🚀 Future Improvements

* Hyperparameter tuning using GridSearchCV
* Cross-validation
* Model deployment using Streamlit
* Saving trained models
* Building an automated prediction pipeline

---

# 👤 Author

Your Name

Machine Learning | Data Science Project
