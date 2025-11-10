Predictive Maintenance for Manufacturing
Project Overview

This project develops a machine learning model to predict equipment failures in manufacturing systems using industrial sensor data.
The main objective is to identify potential failures before they occur, minimizing downtime and optimizing maintenance operations.

Objectives

Build a predictive model to detect machine failures.

Clean and preprocess industrial sensor data.

Evaluate the model using accuracy and ROC AUC metrics.

Generate insights for preventive maintenance decisions.
Dataset Summary

The dataset contains 5,000 records of machine sensor readings.
Each record includes the following parameters:
| Column                  | Description                                 |
| ----------------------- | ------------------------------------------- |
| UDI                     | Unique record identifier                    |
| Product ID              | Product code of the machine                 |
| Type                    | Machine type                                |
| Air temperature [K]     | External air temperature                    |
| Process temperature [K] | Internal operating temperature              |
| Rotational speed [rpm]  | Rotational speed of the machine             |
| Torque [Nm]             | Torque applied to the machine               |
| Tool wear [min]         | Duration of tool wear                       |
| Machine failure         | Indicates machine failure (1 = yes, 0 = no) |
| TWF, HDF, PWF, OSF, RNF | Subcategories of specific failure types     |

Data Preprocessing

Handled missing values using median imputation.
Removed duplicate and noisy records.
Encoded categorical data into numerical format.
Normalized selected features for better model performance.
Focused on parameters like temperature, rotational speed, torque, and tool wear.

Modeling

Algorithm used: Random Forest Classifier
Data split: 80% training and 20% testing
Cross-validation: 5-fold
Evaluation metric: ROC AUC (target > 0.85)
Determined key features contributing to failure prediction.

Results

Achieved an AUC score of approximately 0.90.
Most influential features identified:
1.Tool wear
2.Rotational speed
3.Air temperature
4.Process temperature
5.Torque

Insights and Recommendations

Machines with high tool wear and torque values are more likely to fail.
Regular maintenance should be scheduled based on predicted failure risks.
Monitoring temperature and speed trends can help prevent unexpected breakdowns.


Deliverables
Cleaned dataset with predictions
Python scripts for preprocessing, modeling, and evaluation
Visualizations of performance metrics
Final report and summary presentation

