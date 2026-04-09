# 📡 ETL Telecom Project using SSIS

## 📌 Project Overview
This project implements an ETL (Extract, Transform, Load) pipeline for a telecom company using **SQL Server Integration Services (SSIS)**.

The project is inspired by the Education Garage series by Eng. Mostafa Alaa, originally built using Scala. This version recreates the same concept using SSIS.

---

## 🎯 Objective
A telecom company needs a data pipeline to process customer activity data generated every 5 minutes in CSV format.

The system:
- Extracts data from CSV files
- Transforms and cleans the data
- Loads it into a SQL Server database for analysis

---

## 📂 Data Source
The source is a CSV file generated every 5 minutes containing customer activity records.

---

## 🧾 Dataset Structure

| Column Name | Data Type | Length | Nullable | Description |
|------------|----------|--------|----------|-------------|
| ID         | Int      | —      | No       | Unique record identifier |
| IMSI       | String   | 9      | No       | Subscriber identifier |
| IMEI       | String   | 14     | Yes      | Device identifier |
| CELL       | Int      | —      | No       | Cell tower ID |
| LAC        | Int      | —      | No       | Location Area Code |
| EVENT_TYPE | String   | 1      | Yes      | Type of event |
| EVENT_TS   | Timestamp| —      | No       | Event timestamp |

---

## ⚙️ ETL Process

### 1. Extract
- Read CSV files generated periodically
- Detect and load new files automatically

### 2. Transform
- Data type conversion
- Handle null values
- Clean and validate data

### 3. Load
- Load data into SQL Server tables
- Ensure consistency and integrity

---

## 🛠️ Technologies Used
- SQL Server Integration Services (SSIS)
- SQL Server
- Visual Studio

---

## 📁 Project Structure
- `.sln` → Solution file  
- `.dtproj` → SSIS project file  
- `.dtsx` → SSIS packages  
- `.conmgr` → Connection managers  

---

## 🔒 Security Considerations
- No sensitive data is stored in the repository
- SSIS ProtectionLevel is set to:
