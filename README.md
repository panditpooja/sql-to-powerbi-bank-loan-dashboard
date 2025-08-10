# 📊 Bank Loan Analysis Dashboard (Power BI)

![Power BI](https://img.shields.io/badge/Power%20BI-Interactive%20Dashboard-yellow?logo=power-bi&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-Validation-blue?logo=mysql&logoColor=white)
![CSV](https://img.shields.io/badge/CSV-Data-green?logo=microsoft-excel&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

**Turning raw bank loan data into powerful, interactive Power BI dashboards — validated with SQL for accuracy.**

---

## 📌 Project Overview
This project presents a **multi-page interactive Power BI dashboard** for analyzing financial bank loan data.  
The dataset contains **38,576 rows** and **24 columns**, capturing various loan details such as funded amount, interest rates, loan purposes, home ownership, and more.  

The analysis focuses on providing actionable insights through KPIs, charts, and interactive filters, allowing users to **slice and dice** the dataset based on multiple dimensions.

---

## 🆕 Key Learnings
1. Developed **multi-page dashboards** in Power BI for professional reporting.
2. Applied **major Power BI & SQL functionalities** 
3. Successfully **connected Power BI to MySQL Workbench**.
   - Faced and resolved connection issues by installing **MySQL Database Connector** (`mysql-connector-net-9.4.0`).
4. Created **SQL validation scripts** to verify Power BI results against actual data.
5. Designed KPI cards, charts, maps, and navigation buttons for a complete analytical experience.

---

## 🛠 Tools & Technologies Used
- **MS Excel**: Version 2507 Build 16.0.19029.20136 64-bit  
- **MySQL Workbench**: 8.0  
- **Power BI Desktop**: Version 2.145.1602.0 64-bit (July 2025)  
- **MySQL Connector**: `mysql-connector-net-9.4.0`  

---

## 📂 Data Source
- Raw data: CSV file  
- Database: `bank_loan_db.bank_loan_data` (for validation)  
- Connection: MySQL → Power BI Desktop (for validation purposes)  
- Data Cleaning & Transformation: Performed in Power Query (null handling, removing duplicates, standardizing types & formats).

---

## 🧩 Functionalities Applied

### **SQL – Validation Only**
- `SELECT`, `GROUP BY`, `ORDER BY`, `COUNT`, `DISTINCT`  
- Date functions: `DATENAME`, `DATEPART`, Month, Quarter, Hour, Day  
- Casting & Decimal formatting  
- `LIMIT`, CTE, Partitioning  

### **Power BI**
- Connecting to MySQL Server (for validation)  
- Data Cleaning, Modelling, Processing  
- Power Query transformations  
- Date Tables & Time Intelligence Functions (MTD, MoM)  
- DAX Functions (Date, Text, Filter, Calculate)  
- KPI Cards, Charts (Line, Donut, Tree Map, Shape Map, Bar)  
- Formatting visuals & creating navigation buttons  
- Creating calculated columns & measures  

---

## 📜 Project Workflow

### **Page 1 – Summary Dashboard**
1. Load CSV data into Power BI.
2. Data transformation in Power Query:
   - Handle nulls, remove duplicates.
   - Standardize formats (dates, text).
   - Derive calculated columns and remove unnecessary columns.
3. Create a **Date Table** using DAX:
   ```DAX
   Date Table = CALENDAR(
       MIN('bank_loan_db bank_loan_data'[issue_date]),
       MAX('bank_loan_db bank_loan_data'[issue_date])
   )
   ```
4. Implement **KPI measures** for:
   - Total Loan Applications
   - Total Funded Amount
   - Total Amount Received
   - Avg Interest Rate
   - Avg DTI
5. Create Good Loan vs Bad Loan categories and summary visuals.
6. Add slicers for purpose, date, and grade.

---

### **Page 2 – Overview Dashboard**
- **Line Charts** for monthly trends of loan metrics.
- **Shape Map** for loan applications by state.
- **Donut Chart** for loan term distribution.
- **Bar Charts** for employee length & loan purpose.
- **Tree Map** for loan applications by home ownership.

---

### **Page 3 – Details Dashboard**
- Detailed loan-level table view.
- Added **page navigation buttons** for seamless movement between dashboards.

---

## ✅ Validation
An **SQL validation document** is included to ensure that metrics displayed in Power BI are consistent with raw data outputs from MySQL queries.  
This serves as proof of accuracy for stakeholders.

---

## 📸 Dashboard Snapshots
![Summary Page](images/Dashboard%20Page%201.jpeg)  
![Overview Page](images/Dashboard%20Page%202.jpeg)  
![Details Page](images/Dashboard%20Page%203.jpeg)  

---

## 🚀 How to Use
1. Clone the repository:
   ```bash
   git clone https://github.com/panditpooja/powerbi-survey-data-analytics.git
   ```
2. Open the `.pbix` file in Power BI Desktop to explore the dashboard.  
3. View static previews in JPG or PDF if Power BI Desktop is not installed.  
3. Ensure **MySQL Connector** is installed if you want to run validation queries.

---

## ✍️ Author
**Pooja Pandit**  
Master’s Student in Information Science (Machine Learning)  
The University of Arizona  

[![GitHub](https://img.shields.io/badge/GitHub-panditpooja-black?logo=github)](https://github.com/panditpooja)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-pooja--pandit-blue?logo=linkedin)](https://www.linkedin.com/in/pooja-pandit-177978135/)
