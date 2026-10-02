# ArkiPT food data

Public food-only update package for ArkiPT. No application source code, credentials or user data.

`catalogue.json` schema 1, catalogue version 1, published 2026-10-02.

## Sources and attribution

- 4,232 foods, energy in kJ/100 g, dish identifiers and portion weights: Terveyden ja hyvinvoinnin laitos (THL), Fineli, Release 20.0, copyright 2015. [Open data](https://fineli.fi/fineli/fi/avoin-data). [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). See FINELI-LICENSE.txt for the original dataset description.
- Changes to Fineli data: selected fields extracted into JSON, Finnish names sentence-cased, portion units limited to PORTS, PORTM, PORTL and KPL_VALM. The app converts kJ to kcal by dividing by 4.184.
- 12 manufacturer products: basic name, package weight and energy facts checked against the individual manufacturer pages linked in each record. Each record has its own source URL and checkedAt date. No product images, marketing descriptions or preparation text copied. Fineli's licence does not apply to these separate manufacturer facts.

ArkiPT is not produced or endorsed by THL. A catalogue publication date does **not** mean a new Fineli release or a new verification date for every product. Fineli portion weights are not current commercial package sizes. Check the actual package for current nutritional information and allergens.

## Updates

The application downloads this fixed HTTPS URL only when the user requests an update:

https://raw.githubusercontent.com/alex-maim/arkipt-food-data/main/catalogue.json

It validates the complete package, rejects unsupported schemas and older versions, and stores a local copy for offline searches. Saved meals and calorie entries retain their existing snapshots. No personal data is uploaded.

Maintainers: update and verify source facts in the application workspace, then run `node scripts/export_food_catalogue.ts VERSION YYYY-MM-DD` with a strictly increasing version. Review the resulting food-data files and publish those files only to this repository. Do not change a published package without incrementing its version. The app does not crawl manufacturers or automatically claim fresh Fineli data.
