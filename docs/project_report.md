# Healthcare Comorbidity & Patient Outcome Analysis

## 1. Introduction

Healthcare systems generate large amounts of patient data through hospital encounters, treatments, and diagnoses. However, extracting meaningful insights from this data can be difficult without proper visualization and analysis tools.

This project analyzes hospital patient outcomes and disease comorbidity patterns using the **Diabetes 130-US Hospitals dataset**. The goal of the project is to understand how combinations of diseases such as **Diabetes, Heart Disease, and Cancer** influence hospital outcomes such as length of stay, readmission patterns, treatment intensity, and discharge categories.

Interactive dashboards were created using **Tableau** to visualize these patterns and provide insights into patient outcomes across different disease groups.

---

# 2. Dataset Description

The dataset used in this project is the **Diabetes 130-US Hospitals dataset**, which contains hospital encounter records from multiple hospitals in the United States between 1999 and 2008.

The dataset includes information about:

- Patient demographics
- Diagnoses
- Medication usage
- Treatment procedures
- Hospital stay duration
- Readmission status
- Discharge outcomes

Total number of patient encounters analyzed:

**101,766 records**

Dataset sources:

UCI Machine Learning Repository  
https://archive.ics.uci.edu/ml/datasets/Diabetes+130-US+hospitals+for+years+1999-2008

Kaggle  
https://www.kaggle.com/datasets/brandao/diabetes

---

# 3. Data Preparation

Before visualization, the dataset required several preprocessing and cleaning steps.

The following steps were performed:

- Removed unnecessary columns that were not relevant to the analysis
- Handled missing and inconsistent values
- Standardized categorical variables
- Simplified discharge disposition categories
- Reduced dataset complexity by keeping only relevant fields

The final cleaned dataset contained the following key columns:

- encounter_id
- patient_nbr
- age
- gender
- race
- disease_type
- time_in_hospital
- readmitted
- num_medications
- insulin
- diabetesMed
- discharge_disposition_label

This cleaned dataset allowed for more efficient analysis and visualization in Tableau.

---

# 4. Disease Classification Method

To analyze comorbidity patterns, a new variable called **disease_type** was created.

This variable was derived using the diagnosis columns:

- diag_1
- diag_2
- diag_3

Based on the diagnosis codes, patients were categorized into the following disease groups:

- Diabetes Only
- Heart Disease Only
- Cancer Only
- Diabetes + Heart Disease
- Diabetes + Cancer
- Heart Disease + Cancer
- All Three Diseases
- Other

This grouping enabled the analysis of how combinations of diseases affect hospital outcomes.

---

# 5. Dashboard Design

Two interactive dashboards were developed using **Tableau**.

## Dashboard 1: Comorbidity Impact on Hospital Outcomes

This dashboard provides an overview of how different disease combinations influence hospital outcomes.

Visualizations included:

- Bubble chart showing disease severity and length of hospital stay
- Heatmap showing readmission patterns across disease groups
- Treatment profile showing average medications, procedures, and lab procedures
- KPI indicators for total patient encounters and average hospital stay

---

## Dashboard 2: Diabetes-Related Discharge & Treatment Analysis

This dashboard focuses specifically on diabetes-related patient outcomes.

Visualizations included:

- Discharge category distribution
- Detailed discharge breakdown
- Insulin treatment patterns
- Diabetes medication usage
- Readmission analysis across discharge outcomes

These dashboards allow users to interactively explore hospital outcomes across different patient groups.

---

# 6. Key Insights

Several insights emerged from the analysis:

- Patients with multiple comorbidities tend to have longer hospital stays.
- Readmission rates vary significantly across disease combinations.
- Treatment intensity differs depending on the severity of disease combinations.
- Most patients are discharged home, while smaller groups are transferred or admitted to hospice care.

These findings highlight the importance of considering comorbidities when analyzing patient outcomes.

---

# 7. Conclusion

This project demonstrates how healthcare datasets can be analyzed using data visualization techniques to uncover patterns in patient outcomes.

By using **Tableau dashboards**, complex hospital data was transformed into interactive visual insights that highlight relationships between disease combinations, treatment patterns, and hospital outcomes.

Such analyses can help healthcare professionals and decision makers better understand patient care patterns and improve hospital resource planning.