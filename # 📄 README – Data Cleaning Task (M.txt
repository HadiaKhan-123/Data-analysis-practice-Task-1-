# 📄 README – Data Cleaning Task (Medical Appointment Dataset)

## 💼 Internship Task 1: Data Cleaning and Preprocessing  
**Dataset Used**: Medical Appointment No-Shows (Kaggle)  
**Tools**: Python (Pandas), Jupyter Notebook  
**File Submitted**: `cleaned_appointments1.csv`

---

## 🎯 Objective:
Clean and prepare a raw dataset by handling missing values, fixing data types, removing duplicates, and formatting date columns to a consistent format.

---

## ✅ Steps Performed:

### 1. Loaded the Dataset
- Read the CSV using `pandas.read_csv()`.
- Previewed using `.head()` and `.info()`.

### 2. Checked for Missing Values
- Used `.isnull().sum()` to verify.
- ✅ No missing values found in the dataset.

### 3. Removed Duplicate Rows
- Used `.drop_duplicates()` to eliminate exact row-level duplicates.

### 4. Fixed Column Data Types
- Converted `SCHEDULEDDAY` and `APPOINTMENTDAY` to `datetime` format using:
  ```python
  pd.to_datetime(df['SCHEDULEDDAY'])

Converted AGE to integer:

df['AGE'] = df['AGE'].astype(int)

5. Standardized Date Format
Reformatted date columns to dd-mm-yyyy using .dt.strftime('%d-%m-%Y').

6. Cleaned Column Names
Renamed all column headers to lowercase using:

df.columns = df.columns.str.lower()

7. Saved Final Cleaned Dataset

Exported the cleaned DataFrame to CSV using:

df.to_csv('final_cleaned_appointments.csv', index=False)

