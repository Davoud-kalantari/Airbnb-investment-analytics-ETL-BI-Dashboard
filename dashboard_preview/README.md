# Dashboard Preview

This folder contains a browser-based BI dashboard that reconstructs the logic of the Final Dashboard / Step 4 analysis without requiring Tableau.

## What It Reconstructs

The dashboard follows the same decision path documented in the final analytical layer:

- adjusted occupancy rate screening
- best-city selection
- best house-type ranking by `ADJ_AIRBNB_YROI`
- ROI comparison against `RENT_YROI`
- budget, loan, interest, and difference-to-budget feasibility checks

## Main Files

- `index.html`
- `assets/css/style.css`
- `assets/js/main.js`
- `data/dashboard_data.csv`

## Data Sources Used

The browser dashboard is built from cleaned processed outputs:

- `../data/processed/airbnb_investment_dataset_final.xlsx`
- `../data/processed/occupancy_sensitivity_dataset.xlsx`

These processed files were merged into:

- `data/dashboard_data.csv`

For local double-click compatibility, the dashboard also embeds the public-safe processed records directly in `main.js`, so it does not depend on local fetch permissions.

## Metrics Available

The reconstructed dataset includes:

- `Occupancy Rate` used as the adjusted occupancy screening field
- `ADJ_AIRBNB_YROI`
- `ADJ_AIRBNB_NEW`
- `RENT_YROI`
- `ROI_RATIO`
- `House Price`
- `Annual Airbnb Rent`
- `Annual Rent`
- `Service Cost`

Budget, loan amount, interest rate, annual interest cost, and difference total are interactive scenario calculations in the browser layer.

## Privacy and Publication Notes

This preview does not use the full `listings.csv` file and does not expose:

- host names
- host IDs
- listing names
- exact coordinates
- license fields

## Local Usage

Open locally by double-clicking:

- `index.html`

An internet connection is still needed to load Plotly from CDN.
