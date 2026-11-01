# Customer Data Cleaning & Preprocessing Report

## 1. Project overview
This practice project demonstrates a basic data-cleaning workflow using Python, Pandas, and NumPy. The dataset is fictional and contains customer IDs, names, email addresses, ages, cities, and purchase amounts.

## 2. Input and output
- Input: `raw_customers.csv`
- Outputs: `cleaned_customers.csv` and `cleaned_customers.xlsx`
- Original size: 10 rows × 6 columns
- Final size: 9 rows × 6 columns

## 3. Issues identified
- Inconsistent capitalization and extra spaces in names and city values.
- The known city abbreviation `lhr`.
- One repeated customer email with matching customer details.
- One missing age and one implausible age value (150).
- One missing email and one missing purchase amount.

## 4. Cleaning actions
1. Removed leading/trailing whitespace and standardized names and cities using title case.
2. Replaced the known city abbreviation `Lhr` with `Lahore`.
3. Removed one repeated customer record by email, retaining the first occurrence. This is an exercise assumption based on the matching details in the two records.
4. Treated age 150 as invalid under a provisional rule for this fictional dataset and changed it to a missing value.
5. Calculated the median age from the remaining unique customer records (27) and used it to fill the two missing/invalid age entries.
6. Reset the row index and exported the cleaned dataset.

## 5. Final validation
- Final records: 9
- Repeated email values: 0
- Missing ages: 0
- Missing emails: 1 (preserved)
- Missing purchase amounts: 1 (preserved)
- City values: Karachi, Lahore, Islamabad

## 6. Limitations and professional considerations
The imputed age of 27 is an estimate, not a verified age. The 0–100 age validation assumption is specific to this practice exercise and should be confirmed with a data owner in real work. Duplicate emails should not automatically be deleted in client datasets: conflicting records require investigation. Missing purchase amounts were not replaced with zero because zero and unknown are different values.

## 7. Conclusion
The dataset is more consistent and easier to analyze after the documented cleaning steps. This project demonstrates foundational skills in data inspection, text standardization, duplicate handling, missing-value treatment, validation, and file export.
