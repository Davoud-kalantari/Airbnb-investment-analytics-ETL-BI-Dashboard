# Dashboard Logic

## Objective

The dashboard layer presents city and property-type comparisons for Airbnb-style returns versus traditional rent benchmarks.

## Included Dashboard Assets

- `tableau/dashboards/airbnb_investment_analytics_dashboard.twb`
- `tableau/dashboards/occupancy_sensitivity_dashboard.twb`
- `dashboard_preview/index.html`

## Main Analytical Views

- city-level opportunity screening
- property-type comparison
- Airbnb versus rent yield comparison
- occupancy-adjusted scenario review
- budget and feasibility exploration in the browser preview

## Main Metrics Used

- `adj_airbnb_yroi`
- `rent_yroi`
- `roi_ratio`
- `adjusted_occupancy_rate`
- `annual_airbnb_rent`
- `annual_rent`
- `service_cost`
- `house_price`

## Preview Evidence

- `evidence/screenshots/top_20_cities_by_listing_volume.png`
- `evidence/screenshots/top_5_cities_by_rent_yroi.png`
- `evidence/screenshots/top_5_property_types_by_airbnb_yroi.png`
- `evidence/screenshots/top_5_property_types_by_rent.png`
- `evidence/screenshots/top_5_property_types_by_listing_volume.png`
- `evidence/screenshots/occupancy_adjusted_comparison.png`
- `evidence/screenshots/new_index_comparison.png`
- `evidence/screenshots/city_and_property_type_comparison.png`

## Validation Note

The browser preview is the easiest way to review the analytical story without Tableau. Tableau workbook connections should still be validated inside Tableau Desktop for full tool-level confirmation.
