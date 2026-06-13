# Final GitHub Check

## safe_to_publish

**no**

The portfolio package itself is close to publishable, but the current Git setup is not yet GitHub-ready as a standalone repository. The cleaned project folder is still inside a parent Git working tree, and no remote is configured for this project folder.

## blockers

1. Standalone Git repository not initialized for this cleaned project
   - `git rev-parse --show-toplevel` resolves to `C:/Users/David/OneDrive/Documenti/Sistemazione cartelle`
   - this means `airbnb-investment-analytics-etl-bi-dashboard` is currently inside a parent repository context, not its own repo

2. No Git remote configured
   - `git remote -v` returns no remote
   - `git push` cannot work until a GitHub repository is created and connected

## warnings

1. Tableau files still require manual validation
   - the repository-local path cleanup is documented, but `.twb` and `.tfl` portability is not fully validated inside Tableau Desktop and Tableau Prep

2. Private reference material is still present locally
   - `private_reference/reports/original_academic_report_reference.pdf` exists in the cleaned folder
   - it is ignored by `.gitignore`, but it must stay excluded from public commits

3. Full listings source remains local-only
   - `data/raw/listings.csv` exists locally and is correctly ignored
   - only `data/raw/listings_sample_public.csv` should be committed

4. Temporary file was found during audit
   - `tableau/prep/airbnb_investment_pipeline_final.tfl.tmp` was present as an ignored temp file and should not be committed

## files safe to commit

- `.gitignore`
- `README.md`
- `CLEANUP_SUMMARY.md`
- `FINAL_PUBLICATION_REVIEW.md`
- `FINAL_GITHUB_CHECK.md`
- `dashboard_preview/index.html`
- `dashboard_preview/README.md`
- `dashboard_preview/assets/css/style.css`
- `dashboard_preview/assets/js/main.js`
- `dashboard_preview/data/dashboard_data.csv`
- `data/raw/airbnb_price.xlsx`
- `data/raw/cities_in_sicily.xlsx`
- `data/raw/cities_in_sicily_buy_rent.xlsx`
- `data/raw/house_info.xlsx`
- `data/raw/listings_sample_public.csv`
- `data/raw/occupancy_rate_by_city.xlsx`
- `data/processed/airbnb_investment_dataset_final.xlsx`
- `data/processed/occupancy_sensitivity_dataset.xlsx`
- `docs/dashboard_logic.md`
- `docs/etl_workflow.md`
- `docs/publication_notes.md`
- `docs/tableau_portability_notes.md`
- `evidence/screenshots/*`
- `outputs/.gitkeep`
- `reports/airbnb_investment_analytics_report.pdf`
- `tableau/dashboards/airbnb_investment_analytics_dashboard.twb`
- `tableau/dashboards/occupancy_sensitivity_dashboard.twb`
- `tableau/prep/airbnb_investment_pipeline_early_version.tfl`
- `tableau/prep/airbnb_investment_pipeline_early_version_repo_safe.tfl`
- `tableau/prep/airbnb_investment_pipeline_final.tfl`
- `tableau/prep/airbnb_investment_pipeline_final_repo_safe.tfl`

## files that must stay excluded

- `data/raw/listings.csv`
- `private_reference/`
- `reports/_sanitized_cover_temp*.pdf`
- `*.exe`
- `*.mp4`
- `*.twbr`
- `*.log`
- `*.tmp`
- `*.temp`
- local Tableau caches, logs, and recovery files

## final readiness score

**8.3 / 10**

The project content is strong and mostly public-safe, but Git publication readiness is blocked by repo setup rather than by the portfolio materials themselves.

## exact next Git commands to publish

Run these commands from the cleaned project folder:

```powershell
cd "C:\Users\David\OneDrive\Documenti\Sistemazione cartelle\airbnb-investment-analytics-etl-bi-dashboard"
git init
git branch -M main
git add .
git status
git commit -m "Initial commit: Airbnb Investment Analytics ETL & BI Dashboard"
git remote add origin <YOUR_GITHUB_REPO_URL>
git push -u origin main
```

Optional safety check before the first commit:

```powershell
git status --ignored
```
