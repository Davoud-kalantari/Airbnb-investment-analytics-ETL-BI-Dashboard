# Data Sources

## Public Repository Policy

This repository keeps only files that are safe to publish and useful for understanding the workflow.

Included:

- cleaned raw Excel inputs used by the published Tableau workflow
- a public-safe sample of listing-level Airbnb data
- processed analytical outputs used by the dashboards

Excluded:

- the full private `listings.csv` export
- files containing direct host identifiers, listing names, exact coordinates, or similar sensitive fields
- local temporary exports, caches, and recovery files

## Files Included

### Raw Inputs

- `data/raw/airbnb_price.xlsx`
- `data/raw/house_info.xlsx`
- `data/raw/cities_in_sicily.xlsx`
- `data/raw/cities_in_sicily_buy_rent.xlsx`
- `data/raw/occupancy_rate_by_city.xlsx`
- `data/raw/listings_sample_public.csv`

### Processed Outputs

- `data/processed/airbnb_investment_dataset_final.xlsx`
- `data/processed/occupancy_sensitivity_dataset.xlsx`

## Listings Sample

`data/raw/listings_sample_public.csv` is a reduced public-safe sample created for portfolio publication.

Removed from the public sample:

- host identifiers
- host names
- listing names
- exact latitude and longitude
- license information

Retained in the public sample:

- neighbourhood context
- room type
- price
- minimum nights
- review counts
- availability measures

## Reuse Note

The public repository is designed for portfolio review, documentation, and Tableau asset inspection. It is not a substitute for a fully scripted ETL pipeline with raw private source regeneration.
