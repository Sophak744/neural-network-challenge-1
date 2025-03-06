

# Student Loan Risk Prediction with Deep Learning

## Overview

This project utilizes a deep learning model to predict the risk associated with student loans. It leverages a neural network trained on a dataset of student loan information to assess the likelihood of loan repayment success.

## Dataset

The project uses a dataset named `student-loans.csv`, which contains information about student loans, including features such as credit ranking, income, and loan amount. This dataset is preprocessed and used to train and evaluate the deep learning model.

## Methodology

1. **Data Preparation:**
   - The `student-loans.csv` file is loaded into a Pandas DataFrame.
   - The dataset is split into features (X) and target (y), with "credit_ranking" as the target variable.
   - The data is divided into training and testing sets using `train_test_split`.
   - Features are scaled using `StandardScaler` to improve model performance.

2. **Model Building:**
   - A sequential neural network model is created using TensorFlow's Keras API.
   - The model consists of two hidden layers with ReLU activation and an output layer with a sigmoid activation function.
   - The model is compiled with the "binary_crossentropy" loss function, the "adam" optimizer, and the "accuracy" metric.

3. **Model Training and Evaluation:**
   - The model is trained on the training data using the `fit` method.
   - The model's performance is evaluated on the testing data using the `evaluate` method, calculating loss and accuracy.

4. **Model Saving and Prediction:**
   - The trained model is saved to a Keras file named `student_loan_model.keras`.
   - The saved model is loaded for making predictions on new data.
   - Predictions are generated using the `predict` method and saved to a DataFrame.

5. **Classification Report:**
   - A classification report is generated to assess the model's performance in detail.
   - Precision, recall, F1-score, and support are calculated for each class (credit ranking).

