# EHR Clinical Performance Dashboard — Kenya 2023–2025

## Overview
An end-to-end health data analytics project built entirely in Microsoft Excel, using a synthetic EHR dataset coded with ICD-11 and LOINC standards. 

The project covers data cleaning, transformation, exploratory analysis, 
and interactive dashboard development.

## Dataset
- 120 unique patients
- 402 encounter records
- 2,191 laboratory result records
- Date range: January 2023 – March 2025
- Setting: Primary and secondary care, Kenya
- Diagnostic coding: ICD-11
- Lab and vital sign coding: LOINC

## Project Structure
EHR_Portfolio_Dataset.xlsx
- README (dataset overview and analysis questions)
- 01_Encounters (demographics, vitals, diagnoses, medications)
- 02_Lab_Results (LOINC-coded lab results per encounter)
- 03_ICD11_Reference (diagnosis code lookup table)
- 04_LOINC_Reference (lab and vital sign code lookup table)
- 05_Data_Dictionary (field definitions and allowable values)
- Clean_Dataset (cleaned and transformed data)
- PT1–PT4 (PivotTables per analysis question)
- Dashboard (interactive dashboard with slicers and timeline)

## Data Cleaning Steps
- Identified and handled missing blood pressure values
- Removed impossible BMI entries (negative values)
- Corrected invalid date formats
- Standardised age into clinical bands using IFS formula:
  18–34 (Young Adults), 35–49 (Middle Age), 
  50–64 (Late Middle Age), 65–85 (Senior Adults)
- Flagged dirty records using Data_Quality_Flag column
- Pulled lab results into encounters table using multi-criteria XLOOKUP

## Analysis Questions Answered
Q1 — What proportion of hypertensive patients achieve BP <140/90 at follow-up?
Q2 — Is BMI ≥30 associated with HbA1c ≥7% in T2DM patients?
Q3 — Which diagnosis groups have the highest abnormal lab rates?
Q4 — How does encounter type distribute across counties?
Q5 — Gender disparity in LDL management (<3 mmol/L target)

## Key Findings
- Overall BP control rate: 27.89% — below WHO 50% benchmark
- Middle Age patients (35–49) had the worst BP control at 70.91% uncontrolled
- Metabolic Syndrome was the most common diagnosis
- Average BMI across all patients: 31.56 kg/m² (obese range)
- 17% of patients had no insurance coverage
- Abnormal lab rates highest in UTI, T1DM, and Metabolic Syndrome

## Dashboard Features
- Interactive timeline filter by Encounter_Date (monthly/quarterly/yearly)
- Slicers: Age Group, Sex, Chronic Condition, Smoking Status, Alcohol Use
- KPI cards: Total Patients, Most Common Diagnosis, Average BMI, Total Encounters
- Charts: BP control by age group, encounter type by county, 
  abnormal lab rates by diagnosis, insurance status, patients per facility,
  number of patients by diagnosis

## Tools Used
- Microsoft Excel (PivotTables, PivotCharts, Slicers, Timeline)
- Formulas: XLOOKUP, IFS, COUNTIFS, AVERAGEIF, SUMPRODUCT, INDEX/MATCH
- Coding standards: ICD-11, LOINC

## Limitations
- Fully synthetic dataset — findings do not represent real patient outcomes
- Lab tests not always clinically matched to diagnoses
- HbA1c and LDL data available for subset of patients only
- Polypharmacy analysis limited by random medication assignment

## Project Files
- <a href="https://github.com/mugabepatricia/EHR_Clinical_Performance_Dashboard-Kenya_2023-2025_Excel/blob/main/EHR%20Raw%20Dataset.xlsx">Raw Dataset</a>
- <a href="https://github.com/mugabepatricia/EHR_Clinical_Performance_Dashboard-Kenya_2023-2025_Excel/blob/main/EHR%20Dashboard.png">Dashboard Preview</a>
- <a href="https://github.com/mugabepatricia/EHR_Clinical_Performance_Dashboard-Kenya_2023-2025_Excel/blob/main/EHR%20DATA%20ANALYSIS%20Report.pdf">EHR analysis report</a>

## Author
Patricia Mugabe
Aspiring Health Data Analyst | MBChB Graduate
- <a href="https://www.linkedin.com/in/patricia-mugabe/">My LinkedIn</a>
- <a href="mugabepatricia@gmail.com">Email Me</a>
