<div align="center">

<a name="readme-top"></a>

# 📊 Healthcare Comorbidity & Patient Outcome Analysis

Interactive **Tableau dashboards** analyzing hospital outcomes and comorbidity patterns using the **Diabetes 130-US Hospitals dataset**.

**[🚀 View Live Dashboard](https://public.tableau.com/views/Healthcare_Comorbidity_Patient_Outcome_Analysis/ComorbidityImpactonHospitalOutcomes)**

</div>

---

# 📑 Table of Contents

1. Project Overview  
2. Dataset  
3. Data Cleaning & Preparation  
4. Disease Grouping Strategy  
5. Dashboards  
6. Key Insights  
7. Tools Used  
8. Project Structure  
9. References  

---

# 📊 Project Overview

Healthcare institutions generate vast amounts of patient data, but identifying patterns that influence hospital outcomes can be difficult without effective visualization.

This project analyzes **hospital patient outcomes and disease comorbidity patterns** using the **Diabetes 130-US Hospitals dataset**.

The analysis focuses on understanding how combinations of diseases such as:

• Diabetes  
• Heart Disease  
• Cancer  

affect:

• Hospital length of stay  
• Readmission patterns  
• Treatment intensity  
• Discharge outcomes  

Interactive dashboards were created using **Tableau** to explore these relationships and present insights through intuitive visualizations.

---

# 🗂 Dataset

**Dataset Used**

Diabetes 130-US Hospitals Dataset

**Sources**

• UCI Machine Learning Repository  
https://archive.ics.uci.edu/ml/datasets/Diabetes+130-US+hospitals+for+years+1999-2008  

• Kaggle Dataset  
https://www.kaggle.com/datasets/brandao/diabetes  

The dataset contains hospital encounter records including:

• Patient demographics  
• Diagnoses  
• Treatment information  
• Medication usage  
• Hospital stay duration  
• Readmission status  

Total records analyzed:

**101,766 patient encounters**

---

# 🧹 Data Cleaning & Preparation

The raw dataset required several preprocessing steps before it could be used for visualization.

The following data preparation tasks were performed.

### Data Cleaning

• Removed unnecessary and irrelevant columns  
• Handled missing and inconsistent values  
• Standardized categorical variables  
• Simplified discharge disposition categories  
• Cleaned dataset structure for easier analysis  

### Dataset Simplification

Only relevant columns required for analysis were kept, including:

encounter_id  
patient_nbr  
age  
gender  
race  
disease_type  
time_in_hospital  
readmitted  
num_medications  
insulin  
diabetesMed  
discharge_disposition_label  

Final cleaned dataset contains **101,766 records and 19 columns**.

This produced a **clean dataset optimized for dashboard visualization and analysis**.

---

# 🧾 Spreadsheet Preparation & Validation

• Reviewed detailed discharge disposition labels before grouping them into broader categories.

• Created grouped discharge categories: Discharged, Transferred, Expired, Hospice, and Other.

• Implemented spreadsheet-based grouping logic and refined it after initial incorrect results.

• Used pivot-table-based exploration to validate discharge category distributions before visualization.

• Verified final dataset structure and retained diagnosis fields (diag_1, diag_2, diag_3) for reproducibility of disease classification.

---

# 🧬 Disease Grouping Strategy

A new variable **disease_type** was created to identify disease combinations.

The grouping was derived from diagnosis columns:

diag_1  
diag_2  
diag_3  

Based on these diagnosis codes, patients were categorized into the following groups:

Diabetes Only  
Heart Disease Only  
Cancer Only  
Diabetes + Heart Disease  
Diabetes + Cancer  
Heart Disease + Cancer  
All Three Diseases  
Other  

This grouping enabled analysis of **comorbidity patterns and their impact on hospital outcomes**.

---

# ⚙️ Calculated Fields & Logic

• Created **disease_type** using diagnosis fields (diag_1, diag_2, diag_3) to identify Diabetes, Heart Disease, Cancer, and Other.

• Built **Disease Group** to classify patients into mutually exclusive comorbidity segments.

• Created **Diabetes Encounter** logic to isolate diabetes-specific records for Dashboard 2 (Diabetes-focused dashboard).

• Developed **discharge_category_grouped** to simplify detailed discharge labels into broader categories.

• Implemented KPI calculations including **Total Encounters** and **Average Length of Stay**.

• Used consistent aggregation logic (`COUNT(Patient Nbr)`) across all visualizations to maintain metric consistency.

---

# 📊 Dashboards

Two interactive dashboards were developed using Tableau.

---

## Dashboard 1  
### Comorbidity Impact on Hospital Outcomes

![Dashboard 1](images/dashboard1.png)

This dashboard provides an overview of how disease combinations influence hospital outcomes.

Key components include:

• Disease severity vs hospital stay visualization  
• Readmission patterns across disease groups  
• Treatment intensity indicators  
• KPI for total patient encounters  
• KPI for average hospital stay  

This dashboard highlights how different comorbidity patterns affect hospital outcomes.

---

## Dashboard 2  
### Diabetes-Related Discharge & Treatment Analysis

![Dashboard 2](images/dashboard2.png)

This dashboard focuses specifically on diabetes-related hospital outcomes.

Key visualizations include:

• Discharge category distribution  
• Detailed discharge breakdown  
• Insulin treatment patterns  
• Diabetes medication usage  
• Readmission patterns among diabetes patients  

This dashboard enables deeper exploration of treatment patterns and discharge outcomes.

---

## 🔗 Dashboard Interactions & Features

• Added interactive filters for Age, Gender, and Race across dashboards.

• Implemented click-based drill-down interactions between visualizations.

• Used Tableau action filters with selected field mapping.

• Scoped filters using “Apply to Worksheets → Selected Worksheets” to prevent cross-dashboard interference.

• Designed tooltips and labels to improve readability and reduce clutter.

---

## 🎯 Visualization Design Decisions

• Evaluated multiple visualization types including heatmap, bar chart, bubble chart and other layout variations.

• Replaced cluttered or less readable charts with clearer alternatives.

• Selected final visualizations based on interpretability and user experience.

---

# 🔎 Key Insights

Several insights emerge from the analysis:

• Patients with **multiple comorbidities tend to have longer hospital stays**.

• **Readmission patterns vary across disease combinations**.

• Diabetes treatment intensity is associated with differences in discharge outcomes.

• A majority of patients are **discharged home**, while smaller portions are transferred or admitted to hospice care.

---

# 🛠 Tools & Technologies

• Tableau (Dashboard Development)  
• Tableau Public (Dashboard Deployment)  
• Excel / Google Sheets (Data Cleaning & Preprocessing)  
• GitHub (Project Documentation & Hosting)  

---

# 📁 Project Structure

Healthcare-Comorbidity-Patient-Outcome-Analysis

│  
├── dashboards  
│   └── Healthcare_Comorbidity_Patient_Outcome_Analysis.twbx  

│  
├── dataset  
│   └── hospital_outcome_cleaned.csv  

│  
├── images  
│   ├── dashboard1.png  
│   └── dashboard2.png  

│  
├── docs  
│   └── project_report.md  

│  
└── README.md  

---

# 📊 Live Dashboard

Explore the interactive Tableau dashboards here:

https://public.tableau.com/views/Healthcare_Comorbidity_Patient_Outcome_Analysis/ComorbidityImpactonHospitalOutcomes

---

# 📚 References

• UCI Machine Learning Repository – Diabetes 130-US Hospitals Dataset  
https://archive.ics.uci.edu/ml/datasets/Diabetes+130-US+hospitals+for+years+1999-2008  

• Kaggle Dataset Source  
https://www.kaggle.com/datasets/brandao/diabetes  

---

<div align="right">

[⬆️ Back to top](#readme-top)

</div>
