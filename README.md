# Customer Data Cleaning & Preprocessing with Python

A beginner portfolio project demonstrating how to inspect, clean, validate, and export a fictional customer dataset using **Python, Pandas, and NumPy**.

## Project files

- `raw_customers.csv` — original fictional dataset
- `data_cleaning.ipynb` — step-by-step Jupyter Notebook
- `cleaned_customers.csv` — cleaned dataset in CSV format
- `cleaned_customers.xlsx` — cleaned dataset in Excel format
- `cleaning_report.md` — summary of the cleaning process and decisions
- `requirements.txt` — Python dependencies

## Problems identified

The original dataset contains 10 rows and 6 columns. It includes inconsistent capitalization and whitespace, a known city abbreviation, a repeated customer email, missing values, and an implausible age value of 150.

## Work performed

1. Inspected the dataset structure and missing values.
2. Standardized names and city formatting.
3. Mapped the known abbreviation `Lhr` to `Lahore`.
4. Removed one confirmed duplicate customer record for this exercise, retaining the first occurrence.
5. Treated age 150 as invalid under a provisional exercise-specific rule.
6. Imputed missing/invalid ages using the median of unique customer records (27).
7. Validated the result and exported CSV and Excel files.

## Results

- Starting records: 10
- Final records: 9
- Duplicate records removed: 1
- Missing ages after processing: 0
- Missing emails retained: 1
- Missing purchase amounts retained: 1
- Standardized cities: Karachi, Lahore, Islamabad

## Run it

Install dependencies:

```bash
pip install -r requirements.txt
```

Open `data_cleaning.ipynb` in Jupyter Notebook or VS Code. Keep `raw_customers.csv` in the same working folder when running the notebook.

## Assumptions and limitations

This is a **fictional practice project**, not paid client work and not real customer data.

- The age limit is a provisional rule for this exercise, not a universal standard.
- In a real project, confirm that age 150 is invalid before changing it.
- In this exercise, repeated email plus matching customer details is treated as a duplicate. Investigate conflicting records before deleting them in real work.
- Missing email and purchase amount values are preserved because their correct values are unknown.
- The imputed age is an estimate, not a verified age.
