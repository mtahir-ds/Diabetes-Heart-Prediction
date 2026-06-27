# 🩺 Health Risk Prediction Dashboard (Diabetes & Heart Disease)

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?logo=streamlit&logoColor=white)](https://streamlit.io)
[![Scikit-Learn](https://img.shields.io/badge/scikit--learn-F7931E?logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)
[![XGBoost](https://img.shields.io/badge/XGBoost-15C213?logo=xgboost&logoColor=white)](https://xgboost.ai/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

An end-to-end Machine Learning web application built with **Streamlit** designed to assess patient health risks. The application leverages trained classification models to predict the likelihood of **Heart Disease** and **Diabetes** based on clinical diagnostic metrics and patient health history.

---

## ✨ Key Features

- **🚀 Dual Risk Assessment UI**: Easily toggle between **Heart Disease** and **Diabetes** prediction modules using intuitive navigation tabs.
- **📈 Real-time KPI Tracker**: Monitors total predictions made during the session, tracking heart risk and diabetes queries dynamically.
- **❤️ Heart Disease Predictor**: Evaluates 13 key clinical parameters including Resting Blood Pressure, Cholesterol, Fasting Blood Sugar, Resting ECG, Max Heart Rate Achieved, ST Depression, and Fluoroscopy major vessels.
- **🩸 Diabetes Predictor**: Analyzes 8 critical health indicators including HbA1c Level, Blood Glucose Level, BMI, Hypertension history, Heart Disease history, and Smoking habits.
- **📊 Interactive Visualizations**: Generates dynamic prediction trends, bar charts, and pie charts illustrating risk distributions.
- **📥 Data Logging & Export**: Automatically logs all session predictions with timestamps and allows exporting prediction history directly to a **CSV file**.

---

## 📁 Project Structure

```text
├── app.py                         # Main Streamlit web application dashboard
├── requirements.txt               # Python package dependencies
├── heart_prediction_model.pkl     # Trained Machine Learning model for Heart Disease prediction
├── diabetes_prediction_model.pkl  # Trained Machine Learning model for Diabetes prediction
├── data/
│   ├── HeartDisease_dataset.csv   # Dataset used for Heart Disease analysis and training
│   └── diabetes_dataset.csv       # Dataset used for Diabetes analysis and training
└── notebooks/
    ├── Heart_disease_notebook.ipynb # Exploratory Data Analysis, preprocessing & model training
    └── diabetes_notebook.ipynb      # EDA, SHAP explainability & classification modeling
```

---

## 🧠 Machine Learning Workflow

The models powering this dashboard were developed through extensive research and experimentation documented in the `notebooks/` directory:

1. **Exploratory Data Analysis (EDA)**: Comprehensive data distribution check, correlation matrices, and visual feature relationships using `Seaborn` and `Matplotlib`.
2. **Data Preprocessing & Balancing**: Handled missing values, encoded categorical variables, applied feature scaling (`StandardScaler`), and addressed class imbalance using sampling techniques (`RandomUnderSampler`).
3. **Model Training & Evaluation**: Benchmarked multiple classification algorithms including **Random Forest**, **XGBoost**, **Gradient Boosting**, **Logistic Regression**, and **K-Nearest Neighbors (KNN)**. Evaluated performance using Accuracy, ROC-AUC curves, and Confusion Matrices.
4. **Model Explainability**: Leveraged **SHAP (SHapley Additive exPlanations)** and feature importance plots to interpret the impact of individual clinical features on predictions.

---

## 🛠️ Installation & Setup

### 1. Clone the Repository
```bash
git clone https://github.com/MuhammadTahir-1-9-4/Diabetes-Heart-Prediction.git
cd Diabetes-Heart-Prediction
```

### 2. Create a Virtual Environment (Recommended)
```bash
# On Windows
python -m venv venv
venv\Scripts\activate

# On macOS/Linux
python3 -m venv venv
source venv/bin/activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Run the Streamlit Application
```bash
streamlit run app.py
```

After running the command, your web browser will automatically open the dashboard at `http://localhost:8501`.

---

## 💡 How to Use the Dashboard

1. **Select a Test**: Choose either the **❤️ Heart Disease Prediction** or **🩸 Diabetes Prediction** tab.
2. **Input Patient Metrics**: Adjust the sliders and dropdown menus to enter clinical data (e.g., Age, BMI, Glucose Level, Cholesterol).
3. **Predict**: Click the **🔍 Predict Risk** button to get instant model evaluation results (**High Risk / Low Risk** or **Likely Diabetic / Unlikely Diabetic**).
4. **Review & Export**: Scroll down to the **📄 Prediction Log** section to view previous tests, inspect graphical trends, or download the session data as `predictions.csv`.

---

## ⚠️ Disclaimer

This application is intended for **educational and research purposes only**. It should not be used as a substitute for professional medical advice, diagnosis, or treatment. Always seek the advice of a qualified healthcare provider with any questions regarding a medical condition.

---

## 👤 Author

**Muhammad Tahir**
- GitHub: [@MuhammadTahir-1-9-4](https://github.com/MuhammadTahir-1-9-4)
