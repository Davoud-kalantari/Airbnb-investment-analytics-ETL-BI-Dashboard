# Final Publication Review

## Safe to Publish

**Yes, with warnings**

The repository is now publishable as a portfolio project because the sensitive full listings file is excluded from Git tracking, a public-safe sample is provided, the browser dashboard reconstructs the Final Dashboard / Step 4 logic without Tableau, and the main Tableau paths were improved. Manual Tableau validation is still recommended before claiming full portability.

## Remaining Warnings

1. Tableau validation is still manual
   The workbook and flow paths were improved automatically, but Tableau Desktop and Tableau Prep should still be opened locally to confirm that connections resolve correctly.

2. Public report body wording
   The public PDF has a sanitized portfolio cover page, but pages 2 onward preserve the original report body and still contain some legacy classroom-style phrasing.

3. KPI formula documentation is still partial
   The repository documents the workflow well at a high level, but it does not yet include a full field-by-field data dictionary or formal KPI specification.

## Resolved Publication Risks

### Listings dataset risk

Resolved for publication by:

- excluding `data/raw/listings.csv` from Git tracking
- creating `data/raw/listings_sample_public.csv`
- removing host identifiers, exact coordinates, listing names, and license fields from the public sample

### Recruiter accessibility risk

Resolved for first-pass review by:

- replacing the old static preview with a browser-based interactive dashboard in `dashboard_preview/`
- rebuilding that browser dashboard as a full-width interactive reconstruction of the Tableau Final Dashboard logic
- keeping screenshot evidence in `evidence/screenshots/`
- keeping public-safe PDF report access
- providing a preview path that does not require a Tableau license

### Tableau path risk

Partially resolved by:

- updating both `.twb` files to repository-local processed paths
- creating `repo_safe` `.tfl` variants that point to repository-local raw and processed files

## Files Safe to Commit

- `README.md`
- `.gitignore`
- `CLEANUP_SUMMARY.md`
- `FINAL_PUBLICATION_REVIEW.md`
- `docs/etl_workflow.md`
- `docs/dashboard_logic.md`
- `docs/publication_notes.md`
- `docs/tableau_portability_notes.md`
- `reports/airbnb_investment_analytics_report.pdf`
- `dashboard_preview/*`
- `evidence/screenshots/*`
- `tableau/dashboards/airbnb_investment_analytics_dashboard.twb`
- `tableau/dashboards/occupancy_sensitivity_dashboard.twb`
- `tableau/prep/airbnb_investment_pipeline_final_repo_safe.tfl`
- `tableau/prep/airbnb_investment_pipeline_early_version_repo_safe.tfl`
- `tableau/prep/airbnb_investment_pipeline_final.tfl`
- `tableau/prep/airbnb_investment_pipeline_early_version.tfl`
- `data/raw/airbnb_price.xlsx`
- `data/raw/house_info.xlsx`
- `data/raw/cities_in_sicily.xlsx`
- `data/raw/cities_in_sicily_buy_rent.xlsx`
- `data/raw/occupancy_rate_by_city.xlsx`
- `data/raw/listings_sample_public.csv`
- `data/processed/airbnb_investment_dataset_final.xlsx`
- `data/processed/occupancy_sensitivity_dataset.xlsx`

## Files to Exclude

- `data/raw/listings.csv`
- `private_reference/reports/original_academic_report_reference.pdf`
- `reports/_sanitized_cover_temp*.pdf`
- any future Tableau recovery files, logs, caches, or local temp exports

## Listings.csv Review

- Full file size: `9,985,902` bytes
- Sensitive fields detected in the original full file:
  - `host_name`
  - `host_id`
  - `latitude`
  - `longitude`
  - `name`
  - `license`

Public action taken:

- created `data/raw/listings_sample_public.csv`
- kept only fields useful for ETL/BI demonstration
- removed privacy-sensitive and direct listing-identification fields

Recommendation:

- commit the sample
- keep the full file local only

## Final GitHub Readiness Score

**8.4 / 10**

Why not higher:

- the repository is now safe and understandable for GitHub publication
- recruiter access no longer depends entirely on Tableau or a Tableau license
- the browser dashboard now mirrors the original occupancy -> city -> house type -> financial feasibility narrative more closely
- sensitive raw listing data is no longer part of the tracked public package
- but Tableau Desktop / Prep portability is still not tool-validated end to end

## Remaining Manual Actions

1. Open the updated `.twb` files in Tableau Desktop and confirm that the relative paths resolve correctly.
2. Open the `repo_safe` `.tfl` files in Tableau Prep and confirm that inputs, outputs, and schema refresh work correctly.
3. If desired, remove or archive the legacy non-`repo_safe` `.tfl` files after local validation.
