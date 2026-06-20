# ETL Workflow

## Pipeline Objective

The Tableau Prep workflow combines listing-level Airbnb information, housing attributes, city-level buy/rent benchmarks, and occupancy assumptions into processed datasets for investment analysis.

## Public-Safe Inputs in This Repository

- `data/raw/airbnb_price.xlsx`
- `data/raw/house_info.xlsx`
- `data/raw/cities_in_sicily.xlsx`
- `data/raw/cities_in_sicily_buy_rent.xlsx`
- `data/raw/occupancy_rate_by_city.xlsx`
- `data/raw/listings_sample_public.csv`

## Published Workflow Logic

1. Ingest raw Airbnb, property, and city-level reference files in Tableau Prep.
2. Standardize join keys and clean analytical fields.
3. Combine listing-level and city-level tables into unified analytical records.
4. Compute revenue, rent, service-cost, occupancy-adjusted, and ROI-oriented metrics.
5. Export processed outputs for Tableau Desktop and the browser dashboard reconstruction.

## Repo-Safe Tableau Prep Assets

- `tableau/prep/airbnb_investment_pipeline_final_repo_safe.tfl`
- `tableau/prep/airbnb_investment_pipeline_early_version_repo_safe.tfl`

## Published Outputs

- `data/processed/airbnb_investment_dataset_final.xlsx`
- `data/processed/occupancy_sensitivity_dataset.xlsx`

## Portability Note

The published repository keeps the repo-safe Tableau Prep flows only. They were prepared to point to repository-local files, but should still be opened in Tableau Prep to confirm path resolution and schema refresh behavior.
