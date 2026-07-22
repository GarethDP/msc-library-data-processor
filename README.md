# 📚 Library Loan System & Data Processing Engine

An end-to-end Python-native data processing and validation pipeline built to clean, aggregate, and analyze high-volume library transactional data. Developed as part of the MSc Computer Science curriculum.

---

## 📌 Project Overview
This project processes raw, unvalidated library loan transaction datasets (`bookloans.csv`) alongside catalog metadata (`books.csv`) to recover key operational metrics, evaluate book popularity, and analyze reader genre preferences.

All data parsing, filtering, and metric aggregations are engineered using **pure Python core capabilities** without relying on third-party analytical libraries like `pandas`.

---

## 🚀 Key Features & Pipeline Architecture

1. **Data Cleaning & Epoch Conversion:**
   * Converts Microsoft Excel Epoch timestamps into ISO `YYYY-MM-DD` date strings.
   * Filters corrupted transactions (>250 unmatched IDs, invalid member numbers, and unreturned books).
2. **Object-Oriented Modeling:**
   * Models books, shelves, and loan transactions into clean Python classes (`Book`, `Bookshelf`, `LoanData`).
3. **Statistical Metric Generation:**
   * Computes key performance indicators (KPIs) including average loan duration, overdue transaction percentages, and mean late periods.
4. **Genre & Popularity Reporting:**
   * Measures book popularity by total duration borrowed (days) vs. raw borrow frequency.
   * Exports automated text reports (`library_report_2023.txt` & `reading_preferences_report.txt`).

---

## 📊 Summary Metrics (2023 Data)

| Metric | Result |
| :--- | :--- |
| **Average Loan Period** | ~10.27 Days |
| **Late Return Rate** | ~28.37% |
| **Average Overdue Period** | ~3.49 Days |
| **Top Performing Genre** | Fiction (677 loans) |

---

## 🛠️ Tech Stack & Requirements

* **Language:** Python 3.10+
* **Libraries:** Standard Library only (`csv`, `datetime`, `collections`, `pathlib`, `json`)
