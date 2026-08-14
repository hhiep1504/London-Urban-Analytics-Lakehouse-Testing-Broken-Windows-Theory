# Gold data dictionary

The main output is `cbda_gold.gold_borough_year_panel`. It uses the composite key `borough_key + financial_year`.

| Field | Description |
|---|---|
| `borough_key` | Normalised London borough join key |
| `borough_name` | Display name for the borough |
| `financial_year` | UK financial year, for example `2023-24` |
| `fy_start_year` | Integer start year of the financial year |
| `crime_count` | Aggregated MPS recorded-crime count |
| `crime_rate_per_1000` | Recorded crimes per 1,000 mid-year residents |
| `flytipping_incidents` | Reported fly-tipping incidents |
| `flytipping_rate_per_1000` | Fly-tipping incidents per 1,000 mid-year residents |
| `flytipping_actions` | Recorded local-authority enforcement actions |
| `enforcement_rate` | Enforcement actions divided by fly-tipping incidents |
| `population_mid_year` | ONS mid-year resident population estimate |
| `income_taxpayer_count` | Number of taxpayers in the source estimate |
| `mean_income_gbp` | Mean taxpayer income in GBP |
| `median_income_gbp` | Median taxpayer income in GBP |
| `unemployment_rate_est` | Continuity-filled model-based unemployment estimate |
| `unemployment_rate_was_imputed` | Flag indicating that the annual rate was filled within borough |
| `csi_overall_score` | Population-weighted Civic Strength Index score |
| `living_environment_average_score` | IMD living-environment domain score |
| `income_average_score` | IMD income domain score |
| `employment_average_score` | IMD employment domain score |
| `education_skills_and_training_average_score` | IMD education, skills and training score |
| `health_deprivation_and_disability_average_score` | IMD health deprivation and disability score |
| `crime_average_score` | IMD crime-domain score |
| `barriers_to_housing_and_services_average_score` | IMD housing and services barriers score |
| `pre_covid_period` | Financial year starts in 2018 or earlier |
| `covid_period` | Financial year is 2019–20 or 2020–21 |
| `post_covid_period` | Financial year starts in 2021 or later |

Additional lineage, raw-estimate and quality fields are retained by the notebooks for auditability.
