# Project4_MachineLearning

https://stroke-risk-prediction-group10.streamlit.app/

Step 1: Install Required Libraries

Run the following commands in your terminal to install the necessary Python libraries:
Step 2: Prepare Your Dataset
	•	Download: Obtain the stroke dataset (healthcare-dataset-stroke-data.csv).
	•	Handle Missing Values: Fill missing values for bmi and avg_glucose_level with the mean.

⸻

Step 3: Data Preprocessing
	1.	Import Libraries:
    2.	Load Dataset:
    3.	Handle Missing Values:
    4.	Feature Engineering:
	•	Encode categorical features (gender, ever_married, Residence_type).
	•	One-hot encode smoking_status and work_type.
	•	Create a previous_stroke feature based on the stroke column.
	5.	Define Features and Labels:
    6.	Split Data:

⸻

Step 4: Train and Save the Model
	1.	Train a Logistic Regression Model:
    2.	Train and Save the Scaler:
    3.	Save the Model and Scaler:

⸻

Step 5: Create the app.py Script
	1.	Import Libraries:
    2.	Load Model and Scaler:with open("stroke_risk_model.pkl", "rb") as file:
    model = pickle.load(file)

with open("scaler.pkl", "rb") as file:
    scaler = pickle.load(file)
    3.	Create User Input Form:
	•	Use st.sidebar to collect user input for gender, age, heart disease, hypertension, etc.
	4.	Encode User Input:
	•	Convert categorical inputs to numerical values.
	•	Create a NumPy array of the inputs.
	5.	Predict Stroke Risk:
	•	Standardize input using the loaded scaler.
	•	Predict risk using the loaded model.
	•	Display risk score and recommendations based on the score.
	6.	Display Results:
	•	Show risk score as a percentage.
	•	Provide recommendations based on risk category.

⸻

Step 6: Create requirements.txt
	•	Create a file named requirements.txt and add:streamlit==1.14.0
scikit-learn==1.1.3
pandas==1.5.1
numpy==1.23.5
xgboost==1.7.1

⸻

Step 7: Test Locally

Run the app locally to test:streamlit run app.py

⸻

Step 8: Deploy to Streamlit Cloud
	1.	Push code to GitHub.
	2.	Link GitHub repo to Streamlit Cloud.
	3.	Configure app settings:
	•	Python version (3.10).
	•	Install dependencies from requirements.txt.
	4.	Deploy and test the app.

⸻

Step 9: Fix Common Errors
	•	Missing libraries: Ensure requirements.txt has all required packages.
	•	Pickle errors: Ensure model and scaler files are correctly saved and loaded.

⸻

Step 10: Share Your App
	•	Share the app link:https://stroke-risk-prediction-group10.streamlit.app/