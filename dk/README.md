# Denmark: Frida 5.5

Attribution: Marija Langwagen, Jette Jacobsen, Tue Christensen and Anders Poulsen. The Danish Food Composition Database, Frida version 5.5, November 2025. National Food Institute, Technical University of Denmark. https://doi.org/10.11583/DTU.29500682

Dataset licence: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). ArkiPT adaptation, 2026-10-13; DTU has not endorsed this application. Documentation PDFs have separate copyright and are not redistributed here.

1,381 foods with Danish and source-provided English names; 57 composed dishes in the conservative browsing shortlist. No portion weights are invented. Per-100-g source fields: Energy, labelling (kcal), parameter 359; Protein, labelling 317; Available carbohydrate, labelling 318; Dietary fibre 168; Fat 141. Carbohydrate excludes fibre. These IDs follow the workbook headers; the English documentation contains a swapped-ID sentence for 317/318, so the named table fields are verified explicitly. Energy is represented as source kcal × 4.184, not recalculated from macros.

Source workbook SHA256 is pinned in scripts/export_regional_catalogues.py. catalogue-report.json records omissions, source URL, checksum and count. Unknown values stay unknown, not zero. The shortlist and UI do not establish retail availability or allergens.
