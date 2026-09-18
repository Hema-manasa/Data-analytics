# Day 3 — Real-World Data Cleaning

## Dataset

Worked with a realistic e-commerce dataset containing:

- 122 rows
- 7 original columns
- Customer, Product, Category, Quantity, Price, City, and Date data

## Topics Learned

### Large Dataset Inspection

- Learned how to inspect a dataset before cleaning
- Converted raw data into an Excel Table
- Used filters to identify data-quality issues

### Missing Values

- Used filters to locate missing values
- Learned `ISBLANK()` with `IF()`
- Learned that missing values should not automatically be replaced with zero
- Investigated missing Quantity and Customer values instead of guessing

### Text Cleaning

Learned:

- `TRIM()` — removes unnecessary spaces
- `PROPER()` — standardizes capitalization
- Combining functions such as `PROPER(TRIM())`
- When `PROPER()` should not be used blindly
- Used helper columns to preserve the original data

### Duplicate Detection

- Learned that repeated customers are not necessarily duplicates
- Created a Record ID using multiple fields
- Used `COUNTIF()` to identify repeated records
- Investigated duplicates before removing them
- Created a `Clean_Data` copy while preserving `Raw_Data`
- Removed confirmed duplicate records
- Validated that the remaining records were unique

### Number Validation

- Used `ISNUMBER()` to check whether values are stored as numbers
- Distinguished missing values from numbers stored as text
- Verified Quantity and Price data types

## Key Learning

Data cleaning is not simply changing or deleting values.

The workflow is:

**Inspect → Detect → Investigate → Clean → Validate**

Missing information should not be guessed, and duplicate records should be verified before removal.

## Progress

Data cleaning is still in progress.

Next topics:

- Numeric value validation
- Date validation and cleaning
- Additional data-quality checks
- Final cleaning validation
