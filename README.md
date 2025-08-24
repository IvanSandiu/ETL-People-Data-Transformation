# ETL Project: People Data Transformation  

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)  
![Pandas](https://img.shields.io/badge/Library-Pandas-orange)  
![ETL](https://img.shields.io/badge/Process-ETL-yellow)  

---

## 📖 Overview  

This project implements an **ETL (Extract, Transform, Load) pipeline** that processes people’s data from multiple file formats (`CSV`, `JSON`, `XML`).  

The pipeline:  
1. **Extracts** raw data from all available files in a directory.  
2. **Transforms** units of measurement (inches → meters, pounds → kilograms).  
3. **Loads** the transformed dataset into a CSV file.  
4. Tracks each step in a **log file** with timestamps.  

---

## 📂 Project Structure  

| File / Folder            | Description |
|---------------------------|-------------|
| `etl_people.py`           | Main ETL pipeline script |
| `transformed_data.csv`    | Output dataset in CSV format |
| `log_file.txt`            | Log file with ETL execution details |
| `*.csv / *.json / *.xml`  | Input files containing raw people data |

---

## ⚙️ Requirements  

This project requires **Python 3.8+** and the following libraries:  

```bash
pip install pandas
```

## ⚙️ ETL Pipeline

**Extract**:
Reads all .csv, .json, and .xml files in the current directory and consolidates them into a single DataFrame.

**Transform**:
Reads exchange rates from a CSV file and converts market capitalization values from USD to GBP, EUR, and INR.

**Load**:
Saves the transformed dataset to transformed_data.csv.

**Logging**:
Every ETL stage (start/end of extraction, transformation, loading) is logged into log_file.txt with a timestamp.

## 🚀 How to Run  

Clone the repository or download the script, then execute:  

```bash
python etl_people.py
```

![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)
