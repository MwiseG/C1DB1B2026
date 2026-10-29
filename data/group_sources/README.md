# Group-collected sources

Put **your** extracts here (VGR PxWeb, Vårdgivarwebben, SCB, or other
public files named in the Module 1 KPI-to-data table).

These files are the rest of your architecture. The course-issued
anchor and companions show *how* to map, join, and score. After that
demonstration, Modules 2–4 run on **your** approved columns as well.

Formatting and wiring are **your** work. There is no advanced,
source-specific support: the course team does not know which table
you will find. If the extract cannot cover all five municipalities,
the indicator stays Unresolved.

Do **not** edit `data/manifest.json`. That file is the course-issued
switchboard. Notebooks already read it for the common modules.

## What to do

1. Keep the original download in `raw/` if you wish.
2. In the notebook, map Swedish headers to the course field names
   (`Municipality_Code`, `Year`, …). Do not overwrite the download.
3. Save one analysis-ready CSV in this folder.
4. Add a row to `Source_Register.csv`.
5. Join with the Module 2 rules. Keep all five municipalities.

`Source_Register.csv` is a table, not JSON.
