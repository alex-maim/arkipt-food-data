# Switzerland — Swiss Food Composition Database 7.1 (2026)

© Federal Food Safety and Veterinary Office (FSVO). Swiss Food Composition Database, version 7.1, 1 July 2026. https://www.naehrwertdaten.ch/en/downloads/

The dataset-specific download terms explicitly allow commercial applications with source attribution. This package uses those terms, not a presumed Creative Commons licence.

1,245 foods (1,215 generic and 30 branded records), 62 shortlisted dishes/snacks. Names from the official English workbook; no invented German, French or Italian translations. All included rows specify per 100 g edible portion. Energy uses source kcal × 4.184; macros are protein, total fat, available carbohydrate and dietary fibre. No household portions are supplied. ID = 200,000,000,000 + source numeric ID.

ArkiPT adaptation, 2026-10-15. Five nutrient fields, stable source-based IDs and a conservative meal/snack shortlist. Full food search includes ingredients; dishIds is not the complete catalogue. No recipes, allergens, current retail package sizes or translations are inferred. This is composition data, not store inventory. Missing, trace and non-numeric nutrients stay absent, not zero. Source values refer to edible amounts. Enter weighed grams unless a source portion is offered. Existing saved meals keep their snapshots when the region changes.

Rebuild: `python scripts/import_additional_regions.py`. Download the files named in catalogue-report.json to tmp/regions first. The importer pins SHA256 and named columns. Review changed releases before changing pins. The report records provenance and omissions. Source providers do not endorse ArkiPT. Application interface languages remain Finnish and English.
