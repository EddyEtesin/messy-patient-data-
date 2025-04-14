# messy-patient-data-
# Patient Data Analysis - README

## Overview
This Jupyter notebook performs an analysis on messy patient data, cleaning and transforming the dataset to answer key questions about patient demographics, admission patterns, and hospital stays. The dataset contains information on 132 patients with various date formats and some missing values that needed standardization.

## Key Features
- Data cleaning and standardization of date formats across multiple columns
- Age group categorization for demographic analysis
- Calculation of hospital stay durations
- Identification of admission patterns by month and year
- Outlier detection in patient ages
- Missing data analysis

## Data Cleaning Highlights
1. **Date Standardization**: 
   - Converted 6 different date columns from various formats (e.g., "12/13-2023", "Sep 13, 2024", "42535") to consistent datetime format
   - Handled invalid dates and missing values (represented as NaT)

2. **Age Group Categorization**:
   - Created age bins: 20-29, 30-39, 40-49, 50-59, 60-69, 70-79, 80-84
   - Added new "Age groups" column for demographic analysis

3. **Hospital Stay Calculation**:
   - Computed length of stay as difference between admission and discharge dates
   - Handled negative values by setting them to 0

## Key Findings

### 1. Patient Demographics
- **Average Age**: 52.89 years
- **Gender Distribution**:
  - Female: 67 patients
  - Male: 65 patients
- **Most Common Age Group**: 20-29 years old had the highest number of admissions

### 2. Admission Patterns
- **Monthly Admissions**:
  - December had the highest admissions (31 patients)
  - July and November had the fewest (6 patients each)
- **Yearly Admissions**:
  - 2023: 72 patients
  - 2024: 49 patients
  - 2022 and 2003: 1 patient each

### 3. Hospital Stays
- **Average Length of Stay**: 235.33 days
- **Longest Stay**: Patient PID1103
- **Shortest Stay**: Patient PID1000 (0 days)

### 4. Data Quality
- **Missing/Invalid Dates**: 32.58% of records have either missing admission or discharge dates
- **Age Outliers**: No outliers detected in patient ages

## Usage Notes
1. The notebook requires pandas, numpy, seaborn, and matplotlib libraries
2. Missing values are preserved as NaT/NaN rather than imputed
3. The analysis assumes that negative length-of-stay values are data errors and sets them to 0

## Recommendations
1. Consider investigating the high number of December admissions
2. Review records with missing admission/discharge dates (32.58% of data)
3. Validate the unusually long average stay of 235 days
4. Standardize data collection processes to prevent date format inconsistencies in future records

