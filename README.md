# Cancer Survival Analysis Project

## About
This project focuses on analyzing survival outcomes for patients diagnosed with five primary types of cancer: Lung, Pancreas, Thyroid, Colorectal, and Melanoma. By applying Kaplan-Meier survival analysis, the study evaluates survival disparities based on gender, race, and age groups to uncover critical insights for improving patient outcomes and guiding healthcare strategies.

---

## Business Problem
Cancer remains one of the leading causes of mortality worldwide. Understanding survival outcomes across demographics and cancer types is vital for improving treatment plans and public health policies. This project aims to:
- Evaluate survival rates across five cancer types.
- Analyze the impact of demographic factors such as gender, race, and age.
- Provide actionable insights for personalized healthcare and resource allocation.

---

## Data and Features

### **Dataset Overview**
**Source**: Cancer patient clinical dataset.  
**Number of Patients**: 8,468.  
**Key Features**:
- **Cancer Types**: Lung, Pancreas, Thyroid, Colorectal, Melanoma.
- **Demographics**: Gender, race (White, African-American, Asian/Mideast-Indian, Others), and age groups (e.g., 11–20, 21–30).
- **Event Dates**: Diagnosis date, survival duration, and date of death (censored for patients alive at the end of the analysis).

### **Data Preparation**
1. **Exclusions**: Patients diagnosed after **8/25/2016** were removed.
2. **Independent Observations**: Patients with multiple cancer diagnoses were treated as independent records.
3. **Censoring**: Applied for patients alive as of the analysis cutoff date.

---

## Analytical Approach

### **Survival Analysis**
- **Kaplan-Meier Estimators**:
  - Used to calculate survival probabilities over time.
  - Stratified by cancer type, gender, race, and age group.
- **Group-wise Comparisons**:
  - Analyzed survival disparities within demographic subgroups.
  - Identified the highest and lowest survival outcomes across strata.

---

## Key Findings

### **Cancer-Specific Survival Rates**
1. **Thyroid Cancer**: Exhibited the highest survival rates, with over **90% survival probability** across all demographics.
2. **Lung Cancer**: Had the lowest survival rates, with a steep decline in survival probabilities, particularly among older patients.

---

### **Demographic Insights**
1. **Gender**:
   - **Females** consistently had higher survival probabilities across most cancer types.
   - Example: Females with colorectal cancer had a **94.8% survival rate** after 1,000 days.

2. **Race**:
   - **White patients** had the highest overall survival rates, achieving a **92.6% probability** across all cancers after 2,500 days.
   - **African-Americans** experienced significant disparities, particularly in lung and melanoma cancers.

3. **Age Groups**:
   - Younger patients (11–20 years old) had the best survival outcomes across all cancer types.
   - The oldest group (91–100 years) had the poorest outcomes, often with survival rates below 50% within two years.

---

### **Kaplan-Meier Analysis**
- Kaplan-Meier survival curves provided clear visualizations of survival trends:
  - Thyroid cancer consistently showed the flattest survival curves, indicating favorable outcomes.
  - Lung cancer showed the steepest decline, reflecting its aggressive nature.

---

## Results Summary

### **Survival Statistics by Cancer Type**
| Cancer Type   | Survival Highlight                                   |
|---------------|------------------------------------------------------|
| Thyroid       | >90% survival across all age and gender groups.      |
| Lung          | <50% survival in older groups after two years.       |
| Pancreatic    | 100% survival in the 21–30 age group after one year. |
| Colorectal    | 94.8% survival for females after 1,000 days.         |
| Melanoma      | 97.4% survival for the 61–70 age group over 5 years. |

---

## Why Kaplan-Meier for Survival Analysis?
Kaplan-Meier estimators were chosen for their ability to:
- Handle censored data effectively.
- Provide time-to-event analysis for survival probabilities.
- Enable group-wise comparisons across demographic strata.

---

## Limitations & Future Directions

### Limitations
- Small cohort sizes for specific demographic subgroups.
- Lack of detailed clinical treatment and staging data.
- Cross-sectional data limits longitudinal insights.

### Future Work
1. Integrate treatment regimens and clinical staging data for deeper analysis.
2. Incorporate longitudinal datasets to track survival trends over extended periods.
3. Apply advanced survival modeling techniques, such as Cox proportional hazards, to identify key risk factors.

---

## Deliverables

### Key Outputs
1. **Kaplan-Meier Curves**: Survival plots stratified by cancer type, gender, race, and age group.
2. **Survival Statistics**: Detailed tables summarizing survival probabilities for each demographic subgroup.
3. **Analysis Code**: Scripts implementing Kaplan-Meier estimators and survival comparisons.

### Repository Contents
- **Code**: Includes preprocessing scripts and Kaplan-Meier estimations.
---

## Conclusion
This analysis highlights critical disparities in survival outcomes across cancer types, demographics, and age groups. Thyroid cancer demonstrated the most favorable prognosis, while lung cancer showed the poorest outcomes. Addressing these disparities through targeted interventions and resource allocation can improve survival rates for vulnerable populations. The findings serve as a foundation for future research and policymaking in oncology.
