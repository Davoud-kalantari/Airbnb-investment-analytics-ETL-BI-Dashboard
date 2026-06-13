# Dashboard Logic

## Dashboard Objective

The dashboard layer translates the processed investment dataset into decision-support views that help compare cities and property types under Airbnb and traditional rent scenarios.

## Included Dashboard Files

- `tableau/dashboards/airbnb_investment_analytics_dashboard.twb`
- `tableau/dashboards/occupancy_sensitivity_dashboard.twb`

## Main Analytical Themes

- city-level opportunity screening
- property-type comparison
- Airbnb vs rent yield comparison
- occupancy-adjusted scenario analysis
- investment-oriented KPI review

## Screenshot Evidence Included

- `evidence/screenshots/top_20_cities_by_listing_volume.png`
- `evidence/screenshots/top_5_cities_by_rent_yroi.png`
- `evidence/screenshots/top_5_property_types_by_airbnb_yroi.png`
- `evidence/screenshots/top_5_property_types_by_rent.png`
- `evidence/screenshots/top_5_property_types_by_listing_volume.png`
- `evidence/screenshots/occupancy_adjusted_comparison.png`
- `evidence/screenshots/new_index_comparison.png`
- `evidence/screenshots/city_and_property_type_comparison.png`

## Expected KPI Logic

Based on the final workbook structure and processed dataset fields, the dashboard appears to rely on:

- Airbnb YROI
- Rent YROI
- annual Airbnb revenue
- annual rent benchmark
- service cost adjustments
- city-level averages
- property-type segmentation

## Known Manual Check

The Tableau workbooks were copied from the original project and professionally renamed, but the internal workbook connections should still be validated to ensure they point to the processed dataset inside this repository.
