# TL Performance & Calibration Dashboard (Excel + Power Query) 



## Overview
Operational Excel dashboard built for QA teams to monitor Team Leader (TL) scoring alignment, identify common mis-scored questions, and support calibration/coaching. Uses Power Query for cleaning/anonymisation and an Excel Data Model + PivotTables to drive interactive visuals.

> All data shown in screenshots is anonymised.


## Problem
- Needed a simple way to compare TL scoring vs QA standards and highlight where mis-scoring was occurring.
- Calibration required visibility of the most common discrepancy questions and outcome patterns (tolerance/variance).
- Raw exports included sensitive fields and required cleaning/anonymisation before reporting.


## Approach
- **Extract:** exported CTC scoring/audit data from a SharePoint-based source.
- **Transform (Power Query):** removed confidential fields, standardised types/labels, and anonymised TL identities via a lookup table.
- **Model (Excel):** loaded the cleaned dataset to the Excel Data Model and used PivotTables/measures (e.g., counts, alignment %) as the backend.
- **Report:** built a one-page dashboard with KPI cards, charts and slicers (TL + month) for drilldown.


## Tools Used
- **Excel**
- **Power Query**
- **Excel Data Model**
- **PivotTables**
- **Slicers**


## Result
- Helped QA/TLs prioritise calibration by highlighting the top discrepancy questions and where alignment broke down.


## Outputs (what the dashboard shows)
- KPI cards: total audits, alignment %, most mis-scored question
- Discrepancies by question (ranked)
- Outcome breakdowns (e.g., tolerance/variance and related categories)
- Interactive slicers for TL and month


## Files
- `CTC_Full_Dashboard.png` – dashboard screenshot
- `README.md` – project summary


