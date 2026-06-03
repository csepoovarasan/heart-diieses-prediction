# Heart Diseases Analysis Dashboard 🫀📊

An interactive Power BI business intelligence solution designed to analyze clinical patient data, map critical cardiovascular risk factors, and provide data-driven insights into heart disease prevalence. This project transforms complex medical datasets into a clean, scannable visual interface to help healthcare researchers and clinical analysts identify key demographic and physiological trends.

---

## 📸 Dashboard Preview


*Figure 1: Main interface of the medical analysis dashboard.*  
*(Note: To display your dashboard image, save a snippet inside an `images` folder in this repository and update the path above).*

---

## 🚀 Project Overview

Cardiovascular diseases are a leading cause of global mortality. Identifying high-risk patient profiles early through predictive analytics and data visualization can drastically improve clinical outcomes. This interactive reporting system parses vital health metrics to uncover correlations between patient lifestyles, physiological markers, and historical heart disease diagnoses.

### Key Objectives
* Define demographic risk distributions across varying age brackets and genders.
* Correlate physiological biomarkers (e.g., cholesterol levels, blood pressure, resting heart rate) with diagnostic outcomes.
* Provide an intuitive, responsive interface for healthcare stakeholders to filter metrics dynamically.

---

## 🛠️ Technical Toolkit

* **Core File:** `HEART DISEASES DASHBOARD (1).pbix`
* **BI Platform:** Microsoft Power BI Desktop
* **Data Transformation:** Power Query (ETL pipeline implementation, handling structural null values, standardizing categorical clinical strings)
* **Analytical Modeling:** DAX (Data Analysis Expressions) for dynamic time-intelligence, filtering syntax, and clinical KPI calculations
* **Architecture:** Star Schema optimization featuring normalized dimension attributes branching from central patient diagnostic logs

---

## 📈 Dashboard Architecture & Metrics

The dashboard splits critical medical metadata into key visual components:

* **Clinical KPI Blocks:** Immediate scannable summaries indicating Total Patient Cohort Count, Average Serum Cholesterol Levels, and Patient Breakdown with Positive Diagnostic Flags.
* **Biomarker Risk Cross-Tabs:** Detailed matrix configurations evaluating trends across resting blood pressure thresholds, fasting blood sugar metrics, and exercise-induced angina indicators.
* **Demographic Distributions:** Segmented bar visualizations dividing findings across distinct age categories and physiological sex categories to pinpoint prominent vulnerability vectors.
* **Cross-Filtering Slicers:** Instant dashboard-wide adjustments letting you toggle views based on chest pain severity categories, age intervals, or target outcomes.

---

## ⚙️ Implemented DAX Formulations

Custom measures were coded within the project to ensure highly precise data aggregations. Key structural patterns utilized include:

```dax
// Example pattern for calculating heart disease prevalence rates across filtered segments
Prevalence Rate = 
DIVIDE(
    CALCULATE(COUNT(Patients[PatientID]), Patients[HeartDiseaseFlag] = 1),
    COUNT(Patients[PatientID]),
    0
)
