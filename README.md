# Airbnb Investment Analytics ETL & BI Dashboard

Airbnb and real-estate investment analysis for Sicilian cities, built from cleaned Excel and CSV inputs, prepared in Tableau, and exposed through Tableau workbooks plus a browser dashboard preview.

## Project Scope

This public repository is intentionally limited to:

- public-safe raw inputs
- processed analytical outputs
- Tableau Prep and Tableau Desktop assets that point to repository-local files
- browser dashboard preview files
- documentation needed to understand the workflow

The full private `listings.csv` file is not included. A reduced public-safe sample is provided instead.

## Repository Structure

```text
airbnb-investment-analytics-etl-bi-dashboard/
|-- data/
|   |-- raw/
|   `-- processed/
|-- dashboard_preview/
|-- docs/
|-- evidence/
|   `-- screenshots/
|-- outputs/
|-- reports/
|-- tableau/
|   |-- dashboards/
|   `-- prep/
|-- .gitignore
|-- LICENSE
`-- README.md
```

## Included Data

Public-safe raw inputs:

- `data/raw/airbnb_price.xlsx`
- `data/raw/house_info.xlsx`
- `data/raw/cities_in_sicily.xlsx`
- `data/raw/cities_in_sicily_buy_rent.xlsx`
- `data/raw/occupancy_rate_by_city.xlsx`
- `data/raw/listings_sample_public.csv`

Processed outputs:

- `data/processed/airbnb_investment_dataset_final.xlsx`
- `data/processed/occupancy_sensitivity_dataset.xlsx`

See `docs/data_sources.md` for source notes and publication scope.

## Quick Review Paths

1. Open `dashboard_preview/index.html` for the browser reconstruction of the analysis flow.
2. Open `reports/airbnb_investment_analytics_report.pdf` for the written report.
3. Open the Tableau files under `tableau/` if you want to inspect the original BI assets.

## How to Reproduce the Published Package

1. Clone the repository.
2. Review the public-safe input files under `data/raw/`.
3. Open one of the repo-safe Tableau Prep flows:
   - `tableau/prep/airbnb_investment_pipeline_final_repo_safe.tfl`
   - `tableau/prep/airbnb_investment_pipeline_early_version_repo_safe.tfl`
4. Verify that Tableau Prep resolves the repository-local input files.
5. Compare the flow outputs against:
   - `data/processed/airbnb_investment_dataset_final.xlsx`
   - `data/processed/occupancy_sensitivity_dataset.xlsx`
6. Open the Tableau workbooks in `tableau/dashboards/`.
7. Open `dashboard_preview/index.html` to review the browser-accessible dashboard version.

## Dashboard Preview

The browser dashboard is provided for reviewers who do not have Tableau.

- entry point: `dashboard_preview/index.html`
- local dataset: `dashboard_preview/data/dashboard_data.csv`
- screenshots: `evidence/screenshots/`

The preview uses only public-safe processed data and excludes direct listing identifiers.

## Documentation

- `docs/data_sources.md`
- `docs/etl_workflow.md`
- `docs/dashboard_logic.md`
- `docs/tableau_portability_notes.md`

## Limitations

- The workflow is still Tableau-based, so final validation happens inside Tableau Prep and Tableau Desktop.
- The public repository ships with a public-safe listing sample, not the full private listing export.
- The browser dashboard is a reconstruction of the analysis layer, not a Tableau-native deployment.

## License

MIT License. See `LICENSE`.
