# Cleanup Summary

## Scope

A new clean portfolio folder was created at:

`airbnb-investment-analytics-etl-bi-dashboard`

The original `BIG DATA` folder was not modified.

## Files Copied

### Raw data

- `AirbnbPrice.xlsx` -> `data/raw/airbnb_price.xlsx`
- `HouseInfo.xlsx` -> `data/raw/house_info.xlsx`
- `CitiesInSicily.xlsx` -> `data/raw/cities_in_sicily.xlsx`
- `CitiesInSicily_BUY_RENT.xlsx` -> `data/raw/cities_in_sicily_buy_rent.xlsx`
- `OccupancyRateByCity.xlsx` -> `data/raw/occupancy_rate_by_city.xlsx`
- `listings.csv` -> `data/raw/listings.csv` (local-only source retained, excluded from Git tracking)

### Public-safe raw sample

- `data/raw/listings_sample_public.csv` created from the full listings dataset with sensitive fields removed

### Processed data

- `Final prep ricontrollato.xlsx` -> `data/processed/airbnb_investment_dataset_final.xlsx`
- `Output flow 1 copia 2.xlsx` -> `data/processed/occupancy_sensitivity_dataset.xlsx`

### Tableau Prep

- `Flow1 finale.tfl` -> `tableau/prep/airbnb_investment_pipeline_final.tfl`
- `AirbnbDataPipeline.tfl` -> `tableau/prep/airbnb_investment_pipeline_early_version.tfl`
- `tableau/prep/airbnb_investment_pipeline_final_repo_safe.tfl` created with repository-local paths
- `tableau/prep/airbnb_investment_pipeline_early_version_repo_safe.tfl` created with repository-local paths

### Tableau Desktop

- `FINAL DESKTOP 2.twb` -> `tableau/dashboards/airbnb_investment_analytics_dashboard.twb`
- `STEP 4.twb` -> `tableau/dashboards/occupancy_sensitivity_dashboard.twb`

### Screenshots

- `20 city and 5 Housetype.png` -> `evidence/screenshots/city_and_property_type_comparison.png`
- `The same of field 4 with ADJ.png` -> `evidence/screenshots/occupancy_adjusted_comparison.png`
- `The same of field 5 with NEW INDEX.png` -> `evidence/screenshots/new_index_comparison.png`
- `The top 20 cities .png` -> `evidence/screenshots/top_20_cities_by_listing_volume.png`
- `Top 5 cities avg RENT Yroi (Cities must have at least 300 houses).png` -> `evidence/screenshots/top_5_cities_by_rent_yroi.png`
- `Top 5 type of house (avg AIRBNBYroi).png` -> `evidence/screenshots/top_5_property_types_by_airbnb_yroi.png`
- `Top 5 type of house (avg RENT).png` -> `evidence/screenshots/top_5_property_types_by_rent.png`
- `Top 5 type of house .png` -> `evidence/screenshots/top_5_property_types_by_listing_volume.png`

## Publication Improvements Added

- `listings.csv` excluded from Git tracking
- `listings_sample_public.csv` created as a public-safe sample
- old static preview replaced with a full interactive browser dashboard in `dashboard_preview/`
- browser dashboard rebuilt as a reconstruction of the Tableau Final Dashboard / Step 4 logic
- `docs/tableau_portability_notes.md` updated with inspected files, paths found, changes applied, and remaining manual validation steps

## Files Renamed

All copied assets were renamed into English, recruiter-friendly names with consistent lowercase formatting and business-oriented semantics.

## Files Excluded

### Explicitly excluded categories

- installers
- videos
- lecture recordings
- slide decks / support slides
- Tableau logs
- Tableau recovery files
- local Tableau repository cache
- duplicate `.tfl` versions not needed for publication
- duplicate `.twb` versions
- temporary files
- files with personal or academic identifiers

### Important exclusions

- `calendar.csv`
- `data/raw/listings.csv` from Git tracking
- all `.exe` files
- all `.mp4` files
- `SupportSlide_AirBNBUseCase_Part1.pdf`
- academic report files from the public package
- `Repository personale di Tableau Prep/Log`
- `Repository personale di Tableau Prep/Flussi recuperati`
- `CORPORATE%20FINANCE%20-%20Budget%20Controlling.twbx`
- all `.twbr` recovery files

## Open Risks

- Tableau files still require manual validation inside Tableau Desktop / Tableau Prep.
- Public report body pages still retain some legacy classroom-style wording after the sanitized cover page.
- Workbook metadata may still contain tool-level details not visible from plain text inspection alone.

## Manual Checks Needed Before GitHub Publication

1. Open the `repo_safe` Tableau Prep flows and validate every input/output path.
2. Open the Tableau Desktop workbooks and confirm that the repository-local processed files refresh correctly.
3. Confirm that the selected processed workbooks are the intended canonical outputs.
4. Optionally retire the legacy non-`repo_safe` Prep flows after validation.
