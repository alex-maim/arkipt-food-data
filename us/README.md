# US food package preparation

Prepared 2026-10-13. `candidate.json` preserves import provenance; `catalogue.json` is the app's schema-2 distribution package. The application changes are not yet in a new APK.

Contains 5,752 foods: 5,431 Survey (FNDDS) foods and 321 Foundation foods. Sources are the official [USDA downloads](https://fdc.nal.usda.gov/download-datasets/): FNDDS release 2024-10-31 and Foundation release 2026-04-30. USDA publishes FoodData Central data under [CC0](https://fdc.nal.usda.gov/). Attribution: U.S. Department of Agriculture, Agricultural Research Service, FoodData Central.

Reproduce with `python scripts/import_usda.py --survey tmp/usda/fndds.zip --foundation tmp/usda/foundation.zip`. ZIP hashes are pinned in the importer; updating releases requires reviewing and updating both provenance and hashes. No API key or runtime server is required. `import-report.json` records source hashes, counts, omitted values and output checksum. Missing or invalid values are not converted into zeroes. Foods without usable energy are excluded.

The candidate uses namespaced IDs, English source names and amounts per 100 g. USDA carbohydrate by difference (nutrient 1005) remains explicitly distinct from European available carbohydrate; see [USDA FAQ](https://fdc.nal.usda.gov/faq/). Energy comes from the source; it is not recalculated from macros. Portion weights are source measures, not retail pack sizes. Keep source amount and label together when interpreting a portion; Foundation modifiers alone may not describe the complete measure.

Implemented integration:

- Schema 2 uses reserved numeric IDs (100,000,000 + USDA FDC ID) for compatibility with existing saved numeric identities. Original IDs remain recoverable. Existing FI/SE IDs are unchanged.
- Carbohydrate is explicitly tagged `by-difference`; the app labels it as including fibre. Mixed US/EU carbohydrate totals remain unknown with a different-definitions label; other macros and source energy still sum normally. No fibre subtraction is guessed.
- Source portion descriptions retain the complete amount and measure; ambiguous RACC/unspecified measures are omitted. The picker offers g/oz/lb; cup and spoon weights are food-specific. Stored calculations use grams.
- Region-specific updates and backups retain every installed region and all saved recipe snapshots. UI language remains FI/EN; US food names are English. 1,303 conservative meal/snack candidates are distinguished from all 5,752 foods.

Remaining release checks:

1. Build a fresh APK and test fresh install, region switching, custom recipes, shopping quantities and backup restoration on Android.
2. Review dish-shortlist coverage with testers. It is not a claim of balanced meals, ingredient completeness or allergen safety.

This dataset includes generic prepared foods. It is not a store inventory and does not establish product availability, brands, allergens or package sizes.
