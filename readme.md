# Credit Card Churn Prediction using Artificial Neural Networks

This project demonstrates a machine learning pipeline to predict customer churn using a fully connected neural network built with TensorFlow/Keras. The dataset used is the popular Churn_Modelling.csv, and it involves various stages such as preprocessing, encoding, normalization, model building, training, and evaluation.

📁 Dataset
File: Churn_Modelling.csv
This dataset includes customer-level information for a bank’s clients, including demographics, account information, and whether the customer has exited (churned).

🛠️ Features Used
CreditScore
Geography (One-Hot Encoded)
Gender (Label Encoded)
Age
Tenure
Balance
NumOfProducts
HasCrCard
IsActiveMember
EstimatedSalary
Target variable: Exited (0 = Stayed, 1 = Churned)

📊 Preprocessing Steps
Drop Irrelevant Columns: RowNumber, CustomerId, Surname
Label Encoding: Gender
One-Hot Encoding: Geography
Feature Scaling: Standardization of numerical features using StandardScaler

🧠 Model Architecture
A simple feedforward neural network built with Keras:
Input Layer: 12 features
Hidden Layer 1: Dense(8, activation='relu')
Hidden Layer 2: Dense(8, activation='relu')
Output Layer: Dense(1, activation='sigmoid')

Optimizer: Adam
Loss Function: Binary Crossentropy
Metrics: Accuracy
Callback: EarlyStopping with patience=5 to prevent overfitting

🔍 Model Evaluation
Training and validation accuracy and loss are plotted for visual inspection.
Final predictions are thresholded at 0.5 to convert probabilities into binary class predictions (0 or 1).
📈 Visualizations
The training process includes plots for:
Training Loss
Validation Loss
Training Accuracy
Validation Accuracy
