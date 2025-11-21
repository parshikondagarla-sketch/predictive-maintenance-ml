🔧 Predictive Maintenance for Industrial Machines

Author: Kondagurla Parshi,
Tools: Python, Pandas,  Scikit-learn, XGBoost, Matplotlib, Seaborn, Google Colab
Goal: Predict whether a machine is going to fail based on sensor readings so industries can prevent breakdowns and reduce maintenance costs.

🚀 Project Overview

This project uses the AI4I 2020 Predictive Maintenance Dataset to predict machine failures using sensor data such as temperature, rotational speed, torque, and tool wear.

It is a binary classification problem:

1 → Machine Failure

0 → Normal Operation

The project demonstrates how ML can support Industry 4.0 through early fault detection.

🧩 Workflow
1. Data Cleaning

Removed special characters in column names

Verified missing values (dataset is clean)

Checked outliers using boxplots + IQR (no removal needed)

Converted categorical variables (Failure Type) into binary target

2. Feature Engineering

Standardized all sensor features using StandardScaler

Correlation analysis

Removed irrelevant columns (e.g., product ID)

3. Exploratory Data Analysis (EDA)

Heatmap to identify relationships

Boxplots to inspect outliers

Distribution of failure types

Sensor behavior comparison (RPM, Torque, Temperatures)

4. Model Building

Trained and compared:

Logistic Regression

Random Forest Classifier

XGBoost Classifier (Best)

5. Evaluation

Compared models using:

Accuracy

Precision

Recall

F1-score

Confusion Matrix

6. Insights

RPM, Torque, and Tool Wear are the strongest indicators

Failures follow clear sensor patterns

XGBoost gives best recall → catches more potential failures early

📊 Results
Model	Accuracy	Precision	Recall	F1-Score
Logistic Regression	~0.85	~0.80	~0.77	~0.78
Random Forest	~0.93	~0.92	~0.91	~0.91
XGBoost (Best)	~0.95	~0.94	~0.94	~0.94
🔹 Best Model: XGBoost Classifier
🔹 Key Drivers: RPM, Torque, Tool Wear, Temperatures
🔹 Business Impact:

Early detection prevents breakdowns

Saves maintenance cost

Supports predictive maintenance in Industry 4.0

📂 Project Structure
predictive-maintenance/
│
├── notebooks/
│   └── predictive_maintenance.ipynb
│
├── data/
│   └── ai4i2020.csv
│
├── reports/
│   ├── figures/
│   │   ├── heatmap.png
│   │   ├── boxplot_sensors.png
│   │   ├── confusion_matrix.png
│   │   └── feature_importance.png
│   └── model_report.txt
│
└── README.md
