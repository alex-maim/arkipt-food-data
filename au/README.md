# Australia — Australian Food Composition Database Release 3 (2025)

© Food Standards Australia New Zealand (FSANZ). Australian Food Composition Database, Release 3. Adapted by ArkiPT, 2026.
Source: https://www.foodstandards.gov.au/science-data/food-nutrient-databases/afcd/data-files

This derivative data package is distributed under the SAME FSANZ Data User Licence Agreement, based on CC BY-SA 3.0 Australia with additional terms. Full agreement: LICENSE.txt and https://www.foodstandards.gov.au/science-data/monitoringnutrients/afcd/datauserlicenceagreement . Retain attribution, notices, licence and limitations with redistribution. The open data package is separate from the application; no restrictions or DRM are imposed on this package.

1,588 foods, 51 shortlisted dishes/snacks. English source names. Uses ONLY the all-solids-and-liquids per-100-g sheet, not the separate per-100-mL sheet. Energy with dietary fibre (kJ) is stored directly, displayed kcal = kJ / 4.184. Protein, total fat, total dietary fibre and available carbohydrate WITH sugar alcohols are retained. AFCD notes some labelled carbohydrate may originate from by-difference estimates; we preserve its published available-carbohydrate field without inventing conversions. ID = 400,000,000,000 + numeric part of public food key Fxxxxxx. No household portions are supplied.

Based on Australian data which may not be appropriate for use in other countries.

Limitation of Data Statement: There are limitations associated with food composition databases. Food composition data used in the database or databases may represent an average of the nutrient content of a particular sample of foods and ingredients, determined at a particular time. The nutrient composition of foods and ingredients can vary substantially between batches and brands because of a number of factors, including changes in season, processing practices and ingredient source, and methods of calculation.

ArkiPT adaptation, 2026-10-15. Five nutrient fields, stable source-based IDs and a conservative meal/snack shortlist. Full food search includes ingredients; dishIds is not the complete catalogue. No recipes, allergens, current retail package sizes or translations are inferred. This is composition data, not store inventory. Missing, trace and non-numeric nutrients stay absent, not zero. Source values refer to edible amounts. Enter weighed grams unless a source portion is offered. Existing saved meals keep their snapshots when the region changes.

Rebuild: `python scripts/import_additional_regions.py`. Download the files named in catalogue-report.json to tmp/regions first. The importer pins SHA256 and named columns. Review changed releases before changing pins. The report records provenance and omissions. Source providers do not endorse ArkiPT. Application interface languages remain Finnish and English.

Catalogue version 2 includes the source spelling “yoghurt” in the snack shortlist as well as “yogurt”.
