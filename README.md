# C1DB1B (2026) – Data Management for Decision-Making
*Datahantering för beslutsfattande (7,5 högskolepoäng / 7.5 ECTS credits)*  
*Program*: Systemvetarutbildningen, Högskolan i Borås  
*Term*: Spring 2026  

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/MwiseG/C1DB1B2026/main?labpath=starter_m1.ipynb)

---

## 🚀 Quick Start: Run in Your Browser with Binder

This repository is configured for **MyBinder.org**, allowing students and instructors to run all interactive Jupyter notebooks immediately in the cloud—**zero local installation, Python setup, or environment configuration required**.

1. Click the **[Launch Binder](https://mybinder.org/v2/gh/MwiseG/C1DB1B2026/main?labpath=starter_m1.ipynb)** badge above.
2. Wait 1–2 minutes for the cloud Jupyter environment to build and launch.
3. Open `starter_m1.ipynb` in the file browser.
4. Follow the step-by-step instructions, complete the `# TODO:` coding tasks for your assigned municipality, and answer the Strategic Reflection Prompts.

> ⚠️ **Important Submission Notice for Binder Users**:  
> Binder sessions are temporary and reset when idle. **Always download your completed notebook** to your local computer before closing your browser:  
> **File $\rightarrow$ Download** (as `.ipynb`)  
> Submit your completed file to Canvas / course LMS as instructed.

---

## 📘 Course & Workshop Overview

### Workshop 1: Demographic Data Curation, Descriptive Statistics & Strategic Healthcare Decision Support

In this workshop, students take on the executive role of a **Healthcare Data Analyst & Decision Support Specialist** advising the leadership of **Västra Götalandsregionen (VGR)**. VGR oversees healthcare delivery across 49+ municipalities and faces urgent capital expenditure decisions regarding where to allocate eldercare and geriatric care facilities from a **500 million SEK investment pool**.

#### Core Learning Objectives:
- **Data Engineering & Curation**:
  - Ingest raw administrative multi-header spreadsheets (`VGR_Demographics_Raw.xlsx`).
  - Forward-fill merged hierarchical headers (regions, single-year age cohorts).
  - Handle missing and corrupted data markers (`..`, whitespace) and export an audit-ready dataset (`VGR_Demographics_2015_2025.csv`).
- **Descriptive Statistics for Decision Support**:
  - Compute weighted central tendency: **Mean Age ($\bar{x}$)** vs. **Median Age**.
  - Quantify dispersion: **Standard Deviation ($\sigma$)**.
  - Measure relative volatility: **Coefficient of Variation ($CV = (\sigma / \bar{x}) \times 100$)**.
  - Track 10-year demographic momentum and volatility for the vulnerable **80+ cohort (2015–2025)**.
- **Statistical Interpretation & Skewness**:
  - Diagnose distribution asymmetry ($\bar{x} > \text{Median}$ vs. $\text{Median} > \bar{x}$).
  - Understand why relying purely on arithmetic means distorts healthcare capital allocation.
- **Strategic KPI Formulation**:
  - Formulate quantitative Key Performance Indicators (*Aging Intensity Ratio*, *Elderly Growth Velocity*) to justify capital budget allocations.

---

## 🔧 Repository Contents & Release Schedule

> 💡 **Pedagogical Workflow**:  
> In accordance with course design, **starter notebooks** (`starter_m*.ipynb`) and datasets are published prior to each workshop so students can prepare and follow along in real time. **Benchmark solution notebooks** (`solution_m*.ipynb`) are released to this repository following the completion of each module workshop.

| File | Release Status | Description |
| :--- | :--- | :--- |
| **`starter_m1.ipynb`** | 🟢 **Available Now** | Scaffolded student workshop notebook with step-by-step Python explanations, `# TODO:` coding tasks, and structured business decision questions. |
| **`solution_m1.ipynb`** | 🔒 *Released After Workshop* | Complete benchmark reference solution with model answers, visualizations, and 53-municipality county ranking. |
| **`VGR_Demographics_Raw.xlsx`** | 🟢 **Available Now** | Raw Statistics Sweden (SCB) administrative table containing VGR demographic counts by region, single-year age (0–100+), gender, and year (2015–2025). |
| **`VGR_Demographics_2015_2025.csv`** | 🟢 **Available Now** | Normalized, audit-ready CSV produced during Step 1 (16,218 rows $\times$ 28 columns). |
| **`requirements.txt`** | 🟢 **Available Now** | Package dependencies for Binder (Pandas, NumPy, SciPy, Matplotlib, Seaborn, OpenPyXL). |

---

## 💻 Local Setup (Alternative to Binder)

If you prefer to run the workshop locally on your own machine:

```bash
# 1. Clone this repository
git clone https://github.com/MwiseG/C1DB1B2026.git
cd C1DB1B2026

# 2. (Optional) Create and activate a virtual environment
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate

# 3. Install required dependencies
pip install -r requirements.txt

# 4. Launch JupyterLab
jupyter lab
```

---

## 📚 Required Literature & References

1. **Lane, D.** (2022): *Introductory Statistics*. Open Educational Resource.
2. **Huntsinger, R.**: *Business Analytics: Methods and Cases for Data-Driven Decisions*.
3. **Brunsson, K. & N.** (2017): *Decisions – The complexities of individual and organizational decision-making*.
4. **Statistics Sweden (SCB)**: Population statistics by region, age, sex, and year (Table BE0101).

---

## ✉️ Support & Course Contact

Course Instructor: **Gideon Mbiydzenyuy**  
Email: [gideon.mbiydzenyuy@hb.se](mailto:gideon.mbiydzenyuy@hb.se)  
Institution: Faculty of Business, Work Life and Social Welfare, University of Borås
