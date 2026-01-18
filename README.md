# 🏡 Housing Prices Data Wrangling

## 📖 Overview
This repository contains a data wrangling pipeline for a housing prices dataset. The goal is to transform raw property listings into a clean, structured dataset ready for exploratory analysis and modeling.  

The project demonstrates practical techniques for handling missing data, fixing inconsistencies, converting mixed measurement units, and engineering new features.

---

## 📂 Repository Structure
- `datasets/` → Raw dataset (`house_prices.csv`)
- `notebooks/` → Jupyter notebooks with the wrangling pipeline
- `README.md` → Project documentation

---

## ⚙️ Data Wrangling Workflow
### 1. Missing Data Handling
- Mode imputation for categorical features (`location`)
- Median imputation for numeric features (`bath`, `balcony`)
- Dropped high‑missing column (`society`)
- Removed rows with irrecoverable nulls (`size`)

### 2. Data Standardization
- Normalized text fields (`area_type`, `location`) by fixing spacing and capitalization
- Converted mixed units (`Sq. Meter`, `Sq. Yard`, `Acres`, `Cents`, `Guntha`, `Ground`, `Perch`) into **square feet**
- Split `size` column into structured features (`bedroom`, `hall`, `kitchen`)

### 3. Feature Engineering
- Extracted `sqft_min`, `sqft_max`, and `sqft_avg` from `total_sqft` values (including ranges)
- Converted object columns to numeric types for analysis

### 4. Outlier Detection (planned)
- IQR‑based filtering for extreme values in sqft and price per sqft

---

## 📊 Dataset Summary
- **Rows**: 13,320  
- **Columns**: 9 (numeric + categorical)  
- **Key Features**:  
  - `location`, `area_type`  
  - `bedroom`, `hall`, `kitchen`, `bath`, `balcony`  
  - `sqft_min`, `sqft_max`, `sqft_avg`  
  - `price`

---

## 🚀 Getting Started
### Prerequisites
- Python 3.8+
- Libraries: `pandas`, `numpy`, `matplotlib`

### Installation
Clone the repository:
```bash
git clone https://github.com/seyiodunlade/housing-prices-wrangling.git
cd housing-prices-wrangling
