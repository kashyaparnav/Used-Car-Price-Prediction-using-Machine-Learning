# Used-Car-Price-Prediction-using-Machine-Learning
A complete Data Science project that predicts the selling price of used cars based on various features such as car name, company, manufacturing year, fuel type, and kilometers driven.
Project Overview

The used car market is highly dynamic, making it difficult for buyers and sellers to determine a fair price. This project leverages Machine Learning techniques to predict the price of used cars using historical data from Quikr listings.

The project includes:

Data Cleaning & Preprocessing
Exploratory Data Analysis (EDA)
Feature Engineering
Machine Learning Model Building
Model Evaluation
Price Prediction System

Problem Statement

Predict the selling price of a used car based on:

Car Name
Company
Manufacturing Year
Fuel Type
Kilometers Driven

This helps buyers and sellers estimate a fair market value.
Dataset Information

The dataset contains information about used cars listed on Quikr.

Features
Feature	Description
name	Car Model Name
company	Car Manufacturer
year	Manufacturing Year
Price	Selling Price (Target Variable)
kms_driven	Kilometers Driven
fuel_type	Fuel Type

Technologies Used
Python
Pandas
NumPy
Matplotlib
Seaborn
Scikit-Learn
Jupyter Notebook

Exploratory Data Analysis

The following analyses were performed:

Price Distribution
Understanding the spread of car prices.

Company-wise Analysis
Identifying manufacturers with the most listings.

Fuel Type Analysis
Distribution of Petrol, Diesel, LPG, and CNG vehicles.

Price vs Year
Analyzing how vehicle age affects price.

Price vs Kilometers Driven
Studying depreciation based on usage.

Correlation Analysis
Understanding relationships between numerical features.

Data Preprocessing

The dataset required extensive cleaning:

Year Cleaning
Removed invalid year values
Converted year to integer format
Price Cleaning
Removed rows containing "Ask For Price"
Converted price to numeric values
Kilometers Driven Cleaning
Removed text symbols
Converted to integer values
Missing Value Handling
Filled missing fuel types with mode values
Feature Engineering
Simplified car names
Removed irrelevant information
Reset indices

Machine Learning Model
Algorithm Used

Linear Regression

Linear Regression was selected because:

Easy to interpret
Works well for regression problems
Fast training time
Good baseline model
 Model Evaluation Metrics

The model was evaluated using:

R² Score
Mean Absolute Error (MAE)
Root Mean Squared Error (RMSE)
from sklearn.metrics import r2_score
from sklearn.metrics import mean_absolute_error
from sklearn.metrics import mean_squared_error
Project Structure
Used-Car-Price-Prediction/
│
├── quikr_car.csv
├── Used_Car_Price_Prediction.ipynb
├── car_price_model.pkl
├── README.md
│
├── images/
│   ├── price_distribution.png
│   ├── fuel_type_distribution.png
│   ├── actual_vs_predicted.png
│
└── requirements.txt
 Installation
Clone Repository
git clone https://github.com/kashyaparnav/Used-Car-Price-Prediction-using-Machine-Learning/edit/main/README.md
Navigate to Project
cd Used-Car-Price-Prediction
Install Dependencies
pip install -r requirements.txt
 Running the Project

Open Jupyter Notebook:

jupyter notebook

Run:

Used_Car_Price_Prediction.ipynb
 Example Prediction
sample = pd.DataFrame({
    'name':['Maruti Suzuki Alto'],
    'company':['Maruti'],
    'year':[2018],
    'kms_driven':[30000],
    'fuel_type':['Petrol']
})

prediction = model.predict(sample)
Output
Predicted Price: ₹3,50,000

(Example output may vary depending on training data.)

Future Improvements
Random Forest Regressor
XGBoost Regressor
Hyperparameter Tuning
Model Deployment using Flask
Streamlit Web Application
Real-time Car Price Prediction API

 Sample Visualizations
Price Distribution

Shows how car prices are distributed across the dataset.

Actual vs Predicted Prices

Visual comparison of model performance.

Fuel Type Analysis

Distribution of different fuel categories.

Learning Outcomes

Through this project, I gained practical experience in:

Data Cleaning
Data Wrangling
Exploratory Data Analysis
Feature Engineering
Machine Learning Pipelines
Regression Modeling
Model Evaluation
Model Serialization
