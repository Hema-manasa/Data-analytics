# Day 3 — Real-World Data Cleaning

## Dataset

Worked with a realistic e-commerce dataset containing:

- 122 rows
- 7 original columns
- Customer, Product, Category, Quantity, Price, City, and Date data

## Topics Learned

### 1. Large Dataset Inspection

- Learned how to inspect a dataset before cleaning
- Converted raw data into an Excel Table
- Used filters to identify data-quality issues
- Learned not to manually inspect every row in a large dataset

### 2. Missing Values

- Used filters to locate missing values
- Used `ISBLANK()` with `IF()` to identify missing values
- Learned that missing values should not automatically be replaced with zero
- Investigated missing Quantity, Price, and Customer values
- Learned not to guess missing information when reliable source data is unavailable

### 3. Text Cleaning

Learned:

- `TRIM()` — removes unnecessary spaces
- `PROPER()` — standardizes capitalization
- Combining functions such as `PROPER(TRIM())`
- When `PROPER()` should and should not be used
- Used helper columns to preserve original data

Applied text cleaning to:

- Customer
- Product
- Category
- City

### 4. Duplicate Detection and Removal

- Learned that repeated customers are not necessarily duplicate transactions
- Created a Record ID using multiple fields
- Used `COUNTIF()` to identify repeated records
- Investigated duplicates before removing them
- Created a `Clean_Data` sheet while preserving `Raw_Data`
- Removed confirmed duplicate records
- Performed a final duplicate validation

### 5. Number and Data-Type Validation

Used:

```excel
=IF(ISNUMBER(F2),"Number","Not a Number")
```

and similar checks to:

- Verify Quantity and Price data types
- Distinguish missing values from numbers stored as text
- Identify missing numeric values

### 6. Numeric Value Validation

Validated Quantity and Price values to identify:

- Missing values
- Zero values
- Negative values
- Valid positive values

Example:

```excel
=IF(E2="","Missing",IF(E2<=0,"Invalid","Valid"))
```

Results:

- Quantity: 2 missing, 0 invalid
- Price: 1 missing, 0 invalid

### 7. Date Validation

Learned:

- How Excel stores dates
- How to check whether a value is a valid date
- How to remove unnecessary time display through date formatting
- How to validate whether dates fall within the expected range

Dataset date range:

- Earliest: 01-08-2026
- Latest: 31-08-2026

All dates were within the expected range.

### 8. Business Logic Validation

Checked whether Product and Category combinations were logically consistent.

Examples:

- Mouse → Electronics
- Keyboard → Electronics
- T-Shirt → Clothing
- Shoes → Footwear

No Product ↔ Category inconsistencies were found.

### 9. Final Data Validation

Performed final checks for:

- Duplicate records
- Unexpected blanks
- Text consistency
- Numeric validity
- Date validity
- Business logic consistency

Final validation showed no additional unexpected issues.

## Cleaning Workflow

**Inspect → Detect → Investigate → Clean → Validate**

## Key Learning

Data cleaning is not simply changing or deleting values.

A data analyst should investigate an issue before modifying the data and should never guess missing information without reliable evidence.

## Day 3 Outcome

Successfully completed a full real-world data-cleaning workflow on a 122-row e-commerce dataset.

Skills practiced:

- Data inspection
- Missing-value handling
- Text standardization
- Duplicate detection and removal
- Data-type validation
- Numeric validation
- Date validation
- Business-logic validation
- Final data-quality validation

## Next Step

Practice data cleaning on another realistic dataset containing different types of data-quality problems before moving to data visualization.
