# Sweden food package

Source: **Livsmedelsverkets Livsmedelsdatabas**, source record version dates up to **2026-07-01**, retrieved 2026-10-09.

- Original data: https://www.livsmedelsverket.se/livsmedel-och-innehall/naringsamne/livsmedelsdatabasen/
- API and licence declaration: https://dataportal.livsmedelsverket.se/livsmedel/swagger/index.html
- Licence: **CC BY 4.0**, https://creativecommons.org/licenses/by/4.0/
- ArkiPT is independent and is not endorsed by Livsmedelsverket.

2,606 generic foods and dishes, Swedish and English source names. No user data, app code or credentials. This is not a retailer assortment, product barcode database or recipe-instruction collection.

Changes: selected energy (kJ), protein (PROT), available carbohydrates (CHO), total fat (FAT), total fibre (FIBT), all per 100 g edible food; other fields omitted. The application divides kJ by 4.184 for kcal. Source IDs are namespaced by adding 5,000,000 to prevent collisions with Fineli. `fineliRelease` is a legacy schema field holding the source version date for this package; it does not indicate Fineli as the source. No food values are translated or remapped to another food.

Missing values remain missing. Source item 3418 (Matolja) reports 102 g fat/100 g; that fat value is omitted, not clamped or replaced with zero. Energy is retained. See import-report.json. One energy record lacks the redundant matrix code; its documented 100 g food basis is used. Explicit other matrix codes or units abort import.

`dishIds` is an ArkiPT convenience shortlist based on Swedish names, not a source-provided claim of a complete meal or industrial ready food. No source portion weights are available: portions is empty and users enter a weighed amount. Names retain raw/cooked/dried qualifiers. Check actual packaging for allergens and preparation state.

Maintainers: run `python scripts/import_sweden.py --version N --cache tmp/slv-YYYY-MM-DD` in the application workspace. Use a fresh cache for each source refresh. Review the import report and run the regional tests, then publish only this directory to `arkipt-food-data/se/`. Increment version before changing published data. The runtime downloads the single catalogue.json on request, validates it, and keeps both regions locally. It does not call the source API or upload personal data.
