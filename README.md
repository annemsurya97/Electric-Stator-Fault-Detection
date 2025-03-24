# Electric-Stator-Fault-Detection
Electric Stator Fault Detection using Motor Parameters and IoT sensor data
Permanent Magnet Synchronous Machines

**Project Overview**

This project focuses on the detection of false faults in Permanent Magnet Synchronous Machines (PMSMs) to improve preventive maintenance strategies. The model leverages machine learning algorithms to classify whether a stator fault is present or not. The project utilizes Ridge Classifier and CatBoost Classifier to predict faults based on sensor data.

**Dataset**
The dataset used in this project contains various features representing the machine's operating conditions and fault states. It includes:

Sensor readings

Operational parameters

Target labels (0 for No Fault, 1 for Fault)

The dataset is preprocessed by handling missing values, encoding categorical variables, and normalizing numerical features.

Installation

**Prerequisites**

Ensure you have the following dependencies installed:

Python 3.7.6

NumPy

Pandas

Matplotlib

Seaborn

Scikit-learn

CatBoost

**To install the required dependencies, run:**

pip install numpy pandas matplotlib seaborn scikit-learn catboost

**Data Processing**

Loading the Dataset: The dataset is loaded from Dataset/dataset.csv.

**Exploratory Data Analysis (EDA):**

Data summary, correlation analysis, and null value checks are performed.

A count plot is generated to visualize the distribution of fault classes.

**Feature Selection:**

profile_id is dropped as it does not contribute to fault detection.

The target variable (target) is separated from independent features.

**Model Training**

The dataset is split into training and testing sets (70% training, 30% testing). The following classifiers are trained:

1. Ridge Classifier

The model is trained using RidgeClassifier() from scikit-learn.

If a pre-trained model exists, it is loaded from model/RidgeClassifier.npy; otherwise, it is trained and saved.

2. CatBoost Classifier

The model is trained using CatBoostClassifier().

If a pre-trained model exists, it is loaded from model/CatBoostClassifier.npy; otherwise, it is trained and saved.

**Performance Evaluation**

The models are evaluated using the following metrics:

Accuracy

Precision

Recall

F1-Score

Confusion Matrix Visualization

Performance metrics are displayed in both textual format and tabular form for better comparison.

**Prediction on Test Data**

The trained CatBoost model is used to predict faults on new test data (Dataset/test.csv). The predictions are stored in a new column named Prediction, labeling each row as either No Fault or Fault.

**Results**

Ridge Classifier and CatBoost Classifier were implemented and evaluated.

A tabular comparison of model performance is provided.

Predictions on new test data are displayed with corresponding model outputs.

**Usage**

To run the project:

python main.py

Ensure the dataset files (dataset.csv and test.csv) are correctly placed in the Dataset/ directory.

Future Improvements

Enhancing feature engineering for better classification.

Experimenting with deep learning models for improved accuracy.

Implementing real-time monitoring and anomaly detection in PMSMs.

**License**

This project is open-source and available for further enhancements and contributions.

**Contributors**
Developer: A. Surya Prakash

Contact: annem.suryaprakash97@gmail.com
