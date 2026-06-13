# ETL Workflow

## Pipeline Objective

The ETL pipeline consolidates Airbnb listing data, housing characteristics, city-level market benchmarks, and occupancy assumptions into a prepared dataset for investment analysis and Tableau Desktop reporting.

## Main Inputs

- `data/raw/airbnb_price.xlsx`
- `data/raw/house_info.xlsx`
- `data/raw/cities_in_sicily.xlsx`
- `data/raw/cities_in_sicily_buy_rent.xlsx`
- `data/raw/occupancy_rate_by_city.xlsx`
- `data/raw/listings.csv`

## Transformation Logic

The original project evidence indicates the following core ETL pattern:

1. Source ingestion
   Raw Excel and CSV files are loaded into Tableau Prep.

2. Data cleaning
   Fields used for integration are standardized and cleaned before join operations.

3. Data integration
   Listing-level data is combined with property details and city-level buy/rent reference information.

4. Business calculations
   The flow computes analytical fields related to Airbnb revenue potential, rent comparison, service cost, annual values, and return-oriented metrics.

5. Analytical output
   The final output is exported as an Excel dataset for Tableau Desktop dashboards.

## Selected Prep Assets

- `tableau/prep/airbnb_investment_pipeline_final.tfl`
- `tableau/prep/airbnb_investment_pipeline_early_version.tfl`

## Final Processed Output Included

- `data/processed/airbnb_investment_dataset_final.xlsx`

## Known Portability Note

The Tableau Prep files originated in a local working environment and may still contain machine-specific path references. Before publication or reuse, the flow should be opened and all inputs/outputs should be repointed to the files inside this repository.
