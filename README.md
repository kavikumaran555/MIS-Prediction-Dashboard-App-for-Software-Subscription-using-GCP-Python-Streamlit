Monthly Recurring Revenue (MRR) Prediction Dashboard

This project builds an end-to-end data pipeline and dashboard to predict Monthly Recurring Revenue (MRR) using historical MIS data.

It includes:

Data storage using Google BigQuery
Data cleaning using SQL
Machine Learning model using Python
Interactive dashboard using Streamlit
Dataset Description

The dataset contains software business metrics:

Client_ID – Unique identifier for each client
Date – Date of record
Users_Count – Number of users
Contract_Length_Months – Subscription duration
Feature_Usage_Score – Product usage intensity
Discount_Percent – Discount applied
One_Time_Revenue – One-time revenue
Monthly_Recurring_Revenue – Target variable (MRR)

Step 1: Data Upload & Cleaning (BigQuery)
Created a project in Google BigQuery
Uploaded CSV dataset into table: mis_demo.software_mis_table
Cleaned data using SQL:
Removed null Client_ID rows
Created final cleaned table: mis_demo.software_mis_table_final
Step 2: Data Analysis (Google Colab)
Connected BigQuery to Colab
Loaded data into Pandas DataFrame
Used:
df.head()
df.describe()
df.info()
df.isnull().sum()

This helped understand:

Data types
Missing values
Data distribution
Step 3: Data Splitting
Training Data → Rows where MRR is available
Future Data → Rows where MRR is missing

Used missing MRR rows for prediction.

Step 4: Model Training
Used Linear Regression from scikit-learn
Input features:
Users_Count
Contract_Length_Months
Feature_Usage_Score
Discount_Percent
One_Time_Revenue
Target:
Monthly_Recurring_Revenue
Step 5: Predictions
Predicted MRR for training data (to evaluate model)
Predicted MRR for future data (missing values)
Step 6: Visualization

Created two main plots:

Actual vs Predicted (Model Fit)
Shows how well model predictions match actual values
Time-based MRR Plot
Actual MRR (past)
Predicted MRR (past)
Predicted MRR (future)
Step 7: Streamlit Dashboard

Built an interactive dashboard with:

KPI Cards:

R² Score
Mean Absolute Error
Data Points

Charts:

Actual vs Predicted vs Future MRR
Model Fit Scatter Plot

Tables:

Future predictions (top 10)
Actual vs predicted (top 10)
Running the App

Run Streamlit app:

streamlit run app.py

To expose publicly using ngrok:

Start Streamlit
Connect ngrok to port 8501
Screenshots

BigQuery Table Creation


Connecting BigQuery to Colab


Data Exploration


Missing Values Detection


Dataset Split


Model Fit (Actual vs Predicted)


Time-based Predictions


Streamlit Dashboard Code


Final Dashboard Output


Tech Stack

Python
Pandas
Scikit-learn
Matplotlib
Google BigQuery
Streamlit
Ngrok

Outcome
Built an end-to-end ML pipeline
Predicted missing MRR values
Created an interactive dashboard
Generated business insights from data
Future Improvements
Use advanced models (XGBoost, Random Forest)
Add filters (date, client)
Deploy on cloud (Streamlit Cloud / GCP)
Add real-time data refresh
