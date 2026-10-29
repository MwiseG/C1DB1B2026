# C1DB1B – Data Management for Decision-Making
*Datahantering för beslutsfattande (7,5 högskolepoäng / 7.5 ECTS credits)*  
*Program*: Systemvetarutbildningen, Högskolan i Borås  
*Offering*: current Canvas instance (rooms and clock times live there)

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/MwiseG/C1DB1B2026/main?labpath=starter_m1.ipynb)

---

## How you will work

**Bring a laptop** to every workshop. Run the notebooks **locally**. Binder is a backup only.

Hand in your work on **Canvas**. Do not push notebooks, data, or pull requests into this repository. Optional backup on your own GitHub account is fine; it is not the submission.

Starter notebooks for Modules 1–4 are in this repository from the start. Complete the matching starter **before** each workshop. Instructor solutions (`solution_m*.ipynb`) are published here only **after** that workshop.

---

## 1. Recommended: Miniconda or Anaconda on your laptop

Install [Miniconda](https://docs.conda.io/en/latest/miniconda.html) or [Anaconda](https://www.anaconda.com/download) before Workshop 1.

Then, in **Anaconda Prompt** (Windows) or a terminal (macOS/Linux):

```bash
git clone https://github.com/MwiseG/C1DB1B2026.git
cd C1DB1B2026
```

If you do not use git, download the repository ZIP from GitHub (Code → Download ZIP) and unzip it.

Create an environment and install the packages:

```bash
conda create -n c1db1b python=3.11 -y
conda activate c1db1b
pip install -r requirements.txt
jupyter lab
```

Open `starter_m1.ipynb` and confirm that it runs. The notebook must be able to see the `data/` folder next to it.

Before each later workshop, open the matching starter (`starter_m2.ipynb`, `starter_m3.ipynb`, `starter_m4.ipynb`) the same way.

---

## 2. Binder (backup only)

Use Binder if local installation fails. Click the badge above, wait for the session to start, and open the starter you need.

Treat Binder with caution:

- The session is temporary. Closing the tab, losing wifi, or leaving it idle **deletes your work**.
- After every substantial change: **File → Download** as `.ipynb`.
- Download again before you close the window.
- Submit that downloaded file on Canvas. Binder is not a store.

Do not rely on Binder as the main runtime in the three-hour workshop. The freeze, live injection, and upload all need a file that stays on your laptop.

---

## Course and workshop overview

Recorded lectures Fö A1–A4 precede Workshops 1–4. Each workshop executes the matching module. Rooms and clock times live on Canvas, not in this file.

Group-collected files are formatted and joined by the group; there is no source-specific support. Prediction is optional (own model with a Module 2 hold-out of about 20% of eligible observations, or an external forecast); either way, justify it.

### Workshop 1: Decision Framing, KPI-to-Data Mapping & Baseline Demonstration

Students advise **Vårdlyftet** on where (if anywhere) to establish its next primary care centre, using an allocated portfolio of **five municipalities**. Module 1 does not require a winning municipality. It requires a decision statement, a KPI-to-data map, three prescribed demographic indicators, initial weights, and a live sensitivity rehearsal.

Years, file paths, and vintage are read from `data/manifest.json`. See Document B (`Data_Stream.tex`) for how the course team can replace extracts without rewriting notebooks.

#### Core learning objectives
- Frame the establishment decision (client, alternatives, option not to proceed).
- Load the Module 1 anchor table and pass structural checks on the five-municipality extract.
- Calculate $S_{80+}$, the demographic dependency ratio, and $G_{80+}$ using $t_0$ and $t_1$ from the manifest.
- Map at least six scored indicators to actual fields, including competition/accessibility and financial/operational coverage.
- Record a provisional weight profile and apply a controlled input change on a copy of the baseline.

---

### Workshop 2: Data Preparation, Hygiene & Pipeline Integration

Module 2 turns the Module 1 decision architecture into a checkable, analysis-ready evidence table. You are still **not** required to pick a winning municipality.

Work in this order:

**Input Contract** → **Integration** → **Diagnosis** → **Treatment** → **Verified Output**

The course team issues a **common companion exercise** under `data/02_module2/`. Apply it to your five allocated municipalities. Then apply the same checks to any additional sources in your approved KPI-to-data table. There is no fixed dataset count and no requirement to use different transformations merely to show variety.

The issued common path does not include a prediction file. Prediction is **optional**: build a model (Module 2 may hold out about 20% of eligible observations) or use a published forecast; justify either. Do not split the five alternatives as an MCDA training/test set. If the group does not take it up, mark **Not assigned**.

---

### Workshop 3: Decision Modelling, MCDA & Sensitivity

Module 3 compares the five municipalities with two checkable methods (WSM and TOPSIS) under explicit weights. You may now form a **provisional** recommendation; it can still be “do not proceed,” and a high rank is not by itself an establishment decision.

Work in this order: check the matrix → review overlap → WSM → TOPSIS from the **raw** values → compare ranks → three weight profiles → recommendation.

Complete the synthetic benchmark in `data/03_module3/` first, then apply the same functions to your portfolio table. Insert a predicted column only if the group justified it in Module 2.

#### Core learning objectives
- Score only approved numerical columns that are finite for all five alternatives.
- Treat $|r|>0.8$ as a review flag, not an automatic deletion.
- Implement direction-aware min–max WSM and vector-normalized TOPSIS with the course edge-case conventions.
- Compare rankings without treating Spearman $\rho$ as proof of quality.
- Test baseline, equal, and one priority weight profile on both methods.
- Explain a conditional recommendation, including method disagreement.

---

### Workshop 4: From Model Results to Defensible Action

Module 4 turns the approved Module 3 package into management advice: **Go**, **Conditional Go**, or **No-Go**. No new scoring method is required.

Work in this order: trace evidence and constraints → one operating-cost scenario → one combined adverse scenario → robustness claim → prediction status → five-sentence recommendation → Decision Model Zero reflection → defense rehearsal.

Complete the common rehearsal in `data/04_module4/` first. Then apply the analogous scenarios to your portfolio table. If the group built a model, evaluate the Module 2 hold-out here. These scenario files are not a hold-out.

#### Core learning objectives
- Keep ranking, prediction, and feasibility claims distinct.
- Run specified stress scenarios on copies; do not overwrite the baseline.
- Recheck absolute cost ceilings when a uniform scaling leaves ranks unchanged.
- State verifiable conditions, not “proceed if costs seem reasonable.”
- Return to Decision Model Zero and analyse a recorded episode, not personalities.

---

## Repository contents and release schedule

Starter notebooks for all four modules are available now. Prepare the matching starter before each workshop. **Benchmark solutions** are released to this repository only after that workshop.

| File | Release status | Description |
| :--- | :--- | :--- |
| **`starter_m1.ipynb`** | Available now | Module 1: framing, structural checks, three indicators, KPI-to-data table, weights, sensitivity rehearsal. |
| **`starter_m2.ipynb`** | Available now | Module 2: source register, joins, missingness, treatment comparison, five-row decision table. |
| **`starter_m3.ipynb`** | Available now | Module 3: benchmark WSM/TOPSIS, portfolio scoring, overlap, weight profiles, provisional recommendation. |
| **`starter_m4.ipynb`** | Available now | Module 4: evidence/constraints, two stress scenarios, Go / Conditional Go / No-Go, reflection, defense rehearsal. |
| **`data/`** | Available now | Versioned data stream (`manifest.json`, Decision Model Zero, Module 1–4 files, `group_sources/`). |
| **`requirements.txt`** | Available now | Package list for local install and Binder. |
| **`solution_m1.ipynb`** | After Workshop 1 | Instructor benchmark for the demonstration portfolio. |
| **`solution_m2.ipynb`** | After Workshop 2 | Instructor benchmark for the demonstration portfolio. |
| **`solution_m3.ipynb`** | After Workshop 3 | Instructor benchmark for the demonstration portfolio. |
| **`solution_m4.ipynb`** | After Workshop 4 | Instructor benchmark for the demonstration portfolio. |
| **`VGR_Demographics_Raw.xlsx`** | Available now | Raw Statistics Sweden (SCB) administrative table (2015–2025). |
| **`VGR_Demographics_2015_2025.csv`** | Available now | Curated demographic extract used to build the Module 1 anchor. |
| **`VGR_External_Health_Socioeconomic.csv`** | Available now | Source extract behind the Module 2 travel-time field. Use the issued companion files in `data/02_module2/`, not this file as a silent extra join. |
| **`VGR_Training_Model_Set.csv`** | Not used in 2026.1 Module 2 | Legacy 52-municipality split. Do not treat this as the Module 2 decision table. |
| **`VGR_Holdout_Test_Set.csv`** | Not used in 2026.1 Module 2 | Legacy hold-out file. Do not treat it as the group's optional 20% test set. |

---

## Required literature and references

1. **Lane, D.** (2022): *Introductory Statistics*. Open Educational Resource.
2. **Huntsinger, R.**: *Business Analytics: Methods and Cases for Data-Driven Decisions*.
3. **Brunsson, K. & N.** (2017): *Decisions – The complexities of individual and organizational decision-making*.
4. **Statistics Sweden (SCB)**: Population statistics by region, age, sex, and year (Table BE0101).

---

## Support and course contact

Course Instructor: **Gideon Mbiydzenyuy**  
Email: [gideon.mbiydzenyuy@hb.se](mailto:gideon.mbiydzenyuy@hb.se)  
Institution: Faculty of Business, Work Life and Social Welfare, University of Borås
