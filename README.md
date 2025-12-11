# Medical Data Warehouse – XML to Multidimensional Model

---

## Project Overview
This project focuses on **transforming and analyzing over 1,500 medical XML documents** into a **robust multidimensional data warehouse**. The main objective is to structure unorganized medical data into a star-schema model, enabling advanced analytical operations, OLAP queries, and reporting for healthcare applications.  

The warehouse supports **data-driven decision-making**, epidemiological studies, and comprehensive medical data visualization.  

---

## Objectives
1. **Data Understanding:** Comprehend the structure and semantics of medical XML documents.  
2. **Data Cleaning:** Standardize formats (dates, text normalization), handle missing values, and ensure data quality.  
3. **Multidimensional Modeling:** Design a star-schema with fact and dimension tables to enable multidimensional analysis.  
4. **Data Loading:** Load cleaned and structured data into a MySQL-based data warehouse.  
5. **Analysis & Reporting:** Provide insights using OLAP queries, descriptive statistics, and visual exploration.  

---

## Input and Output

**Input:**  
- 1,500+ medical XML documents containing information such as:  
  - Patient data (ID, age, sex, case ID)  
  - Medical reports (description, diagnosis, department, author)  
  - Event timestamps (creation date, report date and time)  
  - Domain-specific details (medical domain, anatomy, chapter)  

**Output:**  
- A fully structured **multidimensional data warehouse**, consisting of:  
  - **Fact Table:** `FactMedicalReport`  
  - **Dimension Tables:** Patient, Medical Diagnosis, Date, Medical Domain, Medical Description, Author, Creation Date  

---

## Multidimensional Modeling

**Fact Table:**  
- Contains key metrics from medical reports, such as: report ID, ACR, state, order.  

**Dimension Tables:**  
- **Patient:** case ID, age, sex  
- **Medical Diagnosis:** diagnosis, department, commentary  
- **Date:** report date, report time  
- **Medical Domain:** medical domain category  
- **Medical Description:** description, anatomy, chapter  
- **Creation Date:** creation date  
- **Author:** report author  

**Rationale for Star Schema:**  
- Star schema is chosen for its **query performance**, **ease of understanding**, and **flexibility in OLAP operations**.  
- Compared to snowflake schema, it reduces query complexity and improves readability for medical analysts.  

---

## Data Processing Pipeline

1. **Parsing XML Documents:**  
   - Extract relevant tags and attributes from XML.  
   - Convert into structured CSV format for easier processing.  

2. **Data Cleaning:**  
   - Handle missing and inconsistent data.  
   - Standardize dates and timestamps.  
   - Remove duplicates and normalize textual fields.  

3. **Schema Design & Creation:**  
   - Define fact and dimension tables with proper primary and foreign key constraints.  
   - Enforce referential integrity.  

4. **Data Loading:**  
   - Load cleaned data into MySQL using Python and SQLAlchemy.  
   - Optimize table structures for analytical queries.  

5. **Analysis & Reporting:**  
   - Generate descriptive statistics (counts, distributions).  
   - Enable multidimensional queries on patient age, diagnosis, date, and medical domain.  

---

## Technologies & Tools
- **Programming Languages:** Python (pandas, SQLAlchemy, xml.etree)  
- **Database:** MySQL / MariaDB  
- **Data Formats:** XML, CSV  
- **Analysis:** Jupyter Notebook for descriptive statistics and multidimensional queries  
- **Modeling:** Star schema multidimensional model  

---

## Results
- Successfully parsed and transformed 1,500+ XML medical reports.  
- Designed and implemented a **star-schema data warehouse** with 7 dimensions and 1 fact table.  
- Enabled fast, flexible OLAP analysis for medical reporting.  
- Created a reusable **Python ETL pipeline** for future medical datasets.  

---

## Conclusion
- The project demonstrates the **end-to-end workflow of a medical data warehouse**, from raw XML data to structured, analyzable data.  
- The multidimensional model enables **fast queries, reporting, and dashboards**, supporting medical research and clinical decision-making.  
- This project provides a **scalable foundation** for extending to larger datasets or integrating additional medical sources.  

---

## Future Work
- Integrate **real-time medical data streams**.  
- Develop **visual dashboards** for hospital administration and epidemiologists.  
- Implement **advanced analytics**: trends, anomaly detection, and predictive insights.  

---

## Author
- **Khaoula Boughattas** – Data Engineering & Decision Systems Student at ENET’COM  
