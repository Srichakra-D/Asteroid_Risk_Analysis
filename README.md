# NSSC Data Analytics Event - Cosmic Collision

## Project Overview
This repository contains the analysis and model building process undertaken for the **NSSC Data Analytics Event**. The project, titled **Cosmic Collision: Analyzing Asteroid Risks with Data**, focuses on understanding asteroid data, engineering features, and developing robust classifiers to predict the hazard level of asteroids. The event was hosted at **IIT Kharagpur**.

### Team Information
- **Team Name:** Finishers
- **Team ID:** T-0812526
- **Team Members:**
  - Nitin Gandem
  - Srinath Duvvuri
  - Srichakra Devarakonda
  - Gandem VijayKumar

---

## Project Objectives
1. **Data Understanding:** Perform exploratory data analysis (EDA) to inspect, visualize, and preprocess the dataset.
2. **Feature Engineering:** Create new features to enhance prediction accuracy.
3. **Classification:** Develop a robust model to classify asteroids as hazardous or not hazardous.
4. **Anomaly Detection:** Identify anomalies in the dataset using library-based and custom methods.

---

## Methodologies

### 1. Exploratory Data Analysis (EDA)
- **Data Inspection:**
  - Identified numerical and categorical features.
  - Calculated statistics such as range, mean, median, and standard deviation.
  - Handled missing values using imputation methods:
    - **Numerical Features:** Filled missing values with the median.
    - **Categorical Features:** Filled missing values with the mode.
- **Data Normalization:** Applied Min-Max scaling to numerical features.
- **Outlier Detection:** Identified and removed outliers using the Interquartile Range (IQR) method.
- **Correlation Analysis:** Analyzed feature relationships using heatmaps.

### 2. Feature Engineering
- Combined year, month, and day features into a single "Day of the Year" feature.
- Calculated:
  - Miss Distance Ratio.
  - Time Until Approach.
  - Orbital properties such as eccentricity, perihelion/aphelion velocities, and more using Kepler’s laws.
- Added innovative features like gravitational influence and perihelion-to-aphelion ratios.

### 3. Classification
- Built a **Random Forest Classifier** for hazardous classification:
  - Addressed class imbalance using **SMOTE**.
  - Tuned hyperparameters with **RandomizedSearchCV**.
  - Evaluated the model with metrics such as accuracy, confusion matrix, and classification report.
- Implemented **K-Fold Cross Validation** (K=2 to 10) to assess model performance.

### 4. Anomaly Detection
- **Library-based Method:** Used Isolation Forest to detect anomalies.
- **Custom Method:** Implemented Z-score-based anomaly detection.
- Compared the two methods and visualized results with a confusion matrix.

---

## Key Results
- **Classification Accuracy:** Achieved a high accuracy of **90%** with the Random Forest Classifier.
- **ROC Curve Insights:** Demonstrated excellent model sensitivity and specificity.
- **Feature Importance:** Identified key features using SHAP values, permutation importance, and partial dependence plots.
- **Anomalies:** Flagged and analyzed anomalies using both inbuilt and custom methods.

---


### Prerequisites
- Python 3.1
- Required libraries:
  - pandas
  - numpy
  - scikit-learn
  - matplotlib
  - seaborn
  - SHAP