# 💾 Data Cleaning using SQL

## 📄 Project Description

This project focuses on cleaning a real-world employee layoffs dataset sourced from [Kaggle](https://www.kaggle.com/). The raw data was imported into **MySQL**, where several SQL operations were used to clean and prepare the dataset for analysis.

The objective was to resolve issues in the raw data such as:
- Duplicate records  
- Inconsistent text formatting  
- Missing or null values  
- Incorrect data types  

---

## 🛠️ Tools Used

- **MySQL**
- **MySQL Workbench**
- **Kaggle** (for data source)

---

## 🧹 Data Cleaning Workflow

### ✅ 1. Duplicate Removal

- Identified duplicate rows using `ROW_NUMBER()` with a CTE.
- Retained only the first occurrence, and deleted the rest.

<p align="center">
  <img src="https://i.imgur.com/g5ptuNC.png" width="80%" alt="Duplicate removal in SQL"/>
</p>

---

### ✅ 2. Data Standardization

- Trimmed extra white spaces from the `company` column.
- Replaced inconsistent values like:
  - `"united states"` → `"United States"`
  - `"crypto currency"` → `"crypto"`
- Converted the `date` column from **TEXT** to **DATE** type using `STR_TO_DATE()` and `ALTER TABLE`.

<p align="center">
  <img src="https://i.imgur.com/rSQZ7ut.png" width="80%" alt="Standardizing text and dates"/>
</p>

---

### ✅ 3. Handling Null & Missing Values

- Replaced empty strings in `industry` with `NULL`.
- Used self-joins to fill in missing industry values based on the company.
- Removed rows where both `total_laid_off` and `percentage_laid_off` were null.

<p align="center">
  <img src="https://i.imgur.com/R362hTy.png" width="80%" alt="Null value treatment in SQL"/>
</p>

---

### ✅ 4. Final Cleanup

- Dropped helper columns like `row_num` used during the cleaning process.

<p align="center">
  <img src="https://i.imgur.com/oGy8UFP.png" width="80%" alt="Final cleanup"/>
</p>

---

## 📌 Outcome

The dataset is now clean, consistent, and ready for:
- Exploratory Data Analysis (EDA)
- Dashboard development (e.g., in Power BI, Tableau)
- Reporting and visualization

---
