# C1DB1B data stream (vintage 2026.1)

This folder is the **only** place module datasets should live.

- Contract and dictionaries: `../Data_Stream.tex`
- Machine-readable switchboard: `manifest.json`
- Do not hard-code years or file names in notebooks. Read them from `manifest.json`.

| Folder | Module | Status in 2026.1 |
| :--- | :--- | :--- |
| `00_decision_model_zero/` | Portfolio preference (before allocation) | Issued (`VGRBiddingDataset`) |
| `01_module1/` | Anchor demographics | Issued (`VGR_Demographics_Anchor.csv`) |
| `02_module2/` | Companion joins and hygiene | Issued (annual, static lookup, masked exercise) |
| `03_module3/` | MCDA benchmark | Issued (`MCDA_Benchmark.csv`) |
| `04_module4/` | Module 4 scenarios | Issued (`Scenario_Spec.csv`, `Constraint_Spec.csv`; not a hold-out) |

To refresh a vintage: replace the file in the module folder, update `manifest.json`, and update `Data_Stream.tex`.
