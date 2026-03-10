# Data Cleaning Done Right: Turning Raw Data into Usable Insights

## Overview
Good analysis starts with clean data.

This project demonstrates a complete **data cleaning workflow in Microsoft Excel**.  
The goal was to transform a **raw, unstructured dataset** into a **clean, organized, and analysis-ready dataset** by applying several Excel data cleaning techniques.

Raw data often contains inconsistencies such as duplicates, missing values, extra spaces, formatting issues, and calculation errors. Cleaning the data ensures that it is reliable and ready for further analysis or visualization.

---

## Dataset
The dataset contains information such as:

- Client names  
- Contact names  
- Departments and regions  
- Revenue and profit values  
- Payment information  

The original dataset included several issues such as:

- Inconsistent text formatting  
- Extra characters in client names  
- Duplicate records  
- Blank cells  
- Formula errors  
- Poor readability  

---

## Data Cleaning Process

### 1. AutoFit Rows and Columns
Adjusted row heights and column widths to ensure all values are clearly visible and readable.

---

### 2. Find & Replace
Used Excel's **Find & Replace** feature to remove unnecessary text inside parentheses from client names.

Example:

```
Find: (*)
Replace: [blank]
```

---

### 3. Standardizing Text (LOWER Function)
Converted all client names to lowercase to ensure consistency.

```excel
=LOWER(D2)
```

---

### 4. Cleaning Text with TRIM & PROPER
Removed extra spaces and standardized capitalization of contact names.

```excel
=PROPER(TRIM(E2))
```

---

### 5. Text to Columns
Separated combined data (such as department and region) into separate columns using the **Text to Columns** feature with an underscore `_` delimiter.

Example:

```
Sales_North → Sales | North
```

---

### 6. Removing Duplicates
Used Excel's **Remove Duplicates** feature to identify and remove duplicate rows from the dataset.

---

### 7. Filling Empty Cells
Identified blank cells using **Go To Special → Blanks** and replaced them with `"N/A"`.

---

### 8. Error Handling with IFERROR
Handled calculation errors when dividing profit by revenue using the `IFERROR` function.

```excel
=IFERROR(Profit/Revenue,"N/A")
```

---

### 9. Formatting Headers
Improved readability by formatting the header row with:

- Bold text
- Background color
- Clear column labels

---

### 10. Removing Gridlines
Removed Excel gridlines to create a cleaner and more professional presentation.

---

## Tools Used

- Microsoft Excel
- Excel Functions:
  - LOWER
  - TRIM
  - PROPER
  - IFERROR
- Excel Features:
  - Find & Replace
  - Text to Columns
  - Remove Duplicates
  - Go To Special
  - Formatting

---

## Final Result

After cleaning, the dataset is:

- Structured and organized
- Free of duplicates
- Consistent in formatting
- Free of blank or erroneous values
- Ready for analysis or visualization

---

## Key Takeaway

Clean data is the foundation of reliable data analysis.  
Proper data preparation ensures accurate insights and better decision-making.

---

## Future Improvements

Possible next steps include:

- Creating dashboards in Excel
- Data visualization
- Analysis using Python or Power BI
- Automating cleaning tasks with Excel macros

---

## Author
Altagi Abdallah
