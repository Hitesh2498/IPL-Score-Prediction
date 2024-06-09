# IPL Score Prediction

This project aims to predict the final scores of IPL (Indian Premier League) matches based on various features using different regression models. 

![image](https://github.com/Hitesh2498/IPL-Score-Prediction/assets/96277290/8f56e48b-4e9e-4e81-bace-984a9e8a7520)


## Table of Contents
- [Introduction](#introduction)
- [Data Preprocessing](#data-preprocessing)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Model Training and Evaluation](#model-training-and-evaluation)
- [Prediction Function](#prediction-function)
- [Model Deployment](#model-deployment)
- [Conclusion](#conclusion)
- [Usage](#usage)

## Introduction
This project utilizes machine learning algorithms to predict the total runs scored by a team in an IPL match. The features considered include the batting team, bowling team, current score, wickets, overs completed, and performance in the last 5 overs.

## Data Preprocessing
The preprocessing steps include:
1. Removing irrelevant columns such as `mid`, `date`, `venue`, `batsman`, `bowler`, `striker`, and `non-striker`.
2. Filtering out teams that are not consistent across all IPL seasons.
3. Filtering out overs less than 5.0 to ensure meaningful predictions.
4. Encoding categorical data using `LabelEncoder` and `OneHotEncoder`.

## Exploratory Data Analysis
- Distribution of wickets and total runs were visualized using seaborn.

## Model Training and Evaluation
The following models were trained and evaluated:
1. **Decision Tree Regressor**
2. **Linear Regression**
3. **Random Forest Regressor**
4. **Support Vector Regression (SVR)**
5. **XGBoost Regressor**
6. **K-Nearest Neighbors Regressor (KNR)**

### Evaluation Metrics:
- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)

## Prediction Function
A function `score_predict` is defined to predict the final score based on user inputs for the batting team, bowling team, and match statistics.

## Model Deployment
The trained Random Forest model is saved using `pickle` for deployment.

## Conclusion
The Random Forest Regressor provided the best results for predicting the IPL match scores. This model was saved for future use and deployment.

## Usage
1. Clone the repository:
    ```sh
    https://github.com/Hitesh2498/IPL-Score-Prediction.git
    ```
2. Install the required packages:
    ```sh
    pip install -r requirements.txt
    ```
3. Run the script to train the models and make predictions:
    ```sh
    python IPL_Score_Predictor.ipynb
    ```
4. Save the model in Model Folder
5. Run the App
   ```python
   streamlit run score_app.py
   ```
