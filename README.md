# Clinic Appointment Data Analysis

## 📌 Project Overview
This repository focuses on handling, cleaning, and exploring a clinical dataset sourced from Kaggle[cite: 1]. The primary objectives of this analysis are to perform rigorous **Data Cleaning** and **Exploratory Data Analysis (EDA)** to make the dataset ready for reliable reporting and data visualization[cite: 1].

---

## 🛠️ Data Cleaning Milestones
The source data (`messy_clinic_appointments.csv`) contained significant noise, missing fields, and structural inconsistencies[cite: 1]. The following preprocessing pipeline has been implemented so far:

### 👥 Gender Column Standardization
* **Format Resolution:** Resolved 8 different multi-format string and numeric entries (e.g., `0`, `1`, `M`, `F`, `female`, `male`) into uniform `'Male'` and `'Female'` categorizations[cite: 1].
* **Name Cross-Referencing:** Cross-referenced patient names to accurately map raw binary values (`0` as Female, `1` as Male)[cite: 1].
* **Missing Data Handling:** Standardized the 50 missing values in this column as `'Unknown'` to preserve data integrity for visualizations[cite: 1].

### 📅 Temporal Uniformity
* **Standardization:** Parsed and converted highly inconsistent date text across both `appointment_date` and `booking_date` columns into the standard **ISO 8601** (`YYYY-MM-DD`) format[cite: 1].

### 💰 Financial Data Auditing
* **Currency Identification:** Identified mixed international currencies (£, €, $, and Rs) within the `billing_amount` column[cite: 1].
* **Conversion Strategy:** Formulated a strategy to convert values based on a majority-currency approach[cite: 1].
* **Accountability:** Preserved existing null records as `NaN` to maintain strict financial accountability rather than using predictive imputation[cite: 1].

---

## 💻 Tech Stack & Libraries
* **Python 3**[cite: 1]
* **Pandas** (Data manipulation and structural cleaning)[cite: 1]
* **Matplotlib & Seaborn** (Data visualization and distribution charting)[cite: 1]