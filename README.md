🏥 AI Diabetes Risk Predictor

A web-based application for predicting the risk of diabetes using a trained **Random Forest Classifier** and visualizing the results with **Plotly** and **Gradio**.

 ✨ Features

- 🧠 **AI Risk Prediction** - Uses a Random Forest model trained on the Pima Indians Diabetes Dataset to predict diabetes risk.
- 📊 **Interactive Dashboard** - Real-time visualization of results using Plotly charts within the Gradio interface.
    - **Risk Gauge** for overall prediction confidence.
    - **Bar Chart** comparing user metrics to healthy reference ranges.
    - **Radar Chart** analyzing specific risk factors (Glucose, BMI, Age, etc.).
- 👨‍💻 **Web Interface** - A modern, responsive web application built with Gradio for easy user input and output.
- 🧑‍🔬 **Feature Scaling** - Uses `StandardScaler` to properly normalize input data before prediction.
- 📝 **Personalized Advice** - Provides targeted health advice based on the high or low-risk prediction.

---

 🚀 Setup

### 1. Prerequisites

Ensure you have a Python environment set up.

### 2. Install Dependencies

The required libraries for the model, web interface, and charting are:

```bash
pip install pandas scikit-learn numpy pickle gradio plotly

3. Training and Model Files
The application requires the trained model and scaler objects. The provided script executes these steps:

Dataset Download: Downloads the diabetes dataset (diabetes.csv).

Model Training: Trains a Random Forest Classifier and a StandardScaler.

Model Saving: Saves the trained model to diabetes_model.pkl and the scaler to scaler.pkl.

Ensure these files exist in your project directory before running the app:

diabetes_model.pkl

scaler.pkl

4. Run the Application
Execute the Python script containing the Gradio interface code:

Bash

python your_script_name.py 
(Assuming the script is saved as your_script_name.py)

The application will launch on a local port, typically: http://127.0.0.1:7860 (or a similar address provided by Gradio).

🎯 Usage
Access the Interface: Open the URL provided by the demo.launch() command.

Input Data: Use the sliders to input your health metrics:

Number of Pregnancies

Glucose Level (mg/dL)

Blood Pressure (mm Hg)

Skin Thickness (mm)

Insulin Level (mu U/ml)

BMI (Body Mass Index)

Diabetes Pedigree Function

Age (years)

Analyze Risk: Click the "🔍 Analyze My Risk" button.

View Results: The interface will display:

Risk Assessment: High or Low risk status with confidence level.

Personalized Advice: Specific recommendations based on the prediction.

Detailed Charts: Interactive Plotly visualizations (Risk Gauge, Health Metrics, Risk Factors).

Try Examples: Use the provided example cases to quickly test the model's predictions.

🔧 Tech Stack
Model/Backend: Python, RandomForestClassifier (from scikit-learn)

Data Handling: Pandas, NumPy, Pickle

Feature Preprocessing: StandardScaler

Web Interface: Gradio

Visualization: Plotly (used for Gauge, Bar, and Radar charts)

🧠 Model Details
Algorithm: Random Forest Classifier

Dataset: Pima Indians Diabetes Dataset (fetch_openml('diabetes', version=1))

Training Method: Stratified 80/20 Train-Test Split with random_state=42.

Metrics: Accuracy is reported after training (e.g., 92.33% in the provided output).

Inputs (Features): Pregnancies, Glucose, Blood Pressure, Skin Thickness, Insulin, BMI, Diabetes Pedigree Function, Age.

Output (Target): class (0: tested_negative, 1: tested_positive).

🎨 Design & Styling
Gradio Theme: Uses a custom CSS to apply a modern, dark-blue, professional look.

Visuals: Plotly charts are styled with a dark background and colored indicators (Green for healthy/low risk, Red/Yellow for concerning/high risk).

User Experience: Sliders for easy input and a prominent "Analyze" button.
