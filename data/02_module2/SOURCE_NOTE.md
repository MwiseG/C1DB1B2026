# Module 2 source note — vintage 2026.1

Use this note together with `data/manifest.json`. Do not assume file
names, years, or a predictive split from an older course edition.

## Status

- Common companion exercise: **issued**
- Predictive component: **not issued** as a common file (optional for a group; otherwise mark Not assigned)
- Join key: `Municipality_Code`
- Documented missing-value marker: `..`

Notebooks must read paths and the predictive flag from the manifest.
Reference year `t1` is the Module 1 value in `manifest.json`.

## Files

| File | Grain | Year field? |
| :--- | :--- | :--- |
| `VGR_Companion_Annual.csv` | one municipality at `t1` | yes (`Year` = `t1`) |
| `VGR_Companion_StaticLookup.csv` | one municipality | no |
| `VGR_Masked_TreatmentExercise.csv` | one synthetic record | no |

## Annual companion

Fields: `Municipality_Code`, `Municipality_Name`, `Year`,
`Operating_Clinics`, `Clinics_per_10k`, `Avg_Travel_Time_min`.

- `Operating_Clinics` is a **course-constructed** incumbent count,
  aligned with Decision Model Zero where municipality names match,
  otherwise a size-based placeholder. It is not a live VGR clinic
  register.
- `Clinics_per_10k` is derived:
  `10000 * Operating_Clinics / Pop_Total` at `t1`. Verify it against
  the Module 1 population. It is not an independent measurement.
- `Avg_Travel_Time_min` is a curated accessibility estimate from the
  course extract `VGR_External_Health_Socioeconomic.csv`. Documented
  missing marker `..` for: 1444 Grästorp, 1446 Karlsborg,
  1447 Gullspång, 1465 Svenljunga.

Expected join to the `t1` demographic extract: one-to-one on
`Municipality_Code` (and `Year` after confirming both use `t1`).

## Static lookup

Fields: `Municipality_Code`, `Municipality_Name`, `Care_Need_Index`,
`Est_Premises_Cost_kSEK`.

- There is **no** `Year` column. Do not invent years.
- `Care_Need_Index` is a **course-constructed** teaching index
  (1.0 = national average in the teaching scale), aligned with
  Decision Model Zero where identities match, otherwise 1.0.
- `Est_Premises_Cost_kSEK` is a **course-constructed** teaching
  estimate in thousands of SEK. Documented missing marker `..` for
  1438 Dals-Ed.

If a static value is reused at `t1`, label that as an assumption.
Do not present it as a newly observed annual measurement.

Expected join after the annual table is one row per municipality:
one-to-one on `Municipality_Code`.

## Masked treatment exercise

Fully synthetic. Records E1–E5 are not municipalities.

Observed values: 10, 12, 14, 64 (labelled outlier). One documented
missing marker `..` on E5.

Use for the mean-versus-median rehearsal. Keep the result out of the
five-municipality decision table.

## What students must not do

- Treat `..` or an unmatched join as zero.
- Drop one of the five alternatives because a source is incomplete.
- Split the five municipalities into training and test sets.
- Apply an MCDA scaler in Module 2 merely because units differ.
- Present labelled teaching values as independently verified facts.
