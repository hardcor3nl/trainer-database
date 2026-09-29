# Smart Trainer and Smart Bike Database

Manufacturer-claimed specs, store prices in the store's own currency and what named independent reviewers published about power accuracy and noise for 16 current smart trainers and smart bikes, each with its source link and a checked date. We ran no tests and nothing here is a score. A second file records five cycling apps' subscription prices.

- Canonical page: https://smartbikewiki.com/database/
- Statistics computed from this dataset: https://smartbikewiki.com/smart-trainer-statistics/
- Version: 2026-09-29 (the date the data was last checked)
- Publisher: SmartBikeWiki editorial, an independent research publication at https://smartbikewiki.com
- Size: 16 models

## Files

| File | Contents |
|---|---|
| `trainer-database.csv` | CSV, UTF-8. One row per model. 16 rows. |
| `trainer-database-findings.csv` | CSV, UTF-8. One row per published independent-reviewer finding. 37 rows. |
| `trainer-database-apps.csv` | CSV, UTF-8. One row per cycling app. 5 rows. |
| `trainer-database.json` | The full dataset as JSON, including nested fields. |
| `apps.json` | Companion data file, as published on the site. |
| `schema.json` | JSON Schema for the main file. |
| `METHOD.md` | How the data was compiled and derived. |
| `GAPS.md` | What is missing or unverified. |
| `CHANGELOG.md` | Dated change log. |
| `CITATION.cff` | Citation metadata (Citation File Format 1.2.0). |

## Source method

Every fact traces to a primary source (vendor, government, or a named independent reviewer) linked in the row it belongs to, with the date it was checked. Values are stored as the source states them; nothing is converted between currencies. Empty or null means the source did not state it or could not be read, never a guess. Read METHOD.md for the full rules and GAPS.md for what is missing. We compile from public pages and do not run our own tests.

## Licence

Creative Commons Attribution 4.0 International (CC BY 4.0), https://creativecommons.org/licenses/by/4.0/. You may copy, redistribute and adapt the data, including commercially, if you give credit and **link to the canonical page**: https://smartbikewiki.com/database/. Suggested credit: "Data: Smart Trainer and Smart Bike Database by SmartBikeWiki, https://smartbikewiki.com/database/".

## Cite

SmartBikeWiki editorial. (2026). *Smart Trainer and Smart Bike Database* (Version 2026-09-29) [Data set]. SmartBikeWiki. https://smartbikewiki.com/database/

Machine-readable citation: see `CITATION.cff`.

## Corrections

If you find an error, tell us through the contact page on https://smartbikewiki.com. Corrections are logged in CHANGELOG.md.
