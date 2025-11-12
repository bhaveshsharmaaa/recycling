# ♻️ Recycling & Organic Waste Recovery — Yearly Summary

### 📘 Project Overview

This Python project analyzes multi-year **municipal solid waste datasets** (e.g. _Boralesgamuwa: 2012–2018_).  
It automatically cleans, standardizes, and simulates **waste recovery performance** to estimate recovery efficiency and recycling potential.  
The system produces year-wise and total summaries, along with human-readable insights.

---

## 🧭 Workflow

**Flow:**

Each step is fully automated and modular — the program can handle any CSV with date, waste type, and weight columns.

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

### 📊 Total Recovery Summary by Material

| Material | Collected (kg) | Recovered (kg) | Efficiency (%) |
| -------- | -------------- | -------------- | -------------- |
| Plastics | 6,287,094.0    | 3,457,901.7    | 55.00          |
| Metals   | 334,260.0      | 260,722.8      | 78.00          |
| Glass    | 12,000.0       | 7,800.0        | 65.00          |
| Organic  | 334,260.0      | 83,565.0       | 25.00          |
| MSW      | 6,287,094.0    | 628,709.4      | 10.00          |

---

### 🧠 Interpretation

---

### 💾 Saved Output Files

- outputs/recovery_by_material_20251112_134500.csv
- outputs/recovery_by_year_20251112_134500.csv
- outputs/clean_rows_with_recovered_kg_20251112_134500.csv
