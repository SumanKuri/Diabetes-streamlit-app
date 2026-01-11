Logistic Regression – Diabetes Prediction

1. Project Overview

This project implements a Logistic Regression model to predict whether a person is diabetic or non-diabetic based on medical diagnostic measurements. The project also includes data preprocessing, model evaluation, and deployment using Streamlit**.

The objective is to demonstrate an end-to-end machine learning workflow, from data exploration to model deployment.

2. Problem Statement

Diabetes is a chronic disease that affects millions of people worldwide. Early prediction can help in:

* Preventive healthcare
* Early diagnosis
* Reducing long-term complications

This project predicts diabetes using patient health attributes.

3. Dataset Description

Dataset: Diabetes Dataset (`diabetes.csv`)

### Features:

* `Pregnancies`
* `Glucose`
* `BloodPressure`
* `SkinThickness`
* `Insulin`
* `BMI`
* `DiabetesPedigreeFunction`
* `Age`

4. Target Variable:

* `Outcome`

  * `0` → Non-Diabetic
  * `1` → Diabetic



5.  Machine Learning Approach

* Algorithm Used: Logistic Regression
* Type: Binary Classification
* Reason for Choosing Logistic Regression:

  a.Simple and interpretable
  b.Works well for binary outcomes
  c.Efficient for medical datasets

---

6.  Project Workflow

 a. Data Exploration (EDA)

* Dataset inspection (`info`, `describe`)
* Distribution analysis using histograms
* Correlation analysis using heatmaps

 b. Data Preprocessing

* Handling invalid zero values using median imputation
* Feature-target separation
* Feature scaling using **StandardScaler**

 c. Model Building

* Logistic Regression model using `scikit-learn`
* Model trained on 80% of the dataset

 d. Model Evaluation

* Accuracy
* Precision
* Recall
* F1-score
* ROC-AUC score
* ROC curve visualization

 e. Model Interpretation

* Analysis of feature coefficients
* Identification of important predictors such as:

  a Glucose
  b BMI
  c Age


7.  Streamlit Deployment

a. Deployment Features:

* User-friendly web interface
* Takes real-time patient inputs
* Predicts diabetes instantly
* Model and scaler loaded using `joblib`

 Steps:

1. Train model and save using `joblib`
2. Create `app.py` using Streamlit
3. Run locally using:

   ```bash
   streamlit run app.py
   ```
b. (Optional) Deploy online using Streamlit Community Cloud

8. Project Structure

```
diabetes_streamlit_app/
│── app.py
│── diabetes_model.pkl
│── scaler.pkl
│── requirements.txt
│── README.md
```

9. Requirements

Install required dependencies using:

```bash
pip install -r requirements.txt
```

10. Libraries Used:

* pandas
* numpy
* scikit-learn
* matplotlib
* seaborn
* streamlit
* joblib

---

11. Results

* The model achieves good accuracy on test data
* ROC-AUC score indicates strong classification ability
* Glucose level is the most influential feature

12. Evaluation Metrics Explained

* **Accuracy:** Overall correctness of predictions
* **Precision:** Correct diabetic predictions
* **Recall:** Ability to detect diabetic patients (important in healthcare)
* **F1-score:** Balance between precision and recall

13. Real-World Use Case

* Early diabetes screening
* Healthcare decision support systems
* Preventive medical analysis

14. Key Learnings

* Importance of data preprocessing in healthcare data
* Handling skewed and invalid values
* Model interpretability in medical applications
* Deploying ML models using Streamlit

 ✅ Conclusion

This project successfully demonstrates how logistic regression can be used for medical classification problems, covering the full machine learning lifecycle from data analysis to deployment.





