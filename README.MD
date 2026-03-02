# Clinical SAS: Safety Population Demographics Table

## Overview
This repository contains a specialized SAS program designed to generate a Safety Population Demographic Table (Sex and Race). It utilizes ADaM `ADSL` data to produce a submission-ready RTF report. 

This project demonstrates proficiency in:
- Macro Variable Processing: Dynamic header population using `PROC SQL INTO:`.
- Data Restructuring: Complex data manipulation, merging, and `PROC TRANSPOSE` for clinical reporting.
- Reporting: Advanced `PROC REPORT` techniques including compute blocks and ODS RTF styling.

---

## Key Features
- Total Column Logic: Creates an "ALL" treatment group (TRT01AN=99) by duplicating safety population records.
- Dynamic Headers: Automatically calculates and displays sample sizes (N=XX) in column headers using macro variables.
- Zero-Fill Logic: An array-based post-processing step ensures that missing treatment cells are populated with `0 (0.0)` for clinical accuracy.
- Clinical Formatting: Standardized "Statistic" and "Category" alignment for Gender and Race variables.

---

## 📂 Repository Structure
```text
/sas-clinical-macro-library
│
├── /data                <- Contains ADSL.sas7bdat
├── /macros              <- External RTF styling macros (rtf.sas)
├── /programs            <- Main analysis script (TABLE2.sas)
├── /outputs             <- Final generated report (Safety_Population.rtf)
└── README.md            <- Project documentation
