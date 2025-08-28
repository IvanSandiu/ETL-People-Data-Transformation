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
Reads all .csv, .json, and .xml files in the current directory.
Each file type is processed with a dedicated function (extract_from_csv, extract_from_json, extract_from_xml) and the data is consolidated into a single DataFrame with the columns name, height, and weight.

**Transform**:
Converts measurement units:
- Height: from inches to meters (multiplied by 0.0254) and rounded to two decimals.
- Weight: from pounds to kilograms (multiplied by 0.45359237) and rounded to two decimals

**Load**:
Saves the transformed DataFrame into a CSV file named transformed_data.csv.

**Logging**:
Every ETL phase (start/end of extraction, transformation, and loading) is logged into the log_file.txt file with a timestamp in the format Year-Monthname-Day-Hour-Minute-Second.

## 🚀 How to Run  

Clone the repository or download the script, then execute:  

```bash
python etl_people.py
```

![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)
