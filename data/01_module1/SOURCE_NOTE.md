# Module 1 source note — vintage 2026.1

Use this note together with `data/manifest.json`. Do not assume years
or file names from an older course edition.

## Anchor file

- Path: `data/01_module1/VGR_Demographics_Anchor.csv`
- Grain: one row per municipality and calendar year
- Reference years for the prescribed indicators:
  - $t_0$ = **2015**
  - $t_1$ = **2025**
- These two numbers are also stored in `manifest.json` under `module1.t0`
  and `module1.t1`. Notebooks must read them from the manifest.

## Producer

Statistics Sweden (SCB), population statistics **BE0101**
(*Folkmängd efter region, ålder, kön och år*).

Underlying curated extract: `VGR_Demographics_2015_2025.csv`.

## Construction

- Gender kept: `totalt` only.
- Age `TOT` excluded; single-year ages aggregated to
  `Pop_0_17`, `Pop_18_64`, `Pop_65_79`, `Pop_80_Plus`.
- County total (`region_code = 14`) excluded.
- Integrity: the four age bands sum to `Pop_Total`.

## Required fields

`Municipality_Code`, `Municipality_Name`, `Year`,
`Pop_Total`, `Pop_0_17`, `Pop_18_64`, `Pop_65_79`, `Pop_80_Plus`.

`Municipality_Code` is an identifier, not a numeric feature.

## What this file is not

It is not a clinic register, income register, or accessibility matrix.
Those streams belong to later module releases. It is also not the
Decision Model Zero bidding table.
