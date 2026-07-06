Monthly Recurring Revenue (MRR) Prediction Dashboard

This project builds an end-to-end machine learning pipeline to predict Monthly Recurring Revenue (MRR) and visualize insights using a Streamlit dashboard.

Dataset Description
Client_ID – Unique client identifier
Date – Record date
Users_Count – Number of users
Contract_Length_Months – Subscription duration
Feature_Usage_Score – Usage intensity
Discount_Percent – Discount applied
One_Time_Revenue – One-time revenue
Monthly_Recurring_Revenue – Target variable
Step 1: Data Upload & Cleaning (BigQuery)

Step 2: Data Analysis

Step 3: Missing Values Detection

Step 4: Data Splitting
Training Data → MRR available
Future Data → MRR missing

Step 5: Model Training
Algorithm: Linear Regression
Features:
Users_Count
Contract_Length_Months
Feature_Usage_Score
Discount_Percent
One_Time_Revenue
Step 6: Model Fit (Actual vs Predicted)

Step 7: Time-Based Predictions

Step 8: Streamlit Dashboard
KPI Metrics (R² Score, MAE, Data Points)
Charts:
Actual vs Predicted vs Future
Model Fit
Tables:
Future Predictions
Past vs Predicted
Dashboard Code

Final Dashboard Output

Run the App

streamlit run app.py

Tech Stack
Python
Pandas
Scikit-learn
Matplotlib
Google BigQuery
Streamlit
Outcome
Built end-to-end ML pipeline
Predicted missing MRR values
Created interactive dashboard
Generated business insights
