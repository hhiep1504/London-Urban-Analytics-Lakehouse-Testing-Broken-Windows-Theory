# Methodology

## Research question

To what extent are environmental disorder, deprivation, civic strength and annual socioeconomic context associated with recorded crime rates across London boroughs over time?

## Analytical design

The unit of analysis is one London borough in one UK financial year. Monthly crime records are aggregated to financial years so they align with annual fly-tipping and socioeconomic data. Crime and fly-tipping counts are divided by annual mid-year population and expressed per 1,000 residents.

This design produces 416 expected observations: 32 boroughs across 13 financial years from 2011–12 to 2023–24.

## Data engineering controls

- Borough names are normalised to stable lower-case keys before joins.
- The City of London and unknown geographies are excluded to maintain a consistent 32-borough panel.
- Delta tables retain dataset, source-file, source-path and ingestion-time lineage in Bronze.
- The Gold layer checks row count, distinct boroughs, distinct years and duplicate composite keys.
- Five missing fly-tipping-rate rows remain null for auditability and are excluded only when a model or correlation requires that feature.
- Missing unemployment values are filled within borough using the nearest available temporal value and explicitly flagged.
- Static CSI and IMD features are treated as contextual controls, not annual causal measurements.

## Modelling

Three models are compared:

1. A linear regression using fly-tipping rate only.
2. A controlled regularised linear model using environmental, demographic, socioeconomic, civic and period variables.
3. A random forest using the same contextual panel features.

The evaluation is temporal: observations through 2020–21 form the training set, while 2021–22 to 2023–24 form the held-out test set. RMSE, MAE and R² are logged to MLflow. Separate OLS evidence is calculated for coefficient direction, standard error and significance.

## Interpretation limits

- Administrative records reflect reporting and enforcement behaviour as well as underlying events.
- Per-resident crime rates can be inflated in central boroughs with large commuter, visitor and nightlife populations.
- Borough averages hide within-borough variation.
- The panel is observational and cannot identify causal effects.
- A high predictive R² from the random forest should not be interpreted as evidence for Broken Windows Theory.
