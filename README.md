# Student Performance Prediction (CGPA)

A simple Python project that predicts a student's Cumulative Grade Point Average (CGPA) based on the number of hours they study. The model is built using a dataset with 24,000 records.

## 📊 Model Results
* **Model Accuracy (\(R^2\) Score):** 81% (the model successfully captures the relationship in the data).
* **Average Error (RMSE):** 0.61 points. On average, the model's predictions deviate by only 0.61 CGPA points.
* **Error Percentage:** 9.3% relative to the average score.

During the evaluation phase, testing higher-order functions proved that increasing model complexity (polynomial features) is unnecessary because the relationship between study hours and grades is strictly linear.

## 🛠 Tech Stack
* **Language:** Python
* **Libraries:** Pandas, NumPy, Scikit-Learn (LinearRegression), Matplotlib, Seaborn, Joblib

## 🚀 How to Run and Predict

1. Install the required libraries:
```bash
pip install -r requirements.txt
```

2. Run this Python code to get a prediction:
```python
import joblib
import numpy as np

# Load the saved model artifact
model = joblib.load('LinearRegression_model.pkl')

# Input the number of study hours (e.g., 45 hours)
hours = np.array([[45.0]])

# Make prediction
prediction = model.predict(hours)
```


