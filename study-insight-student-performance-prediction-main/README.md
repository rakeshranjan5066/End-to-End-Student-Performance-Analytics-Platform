# 📊 Study-Insight: Student Performance Analytics Platform

**Project Maintainer:** Rakesh Ranjan  
**GitHub:** [Rakesh Ranjan](https://github.com/rakeshranjan5066)

- **Dataset:** [View on Kaggle](https://www.kaggle.com/datasets/spscientist/students-performance-in-exams)
- **Application:** Streamlit-based Student Performance Analytics Dashboard

## 📌 Overview

What actually drives a student's academic success? Is it strictly study time, or do hidden factors like nutrition and demographics play a bigger role?

**Study-Insight** is a machine learning platform designed to explore these questions. It analyzes socioeconomic and educational variables to predict a student's mathematics score. It also presents prediction insights and model diagnostics through an interactive Streamlit dashboard.

---

## 🚀 Interactive Analytics Dashboard

The predictive model is integrated into an interactive web application developed using Streamlit.

### 1. Prediction & Insights Panel

Enter a student's profile parameters to obtain a predicted mathematics score, estimated global percentile, estimated class rank, and insights based on the model's output.

![Prediction Dashboard](images/Screenshot%202026-08-05%20170502.png)

### 2. Interactive Model Analytics

The model diagnostics section visualizes actual versus predicted performance and prediction errors, helping users understand how the model performs.

![Model Analytics](images/Screenshot%202026-08-05%20170520.png)

---

## 🧠 Approach & Key Findings

### Phase 1: Exploratory Data Analysis (EDA)

Exploratory data analysis was performed to identify patterns, relationships, and trends within the student performance dataset.

**Key Insights:**

- **The Nutrition Factor:** Students receiving standard lunch programs scored, on average, approximately 11 points higher in mathematics than students receiving free or reduced lunch.

![EDA - Lunch Impact](images/Screenshot%202026-08-05%20170716.png)

- **Gender-Based Performance Differences:** Male students demonstrated slightly higher average mathematics scores, while female students performed better on average in reading and writing.

![EDA - Gender Distribution 1](images/Screenshot%202026-08-05%20170644.png)

![EDA - Gender Distribution 2](images/Screenshot%202026-08-05%20170659.png)

### Phase 2: Model Training & Evaluation

Multiple regression algorithms were trained and evaluated to identify the best-performing model. Model performance was compared using R² Score and Mean Absolute Error (MAE).

**Model Leaderboard:**

1. **Linear Regression: 88.11%**
2. Ridge Regression: 88.05%
3. CatBoost Regressor: 85.16%
4. Random Forest: 85.00%
5. XGBoost: 82.77%

Linear Regression achieved the highest R² score among the evaluated models in the reported experiment.

![Model Leaderboard](images/Screenshot%202026-08-05%20170756.png)

![Regression Plots](images/Screenshot%202026-08-05%20170808.png)

### Phase 3: MLOps & Experiment Tracking

The project includes an MLOps-oriented workflow using MLflow and DagsHub components for experiment tracking, parameter logging, and model evaluation. Remote tracking requires configuring your own account and tracking URI.


---

## 🛠️ Tech Stack

- **Programming Language:** Python
- **Data Analysis:** Pandas, NumPy
- **Machine Learning:** Scikit-Learn, CatBoost, XGBoost
- **Data Visualization:** Matplotlib, Seaborn, Plotly Express
- **Web Application:** Streamlit
- **Experiment Tracking:** MLflow, DagsHub
- **Model Serialization:** Joblib / Pickle
- **Deployment:** Streamlit Community Cloud

---

## 📂 Project Structure

```text
Study-Insight/
│
├── artifacts/
│   ├── model.pkl
│   └── preprocessor.pkl
│
├── images/
│   ├── Screenshot 2026-08-04 200640.png
│   ├── Screenshot 2026-08-05 170502.png
│   ├── Screenshot 2026-08-05 170520.png
│   ├── Screenshot 2026-08-05 170644.png
│   ├── Screenshot 2026-08-05 170659.png
│   ├── Screenshot 2026-08-05 170716.png
│   ├── Screenshot 2026-08-05 170756.png
│   └── Screenshot 2026-08-05 170808.png
│
├── notebook/
├── src/
├── app.py
├── requirements.txt
├── setup.py
├── run_pipeline.py
└── README.md
```

---

## 💻 Run Locally

Clone your repository (replace `Study-Insight` if you chose a different repository name):

```bash
git clone https://github.com/rakeshranjan5066/Study-Insight.git
cd Study-Insight
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run the Streamlit application:

```bash
streamlit run app.py
```

Open the local URL shown in the terminal, usually:

```text
http://localhost:8501
```

The application requires the trained model and preprocessing files to be present in the `artifacts/` directory.

---

## 📞 Let's Connect

- **GitHub:** [Rakesh Ranjan](https://github.com/rakeshranjan5066)

---

## 👨‍💻 Project Maintainer

**Rakesh Ranjan**

This repository is the individually maintained version of the Student Performance Analytics Platform, following the group's decision to allow individual project maintenance.

---

*The project uses the dataset linked above and the included model/preprocessing artifacts. Review the dataset terms and any third-party library/model licenses before redistribution.*
