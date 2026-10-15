# United Kingdom — CoFID 2021

Contains public sector information licensed under the Open Government Licence v3.0. © Crown copyright. Public Health England, McCance and Widdowson’s Composition of Foods Integrated Dataset 2021.
Source: https://www.gov.uk/government/publications/composition-of-foods-integrated-dataset-cofid
Licence: https://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/

2,816 foods, 102 shortlisted dishes/snacks. English source names. Per 100 g fields from Proximates: source kcal × 4.184, Protein, Fat, Carbohydrate and AOAC fibre. Carbohydrate is preserved as monosaccharide equivalents, NOT relabelled as ordinary available carbohydrate. It can exceed 100 g/100 g owing to the hydrolysis convention. Mixed definitions give no combined carbohydrate total in the app. Energy is not recomputed from macros. Trace (Tr), N and blank values remain absent.

Group Q (alcoholic beverages) is excluded because its values are per 100 mL. No density is guessed. Source code 13-669 appears twice for unrelated foods (aubergine and watercress); both records are excluded pending source clarification. Other records retain IDs = 300,000,000,000 + source code digits. No household portions are supplied.

ArkiPT adaptation, 2026-10-15. Five nutrient fields, stable source-based IDs and a conservative meal/snack shortlist. Full food search includes ingredients; dishIds is not the complete catalogue. No recipes, allergens, current retail package sizes or translations are inferred. This is composition data, not store inventory. Missing, trace and non-numeric nutrients stay absent, not zero. Source values refer to edible amounts. Enter weighed grams unless a source portion is offered. Existing saved meals keep their snapshots when the region changes.

Rebuild: `python scripts/import_additional_regions.py`. Download the files named in catalogue-report.json to tmp/regions first. The importer pins SHA256 and named columns. Review changed releases before changing pins. The report records provenance and omissions. Source providers do not endorse ArkiPT. Application interface languages remain Finnish and English.
