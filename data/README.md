# Data availability

Raw and derived datasets are not committed to this repository. This keeps the repository lightweight, avoids duplicating third-party data, and prevents a stale local export from being presented as the final Gold output.

To reproduce the lakehouse, download the source datasets from the official links in [`../docs/data_sources.md`](../docs/data_sources.md), retain their provider licences and land them in ADLS Gen2 using the filenames expected by the Bronze notebook.

The final analytical grain is one row per London borough and UK financial year. A complete run produces 416 rows across 32 boroughs and 13 financial years.
