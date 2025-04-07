# Task 1: Data Cleaning and Preprocessing

## 📌 Objective
As part of an internship with [**Elevate Lab**](https://www.linkedin.com/company/bebwwijwi/), the goal was to clean and prepare the raw **Medical Appointment No Shows** dataset by handling nulls, removing duplicates, standardizing formats, correcting inconsistencies, and ensuring the data is ready for analysis.

## 🧰 Tools Used
- **Python**
- **Pandas**

## 📁 Dataset
**Medical Appointment No Shows** – a public dataset from Kaggle containing information about patients who scheduled medical appointments and whether they showed up or not.

---

## 🔧 Steps Performed

### ✅ 1. **Read and Inspected Data**
- Used `df.info()` and `df.isnull().sum()` to understand data types and check for missing values.
- No missing values were found.

### ✅ 2. **Renamed & Standardized Column Names**
- Converted all column names to lowercase and snake_case.
- Fixed misspelled column names:
  - `Handcap` → `handicap`
  - `Hipertension` → `hypertension`
  - Others like `PatientId`, `AppointmentId`, `ScheduledDay`, `AppointmentDay` were renamed for consistency.

### ✅ 3. **Standardized Text Columns**
- Converted text fields to lowercase and stripped whitespace:
  - `gender`, `no_show`, `neighbourhood`
- Replaced abbreviations in `gender`:
  - `"f"` → `"female"`, `"m"` → `"male"`
- Capitalized values in `neighbourhood` for uniformity.

### ✅ 4. **Converted Date Columns**
- Converted `scheduled_day` and `appointment_day` to `datetime` format.
- Removed timezone info using `.dt.tz_localize(None)`.

### ✅ 5. **Handled Data Types**
- Converted `patient_id` and `appointment_id` to string to avoid scientific notation or mathematical errors.

### ✅ 6. **Outlier Handling**
- Removed invalid age value (`-1`).
- Retained high age values (e.g., 102, 115) as they are rare but realistic in medical contexts.

---

## 📊 Final Dataset Status
- Cleaned and ready for analysis or modeling.
- All columns are properly named and typed.
- Dates are standardized.
- No missing or duplicate data.
- No inconsistent text values.

---

## 📂 Files Included
- `cleaned_medical_appointments.csv` (final cleaned dataset)
- `medical_appointment_no_shows.csv` (original)
- `README.md` (this file)
- `task1_data_cleaning_medical.ipynb` (code)

---

## 📁 Repository Structure
```
task1-data-cleaning/
├── cleaned_medical_appointments.csv      # Final cleaned dataset
├── medical_appointment_no_shows.csv      # Original raw dataset
├── README.md                             # Project overview and summary
└── task1_data_cleaning_medical.ipynb     # Notebook with cleaning steps
```
---

## 🎓 About This Task
This task was undertaken as part of an internship assignment at [**Elevate Lab**](https://www.linkedin.com/company/bebwwijwi/), focused on developing real-world data preprocessing and cleaning skills using Python and Pandas.

---

## 💡 Learnings & Takeaways
- Importance of consistent naming and data types.
- Detecting and fixing spelling inconsistencies in real-world data.
- Awareness of handling edge cases like invalid ages or non-standard text values.

---

✅ **Ready for analysis or model training.**
