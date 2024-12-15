# GO2COD_ML_05
A machine learning model that predicts the weather
Clone the repository:
git clone https://github.com/Amangtt/weather-classification.git

Install dependencies: Navigate to the project directory and run:
pip install numpy pandas sklearn xgboost matplotlib

Run the script:
python weather_classification.py
Description

The script performs the following steps:

1. Data Loading and Preprocessing:

Reads the weather classification data from the location you stored it 
Creates dummy variables for categorical features (Cloud Cover, Season, Location) using pandas' get_dummies function.
Splits the data into features (x) and target labels (y).
Encodes the target labels using a scikit-learn LabelEncoder.
Splits the data further into training, validation, and testing sets using train_test_split.
Creates a separate validation set (x_train_eval, y_train_eval) from the training set for early stopping.

2. Model Training:

Defines an XGBoost classifier with parameters like n_estimators, learning_rate, early_stopping_rounds, and verbosity.
Fits the model using model.fit with the training data and the validation set for evaluation.
Prints the best iteration after early stopping.

3. Evaluation:

Evaluates the model's performance on the training and validation sets using accuracy score.
Prints the accuracy scores.
