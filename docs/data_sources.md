# Data sources

The pipeline combines seven public analytical datasets. A borough boundary file is used only for mapping.

| Dataset | Role in the project | Temporal treatment | Source |
|---|---|---|---|
| MPS Recorded Crime: Geographic Breakdown | Outcome: recorded-crime counts | Monthly records aggregated to financial year | [London Datastore](https://data.london.gov.uk/dataset/mps-recorded-crime-geographic-breakdown-exy3m/) |
| Fly-tipping Incidents | Main visible-disorder proxy and enforcement actions | Annual financial-year series | [London Datastore](https://data.london.gov.uk/dataset/fly-tipping-incidents-e5myg) |
| Estimates of the Population for England and Wales | Population denominators for rates per 1,000 | Annual mid-year estimates | [Office for National Statistics](https://www.ons.gov.uk/peoplepopulationandcommunity/populationandmigration/populationestimates/datasets/estimatesofthepopulationforenglandandwales) |
| Average Income of Tax Payers, Borough | Time-varying economic context | Annual financial-year series | [London Datastore](https://data.london.gov.uk/dataset/average-income-of-tax-payers-borough-2g1nq) |
| Model Based Unemployment Estimates | Time-varying labour-market context | Annual estimates | [London Datastore](https://data.london.gov.uk/dataset/model-based-unemployment-estimates-vq8o6) |
| London Civic Strength Index | Civic strength and collective-efficacy context | Static borough context in this analysis | [London Datastore](https://data.london.gov.uk/dataset/london-civic-strength-index-v8651/) |
| English Indices of Deprivation 2019 | Deprivation and living-environment context | Static 2019 borough context | [London Datastore](https://data.london.gov.uk/dataset/indices-of-deprivation-2l15g) |
| London borough boundaries | Tableau mapping only; not used as a model feature | Static geometry | [housequest-data GeoJSON](https://github.com/radoi90/housequest-data/blob/master/london_boroughs.geojson) |

## Expected Bronze filenames

| Filename | Dataset |
|---|---|
| `mps.csv` | MPS recorded crime |
| `flytipping.csv` | Fly-tipping incidents |
| `population.csv` | ONS population estimates |
| `income.csv` | Taxpayer income |
| `unemployment.csv` | Model-based unemployment |
| `csi.csv` | Civic Strength Index |
| `imd.csv` | Indices of Deprivation domain summaries |

Source schemas and download files can change over time. Validate headers against the Bronze configuration before rerunning the pipeline.
