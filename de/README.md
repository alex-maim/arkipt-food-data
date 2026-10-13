# Germany: BLS 4.0 (2025)

Source: Max Rubner-Institut (2025): Bundeslebensmittelschlüssel (BLS), Version 4.0 — Deutsche Nährstoffdatenbank. Karlsruhe. DOI: https://doi.org/10.25826/Data20251217-134202-0

Dataset licence: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/), confirmed by the [official download page](https://blsdb.de/download). ArkiPT adaptation, 2026-10-13. MRI has not endorsed ArkiPT. Documentation PDFs and site artwork are not redistributed.

7,140 foods with source-provided German and English names. 446 foods in a conservative meal/snack shortlist; the full catalogue remains searchable. These are generic composition records, not retail stock or product packaging. No portions, allergens or translations have been invented. Enter the weighed edible amount in grams.

Per-100-g edible portion fields: ENERCC (kcal), PROT625 (protein Nx6.25), FAT, CHO (available carbohydrate, excluding fibre), FIBT (total dietary fibre). Original kcal are retained via the internal legacy field kj100 = ENERCC × 4.184; this field is not a copy of BLS ENERCJ, which uses different calculation factors. Missing/censored/invalid nutrients are omitted, not zero. Source omissions appear in catalogue-report.json.

Food ID = 400,000,000 + base-36 value of the complete seven-character BLS code. This preserves codes containing internal letters (M5B1600), is reversible, and does not depend on row order. This region reserves IDs through 400,000,000 + 36^7 − 1; future regions must use a different range. Original code can be recovered with `(id - 400000000).toString(36).toUpperCase().padStart(7, '0')`.

Rebuild with `python scripts/import_germany.py` after downloading the official BLS_4_0_2025_DE.zip to tmp/regions/de.zip. The script pins archive SHA256 12b7a6ba62807ec9b301eb276f897dc85f99b2292311618dec3749a12d984c91 and checks named nutrient headers. Changes in source release require review before updating the pin.

The adaptation selects five nutrient fields, creates reversible application IDs, converts the energy storage unit and derives a meal shortlist from English food descriptions. It does not modify the source macro values or supply cooking instructions. New country support does not translate the interface into German.
