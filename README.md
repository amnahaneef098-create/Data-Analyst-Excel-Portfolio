# Data-Analyst-Excel-Portfolio
Excel data pipeline project cleaning raw government fleet data and constructing multi-dimensional Pivot Tables to analyze asset distribution.
# Montgomery County Fleet Equipment Inventory Analysis
An Excel data pipeline project cleaning raw government fleet data and constructing multi-dimensional Pivot Tables to analyze asset distribution.

## 🛠️ Phase 1: Data Cleaning & Preprocessing
To ensure data integrity before analysis, the raw dataset was cleaned using the following rigorous data pipeline steps:
* **Table Standardization:** Formatted the raw dataset into a structured Excel Table to manage rows and columns dynamically.
* **Structural Adjustments:** Optimized column widths across the sheet to prevent clipped text or standard truncated cell display issues (`###`).
* **Data Auditing:** Leveraged Excel **Filters** to identify, isolate, and safely delete empty data rows.
* **Deduplication:** Applied **Remove Duplicates** to isolate and delete duplicate records, ensuring a unique count of fleet entries.
* **Data Quality Check:** Executed full spell-checks to fix localized typing errors in the source data.
* **Whitespace Trimming:** Used **Find and Replace** to remove redundant double-spaces from cells.
* **Advanced Text Manipulation:** Resolved an integration error where data fields were split incorrectly across two columns. Utilized **Flash Fill** to merge and reconstruct unified Department names (e.g., *Board of Elections, Consumer Protection*) and purged the redundant broken columns.

---

## 📈 Phase 2: Statistical Summaries & Pivot Tables
Once data integrity was verified, data summaries and multiple analytical views were constructed:

### 1. AutoSum Baseline Metrics
Key statistical summaries were mapped out for the fleet metrics (Column C) using native Excel functions:
* **SUM:** Total inventory pool calculation.
* **AVERAGE:** Mean asset distribution size.
* **MIN / MAX:** Absolute spectrum bounds of the inventory.
* **COUNT:** Total valid data rows tracked.

### 2. Multi-Dimensional Pivot Table Architecture
To analyze the sum of equipment counts across the county, three distinct Pivot worksheets were developed to view the data from different managerial perspectives:

| Worksheet | Structure | Purpose / Action |
| :--- | :--- | :--- |
| **Pivot Table 1** | **Rows:** Department <br>**Values:** Sum of Equipment Count | Sorted in **descending order** to instantly identify the highest and lowest resource-heavy departments. |
| **Pivot Table 2** | **Rows:** Department ➔ Equipment Class <br>**Values:** Sum of Equipment Count | Hierarchical departmental drill-down. Shows asset types under each department. *Collapsed to isolate the **Transportation** profile.* |
| **Pivot Table 3** | **Rows:** Equipment Class ➔ Department <br>**Values:** Sum of Equipment Count | Asset-first distribution layout. Identifies which departments hold specific equipment classes. *Collapsed to isolate the **CUV** profile.* |

---

## 📁 Repository Structure & Deliverables
* `Montgomery_Fleet_Equipment_Inventory_FA_PART_1_END.xlsx`: Finalized data cleaning workbook.
* `Montgomery_Fleet_Equipment_Inventory_FA_PART_2_END.xlsx`: Finalized multi-dimensional Pivot Tables workbook.

---

## 📷 Project Documentation & Screenshots

## 🛠️ Phase 1: Data Cleaning & Preprocessing
To ensure data integrity before analysis, the raw dataset was cleaned using the following rigorous data pipeline steps:

* **Step 1: Duplicate Records**
  Applied Remove Duplicates to isolate and delete duplicate records, ensuring a unique count of fleet entries.
  ![Removing Duplicates](screenshot%202026-08-31%20182552.png)

* **Step 2: Merging Department Names**
  Resolved an integration error where data fields were split incorrectly across two columns. Reconstructed unified Department names.
  ![Split Columns View](Screenshot%202026-08-31%20181519.png)
  ![Merging Department Names via Formula](screenshot%202026-08-31%20184620.png)

## 📈 Phase 2: Statistical Summaries & Pivot Tables
Once data integrity was verified, multiple analytical views were constructed to analyze startup funding distributions:

* **Step 3: Initializing Pivot Table from Data Range**
  Initialized the analytical framework by creating a new worksheet from the cleaned `Table2` dataset.
  ![Pivot Table Initialization](image_gfonxm.png)

* **Step 5: Exploring Recommended Pivot Tables**
  Utilized Excel’s Recommended Pivot Tables feature to audit alternative data summaries like funding amounts by city location.
  ![Recommended Pivot Tables Tool](image_6zL9GW.png)

* **Step 6 (View A): Analysis by Timeline Slicer**
  Constructed a dynamic interactive Timeline slicer to filter total investment amounts specifically across the Sept - Oct 2019 period.
  ![Date Timeline Filter View](image_Gum2hw.png)

* **Step 6 (View B): Analysis by City Location Slicer**
  Applied a multi-select interactive Slicer for regional distribution analysis, filtering down details for specific hubs like Noida and New York.
  ![City Location Slicer Filter View](image_CRL4GD.png)


