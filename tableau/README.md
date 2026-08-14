# Tableau outputs

The original Tableau workbook is intentionally not published because its connection metadata includes workspace-specific Databricks SQL details. Four dashboard screenshots are available under [`../docs/dashboards`](../docs/dashboards).

To rebuild the dashboards, connect Tableau to the `cbda_tableau` schema produced by `04_analysis_mlflow_tableau.ipynb`. The serving layer includes compact tables for:

- borough-year trends and maps;
- borough profiles and rankings;
- correlation and coefficient evidence;
- model metrics and time-based predictions;
- feature importance and cross-validation results.

Use a new Databricks SQL Warehouse connection and keep credentials outside the repository.
