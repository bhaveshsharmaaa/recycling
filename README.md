# ♻️ RECYCLING SYSTEMS AND MATERIAL RECOVERY

### 📘 Project Overview

This Python project analyzes multi-year **municipal solid waste datasets** (e.g. _Boralesgamuwa: 2012–2018_).  
It automatically cleans, standardizes, and simulates **waste recovery performance** to estimate recovery efficiency and recycling potential.  
The system produces year-wise and total summaries, along with human-readable insights.

---

## 🧭 Workflow

**Flow:**

Each step is fully automated and modular — the program can handle any CSV with date, waste type, and weight columns.

```bash
Raw CSV → Cleaning → Standardization → Simulation → Summarization → Interpretation → Outputs
```

---

## ⚙️ Features

✅ Automatic column detection (handles multiple CSV formats)  
✅ Waste type standardization (dictionary + regex mapping)  
✅ Simulation of recovery rates for each material  
✅ Year-wise and total summaries  
✅ Automated insight generation (top recovery material, composting notes, etc.)  
✅ Timestamped CSV output saving

---

## 🧮 Recovery Rate Reference

| Material Type | Recovery Rate |
| ------------- | ------------- |
| Plastics      | 0.55          |
| Metals        | 0.78          |
| Glass         | 0.65          |
| E-waste       | 0.72          |
| Organic       | 0.25          |
| MSW           | 0.10          |

---

## 📂 Input Dataset

**File:** `boralasgamuwa_2012-2018.csv`

The dataset should include at least these columns (names can vary):

| Column      | Example Values            |
| ----------- | ------------------------- |
| Date        | 2016-03-21                |
| Waste Type  | plastic, food waste, iron |
| Weight (kg) | 125.5                     |

> Don’t worry if column names are different — the code auto-detects them (e.g. `collection_date`, `ticket_date`, `Weight(kg)` etc.)

---

## 🧠 How It Works

### 1️⃣ Cleaning

Removes invalid data, renames columns, and formats text consistently.

### 2️⃣ Standardization

Maps waste type names to standardized material names (Plastics, Metals, Organic, etc.)  
and assigns recovery rates automatically.

### 3️⃣ Simulation

Calculates recovered material using:

```bash
recovered_kg = collected_kg × recovery_rate
```

### 4️⃣ Summarization

Creates two summary tables:

- **by_mat** → Total recovery by material
- **by_year** → Year-wise recovery summary

### 5️⃣ Interpretation

Generates automatic insights:

- Highest recovery efficiency: Metals (78%)
- Largest recovered mass: Organic (500 kg)
- Organic waste recovery (25%) reflects composting potential and collection efficiency.

### 6️⃣ Output Saving

All results are stored in `/outputs/` with unique timestamps.

---

## 📤 Example Output Files

After execution, your folder will look like:

```bash
outputs/
├─ recovery_by_material_20251112_134500.csv
├─ recovery_by_year_20251112_134500.csv
└─ clean_rows_with_recovered_kg_20251112_134500.csv
```

---

## 🚀 How to Run the Script

### 🧱 Prerequisites

- Python 3.8+
- Install required package:
  ```bash
  pip install pandas
  ```
  After this Run the Script

## Output

1. Loading raw CSV…
2. Cleaning data…
3. Standardizing values…
4. Simulating recovery…
5. Summarizing outputs (Year-wise)…

---

### ♻️ Total Recovery Summary by Material

| Material Type | Collected (kg) | Recovered (kg) | Efficiency (%) |
| ------------- | -------------- | -------------- | -------------- |
| MSW           | 62,870,940.0   | 6,287,094.0    | 10.0           |
| Organic       | 3,342,640.0    | 835,660.0      | 25.0           |

---

✅ This table summarizes the **overall waste recovery performance** across all years,  
showing total collected quantities, recovered materials, and recovery efficiency for each category.

### 📅 Year-wise Recovery Summary (first 12 rows)

| Year | Material Type | Collected (kg) | Recovered (kg) | Efficiency (%) |
| ---- | ------------- | -------------- | -------------- | -------------- |
| 2012 | MSW           | 8,981,740.0    | 898,174.0      | 10.0           |
| 2013 | MSW           | 9,246,230.0    | 924,623.0      | 10.0           |
| 2014 | MSW           | 9,730,880.0    | 973,088.0      | 10.0           |
| 2015 | MSW           | 11,240,260.0   | 1,124,026.0    | 10.0           |
| 2016 | MSW           | 7,045,750.0    | 704,575.0      | 10.0           |
| 2016 | Organic       | 392,550.0      | 98,137.5       | 25.0           |
| 2017 | MSW           | 9,384,440.0    | 938,444.0      | 10.0           |
| 2017 | Organic       | 738,840.0      | 184,710.0      | 25.0           |
| 2018 | MSW           | 7,241,640.0    | 724,164.0      | 10.0           |
| 2018 | Organic       | 2,211,250.0    | 552,812.5      | 25.0           |

---

✅ This table shows the **first 12 rows** of the year-wise summary,  
indicating total collected and recovered waste quantities per material each year.

---

### 🧠 Interpretation

---

### 💾 Saved Output Files

- outputs/recovery_by_material_20251112_134500.csv
- outputs/recovery_by_year_20251112_134500.csv
- outputs/clean_rows_with_recovered_kg_20251112_134500.csv

---

## 🤝 Contributors

Anshuman Hoon 22ad10an5@mitsgwl.ac.in

Bhavesh Sharma 22ad10bh639@mitsgwl.ac.in

Krishna Gupta 22ad10kr645@mitsgwl.ac.in

## Supervised by:

- _Dr. Abhishek Bhatt_ (Assistant Professor, CAI Department, MITS)
- _Dr. Vibha Tiwari_ (Assistant Professor, CAI Department)
- Approved by: Dr. _Rajni Ranjan Singh_ (HoD, CAI Department)

---

## 📜 License

This repository is provided for academic and educational purposes only.
Reproduction or redistribution of any content without permission is prohibited.

---

## ⭐ Acknowledgment

We would like to thank Madhav Institute of Technology and Science (MITS), Gwalior,
for providing the resources and guidance needed to complete this research successfully.

---

© 2025 — Team RECYCLING SYSTEMS AND MATERIAL RECOVERY
All rights reserved.
