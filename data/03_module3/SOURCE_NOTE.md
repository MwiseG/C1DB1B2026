# Module 3 source note — vintage 2026.1

## Status

- Common MCDA benchmark: **issued**
- Predictive component: **not issued** as a common file (optional for a group; otherwise mark Not assigned)

## Files

| File | Role |
| :--- | :--- |
| `MCDA_Benchmark.csv` | Synthetic alternatives A–E with two criteria |
| `MCDA_Benchmark_Meta.csv` | Direction (Benefit/Cost) and baseline weights |

These rows are **not** municipalities. Benchmark scores are learning
checks, not establishment evidence.

## Baseline convention

- Opportunity: Benefit, weight 0.60
- Annual cost: Cost, weight 0.40
- Weights are non-negative and sum to 1
- WSM: direction-aware min–max; constant columns → 0, retain weight
- TOPSIS: vector normalization of the **raw** matrix, then weights
- Ties: average rank
- Spearman $\rho$: descriptive only; undefined if a ranking is constant

Reference WSM scores: A 0.60, B 0.65, C 0.60, D 0.50, E 0.40.

Reference TOPSIS closeness (3 d.p.): A 0.565, B 0.648, C 0.588,
D 0.487, E 0.435.

## Portfolio application

Use the group's Module 2 decision table. Score only approved numerical
columns that are finite for all five codes. Exclude source-missing
fields (for example Svenljunga travel time) unless an approved
treatment exists.

## What students must not do

- Feed the WSM min–max matrix into TOPSIS
- Give a Cost criterion a negative weight
- Drop a municipality to make a method run
- Invent a regression target merely to fill the matrix
- Treat method agreement as proof that establishment is justified
