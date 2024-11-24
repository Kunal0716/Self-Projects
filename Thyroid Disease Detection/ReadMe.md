# Thyroid Condition Classification using Machine Learning

This project focuses on developing a machine learning model to detect thyroid conditions (Hyperthyroidism, Hypothyroidism, or Negative) based on demographic information, medical history, and laboratory test results. Using the **Thyroid Disease Dataset** sourced from the UCI Machine Learning Repository, the project demonstrates the application of data preprocessing, feature engineering, and machine learning to address class imbalances and improve predictive accuracy.

---

## Dataset Overview

The dataset contains **9,172 patient records** with **31 attributes**, which include:
- **Demographic Information**: Age, Sex.
- **Medical History**: Medication status, surgeries, specific health conditions.
- **Laboratory Test Results**: Hormone levels (e.g., TSH, T3, TT4).

**Target Variable**:  
- The dataset's original target classes were consolidated into three categories:
  - **Negative**: No thyroid condition.
  - **Hypothyroid**.
  - **Hyperthyroid**.  
  Records unrelated to these categories were excluded for focused analysis.

---

## Project Workflow

1. **Data Preprocessing**:
   - **Handling Missing Values**:
     - Imputed missing values in the `sex` column with its mode.
     - Laboratory test results with missing values (indicating the test was not taken) were imputed with `0`.
   - **Encoding Categorical Features**:
     - Binary columns (`t`/`f`) were mapped to `1` and `0`.
     - `Sex` was encoded (`F` to `0`, `M` to `1`).
   - **Duplicate Removal**: All duplicate records were dropped.

2. **Exploratory Data Analysis (EDA)**:
   - Created visualizations to explore relationships between features and the target variable.
   - Highlighted key insights into the distribution of thyroid conditions across demographic and clinical attributes.

3. **Class Balancing**:
   - Managed the highly imbalanced dataset:
     - **Negative**: 6,767 records.
     - **Hypothyroid**: 601 records.
     - **Hyperthyroid**: 313 records.
   - Used `class_weights` in machine learning models to handle imbalance.

4. **Machine Learning**:
   - Tested multiple classifiers, including:
     - Logistic Regression, Random Forest, ExtraTree Classifier, Gradient Boosting, XGBoost, and CatBoost.
   - Applied **oversampling** and **undersampling** techniques where appropriate.
   - Evaluated models using metrics like:
     - Accuracy.
     - Confusion Matrix.
     - Average Precision Score.
     - Area Under the Precision-Recall Curve (AU-PRC).

5. **Model Selection**:
   - **CatBoost Classifier** performed best:
     - Accuracy: **98.70%**.
     - Average Precision Score: **98.79%**.
     - AU-PRC for Hyperthyroid: **0.97** (highest among tested models).
     - Used `auto_class_weights='Balanced'` and `l2_leaf_reg=1` for regularization.

6. **Model Saving**:
   - Saved the final CatBoost model as a **pickle file** for future use.

---

## Features in the Dataset

The dataset includes the following attributes:

### **Demographic Information**
- **Age**: Patient's age (integer).
- **Sex**: Patient's gender (male/female).

### **Medical History**
- Various boolean indicators for:
  - Medications (e.g., `on_thyroxine`, `on_antithyroid_meds`).
  - Conditions (e.g., `pregnant`, `sick`, `tumor`, `goitre`).
  - Procedures (e.g., `thyroid_surgery`, `I131_treatment`).

### **Laboratory Test Results**
- Measured hormone levels (e.g., TSH, T3, TT4, T4U, FTI).
- Indicators of whether the test was performed.

### **Target Variable**
- Categorized into three classes:
  - **Negative**: No thyroid condition.
  - **Hypothyroid**.
  - **Hyperthyroid**.

---

## Insights from the Project

- **Exploratory Analysis**:
  - Certain thyroid conditions show distinct trends in laboratory results (e.g., extreme TT4 values for hyperthyroidism).
  - Class overlap in specific feature ranges indicates the need for multiple tests for precise diagnosis.

- **Modeling**:
  - The **CatBoost Classifier** emerged as the best model, with robust handling of class imbalance and high precision across all classes.
  - The AU-PRC curve validated the model's effectiveness, particularly for underrepresented classes like Hyperthyroid.

---

## Future Considerations

- **Expand Dataset**: Including more data for underrepresented classes (Hyperthyroid and Hypothyroid) can improve model performance further.
- **Feature Engineering**: Explore advanced techniques like interaction terms or feature transformations to capture complex relationships.
- **Explainability**: Incorporate SHAP or LIME for better interpretability of the model's decisions.
- **Deployment**: Develop APIs or dashboards to integrate the model into clinical workflows.

---

## Next Steps

1. **Model Deployment**: Deploy the model using frameworks like Flask or FastAPI for real-time prediction.
2. **Monitoring and Maintenance**:
   - Monitor the model's performance over time.
   - Regularly update with new data to ensure accuracy.
3. **Integration**: Integrate with hospital systems or electronic medical records for seamless use.

---

## How to Use This Project

1. Clone this repository:
   ```bash
   git clone https://github.com/Kunal0716/Self-Projects.git

## Acknowledgments
This project is based on the Thyroid Disease Dataset from the UCI Machine Learning Repository.
https://archive.ics.uci.edu/dataset/102/thyroid+disease
