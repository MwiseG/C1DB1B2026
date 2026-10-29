# Module 4 source note — vintage 2026.1

## What this release is

Issued scenario parameters for the common Module 4 rehearsal.
They overlay the approved Module 3 benchmark and the group's
five-municipality decision table.

This folder is **not** a predictive hold-out.

## Predictive component

Not issued as a common file. Optional for a group that took up
prediction in Module 2 (own model with a hold-out, or an external
forecast). Otherwise mark **Not assigned**.

Do not split the decision table, invent a test set, or treat
`Scenario_Spec.csv` as reserved outcomes.

## Files

| File | Use |
|---|---|
| `Scenario_Spec.csv` | Named changes for the two required scenarios. |
| `Constraint_Spec.csv` | Teaching constraints. The benchmark ceiling is compulsory for the common rehearsal. The portfolio ceiling is an illustrative demonstration assumption. |
| `SOURCE_NOTE.md` | This note. |

## Required scenarios

1. **S1_baseline** — preserve the approved Module 3 values and weights.
2. **S2_operating** — multiply the named cost field by 1.20. Keep other indicators and baseline weights unchanged.
3. **S3_combined** — the same cost scaling **and** the named cost-priority weights.

Run each scenario on a **copy**. Do not overwrite the baseline.

## Teaching constraints

- Benchmark: `annual_cost <= 6.5` cost units. Synthetic teaching assumption. Not a Vårdlyftet budget.
- Demonstration portfolio: `Est_Premises_Cost_kSEK <= 650`. Illustrative teaching assumption for the instructor notebooks. Groups must label any portfolio ceiling as a **group assumption** unless a case requirement is issued.

Unknown is not Met.

## Why a 20% cost increase can leave rankings unchanged

Under the prescribed min–max and vector normalizations, multiplying one criterion by a positive constant leaves its normalized values unchanged when normalization is recomputed from the scenario matrix. Absolute costs still rise. Recheck the ceiling.

## Live challenge

The instructor may change the multiplier, the ceiling, or both, on a copy of the common benchmark. Preserve prepared results.
