# Method: smart trainer & smart bike database (SmartBikeWiki)

**Checked:** 2026-09-28 (wave 1 update 2026-09-29). **Re-check:** prices monthly, specs and findings quarterly or on new product launches.

## Inclusion
Models currently sold by Wahoo, Garmin/Tacx, Elite, Saris, JetBlack, Wattbike, Stages and Zwift (Ride via its KICKR CORE 2 bundle) that could be verified on the check date. First pass: 16 records. See GAPS.md for models not compiled and why.

## Sources
- Specs: the manufacturer's own product page or spec table (Wahoo, Elite, Saris, Wattbike, JetBlack support), or Garmin's launch press release for the Tacx NEO 3M. Numbers are the manufacturer's *claims*, recorded as stated (units kept: lb/kg, W at stated speed).
- Price: price shown on the manufacturer's (or, for the Zwift Ride bundle, Zwift's) US store on the check date, in USD, taken from page structured data. No conversions were done. The NEO 3M price is the 2023 launch MSRP and is labelled so.
- `publishedFindings`: measurements published by a named independent reviewer, read from the review page, and paraphrased. Each entry names the reviewed model (which may be a predecessor: H3 vs H3 Plus, Atom 2020 vs current Atom) and links the review. Wave 1 (2026-09-29) added findings from BikeRadar, road.cc, PezCycling News, Cycling Weekly, Zwift Insider, OutdoorGearLab, The Triathlete (UK) and Cyclist. Reviewers mostly compare trainer power against pedal, crank or hub power meters; each entry says which. Findings are theirs, not ours, and we ran no tests. Where a review page could not be read in full it is not cited.

## Derived numbers
None. Every value is either a manufacturer claim, a store price, or a reviewer statement.

## Known gaps
See GAPS.md. Main ones: Garmin/Tacx and Stages pages could not be read, Elite prices are absent from static page HTML, and reviewer coverage is single-source.


## Prices in other currencies
Where a manufacturer store showed only euro prices (Elite), the figure is stored as `priceLocal` with `priceCurrency: EUR` and `price` is left null, so nothing is shown as dollars. No exchange-rate conversion is done.

## Apps dataset
`apps.json` records subscription price, trial, platforms and features for Zwift, TrainerRoad, MyWhoosh, ROUVY and Wahoo SYSTM from each vendor's own pages or help centre, checked 2026-09-29. App prices change often: re-check monthly.

## Canonical copy and sync
`data/smartbikewiki/trainer-database/` is the canonical source. `sites/smartbikewiki/src/data/` holds build-time copies of `trainer-database.json`, `apps.json`, `METHOD.md`, `CHANGELOG.md` and `GAPS.md`. Edit only the canonical files, then copy them across (`cp data/smartbikewiki/trainer-database/{trainer-database.json,apps.json,METHOD.md,CHANGELOG.md,GAPS.md} sites/smartbikewiki/src/data/`) in the same commit. The other files in `src/data` (products, affiliates, glossary, review-db-map) belong to the site only.

## Wave 1 audit corrections, 2026-09-29
An independent audit re-read every added finding against its review page. Corrected: road.cc on KICKR CORE 2 (weight, an unsupported racing verdict), Zwift Insider on NEO 2T (the 57.8 dB figure is Tacx's own, and an unsupported racing verdict was a reader comment), road.cc on KICKR BIKE PRO and Wattbike Atom (Proton comparison, rider weight), road.cc on JetBlack Victory and Stages SB20 (figures), and DC Rainmaker on the Victory. The Elite Justo 2 finding from The Triathlete (UK) was removed: it is an affiliate roundup that only repeats the manufacturer claim. Zwift Ride and Saris H3 Plus prices are sale prices; see each record's `priceNote`.
