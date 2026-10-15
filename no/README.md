# Norway — Matvaretabellen 2026

Matvaretabellen 2026. Mattilsynet. www.matvaretabellen.no

Source: https://www.matvaretabellen.no/api/ . Licence: Norwegian Licence for Open Government Data (NLOD), https://data.norge.no/nlod/en . Source attribution requirements: https://www.mattilsynet.no/mat-og-drikke/matvaretabellen/opphavsrett . Registry: https://data.norge.no/nn/datasets/bc57cc76-4d20-3c21-ae1b-c5a3cdcb58f7/matvaretabellen .

2,118 foods, 143 shortlisted dishes/snacks. Source Norwegian and English names. Three records without numeric calories are omitted. Source calories are stored as kcal × 4.184 to preserve kcal display; Protein, Fett, Karbo and Fiber are g/100 g. Source gram weights for named household measures are retained with English labels; these are not retail package weights. ID = 100,000,000,000 + digits of trimmed source code NN.NNN.

ArkiPT adaptation, 2026-10-15. Five nutrient fields, stable source-based IDs and a conservative meal/snack shortlist. Full food search includes ingredients; dishIds is not the complete catalogue. No recipes, allergens, current retail package sizes or translations are inferred. This is composition data, not store inventory. Missing, trace and non-numeric nutrients stay absent, not zero. Source values refer to edible amounts. Enter weighed grams unless a source portion is offered. Existing saved meals keep their snapshots when the region changes.

Rebuild: `python scripts/import_additional_regions.py`. Download the files named in catalogue-report.json to tmp/regions first. The importer pins SHA256 and named columns. Review changed releases before changing pins. The report records provenance and omissions. Source providers do not endorse ArkiPT. Application interface languages remain Finnish and English.

Catalogue version 2 includes the source spelling “yoghurt” in the snack shortlist as well as “yogurt”.
