# TL Performance & Calibration Dashboard (Excel + Power Query) 

## Overview
This project is an operational Excel dashboard designed to help Quality Assurance teams monitor **Team Leader (TL) scoring performance**, identify **mis-scored questions**, and support **calibration and coaching activity** across the organisation.

The dashboard allows users to:
- Track scoring alignment between TLs and QA  
- Analyse which questions are most frequently mis-scored  
- Review tolerance and variance outcomes  
- Assess scoring accuracy by agent tenure  
- Drill down into detailed TL or monthly performance  
- Filter all visuals using interactive slicers  

All data has been fully anonymised for demonstration purposes.

---

## Tools Used
- **Microsoft Excel**
- **Power Query** (ETL and data cleaning)
- **Excel Data Model**
- **PivotTables**
- **KPI Cards & Slicers**
- **Excel Charts (Bar & Pie)**

---


##  Data Cleaning & Transformation (Power Query)
The raw dataset (exported from a SharePoint-based operational data source) was cleaned and transformed using Power Query before being loaded into the Excel Data Model.

### Key transformation steps:
1. **Imported raw CTC audit data** into Power Query  
2. **Merged with anonymised TL lookup table** to replace real TL names  
3. **Removed confidential fields** and unused columns  
4. **Standardised** column names, data types, and category values  
5. **Created final cleaned dataset** containing:  
   - Audit metadata  
   - Anonymous TL name  
   - Discrepancy question numbers  
   - Alignment outcome  
   - Tolerance & Variance  
   - Consumer Duty outcomes  
6. Loaded this cleaned dataset to the **Excel Data Model** for reporting  
7. Raw data query left as **connection-only** to maintain privacy  

---

## Data Pipeline

**Sharepoint → Excel → Power Query → Data Model → PivotTables → Dashboard**

### Pipeline Breakdown:
- **Data Import:** Raw CTC scoring data exported from Sharepoint 
- **Power Query:** Cleaning, column standardisation, anonymisation  
- **Data Model:** Measures created (Row Count, Alignment %)  
- **PivotTables:** Serve as the backend feeding all visuals  
- **Dashboard:** KPI cards, bar charts, pie charts, slicers  

The entire dashboard updates automatically when refreshing the final dataset.

---

## Dashboard Visuals

### **1. KPI Cards**
- **Total Audits**
- **Alignment %**
- **Most Mis-Scored Question**


### **2. Main Visual**
- **Total Discrepancies by Question**  
  Bar chart showing question numbers ranked by discrepancy frequency.


### **3. Supporting Visuals**
- **TL Outcomes** (pie chart)
- **Tolerance Breakdown** (pie chart)
- **Consumer Duty Outcomes** (pie chart)
- **Variance Breakdown** (bar chart)

### **4. Interactive Filters**
- **TL Name Slicer**
- **Month Slicer**

All visuals respond dynamically to slicer selections.

---

## Files Included
'CTC_Full_Dashboard.png' - Screenshot of CTC dashboard
'ReadMe.md' - Project overview and documentation
'ctc_tl_performance_data.csv' - Fully anonymised dataset used for building the dashboard.



> *The Excel file is not included due to sensitive internal source data. All screenshots were taken from an anonymised version of the dashboard.*

---

## Notes
- TL names have been fully anonymised (TL_01, TL_02, TL_03, etc.)  
- No confidential or customer-specific data is included  
- Dashboard structure matches the real internal version while using safe, anonymised data  
- Demonstrates Excel BI design, Power Query cleaning, Data Modelling, and interactive reporting

---

## Key Learnings
- Power Query greatly simplifies data cleaning and anonymisation  
- Excel can deliver BI-quality dashboards with a clear layout and strong UX  
- Separating pivot logic (backend) and visuals (frontend) improves clarity and maintainability  

- KPI cards provide an immediate high-level summary for operational stakeholders  
