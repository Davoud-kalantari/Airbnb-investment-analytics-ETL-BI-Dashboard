# Publication Notes

## What Was Included

This cleaned repository includes the main raw inputs, the main processed output, the main Tableau Prep flows, the primary Tableau Desktop workbooks, and the strongest screenshot evidence.

## What Was Excluded

The following categories were intentionally excluded:

- software installers
- videos and screen recordings
- lecture material
- slides
- Tableau recovery files
- Tableau logs
- local Tableau repository cache
- duplicate dashboard copies
- duplicate Prep flow copies
- files containing direct personal or academic identifiers

## Current Publication Risks

1. Tableau path portability
   The `.twb` and `.tfl` files may still contain local file path references from the original machine.

2. Raw data review
   `data/raw/listings.csv` should receive a final privacy and licensing check before public release.

3. Process lineage documentation
   The repository is now much cleaner, but a deeper field-by-field data dictionary would strengthen public credibility.

4. Output validation
   The processed workbook should be checked one more time against the final Tableau dashboards to confirm it is the intended canonical output.

## Recommended Final Checks Before GitHub Publication

- open each Tableau Prep flow and repoint any broken inputs
- open each Tableau workbook and verify dashboard connections
- confirm that no hidden personal identifiers remain in workbook metadata
- decide whether `listings.csv` should stay in the public repo or be replaced with a documented sample
- optionally export final dashboard screenshots at a consistent size for the README
