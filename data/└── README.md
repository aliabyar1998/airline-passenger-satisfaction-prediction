# Dataset

This project uses the **Airline Passenger Satisfaction** dataset from Kaggle.

## Dataset Source

Kaggle Link:

https://www.kaggle.com/datasets/teejmahal20/airline-passenger-satisfaction

The dataset contains airline passenger survey data used to analyze and predict customer satisfaction.

---

## Dataset Files

After downloading the dataset from Kaggle, place the files inside this folder:

```text
data/
│
└── raw/
    ├── train.csv
    └── test.csv
```

---

## Dataset Features

The dataset includes information about:

* Passenger demographics
* Customer type
* Type of travel
* Travel class
* Flight distance
* Service ratings
* Departure and arrival delays
* Passenger satisfaction label

---

## Target Variable

The prediction target is:

```text
satisfaction
```

Values:

| Value                   | Meaning                    |
| ----------------------- | -------------------------- |
| satisfied               | Passenger is satisfied     |
| neutral or dissatisfied | Passenger is not satisfied |

---

## Usage

The dataset is loaded and processed in:

```text
notebooks/airline-passenger-satisfaction.ipynb
```

The notebook performs:

* Data cleaning
* Feature encoding
* Feature scaling
* Model training
* Model evaluation
* Feature importance analysis
