# -Real-Estate-Dataset
# Real Estate Price Prediction 🏠

This repository contains a Machine Learning pipeline to predict **real estate house prices per unit area** using historical property transaction data. It implements data preprocessing, feature scaling, and evaluates multiple regression algorithms to find the most accurate model.

## 📋 Table of Contents
- [Project Overview](#-project-overview)
- [Dataset Features](#-dataset-features)
- [Technologies Used](#-technologies-used)
- [Workflow Pipeline](#-workflow-pipeline)
- [Model Evaluation & Results](#-model-evaluation--results)
- [Getting Started](#-getting-started)

---

## 🔍 Project Overview
Predicting property values accurately is essential for buyers, sellers, and investors. This project builds and compares three different regression models (**Linear Regression**, **Random Forest**, and **Gradient Boosting**) to determine the best predictor for house pricing based on location, age, and nearby amenities.

## 📊 Dataset Features
The model utilizes a dataset (`Real estate.csv`) consisting of **414 records**. The data includes the following features:

* **X1 transaction date:** The date/year of property transaction.
* **X2 house age:** The age of the house in years.
* **X3 distance to the nearest MRT station:** Proximity to public transit in meters.
* **X4 number of convenience stores:** Count of nearby convenience stores.
* **X5 latitude:** Geographic coordinate.
* **X6 longitude:** Geographic coordinate.
* **Y house price of unit area (Target Variable):** The price of the house per unit area.

---

## 🛠️ Technologies Used
* **Python** (Core Language) [1]
* **Pandas & NumPy** (Data Manipulation) [1]
* **Scikit-Learn** (Machine Learning, Preprocessing, and Metrics) [1]

---

## ⚙️ Workflow Pipeline
1. **Data Cleaning:** Removed irrelevant tracking columns (e.g., `No`).
2. **Train-Test Split:** Partitioned data into an 80% training set (331 samples) and a 20% validation set (83 samples).
3. **Feature Scaling:** Applied standard scaling (`StandardScaler`) to normalize numerical columns for stable model convergence.
4. **Model Training & Comparison:** Trained Linear Regression, Random Forest Regressor, and Gradient Boosting Regressor.
5. **Evaluation:** Evaluated model performances using Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and R² Score metrics.

---

## 🏆 Model Evaluation & Results

The models performed with the following metrics on the test dataset:

| Model | MAE | RMSE | R² Score (%) |
| :--- | :---: | :---: | :---: |
| **Linear Regression** | 5.31 | 7.31 | 68.11% |
| **Random Forest** | 3.96 | 5.71 | **80.59%** |
| **Gradient Boosting** | 3.90 | 5.84 | 79.64% |

### Key Takeaway:
The **Random Forest Regressor** achieved the highest overall performance with an **R² Score of 80.59%**, closely followed by Gradient Boosting. Both ensemble methods significantly outperformed the baseline Linear Regression model.

---

## 🚀 Getting Started

### Prerequisites
Make sure you have Python installed, then run the following command to install the required libraries:
```bash
pip install pandas numpy scikit-learn
```

### Running the Project
1. Clone this repository to your local machine.
2. Place the `Real estate.csv` dataset in the root folder.
3. Open and execute the Jupyter Notebook script to view the end-to-end execution.
