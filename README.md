# Predictive Health Analytics for Chronic Kidney Disease (CKD)

## 1. Background & Overview
Chronic Kidney Disease (CKD) is a rising health concern in the Philippines and globally, often known as a "silent killer" due to its lack of early symptoms. Late-stage diagnosis places a massive burden on healthcare systems and patient quality of life.

Aligned with **UN Sustainable Development Goal 3 (Good Health & Well-Being)**, this project aims to develop a machine learning solution to identify early risk factors for CKD. By leveraging historical patient data, this model serves as a decision-support tool for medical professionals to prioritize high-risk patients for early intervention.

### Key Objectives
* **Minimize false negatives** to ensure no potential CKD patient goes undiagnosed.
* **Identify the top biometrics (features)** that contribute most to kidney disease risk.
* **Support resource allocation** for nephrology departments in resource-constrained settings.

## 2. Data Structure & Methodology
The analysis utilizes a clinical dataset containing physiological measures and patient history. The data was preprocessed to handle missing values and normalize scale-sensitive features before training.

* **Algorithm:** Random Forest Classifier (Chosen for its high accuracy and interpretability via feature importance).
* **Target Variable:** `classification` (CKD vs. Non-CKD).
* **Key Features:** Age, Blood Pressure, Specific Gravity, Albumin, Sugar, and Red Blood Cell count.

### Model Pipeline
1. **Data Cleaning:** Handling null values in medical records.
2. **Feature Selection:** Identifying the most predictive clinical markers.
3. **Training:** Implementing a Random Forest Classifier.
4. **Evaluation:** Measuring **Recall (Sensitivity)** to prioritize minimizing missed diagnoses.

## 3. Summary
> **Headline:** Machine Learning model achieves and **98.75%** **99.5%** accuracy in predicting CKD risk, identifying Hemoglobin and Specific Gravity as primary indicators.

The Random Forest model successfully classified CKD patients with high precision. The analysis revealed that standard blood and urine tests—specifically Specific Gravity and Hemoglobin levels—are the strongest predictors of the disease. This suggests that low-cost, routine screenings can be highly effective for early detection if analyzed correctly.

### Key Metrics
* **Model Accuracy:** 99.5%
* **Recall/Sensitivity:** 100% (Critical for medical screening)
* **Top Risk Factor:** Hypertension and Albumin


## 4. Insights Deep Dive

### Insight 1: The "Silent" Indicators
* **Observation:** Feature importance analysis shows that Hypertension and Albumin levels are top predictors.
* **Medical Impact:** This validates that urine analysis and blood-pressure monitoring are non-invasive, high-impact screening tools. Deviations in these metrics often appear before physical symptoms.

### Insight 2: Anemia as a Comorbidity
* **Observation:** Hemoglobin and Red Blood Cell Count showed a strong negative correlation with CKD presence.
* **Health Story:** Patients flagged for Anemia should automatically be cross-screened for renal issues, creating a more integrated patient care pathway.

## 5. Caveats & Assumptions
* **Clinical Validation:** This model is a decision-support tool and is not intended to replace professional medical diagnosis. All predictions should be verified by a licensed nephrologist.
* **Data Scope:** The dataset represents a specific snapshot of patients. External validation on local Philippine hospital data would be required before clinical deployment to account for genetic or environmental differences.
