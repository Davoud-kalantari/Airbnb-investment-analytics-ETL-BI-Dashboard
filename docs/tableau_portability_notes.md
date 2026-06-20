# Tableau Portability Notes

## Scope

This note checks the copied Tableau Prep and Tableau Desktop assets for machine-specific paths and portability issues that affect GitHub publication and local reuse.

## Files Inspected

### Tableau Desktop

- `tableau/dashboards/airbnb_investment_analytics_dashboard.twb`
- `tableau/dashboards/occupancy_sensitivity_dashboard.twb`

### Tableau Prep

- `tableau/prep/airbnb_investment_pipeline_final_repo_safe.tfl`
- `tableau/prep/airbnb_investment_pipeline_early_version_repo_safe.tfl`

## Paths Found

### Tableau Desktop paths found before cleanup

- `C:/Users/DAVIDE/OneDrive/Documenti/Repository personale di Tableau Prep/Origini dati/Final prep ricontrollato.xlsx`
- `C:/Users/DAVIDE/Desktop/DATA SCIENCE MAGISTRALE/BIG DATA/Repository personale di Tableau Prep/Origini dati/Output flow 1 copia 2.xlsx`

### Tableau Prep paths found in the original working files

- `C:\\Users\\DAVIDE\\Desktop\\DATA SCIENCE MAGISTRALE\\BIG DATA\\HouseInfo.xlsx`
- `C:\\Users\\DAVIDE\\Desktop\\DATA SCIENCE MAGISTRALE\\BIG DATA\\CitiesInSicily_BUY_RENT.xlsx`
- `C:\\Users\\DAVIDE\\Downloads\\AirbnbPrice (1).xlsx`
- `C:\\Users\\DAVIDE\\Desktop\\DATA SCIENCE MAGISTRALE\\BIG DATA`
- `C:\\Users\\DAVIDE\\OneDrive\\Documenti\\Repository personale di Tableau Prep\\Origini dati\\Final prep ricontrollato.xlsx`
- `C:\\Users\\DAVIDE\\Desktop\\DATA SCIENCE MAGISTRALE\\BIG DATA\\listings.csv`

## Paths Changed

### Tableau Desktop changes applied

#### `tableau/dashboards/airbnb_investment_analytics_dashboard.twb`

- Changed from:
  - `C:/Users/DAVIDE/OneDrive/Documenti/Repository personale di Tableau Prep/Origini dati/Final prep ricontrollato.xlsx`
- Changed to:
  - `../../data/processed/airbnb_investment_dataset_final.xlsx`

#### `tableau/dashboards/occupancy_sensitivity_dashboard.twb`

- Changed from:
  - `C:/Users/DAVIDE/Desktop/DATA SCIENCE MAGISTRALE/BIG DATA/Repository personale di Tableau Prep/Origini dati/Output flow 1 copia 2.xlsx`
- Changed to:
  - `../../data/processed/occupancy_sensitivity_dataset.xlsx`

### Tableau Prep repo-safe copies created

The public repository keeps the `repo_safe` Tableau Prep flows only.

#### `tableau/prep/airbnb_investment_pipeline_final_repo_safe.tfl`

Changed paths:

- `C:\\Users\\DAVIDE\\Desktop\\DATA SCIENCE MAGISTRALE\\BIG DATA\\HouseInfo.xlsx`
  - `..\\..\\data\\raw\\house_info.xlsx`
- `C:\\Users\\DAVIDE\\Desktop\\DATA SCIENCE MAGISTRALE\\BIG DATA\\CitiesInSicily_BUY_RENT.xlsx`
  - `..\\..\\data\\raw\\cities_in_sicily_buy_rent.xlsx`
- `C:\\Users\\DAVIDE\\Downloads\\AirbnbPrice (1).xlsx`
  - `..\\..\\data\\raw\\airbnb_price.xlsx`
- `C:\\Users\\DAVIDE\\Desktop\\DATA SCIENCE MAGISTRALE\\BIG DATA`
  - `..\\..\\data\\raw`
- `C:\\Users\\DAVIDE\\OneDrive\\Documenti\\Repository personale di Tableau Prep\\Origini dati\\Final prep ricontrollato.xlsx`
  - `..\\..\\data\\processed\\airbnb_investment_dataset_final.xlsx`

#### `tableau/prep/airbnb_investment_pipeline_early_version_repo_safe.tfl`

Changed path:

- `C:\\Users\\DAVIDE\\Desktop\\DATA SCIENCE MAGISTRALE\\BIG DATA\\listings.csv`
  - `..\\..\\data\\raw\\listings_sample_public.csv`

## Paths That Still Need Manual Tableau Validation

- The updated `.twb` files and `repo_safe` `.tfl` files were text-remapped automatically, but they still need to be opened in Tableau Desktop / Tableau Prep to verify that:
  - relative paths resolve correctly in the local clone
  - sheet names and field mappings still refresh correctly
  - no hidden connection metadata inside Tableau requires manual repair

## Manual Validation Requirement

**Yes**

Tableau Desktop and Tableau Prep should still be opened manually to validate portability. The repository now contains cleaner path references, but automated text replacement is not the same as tool-level confirmation inside Tableau.

## Current Portability Assessment

Current portability status: **cleaned for publication, but not fully tool-validated**

What improved:

- both Tableau Desktop workbooks now point to repository-local processed files
- public-safe Prep flows now point to repository-local raw and processed files
- the sensitivity workbook now has a matching processed dataset inside the cleaned repository

What remains:

- manual Tableau validation
- possible hidden metadata or schema refresh issues that cannot be guaranteed from text inspection alone
