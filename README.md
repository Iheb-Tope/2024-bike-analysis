🚲 2024 Yearly Bike-Share Analysis

Hello! I’m Iheb, a data analyst. This repository consolidates a full ETL & descriptive-analytics workflow across all four quarters of 2024 using Divvy bike‑share data, DuckDB, and JupyterLab.

---

🔍 Project Overview

- Objective:
 Ingest, clean, transform, and summarize ride data from Q1–Q4 2024 to uncover usage patterns (daily counts, durations, peak hours, weekday trends).
- Tech Stack:
  - DuckDB for fast local SQL-based ETL
  - Pandas for DataFrame processing
  - Matplotlib for visualizations
  - JupyterLab for interactive notebooks

---

🗂️ Repository Structure

2024-bike‑analysis/
├── q1-bike‑portfolio/
│   ├── data/                ← Q1 raw CSVs (ignored by Git)
│   ├── Q1_2024_Cleaned.ipynb
│   └── rides_2024_q1.db     ← DuckDB database file
├── q2-bike‑portfolio/       ← same structure for Q2
├── q3-bike‑analysis/        ← same structure for Q3
├── q4-bike‑portfolio/       ← same structure for Q4
├── .gitignore               ← ignores raw data, .db files, checkpoints
├── requirements.txt         ← shared Python dependencies
└── README.txt               ← this file
```

> **Note:** Each quarter lives in its own subfolder. Raw CSVs and DuckDB files are excluded from Git.

---

🚀 Quick Start
1. Clone the repo 
   `git clone https://github.com/Iheb-Tope/2024-bike-analysis.git`  
   `cd 2024-bike-analysis`

2. Install dependencies
   ```bash
   conda create -n bike-env python=3.10 -y
   conda activate bike-env
   pip install --upgrade pip
   pip install -r requirements.txt
   ```

3. Run any quarter’s notebook
   ```bash
   cd q{N}-bike-portfolio    # replace {N} with 1, 2, 3 or 4
   jupyter lab
   ```
   - Open `Q{N}_2024_Cleaned.ipynb`
   - In the first cell, set `YEAR = 2024` and `QUARTER = N`
   - Run ▶ Run All Cells to generate fresh analysis

---

📊 Core Analyses (per quarter)
- Daily Counts – trend of rides over time  
- Hourly Distribution – identify peak usage hours  
- Duration Stats – mean and max ride lengths by month  
- Weekday Mode – busiest day of week  

Each notebook includes SQL ingestion, cleaning, transformation, quality checks, and plots with narrative.

---

🔄 Adding New Data
For any future quarter (or year), simply:
1. Create a new folder `q{N}-bike-portfolio/`
2. Drop your CSVs into `data/{YEAR}_Q{N}_csv/`
3. Copy and adapt an existing quarter’s notebook
4. Update the `YEAR` and `QUARTER` parameters in the first cell
5. Run all cells to regenerate outputs

---

🔧 Dependencies
All packages are listed in `requirements.txt`.  
```bash
pip install -r requirements.txt
```

---

Feel free to explore, fork, or provide feedback. Happy riding!
